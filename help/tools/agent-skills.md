---
title: エージェントスキル
description: Adobeが監修したワークフローと手引きを活用して、AI エージェントがCX Enterpriseのタスクを一貫して進められるようにします。
last-substantial-update: 2026-05-19T00:00:00Z
index: false
source-git-commit: f7ace53bd5988b5902659c89c6da16448398e0c0
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 1%

---


# エージェントのスキル

<!-- last-modified: 2026-05-19 -->

Adobe CX Enterpriseの![担当者のスキル &#x200B;](../assets/hero-agent-skills.png)

エージェントスキルは、Adobeがキュレートしたワークフローで、AI エージェントがAdobe CX Enterpriseのタスクを確実に完了するためのステップバイステップの手順を提供します。 各エージェントスキルは、ドメインの専門知識とベストプラクティスをエンコードすることで、エージェントが改善を必要とせずに、一貫した検証済みの結果を生成できるようにします。 エージェントのスキルは、会話をまたいで繰り返し可能なガイド付きの行動を求めるときに理にかなっています。特に、毎回詳細なプロンプトが必要になるタスクでは、これが重要になります。 これらはMCP サーバーとAPIを補完します。エージェントスキルはエージェントの仕組みを定義し、MCP サーバーとAPIは基礎となるアクセスを提供します。

## Adobe CX Enterpriseの担当者のスキル

そのワークフローのスキルを探るには、以下の機能領域を選択してください。

>[!BEGINTABS]

>[!TAB Adobe Experience Manager]

AEM as a Cloud Service、Edge Delivery Services、AEM 6.5 LTSをまたいだ、Experience Managerの開発、コンテンツ、デザイン、プロジェクト管理のためのエージェントスキル。

[エージェントのスキルの表示](https://github.com/adobe/skills/tree/main/plugins/aem)

>[!TAB Adobe Analytics]

Adobe AnalyticsのKPI モニタリング、funnel分析、エグゼクティブレポートワークフローのエージェントスキル。

[エージェントのスキルの表示](https://github.com/adobe/skills/tree/main/plugins/adobe-analytics)

>[!TAB Customer Journey Analytics]

Customer Journey Analyticsのパフォーマンス比較、ディメンション分析、ワークスペースのオーサリングのためのエージェントスキル。

[エージェントのスキルの表示](https://github.com/adobe/skills/tree/main/plugins/adobe-cja)

>[!TAB Adobe App Builder]

Adobe App Builderを使用したカスタムアプリケーションの基礎、テスト、デプロイのためのエージェントスキル。

[エージェントのスキルの表示](https://github.com/adobe/skills/tree/main/plugins/app-builder)

>[!TAB Creative Cloud]

Creative Cloudを使用した、一括写真編集、テンプレートからのデザイン、動画編集、ソーシャルメディアのバリエーションなどのエージェントのスキル。

[エージェントのスキルの表示](https://github.com/adobe/skills/tree/main/plugins/creative-cloud)

>[!ENDTABS]

## エージェントのスキルを追加

![&#x200B; エージェントスキルの仕組み](../assets/hero-connect-agent-skills.gif)

エージェントスキルとは、AI担当者にAdobeのエージェント型ツールを使用してタスクを完了する方法を伝える一連の指示です。 エージェントがスキルを読み込むと、即興ではなく、そのワークフローに従います。

### エージェントのスキルのインストール

エージェントスキルは、使用しているAI クライアントに基づいてインストールされます。 一部のクライアントは、コマンドラインからの直接インストールをサポートしています。

- **クロード コード**: `/plugin install adobe/skills`
- **ノード環境**: `npx skills add adobe/skills`
- **GitHub CLI**: `gh upskill adobe/skills`

他のクライアントでは、スキルファイルをダウンロードしてAI クライアントに直接追加する必要があります。 クライアントによる完全なインストール手順については、GitHub[&#128279;](https://github.com/adobe/skills#installation)のAdobe Skills READMEを参照してください。

### エージェントのスキルを見つける

利用可能なスキルの完全なリストについては、[Adobe Skills GitHub リポジトリ &#x200B;](https://github.com/adobe/skills)を参照してください。 各エージェントスキルには、詳細なガイダンス、参照、例を含む`SKILL.md` ファイルが含まれています。

`adobe/skills` パッケージをインストールまたは追加した後、一部のAI クライアントでは、利用可能なすべてのスキルを直接一覧表示できます。

- **クロード コード**: `claude /plugin list`
- **ノード環境**: `npx skills list`
- **GitHub CLI**: `gh upskill list`

## エージェントのスキル

担当者のスキル :Adobeの専門知識を利用して、AI クライアント内で作業を進めることができます。これにより、担当者は即興で作業するのではなく、実績のあるワークフローに従うことができるようになります。 以下の各チュートリアルでは、Adobeのベストプラクティスに従って、最初から出力まで、確実に完了した特定のビジネスタスクを示します。

<!--
CARDS

* https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development
  {title = Develop AEM components with AI}
  {description = Use Claude Code or Cursor with Agent Skills to scaffold, code, and refine AEM components guided by Adobe best practices.}
  {cta = Try with Agent Skills}
  {image = ../assets/agent-skills-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Develop AEM components with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" title="AIを活用したAEMコンポーネントの開発" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="AIを活用したAEMコンポーネントの開発"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" title="AIを活用したAEMコンポーネントの開発">AIを使用してAEM コンポーネントを開発</a>
                    </p>
                    <p class="is-size-6">Agent SkillsでClaude CodeまたはCursorを使用して、Adobeのベストプラクティスに従って、AEM コンポーネントを基礎モード化、コード化、調整します。</p>
                </div>
                <a href="https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> エージェントのスキルを試す</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
