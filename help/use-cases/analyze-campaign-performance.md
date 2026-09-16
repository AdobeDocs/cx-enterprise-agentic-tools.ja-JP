---
title: レポートを作成することなくキャンペーンのインサイトを可視化
description: Customer Journey Analytics MCP Serverを使用して、簡単な言葉でパフォーマンスに関する質問をおこない、レポートビルダーを移動することなく回答を得ることができます。
last-substantial-update: 2026-09-16
source-git-commit: a70eede6e0efe0d1dbdc00c5d9de5aeb3b5d75de
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 4%
---

# レポートを作成することなくキャンペーンのインサイトを可視化

<!-- last-modified: 2026-06-02 -->

![ キャンペーンのパフォーマンスを向上させるための次のステップを推奨するAI クライアント ](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png){zoomable="yes"}

*選択してズームします。*

以前は別のツールでレポートを作成する必要があったキャンペーン分析も、今では会話になっています。 このチュートリアルでは、AI クライアントをCustomer Journey Analytics（CJA）に接続し、パフォーマンスに関する質問を平易な言葉で行う方法を説明します。 これにより、insightへの移行が迅速化され、手作業によるレポート作成は不要になります。

| シナリオの詳細 | |
| --- | --- |
| CX エンタープライズアプリケーション | [Customer Journey Analytics （CJA） ](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-overview) |
| エージェント型ツール | [CX Enterprise Coworker](https://experienceleague.adobe.com/ja/docs/cx-enterprise-coworker/content/home)または[Customer Journey Analytics MCP Server](../tools/mcp-servers.md) |
| オーディエンス | アナリスト、キャンペーンマネージャー |
| 前提条件 | MCP対応AI クライアント、CJAアクセス |

各ステップは、代表的なプロンプトとAI応答の例を示しています。 同じセッションで追加の探索を行うために、**さらに達成できる**&#x200B;のセクションを次に示します。

## 始める前に

>[!BEGINTABS]

>[!TAB CX Enterprise Coworker]

これらの質問に答える最も簡単な方法はCX Enterprise Coworkerです。では、サーバーのセットアップやAI クライアントの設定は必要ありません。 [CX Enterprise Coworkerを試す](https://experienceleague.adobe.com/ja/docs/cx-enterprise-coworker/content/home)

独自のAI クライアントをCustomer Journey Analyticsに直接接続する場合は、以下のタブを参照してください。

>[!TAB  クロード.ai]

Customer Journey Analytics MCP Serverをカスタムコネクタとして接続します。

1. Claude.aiの&#x200B;**設定/統合**&#x200B;に移動します。
2. **カスタムコネクタを追加**&#x200B;を選択し、サーバーURLを入力します：`https://cja-mcp.adobe.io/mcp`
3. **Connect**&#x200B;を選択し、Adobe IDでログインします。

完全なセットアップ：[Claude.ai カスタムコネクタのドキュメント ](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

ChatGPT Developer Modeを使用してCustomer Journey Analytics MCP Serverに接続します（Pro、Plus、Business、Enterprise、またはEducation プランが必要）。

1. **ChatGPT設定**&#x200B;で&#x200B;**開発者モード**&#x200B;を有効にします。
2. **設定/統合**&#x200B;に移動し、**カスタムコネクタを追加/リモート MCP サーバー**&#x200B;を選択します。
3. サーバーURLを入力してください：`https://cja-mcp.adobe.io/mcp`
4. **Connect**&#x200B;を選択し、Adobe IDでログインします。

完全なセットアップ：[ChatGPT MCP ドキュメント ](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB その他のAI クライアント ]

Gemini、Microsoft Copilot、Cursor、Claude CodeなどのMCP互換アプリケーションを使用している場合、 次のエンドポイントを使用してCustomer Journey Analytics MCP Serverに接続します。

```
https://cja-mcp.adobe.io/mcp
```

サポートされているすべてのクライアントの完全なセットアップ手順：[AI クライアントに接続](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>プロンプトが表示されたらAdobe IDでログインし、CJA データビューにリンクされているIMS組織を選択します。 間違った組織を選択することは、認証エラーの最も一般的な原因です。
>
>最初の接続時に、AI クライアントからIMS組織の選択またはサンドボックスの指定を求められる場合があります。 そのコンテキストが設定されると、MCP サーバーは残りのセッションにコンテキストを使用します。
>
>一部のツールは、実行前に承認を求めます。 リクエストを確認して承認または辞退します。 確認なしにアクションは実行されません。

## 手順1：利用可能なデータビューの確認

まず、AI クライアントに、CJAアカウントで利用可能なデータビューのリストを依頼します。 レポートを実行する前にクエリできるデータセットを示します。

```
What data views are available in my CJA account?
```

+++回答の例を見る

![使用可能なCJA データビューのAI クライアントリスト ](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step1-data-views.png){zoomable="yes"}

*選択してズームします。*

+++


## ステップ 2：施策のパフォーマンスデータの取得

データビューを特定し、収益とコンバージョン率ごとにキャンペーンのパフォーマンスを確認します。 AIは、技術的なIDを必要とせずに、データビューから指標とディメンションの名前を解決します。

```
For '[data view name]', show me the top campaigns by revenue and conversion rate for the last 30 days.
```

+++回答の例を見る

オムニチャネルのマルチインダストリーデータビューから収益とコンバージョン率で上位キャンペーンを表示する![AI クライアント ](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step2.gif){zoomable="yes"}

*選択してズームします。*

+++


>[!NOTE]
>
>`[data view name]`を手順1のデータビューの名前に置き換えます。 関係者と共有する前に、同じデータビューと日付範囲を使用して、Analysis Workspaceで結果をクロスチェックします。

## ステップ 3：パフォーマンスを促進する要因を特定する

AI クライアントに、キャンペーングループ間のパフォーマンスの違いを何が促しているのかを説明してもらいます。 見出し番号から下の変数に移動します。

```
What factors are driving the results for these campaign groups?
```

+++回答の例を見る

![ キャンペーングループのパフォーマンスを促進する要因を説明するAI クライアント ](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step3.gif){zoomable="yes"}

*選択してズームします。*

+++


## ステップ 4：特定のキャンペーンタイプをドリルダウンする

セグメントレベルの内訳を尋ねることで、特定の結果をフォローアップできます。 これにより、キャンペーンタイプ内でどの顧客タイプがパフォーマンスを促進しているのかを把握できます。

```
Break down Promotional Email Campaigns by Customer Segment and explain what's driving the high conversion rate.
```

+++回答の例を見る

![AI クライアントが顧客セグメント別のプロモーションメールキャンペーンのパフォーマンスを分析](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step4-segment-breakdown.png){zoomable="yes"}

*選択してズームします。*

+++


## ステップ 5：発見したことに対して行動する

セッションで表示されたあらゆる情報にもとづいて、優先順位付けされたレコメンデーションを要求できます。 ビジネス価値の見積もりを依頼することは、最初にどこで行動すべきかを決定するのに役立ちます。

```
Based on these findings, recommend the highest-impact actions to increase revenue and conversion rates. Prioritize recommendations by expected business value and estimate the potential uplift.
```

+++回答の例を見る

![ ビジネス価値の見積もりで優先順位付けされたアクションを推奨するAI クライアント ](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5.gif){zoomable="yes"}

*選択してズームします。*

+++


>[!NOTE]
>
>CJAのツールは、CJA内で、セグメント、計算指標、Workspaceプロジェクトを同じセッションで作成できます。 他のアプリケーションのキャンペーン、ジャーニー、コンテンツを更新するには、関連するMCP サーバーを接続するか、アプリケーションに直接移動します。

## 達成したこと

AI クライアントとCustomer Journey Analyticsを接続し、5つのプロンプトでデータビューの発見からビジネスのレコメンデーションの優先順位付けへと移行しました。 収益とコンバージョン率によって上位のキャンペーンを特定し、キャンペーングループ間のパフォーマンスを促進する要因を明らかにして、特定のキャンペーンタイプに関するセグメントレベルの詳細をドリルダウンし、予想上昇率のランク付きレコメンデーションを受け取りました。 このアプローチにより、レポート作成は、直接的な会話に置き換わり、ビジネス上の質問とデータにもとづいた行動計画との間の時間を短縮できます。

## より多くのことを達成

Customer Journey Analytics MCP Serverは、チュートリアルで学ぶよりもはるかに多くのインサイトを獲得することができます。 以下のシナリオを展開すると、同じセッションで試すことができるプロンプトが表示されます。

+++効果的なものと効果的でないものを見つける

どの施策が成果を上げているのか、どの施策が成果を上げていないのかを容易に把握できるため、詳細なレポートを作成する前に、労力を集中させることができます。 これらのプロンプトを使用すると、1つのセッションでその画像が表示されます。

**プロンプト**

```
Which campaigns are driving the most revenue and conversions?
```

```
Show me the campaigns that need attention this month.
```

```
What channels are outperforming expectations?
```

```
Identify the biggest performance changes compared to last month.
```

```
Show me conversion performance by traffic source.
```

+++

+++成果を上げている要素の把握

見出し指標は、何が起こったのかを教えてくれます。 次のプロンプトは、その理由を理解するのに役立ちます。数字の背後にあるセグメント、チャネル、顧客接点を理解する。

**プロンプト**

```
What factors are driving revenue growth?
```

```
Explain why conversion rates changed this quarter.
```

```
Break down campaign performance by customer segment.
```

```
Which customer segments are growing fastest?
```

```
Which touchpoints contribute most to conversions?
```

+++

+++成長の機会を特定

パフォーマンスが優れている理由を把握できても、その範囲は広くありません。 これらのプロンプトは、より多く投資できる場所、ヘッドルームのあるオーディエンス、拡張できるキャンペーンを特定するのに役立ちます。

**プロンプト**

```
Where should we invest more marketing budget?
```

```
Which audiences have the greatest growth potential?
```

```
Which campaigns should we scale?
```

```
What would have the biggest impact on revenue?
```

+++

+++「

CJAを利用すれば、AIのセッションから離れることなく、CJAでセグメント、オーディエンス、計算指標、Workspaceプロジェクトを直接作成できます。 これらのプロンプトを使用して、発見したことに基づいて行動します。

**プロンプト**

```
Create a segment for high-value customers.
```

```
Build an audience from recent purchasers.
```

```
Create a calculated metric for conversion efficiency.
```

```
Save this analysis as a Workspace project for executive reporting.
```

+++


## 詳細情報

| リソース | 見つかる内容 |
| --- | --- |
| [AI レジストリのCJA MCP Server](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp){target="_blank"} | CJA MCP Serverのツールと機能 |
| [Customer Journey Analytics ドキュメント ](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-landing){target="_blank"} | Adobe CJAのドキュメント |
