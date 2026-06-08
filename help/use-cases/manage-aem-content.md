---
title: コンテンツを最新の状態に保ち、更新をすばやく配信できます
description: AEM Content MCP Serverを使用して、ツールを切り替えることなく、AEM コンテンツを検索、レビュー、更新、公開します。
index: false
source-git-commit: 14488b494c454ce6d1207e2d21024749d93db669
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 1%

---


# コンテンツを最新の状態に保ち、更新をすばやく配信できます

<!-- last-modified: 2026-05-22 -->

![AIを使用したAEM コンテンツの管理](https://placehold.co/1600x900?text=Manage+AEM+Content+with+AI)

ページの検索やコンテンツの確認から、更新や公開に至るまで、Adobe Experience Managerでコンテンツを操作するには、通常、AEMインターフェイスを直接操作する必要があります。 このチュートリアルでは、AEM Content MCP Serverを使用するAI クライアントを通じて、これらのオペレーションを処理する方法を説明します。これにより、ツール間でコンテキストを切り替えることなく、コンテンツチームはより迅速に作業できるようになります。

| | |
| --- | --- |
| CX エンタープライズアプリケーション | Adobe Experience Manager as a Cloud Service |
| エージェント型ツール | AEM Content MCP Server |
| オーディエンス | コンテンツマネージャー，マーケティングチーム |
| 前提条件 | MCP対応AI クライアント、AEM as a Cloud Serviceアクセス |

各ステップは、代表的なプロンプトとAI応答の例を示しています。 同じセッションで追加の探索を行うために、**さらに達成できる**&#x200B;のセクションを次に示します。

## 始める前に

>[!BEGINTABS]

>[!TAB  クロード.ai]

AEM Content MCP Serverをカスタムコネクタとして接続します。

1. Claude.aiの&#x200B;**設定/統合**&#x200B;に移動します。
2. **カスタムコネクタを追加**&#x200B;を選択し、サーバーURLを入力します：`https://mcp.adobeaemcloud.com/adobe/mcp/content`
3. **Connect**&#x200B;を選択し、Adobe IDでログインします。

完全なセットアップ：[Claude.ai カスタムコネクタのドキュメント &#x200B;](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

ChatGPT Developer Modeを使用してAEM Content MCP Serverに接続します（Pro、Plus、Business、Enterprise、またはEducation プランが必要）。

1. **ChatGPT設定**&#x200B;で&#x200B;**開発者モード**&#x200B;を有効にします。
2. **設定/統合**&#x200B;に移動し、**カスタムコネクタを追加/リモート MCP サーバー**&#x200B;を選択します。
3. サーバーURLを入力してください：`https://mcp.adobeaemcloud.com/adobe/mcp/content`
4. **Connect**&#x200B;を選択し、Adobe IDでログインします。

完全なセットアップ：[ChatGPT MCP ドキュメント &#x200B;](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB その他のAI クライアント ]

Gemini、Microsoft Copilot、Cursor、Claude CodeなどのMCP互換アプリケーションを使用している場合、 次のエンドポイントを使用して、AEM Content MCP Serverに接続します。

```
https://mcp.adobeaemcloud.com/adobe/mcp/content
```

サポートされているすべてのクライアントの完全なセットアップ手順：[AI クライアントに接続](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>プロンプトが表示されたらAdobe IDでログインし、AEM as a Cloud Service環境にリンクされているIMS組織を選択します。 権限はAEM レベルで適用されます。 AI クライアントは、アカウントが承認した操作のみを実行できます。
>
>変更を加えずにコンテンツを参照または監査するだけの必要がある場合は、代わりに読み取り専用サーバーエンドポイントを使用してください：`https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly`。 このページのすべての検出およびレビュープロンプトは、両方のサーバーで機能します。
>
>最初の接続時に、AI クライアントから組織またはAEM環境の確認を求められる場合があります。 そのコンテキストが設定されると、MCP サーバーは残りのセッションにコンテキストを使用します。
>
>一部のツールは、実行前に承認を求めます。 提案されたアクションを確認し、承認または辞退します。確認がなければ変更は行われません。

## ステップ 1:AEM環境全体のコンテンツを検索する

まず、AI クライアントにAEM環境を検索してもらい、コンテンツを検索してもらいます。 正確なパスを知らなくても、トピック、キーワード、コンテンツタイプで検索できます。

```
From WKND Dev environment, find all ski related content.
```

+++回答の例を見る

![WKND Dev AEM環境からのスキーコンテンツの検索結果を表示するAI クライアント &#x200B;](../assets/use-cases/manage-aem-content/manage-aem-content-step1-find-ski.png)

+++


## 手順2：特定のページの確認

関連コンテンツを見つけたら、AI クライアントに特定のページを表示するように依頼します。 ページは名前またはパスで参照できます。 MCP サーバーは参照を解決し、コンテンツ構造を返します。

```
Show me the US English Home Page.
```

+++回答の例を見る

![AEMの米国英語ホームページのコンテンツ構造を表示するAI クライアント &#x200B;](../assets/use-cases/manage-aem-content/manage-aem-content-step2-home-page.png)

+++


## ステップ 3：コンテンツの改善

ページコンテンツを表示して、AI クライアントに改善点の提案や適用を依頼します。 AIは、ページの現在の内容に基づいてコピーの変更を提案し、何かを書く前に確認を求めることができます。

```
Improve the Hero CTAs.
```

+++回答の例を見る

![変更を適用する前に、確認プロンプトを使用して改善されたHero CTA コピーを提案するAI クライアント &#x200B;](../assets/use-cases/manage-aem-content/manage-aem-content-step3.gif)

+++


>[!CAUTION]
>
>プロンプトが表示されたら、各変更を確認します。 AEM Content MCP Serverでは、コンテンツを作成、更新、削除できます。 特にライブページでは、承認前に提案された変更を確認します。

## ステップ 4：公開と共有

更新を確認したら、ページを公開し、共有可能なURLを取得します。これらはすべて同じ会話で行われます。

```
Publish the changes and share the URL.
```

+++回答の例を見る

![&#x200B; ページが公開されたことを確認し、ライブ URLを返すAI クライアント &#x200B;](../assets/use-cases/manage-aem-content/manage-aem-content-step4.gif)

+++


## 達成したこと

AEM Content MCP Serverを使用して、AEM インターフェイスを開かずに、コンテンツの検索、ライブページのレビュー、AIが提案した改善点の適用、結果の公開を行いました。 コンテンツの発見、編集、公開を単一のAI セッションで組み合わせることで、コンテンツチームはギャップを特定することから、更新をより迅速かつ少ないコンテクストで配信することに移行できます。 同じワークフローで、複数のページ、コンテンツフラグメント、調整されたキャンペーンのローンチに対応します。

## より多くのことを達成

AEM Content MCP Serverは、チュートリアルで扱うよりもはるかに多くの処理を処理します。 以下のシナリオを展開すると、同じセッションで試すことができるプロンプトが表示されます。

+++サイトのレビューやリニューアルに先手を打つ

手作業ではコンテンツ監査に時間がかかります。 これらのプロンプトを活用すると、古いコンテンツ、出荷されていないドラフト、大規模なプッシュ前に修正が必要なギャップをすばやく確認できます。

**プロンプト**

```
Show me everything updated in the last two weeks.
```

```
What content is sitting in draft and hasn't been published yet?
```

```
Find pages that haven't been touched in over a year.
```

```
Which pages are missing their description field?
```

```
We're reorganizing the taxonomy. Find all articles missing tags or categories.
```

+++

+++SEOとアクセシビリティの問題を大規模に修正

SEOとアクセシビリティのギャップが、大規模なサイト全体で急速に広がっています。 これらのプロンプトは、監査や立ち上げ前に最も重要な問題を見つけ、優先順位を付けるのに役立ちます。

**プロンプト**

```
Pull a list of all pages with an empty meta description.
```

```
Which pages have thin content that's likely to underperform for SEO?
```

```
Find all images missing alt text.
```

```
Our CTAs aren't consistent. Scan the site and flag anywhere the call-to-action wording differs from "Book now."
```

```
The homepage was updated yesterday. Show me what changed compared to the version before.
```

+++

+++アセットライブラリを常に整理して準備しておきましょう

壊れたアセット参照や未処理のアップロードは、コンテンツ制作の遅延につながります。 これらのプロンプトは、ページの更新やキャンペーンをブロックする前にアセットを検索し、管理するのに役立ちます。

**プロンプト**

```
We're building a biking content series. What image assets do we already have?
```

```
Can you upload a placeholder asset from https://placehold.co/800x450/png to the wknd folder and save it as placeholder.png?
```

```
That asset was just uploaded. Is it processed and ready to use in a page?
```

```
I need to replace the hero image across the site. Which fragments are currently using it?
```

+++

+++複数のページをまたいでコンテンツのローンチを調整する

多くの場合、キャンペーンを立ち上げるために、複数のコンテンツフラグメントやページをまたいで変更を調整する必要があります。 これらのプロンプトは、更新をグループ化し、プロモーションする前にレビューし、クリーンに配信するのに役立ちます。

**プロンプト**

```
I need to update the surfing adventure. Show me its content and all its fields.
```

```
Create an EMEA market variation of the ski adventure fragment.
```

```
Bundle everything we changed in this session into a launch called May Updates.
```

```
What launches are open right now, and which ones are ready to promote?
```

```
Before I promote, show me exactly what changed between May Updates and what is currently live.
```

```
Promote the May Updates launch to production.
```

+++


## 詳細情報

| リソース | 見つかる内容 |
| --- | --- |
| [AEM Content MCP Server ドキュメント &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | MCP サーバーの設定と使用ガイド |
| [AI レジストリのAEM Content MCP Server](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) | ツールリストと可用性 |
| [AEM as a Cloud Service のドキュメント](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service) | Adobe AEMのドキュメント |
| [AEM コンテンツフラグメント &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments) | コンテンツフラグメントのオーサリングリファレンス |
| [MCP サーバー](../tools/mcp-servers.md) | AI クライアントをAdobe MCP サーバーに接続する |
