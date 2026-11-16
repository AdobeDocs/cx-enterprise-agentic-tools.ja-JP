---
title: 顧客に影響を与える前に、ジャーニーの問題を把握したい
description: Adobe Journey Optimizer MCP Serverを使用して、アクティブなAJOジャーニーをモニタリングし、キャンペーン設定をレビューし、オーディエンスにリーチする前に運用上の問題を特定します。
last-substantial-update: 2026-11-16
source-git-commit: a75d5f3af3077b259da796bd381d605ae826585d
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 3%
---

# 顧客に影響を与える前に、ジャーニーの問題を把握したい
<!-- last-modified: 2026-06-08 -->

![&#x200B; エグゼクティブサマリーを使用してキャンペーンとジャーニー戦略を要約するAI プラットフォーム &#x200B;](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png){zoomable="yes"}

*選択してズームします。*

ジャーニーの問題が検出されなければ、誰にも気づかれないうちに顧客にリーチできます。 このチュートリアルでは、Adobe Journey Optimizer MCP Serverを使用して、Adobe Journey Optimizerを開かずに平易な言葉で回答を得ることで、アクティブなAJOのジャーニーを確認し、キャンペーン設定を確認し、AI プラットフォームを通じて運用上の問題を明らかにすることで、常に一歩先を行く方法を説明します。

| シナリオの詳細 | |
| --- | --- |
| CX Enterprise製品 | [Adobe Journey Optimizer （AJO） &#x200B;](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/ajo-home) |
| エージェント型ツール | [Adobe CX Enterprise Coworker](https://experienceleague.adobe.com/ja/docs/cx-enterprise-coworker/content/home)、[Adobe CX Enterprise Coworker for AI Platforms](../tools/mcp-servers.md#connect-to-your-ai-platform)または[Adobe Journey Optimizer MCP Server](../tools/mcp-servers.md) |
| オーディエンス | キャンペーンマネージャー，マーケター |
| 前提条件 | AJOへのアクセス、Coworker、AI プラットフォーム用のCoworker付きAI プラットフォーム、MCP対応AI プラットフォーム |

各ステップは、代表的なプロンプトとAI応答の例を示しています。 同じセッションで追加の探索を行うために、**さらに達成できる**&#x200B;のセクションを次に示します。


## 始める前に

>[!BEGINTABS]

>[!TAB Coworker]

これらの回答を最も早く得るには、Coworkerを使用します。Coworkerでは、サーバーのセットアップやAI プラットフォームの設定は必要ありません。 [同僚を試す](https://experienceleague.adobe.com/ja/docs/cx-enterprise-coworker/content/home)

Coworkerを直接使用できない場合や、使用したくない場合は、代わりに自分のAI プラットフォームから使用してください。 AI プラットフォームの&#x200B;**同僚** タブを参照してください。 それでも問題が解決しない場合は、残りのタブを使用して、AI プラットフォームをAdobe Journey Optimizer MCP Serverに直接接続します。

>[!TAB AI プラットフォームの 同僚]

また、自社のAI プラットフォームからAI プラットフォーム向けに開発したCoworkerを使用して、このチュートリアルを完了することもできます。 [AI プラットフォーム用に共同作業者を設定](../tools/mcp-servers.md#connect-to-your-ai-platform) | [Adobe ドキュメント &#x200B;](https://experienceleague.adobe.com/ja/docs/coworker/content/ai-platforms#set-up-coworker)

>[!TAB  クロード.ai]

Adobe Journey Optimizer MCP Serverをカスタムコネクタとして接続します。

1. Claude.aiの&#x200B;**設定/統合**&#x200B;に移動します。
2. **カスタムコネクタを追加**&#x200B;を選択し、サーバーURLを入力します：`https://ajo-mcp.adobe.io/mcp`
3. **Connect**&#x200B;を選択し、Adobe IDでログインします。

完全なセットアップ：[Claude.ai カスタムコネクタのドキュメント &#x200B;](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

ChatGPT Developer Modeを使用してAdobe Journey Optimizer MCP Serverに接続します（Pro、Plus、Business、Enterprise、またはEducation プランが必要）。

1. **ChatGPT設定**&#x200B;で&#x200B;**開発者モード**&#x200B;を有効にします。
2. **設定/統合**&#x200B;に移動し、**カスタムコネクタを追加/リモート MCP サーバー**&#x200B;を選択します。
3. サーバーURLを入力してください：`https://ajo-mcp.adobe.io/mcp`
4. **Connect**&#x200B;を選択し、Adobe IDでログインします。

完全なセットアップ：[ChatGPT MCP ドキュメント &#x200B;](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB その他のAI プラットフォーム ]

Gemini、Microsoft Copilot、Cursor、Claude CodeなどのMCP互換アプリケーションを使用している場合、 次のエンドポイントを使用してAdobe Journey Optimizer MCP Serverに接続します。

```
https://ajo-mcp.adobe.io/mcp
```

サポートされているすべてのAI プラットフォームの完全なセットアップ手順：[AI プラットフォームに接続](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>プロンプトが表示されたらAdobe IDでログインし、AJO環境にリンクされているIMS組織を選択します。 間違った組織を選択することは、認証エラーの最も一般的な原因です。
>
>最初に接続すると、AI プラットフォームからIMS組織の選択やサンドボックスの指定を求められる場合があります。 そのコンテキストが設定されると、MCP サーバーは残りのセッションにコンテキストを使用します。
>
>一部のツールは、実行前に承認を求めます。 リクエストを確認して承認または辞退します。 確認なしにアクションは実行されません。


## ステップ 1：アクティブなジャーニーとその目的を確認する

まず、アクティブなジャーニーのインベントリとその背後にあるビジネス目標を尋ねることから始めます。 これにより、特定のジャーニーに入る前に、全体像を把握できます。

```
What customer journeys are currently available and what business objectives do they support?
```

+++回答の例を見る

![利用可能なカスタマージャーニーとビジネス目標を一覧表示するAI プラットフォーム &#x200B;](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step1.gif){zoomable="yes"}

*選択してズームします。*

+++



## ステップ 2：ジャーニーのステップと顧客体験を見直す

ジャーニーリストを表示して、AI プラットフォームに特定のジャーニーのステップを説明させ、各ステージで顧客体験について説明してもらいます。

```
Walk me through the [journey name] journey and explain the customer experience.
```

+++回答の例を見る

![新規顧客を歓迎するジャーニーの手順と顧客体験を説明するAI プラットフォーム &#x200B;](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step2-welcome-journey.png){zoomable="yes"}

*選択してズームします。*

+++


>[!NOTE]
>
>手順1の結果から`[journey name]`をジャーニーの名前に置き換えます。


## ステップ 3：キャンペーン、オーディエンス、目的の見直し

ジャーニーからキャンペーンへの移行： どの施策が効果的で、誰をターゲットとし、どのような成果を生み出すのかを概要で確認しましょう。

```
Show me our campaigns, the audiences they target, and the outcomes they're designed to drive.
```

+++回答の例を見る

![&#x200B; アクティブなキャンペーンを、オーディエンスターゲティングと意図された結果とともに一覧表示するAI プラットフォーム &#x200B;](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step3.gif){zoomable="yes"}

*選択してズームします。*

+++



## ステップ 4：キャンペーンとジャーニーがどのように連携しているかを把握する

AI プラットフォームに、キャンペーンとジャーニーの間の点を結びつけ、共通のエンゲージメント目標に向けてどのように連携するかを説明してもらいましょう。

```
How do our campaigns and journeys work together to improve customer engagement?
```

+++回答の例を見る

![&#x200B; キャンペーンとジャーニーの関係を説明するAI プラットフォーム &#x200B;](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step4-connection.png){zoomable="yes"}

*選択してズームします。*

+++



## ステップ 5：優先順位の高いレコメンデーションを入手する

ライフサイクルマーケティングマネージャーの視点から構築された、次に注力すべき施策に関する、優先順位に関する推奨事項を尋ねましょう。 これにより、セッションでレビューしたあらゆる情報から、最も効果的なギャップと機会を明らかにできます。

```
If you were our lifecycle marketing manager, what would you prioritize next and why?
```

+++回答の例を見る

![AI プラットフォームがライフサイクルマーケティングに関する推奨事項を優先的に提供](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5.gif){zoomable="yes"}

*選択してズームします。*

+++


>[!NOTE]
>
>AJO MCP Serverは、ジャーニーとキャンペーンの情報を表示しますが、ジャーニー、キャンペーン、コンテンツを変更することはできません。 レコメンデーションを実装するには、AJO アプリケーションに直接移動するか、AEM Content MCP Serverに接続して、同じセッション内のコンテンツの変更を行います。


## 達成したこと

Adobe WorkfrontやAI基盤とAdobe Journey Optimizerを連携させて、5つのプロンプトを通じてジャーニーとキャンペーンのポートフォリオの全体像を構築しました。 アクティブなジャーニーとビジネス目標を調査し、特定のジャーニーのステップバイステップの顧客体験を確認して、アクティブなキャンペーンをオーディエンスと意図される成果にマッピングし、キャンペーンとジャーニーがどのように連携しているかを把握して、次に注力すべき施策についての推奨事項を優先的に提示しました。 これにより、AJOのインターフェイスを開くことなく、ライフサイクルマーケティング担当者やキャンペーンマネージャーは、戦略的な可視性を確保できます。


## より多くのことを達成

Adobe Journey Optimizer MCP Serverでは、AJOの様々なジャーニーとキャンペーンの詳細を確認できます。 以下のシナリオを展開すると、同じセッションで試すことができるプロンプトが表示されます。

+++変更する前に公開されている情報を把握

他に何が実行されているかを知らずにジャーニーを変更するのはリスクがあります。 これらのプロンプトでは、何がアクティブで、何が最近変更されたか、キャンペーンがどのように設定されているかなどを確認できます。

**プロンプト**

```
Show me all journeys modified in the last 7 days.
```

```
Show me all journeys that use SMS as a channel.
```

```
Which campaigns are scheduled to end this week?
```

```
What loyalty challenges are currently active?
```

+++

+++特定のジャーニーの詳細

ジャーニーのレビュー、承認、引き継ぎが必要な場合、AJOを開かずに包括的なロジックを確認できるため、時間を節約できます。 これらのプロンプトは、条件、スケジュール、セグメントのルールをオンデマンドで表示します。

**プロンプト**

```
What is the entry condition for the [journey name] journey?
```

```
What are the exit conditions and timeout rules for the [journey name] journey?
```

```
What messages and wait conditions are in the [journey name] journey?
```

```
Which segment does the [journey name] journey target?
```

+++

+++特定のキャンペーンの詳細

承認、引き渡し、変更を行う前にキャンペーンの全設定を確認する必要がある場合、これらのプロンプトは、AJOを開かずに、オーディエンスルール、チャネル設定、スケジュールの詳細を表示します。

**プロンプト**

```
Walk me through the full configuration of the [campaign name] campaign.
```

```
What audience does the [campaign name] campaign target and how large is that segment?
```

```
What frequency cap and send schedule apply to the [campaign name] campaign?
```

```
Are any campaigns targeting overlapping audiences?
```

```
What channel configurations are set up in our AJO environment?
```

+++



## 詳細情報

| リソース | 見つかる内容 |
| --- | --- |
| [AI レジストリのAJO MCP Server](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server){target="_blank"} | AJO MCP Serverのツールと機能 |
| [AJO ドキュメント &#x200B;](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/ajo-home){target="_blank"} | Adobe AJOのドキュメント |
