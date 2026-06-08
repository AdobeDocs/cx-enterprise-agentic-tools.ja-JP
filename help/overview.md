---
title: Adobe CX Enterprise Agentic Tools
description: MCP サーバー、エージェントスキル、APIを使用して、AI エージェントと開発ツールをAdobe CX Enterpriseの機能に接続します。
index: false
source-git-commit: bb341fa02a8e1e8b3efbf832359846c94441df88
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 1%

---


# Adobe CX Enterprise Agentic Tools

<!-- last-modified: 2026-06-08 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491242/?captions=jpn&learn=on&enablevpops)

Adobe CX EnterpriseのパートナーはAI。 AI クライアントをキャンペーン、オーディエンス、ジャーニー、コンテンツに結び付け、既に使用しているあらゆるツールから、わかりやすい言葉で操作できます。 新しいインターフェイスも、コンテキストの切り替えも、コーディングも必要ありません。

>[!TIP]
>**CX Enterprise MCPで始めます。** 1つの接続で、組織のライセンスに基づいて、AI クライアントはAdobe Journey Optimizer、Customer Journey Analytics、Real-Time CDPにアクセスできます。 [今すぐ接続](tools/mcp-servers.md#cx-enterprise-mcp)

<!--
CARDS

* tools/mcp-servers.md
  {title = MCP Servers}
  {description = Connect any MCP-compatible AI client to Adobe CX Enterprise workflows. Query data, analyze campaigns, and access audiences without leaving your AI tool.}
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
                    <a href="tools/mcp-servers.md" title="MCP サーバー" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/mcp-servers-card.png" alt="MCP サーバー"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/mcp-servers.md" target="_blank" rel="referrer" title="MCP サーバー">MCP サーバー</a>
                    </p>
                    <p class="is-size-6">MCP対応のあらゆるAI クライアントとAdobe CX Enterpriseのワークフローを接続。 AI ツールから直接、データのクエリ、キャンペーンの分析、オーディエンスのアクセスを実行できます。</p>
                </div>
                <a href="tools/mcp-servers.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">MCP サーバーの探索</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/agent-skills.md" title="エージェントスキル" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/agent-skills-card.png" alt="エージェントスキル"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/agent-skills.md" target="_blank" rel="referrer" title="エージェントスキル"> エージェントのスキル </a>
                    </p>
                    <p class="is-size-6">Adobeがキュレートしたワークフローにより、エージェントはCX エンタープライズタスクを進めることができます。 一度符号化されたドメインの専門知識は、一貫して適用されます。</p>
                </div>
                <a href="tools/agent-skills.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> エージェントのスキルを探る</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/apis.md" title="ビルダー用API" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/apis-card.png" alt="ビルダー用API"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        ビルダー</a>の<a href="tools/apis.md" target="_blank" rel="referrer" title="ビルダー用API">API
                    </p>
                    <p class="is-size-6">Claude CodeやCursorなどのエージェント型コーディングツールを使用して、カスタムのAdobe CX エンタープライズアプリケーションを構築できます。</p>
                </div>
                <a href="tools/apis.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> ビルダー用APIの探索</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/mcp-servers.md" title="MCP サーバー" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/mcp-servers-card.png" alt="MCP サーバー"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/mcp-servers.md" target="_blank" rel="referrer" title="MCP サーバー">MCP サーバー</a>
                    </p>
                    <p class="is-size-6">MCP対応のあらゆるAI クライアントとAdobe CX Enterpriseのワークフローを接続。 AI ツールから直接、データのクエリ、キャンペーンの分析、オーディエンスのアクセスを実行できます。</p>
                </div>
                <a href="tools/mcp-servers.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">MCP サーバーの探索</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/agent-skills.md" title="エージェントスキル" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/agent-skills-card.png" alt="エージェントスキル"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/agent-skills.md" target="_blank" rel="referrer" title="エージェントスキル"> エージェントのスキル </a>
                    </p>
                    <p class="is-size-6">Adobeがキュレートしたワークフローにより、エージェントはCX エンタープライズタスクを進めることができます。 一度符号化されたドメインの専門知識は、一貫して適用されます。</p>
                </div>
                <a href="tools/agent-skills.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> エージェントのスキルを探る</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/apis.md" title="ビルダー用API" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/apis-card.png" alt="ビルダー用API"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        ビルダー</a>の<a href="tools/apis.md" target="_blank" rel="referrer" title="ビルダー用API">API
                    </p>
                    <p class="is-size-6">Claude CodeやCursorなどのエージェント型コーディングツールを使用して、カスタムのAdobe CX エンタープライズアプリケーションを構築できます。</p>
                </div>
                <a href="tools/apis.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
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

互換性のあるAI クライアントを使用して、コーディング不要で平易な言語で顧客体験エンタープライズアプリケーションにアクセスできます。 CX Enterprise MCPを使用して、AJO、CJA、Real-Time CDPに1回接続するか、AEMやその他のアプリケーションに直接接続できます。

- Claude、Cursor、ChatGPTなどのMCP互換クライアントから数分で接続できます
- 自然言語を使用して、キャンペーン、オーディエンス、ジャーニーデータをクエリ
- 新しいインターフェイスやトレーニングは必要ありません

[MCP サーバーの基本を学ぶ](tools/mcp-servers.md)

>[!TAB  エージェントのスキル ]

Agent Skillsは、AI クライアントが従うことのできる指示として、Adobeドメインの専門知識をエンコードします。 担当者はメッセージを即興ではなく、確実に、繰り返し、Adobeのベストプラクティスに従って行動できるようになりました。

- 反復可能な顧客体験の大規模なワークフローにおける一貫した結果
- 担当者にAdobe Adobeについて説明する必要はありません。担当者が対応します
- エージェントのスキルをサポートするAI クライアント全体で動作

[エージェントのスキルを見る](tools/agent-skills.md)

>[!TAB ビルダーの API]

Adobe製品と同じAPIに、プログラムを利用して直接アクセスできます。 カスタムアプリケーションと統合機能を構築して、チームが特定の顧客体験企業ワークフローに集中して管理されたアクセスを得られるようにします。

- 一度構築すれば、組織全体に展開
- チームが必要とするガードレール、承認、カスタムロジックの追加
- Claude Code、Cursorなどのエージェント型コーディングツールを使用して、より迅速に構築できます

[ビルダー用APIの確認](tools/apis.md)

>[!ENDTABS]

## エージェント型ツールの活用例

Adobe CX Enterpriseのエージェント型ツールの実際をご覧ください。 各チュートリアルでは、設定から成果までの実際のビジネスシナリオを取り上げ、AI クライアントの接続方法、求めるべき事項、そして返される結果を正確に提示します。

<!--
CARDS

* use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Review AJO journey status, Real-Time CDP audience activation, and CJA performance data in one AI session. Uses CX Enterprise MCP.}
  {cta = Start walkthrough}

* use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Surface Customer Journey Analytics comparisons and conversion trends through plain-language questions. Uses CX Enterprise MCP.}
  {cta = Start walkthrough}

* use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Run a cross-channel campaign review">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/cross-channel-campaign-review.md" title="クロスチャネルキャンペーンのレビューの実施" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review" alt="クロスチャネルキャンペーンのレビューの実施"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" title="クロスチャネルキャンペーンのレビューの実施"> クロスチャネルキャンペーンレビューの実行</a>
                    </p>
                    <p class="is-size-6">AJOジャーニーのステータス、Real-Time CDPオーディエンスのアクティベーション、CJAのパフォーマンスデータを1つのAI セッションで確認できます。 Cx Enterprise MCPを使用します。</p>
                </div>
                <a href="use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> チュートリアルを開始</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/analyze-campaign-performance.md" title="キャンペーンのパフォーマンスを分析" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Analyze+Campaign+Performance" alt="キャンペーンのパフォーマンスを分析"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" title="キャンペーンのパフォーマンスを分析"> キャンペーンパフォーマンスの分析</a>
                    </p>
                    <p class="is-size-6">平易な言葉で質問し、Customer Journey Analyticsの比較とコンバージョンの傾向を把握できます。 Cx Enterprise MCPを使用します。</p>
                </div>
                <a href="use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> チュートリアルを開始</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Manage AEM content with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-aem-content.md" title="AIを活用したAEMコンテンツの管理" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Manage+AEM+Content+with+AI" alt="AIを活用したAEMコンテンツの管理"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-aem-content.md" target="_blank" rel="referrer" title="AIを活用したAEMコンテンツの管理">AIを使用したAEM コンテンツの管理</a>
                    </p>
                    <p class="is-size-6">AEMの自然言語を使用して、ページとコンテンツフラグメントを検索、更新、公開できます。</p>
                </div>
                <a href="use-cases/manage-aem-content.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> チュートリアルを開始</span>
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
| [Adobe AI レジストリ &#x200B;](https://developer.adobe.com/ai-registry/?type=mcp) | MCP サーバーの完全カタログ |
| [Adobe Agent Skills](https://github.com/adobe/skills) | Adobeが監修したCX エンタープライズワークフロー向けのエージェントのスキル |
| [Adobe API カタログ &#x200B;](https://developer.adobe.com/apis) | Adobe CX Enterprise API リファレンスの完全版 |
| [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) | API プロジェクトの設定と認証 |
| [Adobe Admin Console](https://adminconsole.adobe.com) | ユーザーと製品のアクセス管理 |
| [Experience League](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/home) | Adobeのアプリケーションに関するドキュメントとチュートリアル |
