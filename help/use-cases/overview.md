---
title: エージェント型ツールの活用例
description: 実際のビジネスワークフローに適用されたAdobe CX Enterprise Agentic Toolsを示すステップバイステップのウォークスルー。
last-substantial-update: 2026-06-08T00:00:00Z
index: false
source-git-commit: c88de99df4cabf47cce195de1a6a888f4f780fe9
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# エージェント型ツールの活用例

<!-- last-modified: 2026-06-08 -->

![&#x200B; エージェント ツールの動作](../assets/hero-agentic-tools-in-action.png)

Adobe CX Enterpriseの実際のワークフローをステップバイステップで解説します。 各ウォークスルーは、設定が終わる場所から始まり、ツールをつなぎ合わせ、実際のワークフローが完了します。

<!--
CARDS

* analyze-campaign-performance.md
  {title = Campaign insights without reports}
  {description = Ask performance questions in plain language and get answers from Customer Journey Analytics, without building a single report.}
  {cta = Surface campaign insights}

* query-audiences.md
  {title = Audience activation at a glance}
  {description = See which audiences are live, where they are flowing, and whether destinations are healthy, without navigating Real-Time CDP.}
  {cta = Check audience activation}

* manage-ajo-journeys.md
  {title = Catch journey issues early}
  {description = Monitor active journeys and surface operational issues before they reach your audience.}
  {cta = Monitor your journeys}

* manage-aem-content.md
  {title = Ship content updates faster}
  {description = Find, update, and publish AEM pages and content fragments faster, without switching to the AEM interface.}
  {cta = Ship content faster}

* optimize-content-with-performance-data.md
  {title = Close content performance gaps}
  {description = Surface conversion gaps in CJA, trace them to underperforming content in AEM, and apply the fix in a single AI session.}
  {cta = Close performance gaps}

* aem-cloud-manager-mcp.md
  {title = Deploy AEM changes with confidence}
  {description = Check environment health, review pipeline history, and deploy to AEM from your AI client, without switching tools.}
  {cta = Deploy with confidence}
  {image = ../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step4-01-ai.png}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Campaign insights without reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="analyze-campaign-performance.md" title="レポートを使用しないキャンペーンインサイト">
                        <img class="is-bordered-r-small" src="../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="レポートを使用しないキャンペーンインサイト"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        レポートのない<a href="analyze-campaign-performance.md" title="レポートを使用しないキャンペーンインサイト"> キャンペーンインサイト </a>
                    </p>
                    <p class="is-size-6">単一のレポートを作成することなく、平易な言語でパフォーマンスに関する質問をおこない、Customer Journey Analyticsから回答を得ることができます。</p>
                </div>
                <a href="analyze-campaign-performance.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> キャンペーンのインサイトを表示</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Audience activation at a glance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="query-audiences.md" title="オーディエンスのアクティベーション概要">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="オーディエンスのアクティベーション概要"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="query-audiences.md" title="オーディエンスのアクティベーション概要"> オーディエンスのアクティベーション概要</a>
                    </p>
                    <p class="is-size-6">Real-Time CDPを使わずに、どのオーディエンスがライブなのか、どこを流れているのか、宛先が健全なのかを確認できます。</p>
                </div>
                <a href="query-audiences.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> オーディエンスのアクティブ化を確認</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Catch journey issues early">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="manage-ajo-journeys.md" title="ジャーニーの課題を早期に把握">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png" alt="ジャーニーの課題を早期に把握"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="manage-ajo-journeys.md" title="ジャーニーの課題を早期に把握"> ジャーニーの問題を早期に検出</a>
                    </p>
                    <p class="is-size-6">アクティブなジャーニーを監視し、オーディエンスにリーチする前に運用上の問題を特定します。</p>
                </div>
                <a href="manage-ajo-journeys.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> ジャーニーの監視</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Ship content updates faster">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="manage-aem-content.md" title="コンテンツの更新をより迅速に配信">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="コンテンツの更新をより迅速に配信"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="manage-aem-content.md" title="コンテンツの更新をより迅速に配信"> コンテンツの更新をより迅速に配信</a>
                    </p>
                    <p class="is-size-6">AEMのインターフェイスに切り替えることなく、AEMのページとコンテンツフラグメントをより迅速に検索、更新、公開できます。</p>
                </div>
                <a href="manage-aem-content.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> コンテンツの迅速な配信</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Close content performance gaps">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="optimize-content-with-performance-data.md" title="コンテンツのパフォーマンスのギャップを埋める">
                        <img class="is-bordered-r-small" src="../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png" alt="コンテンツのパフォーマンスのギャップを埋める"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="optimize-content-with-performance-data.md" title="コンテンツのパフォーマンスのギャップを埋める"> コンテンツパフォーマンスのギャップを埋める</a>
                    </p>
                    <p class="is-size-6">CJAでコンバージョンのギャップを明らかにし、AEMでコンバージョンの低いコンテンツをたどり、それを修正するために1回のAI セッションを実施します。</p>
                </div>
                <a href="optimize-content-with-performance-data.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> パフォーマンス ギャップを閉じる</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Deploy AEM changes with confidence">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="aem-cloud-manager-mcp.md" title="AEMの変更を確実にデプロイ">
                        <img class="is-bordered-r-small" src="../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step4-01-ai.png" alt="AEMの変更を確実にデプロイ"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="aem-cloud-manager-mcp.md" title="AEMの変更を確実にデプロイ">自信を持ってAEMの変更をデプロイ </a>
                    </p>
                    <p class="is-size-6">ツールを切り替えることなく、環境の健全性を確認し、パイプラインの履歴を確認し、AI クライアントからAEMにデプロイできます。</p>
                </div>
                <a href="aem-cloud-manager-mcp.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">自信を持ってデプロイ </span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
