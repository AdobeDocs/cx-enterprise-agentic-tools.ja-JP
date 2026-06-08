---
title: パフォーマンスデータに基づくコンテンツの最適化
description: CJAとAEMのMCP サーバーを連携することで、ツールを切り替えることなく、パフォーマンスの低いコンテンツを特定して更新できます。
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 3%

---


# パフォーマンスデータに基づくコンテンツの最適化

<!-- last-modified: 2026-05-21 -->

![ パフォーマンスデータに基づいてコンテンツを最適化](https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data)

コンテンツパフォーマンスデータとコンテンツの更新を連携させるには、通常、Adobe AnalyticsとAdobe CMSを切り替える必要があります。 このチュートリアルでは、Customer Journey AnalyticsとAEMを同じAI セッションで連携させて、パフォーマンスの低いページを特定して更新する方法を説明します。

| | |
| --- | --- |
| CX エンタープライズアプリケーション | Customer Journey Analytics、Adobe Experience Manager as a Cloud Service |
| エージェント型ツール | CX Enterprise MCP Gateway、AEM Content MCP Server |
| オーディエンス | キャンペーンマネージャー，コンテンツストラテジスト，マーケティングオペレーション |
| 前提条件 | MCP対応AI クライアント、CJAアクセス、AEM as a Cloud Serviceアクセス |

各ステップは、代表的なプロンプトとAI応答の例を示しています。 同じセッションで追加の探索を行うために、**さらに達成できる**&#x200B;のセクションを次に示します。

## 始める前に

>[!BEGINTABS]

>[!TAB  クロード.ai]

両方のMCP サーバーをカスタムコネクタとして接続します。 それぞれを別々に追加します。

1. Claude.aiの&#x200B;**設定/統合**&#x200B;に移動します。
2. **カスタムコネクタを追加**&#x200B;を選択し、サーバーURLを入力して、**接続**&#x200B;を選択します。
3. Adobe IDでログインし、2台目のサーバーに対してこれを繰り返します。

| サーバー | エンドポイント |
| --- | --- |
| CX Enterprise MCP Gateway | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP Server | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

完全なセットアップ：[Claude.ai カスタムコネクタのドキュメント ](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

ChatGPT デベロッパーモードを使用して両方のMCP サーバーを接続します（Pro、Plus、Business、Enterprise、またはEducation プランが必要）。 各サーバーを個別に追加します。

1. **ChatGPT設定**&#x200B;で&#x200B;**開発者モード**&#x200B;を有効にします。
2. **設定/統合**&#x200B;に移動し、**カスタムコネクタを追加/リモート MCP サーバー**&#x200B;を選択します。
3. サーバーURLを入力し、**Connect**&#x200B;を選択して、Adobe IDでログインします。
4. 2番目のサーバーに対してこれを繰り返します。

| サーバー | エンドポイント |
| --- | --- |
| CX Enterprise MCP Gateway | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP Server | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

完全なセットアップ：[ChatGPT MCP ドキュメント ](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB その他のAI クライアント ]

Gemini、Microsoft Copilot、Cursor、Claude CodeなどのMCP互換アプリケーションを使用している場合、 以下のエンドポイントを使用して、両方のMCP サーバーに接続します。

| サーバー | エンドポイント |
| --- | --- |
| CX Enterprise MCP Gateway | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP Server | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

サポートされているすべてのクライアントの完全なセットアップ手順：[AI クライアントに接続](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>プロンプトが表示されたらAdobe IDでログインし、CJAおよびAEM環境にリンクされているIMS組織を選択します。 間違った組織を選択することは、認証エラーの最も一般的な原因です。
>
>最初の接続時に、AI クライアントからIMS組織の選択またはサンドボックスの指定を求められる場合があります。 そのコンテキストが設定されると、MCP サーバーは残りのセッションにコンテキストを使用します。
>
>一部のツールは、実行前に承認を求めます。 リクエストを確認し、承認または辞退します。確認がなければアクションは実行されません。

## ステップ 1：パフォーマンスの低いコンテンツの特定

CX Enterprise MCP Gatewayを使用して、Customer Journey Analyticsのエンゲージメント指標とコンバージョン指標でページをランク付けします。 目標は、注意が必要な明確で優先順位付けされたコンテンツリストです。

```
Show me the 10 pages with the lowest engagement rate over the last 60 days.
```

+++回答の例を見る

最も低いエンゲージメントページ（2026年3月22日～5月21日）:

| ランク | ページ | エンゲージメント率 | バウンス率 | 平均。 ページ滞在時間 |
| --- | --- | --- | --- | --- |
| 1 | /en/products/analytics | 8.2% | 74% | 0:42 |
| 2 | /en/resources/whitepapers | 9.1% | 71% | 0:38 |
| 3 | /en/solutions/retail | 10.4% | 69% | 0:51 |
| 4 | /en/blog/2025-q4-recap | 11.0% | 68% | 0:44 |
| 5-10 | ... | 12.3～14.1% | 63～67% | 0:35-1:10 |

サイト平均エンゲージメント率は34.7%です。 これらのページは平均の2～4倍です。

+++

## 手順2:AEMのコンテンツを確認する

AI セッションを終了することなく、AEMからページの現状を取り込むことができます。 コンテンツの内容を理解することは、何を変えるべきかを知るための最初のステップです。

```
Show me the current content on the /en/products/analytics page in AEM.
```

+++回答の例を見る

**ページ：** `/en/products/analytics`
**最終更新日：** 2026年4月30日T. MacMillan
**ステータス：**&#x200B;公開済み

**ヒーローセクション：**
見出し：「あらゆる部門でデータにもとづく意思決定」
小見出し：「Adobe Analyticsは、企業がアクションを実行するためのインサイトを提供します」
CTA:「導入のご相談」 → /contact/demo

**本文：** 3つの機能ブロックの後に、お客様のロゴ ストリップとセカンダリ CTAが続きます。 ビデオやインタラクティブな要素がありません。 このページは21日間更新されていません。

**Metaの説明：** 「Adobe Analytics：企業チーム向けのリアルタイムのレポートとAI インサイト」

+++

## ステップ 3：ターゲットを絞った更新

パフォーマンスデータと現在のコンテンツを確認したら、データが示した内容にもとづいて更新を行います。

```
Update the hero headline on the analytics product page to Make faster decisions with AI-powered analytics.
```

+++回答の例を見る

**変更を提案：**

| フィールド | 現在の値 | 新しい値 |
| --- | --- | --- |
| Hero headline | あらゆる部門にデータにもとづく意思決定 | AIを活用した分析で意思決定を迅速化 |

ページ：`/en/products/analytics`

この変更を確認しますか？ 「はい」と返信すると、更新がAEMに書き込まれます。 明示的に再公開するまで、ページは現在の状態で公開されたままになります。

+++

>[!CAUTION]
>
>プロンプトが表示されたら、各コンテンツの変更を確認します。 ライブページの更新を承認する前に、完全な差分を確認してください。

## 手順4：検証と公開

変更内容をすべて確認し、更新に満足したらコンテンツをプロモーションして、ループを終了します。

```
Show me a summary of all changes made in this session.
```

+++回答の例を見る

**セッションの概要 – 2026年5月21日：**

| ページ | 変更 | ステータス |
| --- | --- | --- |
| /en/products/analytics | ヒーローの見出しを更新 | 保存済み、未公開 |

1 ページ更新しました。 確認したら公開する準備ができました。

**残りの低エンゲージメントリスト：** 9 ページは、このセッションで更新されていません。 次のページを続行するか、公開前にバッチ レビュー用のローンチを作成しますか？

+++

## 達成したこと

Customer Journey AnalyticsとAEMを単一のAI セッションで連携し、パフォーマンスデータを使用してコンテンツの変更を直接通知しました。 ツールを切り替えずに指標から更新に移行することで、Analytics insightと公開コンテンツのフィードバックループを短縮しました。 これは、大規模な施策では特に重要です。何十ものページで注意が必要となり、手作業によるクロスツールのワークフローで遅延が発生することがあります。

## より多くのことを達成

CJAとAEM MCP サーバーは、問題の特定から問題の解決までのサイクル全体をサポートします。 以下のシナリオを展開すると、同じセッションで試すことができるプロンプトが表示されます。

+++パフォーマンスを妨げているコンテンツを特定

エンゲージメントが低いトラフィックは、トラフィックの問題ではなく、コンテンツの問題を示します。 これらのプロンプトを活用することで、キャンペーンが期限を迎える前に注意が必要な特定のページやパターンを特定することができます。

**プロンプト**

```
Show me the 10 pages with the lowest conversion rate this quarter.
```

```
Which pages have a high bounce rate but also high traffic?
```

```
Compare engagement rates for blog posts versus product pages.
```

```
Find AEM pages that haven't been updated in over 60 days.
```

+++

+++データの内容を修正する

パフォーマンスが低い施策を把握したら、次のステップは的を絞った変更です。 これらのプロンプトを使用して、パフォーマンスデータで明らかになった内容に基づいて、見出し、CTA、メタディスクリプションを更新できます。

**プロンプト**

```
Update the CTA on the /en/solutions/retail page to 'See how it works'.
```

```
Add a note to the hero subheadline on the analytics page: Now with AI-powered anomaly detection.
```

```
Update the meta description on all pages in /en/products/ that contain the word 'legacy'.
```

```
Which pages updated in this session still need their CTAs reviewed?
```

+++

+++次のキャンペーンの前に改善を出荷する

セッション中に加えた変更は、すぐに積み重なることができます。 これらのプロンプトは準備状況を確認し、更新をレビュー可能なローンチにグループ化し、キャンペーンが公開される前にクリーンにプロモーションするのに役立ちます。

**プロンプト**

```
Show me all pages updated in this session that are still unpublished.
```

```
Create a launch with all changes from this session for review before publishing.
```

```
Give me a summary of all changes made in this session.
```

```
Promote everything in the current launch to production.
```

+++

## 詳細情報

| リソース | 見つかる内容 |
| --- | --- |
| [Analytics MCP ドキュメント ](https://developer.adobe.com/analytics-mcp/docs/) | CJA MCPの設定とツールリファレンス |
| [AEM as a Cloud Service のドキュメント](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service) | Adobe AEMのドキュメント |
| [AI レジストリのCJA MCP Server](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | CJA MCP Serverのツールと機能 |
| [AI レジストリのAEM Content MCP Server](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) | AEM Content MCP Serverのツールと可用性 |
| [MCP サーバー](../tools/mcp-servers.md) | AI クライアントをAdobe MCP サーバーに接続する |
