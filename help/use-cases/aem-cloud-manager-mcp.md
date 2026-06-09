---
title: 確実なAEM as a Cloud Serviceへのデプロイ
description: AI クライアントを離れることなく、環境の健全性を確認し、パイプラインの履歴を確認し、デプロイメントをトリガーまたは管理できます。
last-substantial-update: 2026-05-21T00:00:00Z
index: false
source-git-commit: 093448ea6a9840d1d2027b76e177b145400a9202
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 1%

---


# 確実なAEM as a Cloud Serviceへのデプロイ

<!-- last-modified: 2026-05-21 -->

>[!VIDEO](https://video.tv.adobe.com/v/3480343/?captions=jpn&learn=on&enablevpops)

Adobe Experience Manager環境の管理とは、通常、Cloud Managerにログインし、パイプラインと環境を移動し、デプロイメントステータスを追跡するためにコンテキストを切り替えることを意味します。 このチュートリアルでは、AEM Cloud Manager MCP Serverを使用してAI クライアントからこれらのオペレーションを処理する方法を示します。これにより、デベロッパーとオペレーション部門は、AI環境から離れることなく、ステータスの確認、パイプラインのレビュー、デプロイメントの詳細の処理を行うことができます。

| | |
| --- | --- |
| CX エンタープライズアプリケーション | Adobe Experience Manager Cloud Manager |
| エージェント型ツール | AEM Cloud Manager MCP Server |
| オーディエンス | 開発、DevOps、運用チーム |
| 前提条件 | MCP対応AI クライアント、AEM Cloud Managerアクセス |

各ステップは、代表的なプロンプトとAI応答の例を示しています。 同じセッションで追加の探索を行うために、**さらに**&#x200B;個のセクションを試すよう求めるプロンプトが表示されます。

## 始める前に

>[!BEGINTABS]

>[!TAB  クロード コード ]

最初にプロジェクトディレクトリに移動し、CLIを使用してCloud Manager MCP Serverを追加します。

```bash
claude mcp add --transport http adobe-cloud-manager https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager
```

または、プロジェクト ルートの`.mcp.json`に手動で追加します。

```json
{
  "mcpServers": {
    "adobe-cloud-manager": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager"
    }
  }
}
```

Claude Codeを再起動します。 Cloud Managerのツールは、次回のセッションで利用できます。

完全なセットアップ：[Claude Code MCP ドキュメント &#x200B;](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB  カーソル ]

Cloud Manager MCP Serverをプロジェクトルートの`~/.cursor/mcp.json` （グローバル）または`.cursor/mcp.json`に追加します。

```json
{
  "mcpServers": {
    "adobe-cloud-manager": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager"
    }
  }
}
```

**Settings > MCP**&#x200B;を開き、サーバーの横にある&#x200B;**Connect**&#x200B;を選択し、Adobe IDでログインします。

完全なセットアップ：[&#x200B; カーソル MCP ドキュメント &#x200B;](https://cursor.com/docs/mcp)

>[!TAB GitHub コパイロット ]

プロジェクト ルートの`.vscode/mcp.json`にCloud Manager MCP Serverを追加します。

```json
{
  "servers": {
    "adobe-cloud-manager": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager"
    }
  }
}
```

注意：VS Codeは`"mcpServers"`ではなく、`"servers"`を最上位キーとして使用します。

**GitHub Copilot Chat** パネルを開き、**エージェントモード**&#x200B;に切り替え、サーバーの横にある&#x200B;**Connect**&#x200B;を選択します。 MCP ツールは、エージェントモードでのみ使用できます。

完全なセットアップ：[VS Code MCP サーバーのドキュメント &#x200B;](https://code.visualstudio.com/docs/copilot/customization/mcp-servers)

>[!TAB その他のAI クライアント ]

別のMCP互換の環境を使用していますか？ 次のエンドポイントを使用してCloud Manager MCP Serverに接続します。

```
https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager
```

サポートされているすべてのクライアントの完全なセットアップ手順：[AI クライアントに接続](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>プロンプトが表示されたらAdobe IDでログインし、AEM as a Cloud Service プログラムにリンクされているIMS組織を選択します。 権限はCloud Managerレベルで適用されます。AI クライアントは、アカウントが承認された操作のみを実行できます。
>
>最初の接続時に、AI クライアントから組織またはAEM プログラムの確認を求められる場合があります。 そのコンテキストが設定されると、MCP サーバーは残りのセッションにコンテキストを使用します。
>
>一部のツールは、実行前に承認を求めます。 提案されたアクションを確認し、承認または拒否します。確認がなければアクションは実行されません。

## 手順1：環境ステータスの確認

リリースを開始する前に、環境が正常であり、アクティブに実行されていないことを確認します。

```
What is the status of the production environment?
```

+++回答の例を見る

![Cloud Managerの本番環境のステータスを表示するAI クライアント &#x200B;](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step1-01-ai.png)

+++


## ステップ 2: パイプライン実行の確認

最近のパイプライン履歴を確認して、デプロイメントパターンを理解し、次のリリースをブロックする前にエラーを検出します。

```
Show me the last five pipeline runs for the production pipeline.
```

+++回答の例を見る

実稼動パイプラインの最後の5つのパイプライン実行を示す![AI クライアント &#x200B;](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step2-01-ai.png)

+++


## ステップ 3: パイプラインのトリガー

AI クライアントから直接パイプラインを開始します。 サーバーはターゲット環境を確認し、開始する前に承認を求めます。

```
Run the Fullstack pipeline against dev environment of WKND sandbox program.
```

+++回答の例を見る

![&#x200B; パイプラインのトリガー確認と、実行中のパイプラインを反映したCloud Manager UIを表示するAI クライアント &#x200B;](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step3.gif)

+++


>[!CAUTION]
>
>AI クライアントは、実行をトリガーする前に、パイプライン名の確認を求めます。 正確なパイプライン名を入力して続行します。 確認する前に、特に実稼動環境にデプロイするパイプラインについて、ターゲット環境を慎重に確認します。

## 手順4：パイプラインステータスの確認

実行をトリガーした後、Cloud Manager インターフェイスに切り替えずに、AI クライアントにステータスの更新を依頼します。

```
What is the status of the triggered pipeline?
```

+++回答の例を見る

![&#x200B; トリガーされたパイプライン実行のステータスを表示するAI クライアント &#x200B;](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step4-01-ai.png)

+++


## 達成したこと

AEM Cloud Manager MCP Serverを使用すると、Cloud Manager インターフェイスを開かずに、環境の正常性の確認、パイプライン履歴の確認、デプロイメントのトリガー、ステータスの検証を行うことができます。 開発部門と運用部門は、環境の可視化と展開の制御を単一のAI セッションで組み合わせることで、問題により迅速に対応し、既に使用しているツールの中でワークフローを維持することができます。

## より多くのことを達成

Cloud Manager MCP Serverは、上記のチュートリアルよりもはるかに多くの処理を処理します。 以下のシナリオを展開すると、同じセッションで試すことができるプロンプトが表示されます。

+++リリースが公開される前に問題を発見する

パイプラインを実行する前に表示されていた理由で、デプロイメントが失敗することがよくあります。 これらのプロンプトは、環境の正常性を確認し、競合する実行を確認し、リリースにコミットする前に環境間のバージョン調整を検証するのに役立ちます。

**プロンプト**

```
We're about to kick off a production release. Give me a full status check on all environments first.
```

```
Is there anything currently running in the staging pipeline? I don't want to queue on top of an active run.
```

```
Before I promote main branch to production, confirm main was deployed to Dev and all environments are on the same AEM version.
```

```
What repositories are connected to the WKND program?
```

+++

+++既に実行中のデプロイメントのコース修正

偶発的なトリガーや停滞した承認ゲートは、ブロックされたパイプラインや望ましくないデプロイにカスケード接続される可能性があります。 これらのプロンプトを使用すると、Cloud Manager インターフェイスに切り替えることなく、実行中のパイプラインをキャンセルまたは進行できます。

**プロンプト**

```
The staging pipeline kicked off by mistake. Cancel it before it deploys.
```

```
The release pipeline is waiting at the approval gate. Advance it to continue the deployment.
```

+++

+++デプロイメントの実績を把握

最後に成果を上げたタイミング、パイプラインの実行時間、パターンの変化を把握することで、インシデントが発生する前にリリースを計画し、時間のかかる劣化を特定することができます。 必要に応じて履歴を取得できます。

**プロンプト**

```
What is the status of the last production pipeline execution? If it failed, explain why.
```

```
When was the last successful deployment to the staging environment?
```

```
Our pipeline times are creeping up. What's the longest run we've had in the last 30 days?
```

+++

+++壊れたビルドを元に戻す

パイプラインが失敗した場合、解決への最短の道は、パイプラインが破損した場所とその理由を正確に把握することです。 これらのプロンプトを通じて障害の詳細、変更履歴、品質ゲートの問題を明らかにし、ログを手動で調べることなく診断と修正を実施できます。

**プロンプト**

```
We're seeing a regression on the live site. What changed in production over the last week?
```

```
Which pipelines have failed in the last 7 days, and at what stage did they fail?
```

```
The last pipeline failed at the code quality step. What specific issues need to be fixed before I can retry?
```

```
Pull the step logs for the last failed run. I need to see exactly what the quality gate flagged.
```

+++


## 詳細情報

| リソース | 見つかる内容 |
| --- | --- |
| [AEM Cloud Manager ドキュメント &#x200B;](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/introduction-to-cloud-manager) | Adobe Cloud Managerのドキュメント |
| [AEM as a Cloud Service のドキュメント](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service) | Adobe AEMのドキュメント |
| [MCP サーバー](../tools/mcp-servers.md) | AI クライアントをAdobe MCP サーバーに接続する |
