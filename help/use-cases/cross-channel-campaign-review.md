---
title: クロスチャネルキャンペーンのレビューの実施
description: 単一のAI セッションでCX Enterprise MCPを使用し、ジャーニー、オーディエンス、パフォーマンスをまたいで、AJO、CJA、Real-Time CDPのキャンペーンの健全性を一元的に把握できます。
last-substantial-update: 2026-06-09T00:00:00Z
index: false
source-git-commit: 6a2b8b54eb9fe040f5f9defa9e6681e46a5e65cf
workflow-type: tm+mt
source-wordcount: '1412'
ht-degree: 5%

---


# クロスチャネルキャンペーンのレビューの実施

<!-- last-modified: 2026-05-21 -->

![ クロスチャネルキャンペーンレビューの実行](https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review)

キャンペーンの健全性を包括的に把握するには、複数のシステムからのデータが必要です。AJOのアクティブジャーニー、Real-Time CDPのオーディエンスアクティベーションステータス、CJAのパフォーマンス指標などです。 このチュートリアルでは、3つのAI セッションすべてを接続する方法を示します。これにより、3つの個別のツールではなく、1つの会話でジャーニーのステータスからオーディエンスの健全性、パフォーマンスのトレンドに移行できます。

| シナリオの詳細 | |
| --- | --- |
| CX エンタープライズアプリケーション | [Adobe Journey Optimizer](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/ajo-home)、[Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview)、[Real-Time CDP](https://experienceleague.adobe.com/ja/docs/experience-platform/rtcdp/home) |
| エージェント型ツール | [CX エンタープライズ MCP](../tools/mcp-servers.md#cx-enterprise-mcp-servers) |
| オーディエンス | キャンペーンマネージャー，マーケティングオペレーション |
| 前提条件 | MCP対応のAI クライアント、AJO、CJA、Real-Time CDPへのアクセス |

各ステップは、代表的なプロンプトとAI応答の例を示しています。 同じセッションで追加の探索を行うために、**さらに達成できる**&#x200B;のセクションを次に示します。

## 始める前に

>[!BEGINTABS]

>[!TAB  クロード.ai]

CX Enterprise MCPをカスタムコネクタとして接続します。 1つの接続からAJO、CJA、Real-Time CDP ツールにアクセスできます。

1. Claude.aiの&#x200B;**設定/統合**&#x200B;に移動します。
2. **カスタムコネクタを追加**&#x200B;を選択し、サーバーURLを入力します：`https://cx-enterprise.adobe.io/mcp`
3. **Connect**&#x200B;を選択し、Adobe IDでログインします。

完全なセットアップ：[Claude.ai カスタムコネクタのドキュメント ](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

ChatGPT デベロッパーモードを使用してCX エンタープライズ MCPを接続します（Pro、Plus、Business、Enterprise、またはEducation プランが必要）。

1. **ChatGPT設定**&#x200B;で&#x200B;**開発者モード**&#x200B;を有効にします。
2. **設定/統合**&#x200B;に移動し、**カスタムコネクタを追加/リモート MCP サーバー**&#x200B;を選択します。
3. サーバーURLを入力してください：`https://cx-enterprise.adobe.io/mcp`
4. **Connect**&#x200B;を選択し、Adobe IDでログインします。

完全なセットアップ：[ChatGPT MCP ドキュメント ](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB その他のAI クライアント ]

Gemini、Microsoft Copilot、Cursor、Claude CodeなどのMCP互換アプリケーションを使用している場合、 次のエンドポイントを使用してCX Enterprise MCPに接続します。

```
https://cx-enterprise.adobe.io/mcp
```

サポートされているすべてのクライアントの完全なセットアップ手順：[AI クライアントに接続](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>プロンプトが表示されたらAdobe IDでログインし、AJO、CJAおよびReal-Time CDP環境にリンクされているIMS組織を選択します。 間違った組織を選択することは、認証エラーの最も一般的な原因です。
>
>最初の接続時に、AI クライアントからIMS組織の選択またはサンドボックスの指定を求められる場合があります。 そのコンテキストが設定されると、MCP サーバーは残りのセッションにコンテキストを使用します。
>
>一部のツールは、実行前に承認を求めます。 リクエストを確認して承認または辞退します。 確認なしにアクションは実行されません。

## ステップ 1：アクティブなジャーニーとキャンペーンの確認

AJOを導入し、現在実行している施策を把握する。 公開中のジャーニーと最近変更されたジャーニーを把握することで、残りのレビューの基盤を構築できます。

```
What journeys are currently active in AJO?
```

+++回答の例を見る

AJOで8つのアクティブなジャーニーが見つかりました。

| ジャーニー | チャネル | 最終変更日 |
| --- | --- | --- |
| ウェルカムシリーズ：新メンバー | 電子メール、プッシュ | 2026年5月18日（PT） |
| 購入後のフォローアップ | 電子メール，SMS | 2026年5月14日（PT） |
| ロイヤルティ再エンゲージメント | メール | 2026年5月20日（PT） |
| カート放棄：24時間 | 電子メール，SMS | 2026年5月10日（PT） |
| 春プロモーション | 電子メール、プッシュ | 2026年5月19日（PT） |
| ウィンバック：90日間の非アクティブ | メール | 2026年4月28日（PT） |
| バースデイ・リワード | メール | 2026年4月15日（PT） |
| リエンゲージメント：プッシュオプトアウト | SMS | 2026年5月12日（PT） |

過去7日間に3つのジャーニーが変更されました。 これらのいずれかに関する詳細が必要ですか？

+++


## 手順2：オーディエンスのアクティベーションステータスの確認

ジャーニーを表示して、これらのキャンペーンを強化しているオーディエンスが、配信先に正しく流れていることを確認します。

```
Show me the activation status for the high-value loyalty segment.
```

+++回答の例を見る

**価値の高いロイヤルティセグメント**：宛先をまたいだアクティベーションステータス：

| 宛先 | ステータス | 前回成功した実行 | オーディエンスサイズ |
| --- | --- | --- | --- |
| Google 広告 | アクティブ | 2026年5月21日午前02:14 | 48,320 |
| Meta Ads | アクティブ | 2026年5月21日午前01:58 | 48,295 |
| Salesforce Marketing Cloud | アクティブ | 2026年5月20日午後11:30 | 47,940 |
| Adobe Target | アクティブ | 2026年5月21日午前12:00 | 48,320 |

データフローエラーが検出されませんでした。 すべてのアクティベーションは、過去3時間以内に完了しました。

+++


## ステップ 3:CJAからパフォーマンス指標を取得する

ジャーニーとオーディエンスのコンテキストを確立したら、CJAを使用して、そうしたキャンペーンがどのようにコンバージョンに達し、エンゲージメントがどこで低下するかを評価します。

```
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
```

+++回答の例を見る

**ロイヤルティ再エンゲージメントキャンペーン**: 2026年4月21日～5月21日：

| チャネル | 送信数 | CTR | コンバージョン数 | Conv. 割合 |
| --- | --- | --- | --- | --- |
| メール | 48,320 | 8.4% | 1,973 | 4.1% |
| プッシュ | 31,200 | 12.1% | 987 | 3.2% |

コンバージョン率：3.8% メール CTRは、前の30日間に対して1.2%増加しました。 プッシュコンバージョンは横ばいです。

+++


## ステップ 4: キャンペーンのヘルスサマリーの合成

AI クライアントに、3つのソースすべてで画像を統合し、注意が必要なものを表示するように依頼します。

```
Give me a summary of our campaign health: what is running, which audiences are activated, and how performance looks against last month.
```

+++回答の例を見る

以下に、AJO、Real-Time CDP、CJAの現在のキャンペーンの健全性の概要を示します。

**アクティブなジャーニー：** 8件がライブで、3件が今週変更されました。 ロイヤルティ再エンゲージメントジャーニーは最新の状態です。

**オーディエンスのアクティブ化：**&#x200B;すべてのセグメントが4つの宛先に正しく流れています。 データフローエラーが検出されませんでした。

**パフォーマンス：**&#x200B;電子メール CTRは、ロイヤルティキャンペーン全体で上昇しています。 プッシュコンバージョンは横ばいです。 大きく低下しているチャネルはない。

**注目用フラグ：**

- ウィンバックジャーニー（90日間の非アクティブ）は23日前に最終変更され、最近レビューされていません。
- プッシュコンバージョン率は3期連続で横ばいであり、メッセージやタイミングを見直す価値があります。

重大な問題は検出されませんでした。 上記の2つの項目は、次のキャンペーン開始の前にレビューが必要です。

+++


ここで、マルチサーバーアプローチの出番です。AI クライアントの理由を、ジャーニーの設定、オーディエンスステータス、パフォーマンスデータをまたいで1回の会話で確認できます。

## ステップ 5：発見したことに対して行動する

審査には2つの項目がありました。 AI クライアントに、それぞれの優先順位とルーティングを支援してもらいましょう。

```
For each flag you identified, what should I do and where should I go to do it?
```

+++回答の例を見る

以下は、2つのフラグの優先順位付けされたアクションプランです。

**1. Win-Back ジャーニー – 再入力条件のレビュー（AJO MCP、変更が必要な場合はAJO アプリケーション）**

「ウィンバック」ジャーニーは、23日間は変更されていません。 現在の再エントリ条件と離脱ロジックについて説明してもらいます。 条件が古くなったり、正しく見えない場合は、ジャーニーフローの構造的な変更を行うには、AJOを開く必要があります。 頻度の上限とオーディエンスの更新は、ここで行うことができます。

**2. コンバージョンを3期間フラットにプッシュ – メッセージの更新またはバリエーションのテスト**

通常、フラットコンバージョンは、メッセージの疲労や、オファーとオーディエンスの不一致を示します。 2つのパス：

- **今すぐプッシュコンテンツを更新（AEM MCP）:** プッシュ通知がランディングページにリンクする場合は、AEM Content MCP Serverを追加し、ツールを切り替えずにページコピーまたはCTAを更新します。
- **プッシュ A/B テストを実行する（AJO アプリケーション）:**&#x200B;異なるメッセージングを持つキャンペーンレベルのバリエーションを作成して、それがコンテンツであるかターゲティングであるかを判断します。 AJOに直接移動する必要があります。

どのフィールドから始めますか？

+++


## 達成したこと

AJO、Real-Time CDP、CJAを1つのAI セッションに接続して、クロスチャネルのキャンペーン正常性レビューを実行しました。 3つのアプリケーションを開いて画像を手作業で組み立てるのではなく、ジャーニーのステータス、オーディエンスのアクティベーション、パフォーマンスデータを、ひとつの会話で確認することができます。 この要約により、キャンペーンマネージャーは、何が機能しているのか、何を調整する必要があるのか、次に注力すべき場所を特定するための迅速な方法を得ることができます。

## より多くのことを達成

AJO、CJA、Real-Time CDPを同じセッションで接続することで、チュートリアルの枠を超えることができます。 以下のシナリオを展開して、試せるプロンプトを表示します。

+++新しい施策を立ち上げる前に、現在の状況を正確に把握しましょう

重複するジャーニー、最近変更されたキャンペーン、まだレビューしていないチャネルはすべて、新しいローンチに影響を与える可能性があります。 これらのプロンプトを使用すると、何かを追加する前に現在の状態を明確に把握できます。

**プロンプト**

```
Which journey has the most active profiles right now?
```

```
Show me all journeys modified in the last 7 days.
```

```
Which campaigns are scheduled to end this week?
```

```
Are any journeys targeting the same segment as the campaign I'm about to launch?
```

+++

+++オーディエンスが適切な配信先にリーチしていることを確認し

アクティベーションの問題は沈黙し、セグメントの流れが止まり、警告なしでキャンペーンがより小さなリストに送信されます。 これらのプロンプトは、結果に影響を与える前に、ギャップやエラーを表します。

**プロンプト**

```
Which audiences have grown the most in the last 30 days?
```

```
Are there any dataflow errors across my active destinations?
```

```
How many records were exported to each destination in the last 7 days?
```

```
Are there any audiences with no active destinations?
```

+++

+++何が機能して、どこに集中すべきかを把握できます

チャネル全体のパフォーマンストレンドにより、どこに投資し、何を後押しするべきかを把握できます。 これらのプロンプトは、成果を上げている要素や、今後の施策で注目すべき点を特定するのに役立ちます。

**プロンプト**

```
Show me email performance trends for the last 90 days.
```

```
Which campaigns are underperforming against their conversion targets?
```

```
What is the average revenue per conversion this month compared to last month?
```

```
Which channel has the highest conversion rate across all active campaigns?
```

+++


## 詳細情報

| リソース | 見つかる内容 |
| --- | --- |
| [AJO ドキュメント ](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/ajo-home){target="_blank"} | Adobe AJOのドキュメント |
| [AI レジストリのAJO MCP Server](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server){target="_blank"} | AJO MCP Serverのツールと機能 |
| [AI レジストリのCJA MCP Server](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp){target="_blank"} | CJA MCP Serverのツールと機能 |
