---
title: Adobe CX Enterprise Agentic Tools
description: MCP サーバー、エージェントスキル、APIを使用して、AI エージェントと開発ツールをAdobe CX Enterpriseの機能に接続します。
index: false
source-git-commit: d6c236f5405fac4b9813280d9fac2d4a60968924
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 1%

---


# Adobe CX Enterprise Agentic Tools

<!-- last-modified: 2026-05-08 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491235/?learn=on&enablevpops)

**Adobe CX Enterprise**&#x200B;のデータ、ワークフロー、オートメーションにAIを直接接続します。 互換性のあるAI クライアントや開発ツールから、**平易な言語**&#x200B;でキャンペーンのクエリ、オーディエンスのアクティブ化、ジャーニーの管理を行うことができます。

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

## あらゆる部門に対応するエージェント型ツール

>[!BEGINTABS]

>[!TAB  ビジネスリーダー]

Adobeのエージェンティックツールのビジネス価値と、それがAdobeへの投資をどのように拡大するのかを理解します。

- 担当者は、チームを交代させることなく、マーケティングとオペレーションのワークフローを加速させます
- アクセス制御、監査証跡、Human-in-the-loop ワークフローは最初から組み込まれています
- エージェンティックツールは、Adobeのサーフェスだけでなく、互換性のあるあらゆるAI クライアントで動作します
- ユーザーのデータは、ユーザーの権限によって管理された環境に保持されます

[実際のウォークスルー](agentic-tools-in-action.md)を参照して、今日これらのエージェント型ツールでチームが何をしているのかを確認してください。

>[!TAB  ビジネスユーザー]

エージェンティックツールが、どのようにAdobeの日々のワークフローを加速するのかをご確認ください。

- [MCP サーバー](tools/mcp-servers.md)を使用して、AI クライアントを数分でAdobe データに接続します
- 一般的な[&#x200B; キャンペーン &#x200B;](use-cases/analyze-campaign-performance.md)、[&#x200B; オーディエンス &#x200B;](use-cases/query-audiences.md)、[&#x200B; ジャーニー](use-cases/manage-ajo-journeys.md)のタスクについて、順を追って説明します
- 既に使用しているAI環境で作業する

>[!TAB  ビルダーと開発者]

Adobe CX Enterpriseの機能をカスタムアプリケーションやエージェントに統合できます。

- 機能領域ごとにビルダー[&#128279;](tools/apis.md)のAPIを参照し、開発環境の[MCP サーバー](tools/mcp-servers.md)に接続します
- Adobe APIと共に、[Claude Code](https://docs.anthropic.com/en/docs/claude-code/mcp)や[Cursor](https://cursor.com/docs/mcp)などのAI支援コーディングツールを使用します
- [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)で認証と資格情報を設定します
- サポートされているAI クライアントとセットアップ手順の完全なリストについては、[MCP サーバー](tools/mcp-servers.md)を参照してください

>[!TAB 管理者]

アクセスを管理し、承認済みのエージェント型ツールを管理し、組織全体の監視を維持しましょう。

- [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)を介したMCP サーバーおよびAPIの認証を構成します
- Identity Management System （IMS）組織レベルの権限を設定して、エージェント型ツールにアクセスできるユーザーとチームを制御します
- 組織での使用を承認されたAI クライアントとMCP サーバーを定義し、適用します
- 使用状況の監視、監査証跡の確認、エージェンティックアクティビティがコンプライアンス要件を満たしていることを確認します

認証設定については[MCP サーバー](tools/mcp-servers.md)、資格情報およびプロジェクト管理については[Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)を参照してください。

>[!ENDTABS]

## エージェント型ツールの活用例

Adobe CX Enterpriseのエージェント型ツールの実際をご覧ください。 各チュートリアルでは、設定から成果までの実際のビジネスシナリオを取り上げ、AI クライアントの接続方法、求めるべき事項、そして返される結果を正確に提示します。

<!--
CARDS

* use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use the CX Enterprise MCP Gateway to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use the CX Enterprise MCP Gateway to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use the CX Enterprise MCP Gateway to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine CJA and AEM MCP Servers to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Connect AJO, CJA, and Real-Time CDP in one AI session for a unified view of campaign health.}
  {cta = Start walkthrough}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
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
                    <p class="is-size-6">CX Enterprise MCP Gatewayを使用して、あらゆるAI クライアントからCustomer Journey Analyticsの指標とインサイトを可視化します。</p>
                </div>
                <a href="use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> チュートリアルを開始</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/query-audiences.md" title="オーディエンスの照会" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Query+Audiences" alt="オーディエンスの照会"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/query-audiences.md" target="_blank" rel="referrer" title="オーディエンスの照会"> オーディエンスのクエリ </a>
                    </p>
                    <p class="is-size-6">CX Enterprise MCP Gatewayを使用して、平易な言語プロンプトを使用してReal-Time CDP オーディエンスと宛先データをクエリします。</p>
                </div>
                <a href="use-cases/query-audiences.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> チュートリアルを開始</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Review AJO journeys">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-ajo-journeys.md" title="AJO ジャーニーのレビュー" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Review+AJO+Journeys" alt="AJO ジャーニーのレビュー"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" title="AJO ジャーニーのレビュー">AJO ジャーニーのレビュー</a>
                    </p>
                    <p class="is-size-6">CX Enterprise MCP Gatewayを使用して、AI クライアントからAJO ジャーニー、キャンペーンステータス、ジャーニー条件にアクセスします。</p>
                </div>
                <a href="use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
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
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Optimize content based on performance data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/optimize-content-with-performance-data.md" title="パフォーマンスデータに基づくコンテンツの最適化" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data" alt="パフォーマンスデータに基づくコンテンツの最適化"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" title="パフォーマンスデータに基づくコンテンツの最適化"> パフォーマンスデータに基づいてコンテンツを最適化</a>
                    </p>
                    <p class="is-size-6">CJAとAEM MCP サーバーを組み合わせることで、パフォーマンスの低いコンテンツを特定し、1回のセッションで更新できます。</p>
                </div>
                <a href="use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> チュートリアルを開始</span>
                </a>
            </div>
        </div>
    </div>
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
                    <p class="is-size-6">AJO、CJA、Real-Time CDPを単一のAI セッションで連携することで、キャンペーンの健全性を包括的に把握できます。</p>
                </div>
                <a href="use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> チュートリアルを開始</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Adobeの業界トレンド

| リソース | 見つかる内容 |
| --- | --- |
| [Adobe AI レジストリ &#x200B;](https://developer.adobe.com/ai-registry/?type=mcp) | 利用可能なMCP サーバーとエージェントスキルの完全カタログ |
| [Adobe API カタログ &#x200B;](https://developer.adobe.com/apis) | Adobe CX Enterprise API リファレンスの完全版 |
| [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) | API プロジェクトの設定と認証 |
| [Experience League](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/home) | Adobeのアプリケーションに関するドキュメントとチュートリアル |
