---
title: Adobe CX Enterprise Agentic Tools
description: MCP サーバー、エージェントのスキル、API を使用して、AI エージェントと開発ツールを Adobe CX Enterprise 機能に接続します。
last-substantial-update: 2026-11-16
source-git-commit: a75d5f3af3077b259da796bd381d605ae826585d
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 5%
---

# Adobe CX Enterprise Agentic Tools

<!-- last-modified: 2026-06-08 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491235/?learn=on&enablevpops)

AIを活用したAdobe CX Enterpriseの共同作業。 AI プラットフォームをキャンペーン、オーディエンス、ジャーニー、コンテンツに接続します。 あらゆるツールから平易な言葉で顧客とやり取りできます。 新しいインターフェイスも、コンテキストの切り替えも、コーディングも必要ありません。

>[!TIP]
>**Adobe CX Enterprise Coworkerで開始します。** お使いのCX Enterpriseアプリケーションと互換性があり、サーバーの設定やAI プラットフォームの設定は必要ありません。 [同僚を試す](https://experienceleague.adobe.com/ja/docs/cx-enterprise-coworker/content/home)
>
>Claude、ChatGPT、Microsoft 365 Copilot、その他のAI プラットフォームに滞在することを好みますか？ AI プラットフォームに[Adobe CX Enterprise Coworkerを使用](tools/mcp-servers.md#connect-to-your-ai-platform)。 どちらの機能も使用できない場合は、AI プラットフォームを[製品MCP サーバー](tools/mcp-servers.md#connect-to-your-ai-platform)に接続します。

<!--
CARDS

* tools/mcp-servers.md
  {title = MCP Servers}
  {description = Connect any MCP-compatible AI platform to Adobe CX Enterprise workflows. Query data, analyze campaigns, and access audiences without leaving your AI tool.}
  {cta = Explore MCP Servers}
  {image = assets/mcp-servers-card.png}

* tools/agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflows that guide agents through CX Enterprise tasks. Domain expertise encoded once, applied consistently.}
  {cta = Explore Agent Skills}
  {image = assets/agent-skills-card.png}

* tools/apis.md
  {title = APIs for Builders}
  {description = Build custom Adobe CX Enterprise applications using agentic coding tools like Claude Code and Cursor.}
  {cta = Explore APIs for Builders}
  {image = assets/apis-card.png}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/mcp-servers.md" title="MCP サーバー">
                        <img class="is-bordered-r-small" src="assets/mcp-servers-card.png" alt="MCP サーバー"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/mcp-servers.md" title="MCP サーバー">MCP サーバー</a>
                    </p>
                    <p class="is-size-6">MCP対応のあらゆるAI基盤をAdobe CX Enterpriseワークフローに接続。 AI ツールから直接、データのクエリ、キャンペーンの分析、オーディエンスのアクセスを実行できます。</p>
                </div>
                <a href="tools/mcp-servers.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">MCP サーバーの探索</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/agent-skills.md" title="エージェントスキル">
                        <img class="is-bordered-r-small" src="assets/agent-skills-card.png" alt="エージェントスキル"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/agent-skills.md" title="エージェントスキル"> エージェントのスキル </a>
                    </p>
                    <p class="is-size-6">Adobeがキュレートしたワークフローにより、エージェントはCX Enterpriseのタスクを進めることができます。 一度符号化されたドメインの専門知識は、一貫して適用されます。</p>
                </div>
                <a href="tools/agent-skills.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> エージェントのスキルを探る</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/apis.md" title="ビルダー用API">
                        <img class="is-bordered-r-small" src="assets/apis-card.png" alt="ビルダー用API"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        ビルダー</a>の<a href="tools/apis.md" title="ビルダー用API">API
                    </p>
                    <p class="is-size-6">Claude CodeやCursorなどのエージェント型コーディングツールを使用して、カスタムAdobe CX Enterpriseアプリケーションを構築します。</p>
                </div>
                <a href="tools/apis.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> ビルダー用APIの探索</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## あらゆる部門に対応するエージェント型ツール

>[!BEGINTABS]

>[!TAB MCP サーバー]

互換性のある任意のAI プラットフォームを使用して、CX Enterpriseアプリケーションに平易な言語でアクセスできます。 コーディングは必要ありません。 アプリケーションをまたいで最速のパスを得るために、Adobe Workfrontを導入する。 自社のAI プラットフォームの利用を続けるには、AI プラットフォームにCoworkerを利用します。 どちらも機能しない場合は、AJO、CJA、AEMなどのアプリケーションに、独自のMCP サーバーで直接接続します。

- Claude、Cursor、ChatGPTなどのMCP対応AI プラットフォームから数分で接続できます
- 自然言語を使用して、キャンペーン、オーディエンス、ジャーニーデータをクエリ
- 新しいインターフェイスやトレーニングは必要ありません

[MCP サーバーの基本を学ぶ](tools/mcp-servers.md)

>[!TAB  エージェントのスキル ]

Agent Skillsは、AI プラットフォームが従うことのできる指示として、Adobeドメインの専門知識をエンコードします。 担当者は助言を入れるのではなく、何をすべきかを正確に把握し、Adobeのベストプラクティスに従って、信頼性の高い反復的な作業を行います。

- 繰り返し利用できるCX Enterpriseワークフローで一貫した結果を得る
- 担当者にAdobeについて説明する必要はありません。担当者が対応します
- エージェントのスキルをサポートするAI プラットフォーム全体で動作

[エージェントのスキルを見る](tools/agent-skills.md)

>ビルダー]の[!TAB API

Adobe製品と同じAPIに、プログラムを利用して直接アクセスできます。 カスタムアプリケーションと統合機能を構築して、部門全体で特定のCX Enterpriseワークフローに集中してアクセスできるようにします。

- 一度構築すれば、組織全体に展開
- チームが必要とするガードレール、承認、カスタムロジックの追加
- Claude Code、Cursorなどのエージェント型コーディングツールを使用して、より迅速に構築できます

[ビルダー用APIの確認](tools/apis.md)

>[!ENDTABS]

## エージェント型ツールの活用例

Adobe CX Enterpriseのエージェント型ツールの実際。 各ウォークスルーでは、設定から結果までの実際のビジネスシナリオを取り上げ、CoworkerやAI プラットフォームの使い始め方、質問すべき点、そして取り戻すべき点を正確に示します。

<!--
CARDS

* use-cases/analyze-campaign-performance.md
  {title = Campaign insights without reports}
  {description = Ask performance questions in plain language and get answers from Customer Journey Analytics, without building a single report.}
  {cta = Surface campaign insights}

* use-cases/manage-aem-content.md
  {title = Ship content updates faster}
  {description = Find, update, and publish AEM pages and content fragments faster, without switching to the AEM interface.}
  {cta = Ship content faster}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Campaign insights without reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/analyze-campaign-performance.md" title="レポートを使用しないキャンペーンインサイト">
                        <img class="is-bordered-r-small" src="assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="レポートを使用しないキャンペーンインサイト"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        レポートのない<a href="use-cases/analyze-campaign-performance.md" title="レポートを使用しないキャンペーンインサイト"> キャンペーンインサイト </a>
                    </p>
                    <p class="is-size-6">単一のレポートを作成することなく、平易な言語でパフォーマンスに関する質問をおこない、Customer Journey Analyticsから回答を得ることができます。</p>
                </div>
                <a href="use-cases/analyze-campaign-performance.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> キャンペーンのインサイトを表示</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Ship content updates faster">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-aem-content.md" title="コンテンツの更新をより迅速に配信">
                        <img class="is-bordered-r-small" src="assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="コンテンツの更新をより迅速に配信"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-aem-content.md" title="コンテンツの更新をより迅速に配信"> コンテンツの更新をより迅速に配信</a>
                    </p>
                    <p class="is-size-6">AEMのインターフェイスに切り替えることなく、AEMのページとコンテンツフラグメントをより迅速に検索、更新、公開できます。</p>
                </div>
                <a href="use-cases/manage-aem-content.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> コンテンツの迅速な配信</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

**[すべてのチュートリアルを見る](use-cases/overview.md)**

## Adobeの業界トレンド

| リソース | 見つかる内容 |
| --- | --- |
| [Adobe AI レジストリ ](https://developer.adobe.com/ai-registry/?type=mcp) | 一部のAdobe MCP サーバーのマネージドコネクタとサーバーの詳細 |
| [Adobe Agent Skills](https://github.com/adobe/skills) | CX Enterpriseワークフロー用にAdobeが監修した担当者のスキル |
| [Adobe API カタログ ](https://developer.adobe.com/apis) | Adobe CX Enterprise API リファレンスの完全版 |
| [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) | API プロジェクトの設定と認証 |
| [Adobe Admin Console](https://adminconsole.adobe.com) | ユーザーと製品のアクセス管理 |
| [Experience League](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/home) | Adobeのアプリケーションに関するドキュメントとチュートリアル |
