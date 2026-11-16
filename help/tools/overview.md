---
title: エージェント型ツール
description: MCP サーバー、エージェントスキル、ビルダー用APIを比較し、Adobe CX Enterpriseワークフローに適したエージェント型ツールを選択します。
last-substantial-update: 2026-11-16
source-git-commit: a75d5f3af3077b259da796bd381d605ae826585d
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 2%
---

# エージェント型ツール

<!-- last-modified: 2026-06-08 -->

あらゆるエージェンティックツールが同じニーズに対応するわけではありません。 それぞれが何をするのか、いつ使用するのか、どのように始めるべきかを検討し、状況に適した出発点を選択できるようにします。

<!--
CARDS

* mcp-servers.md
  {title = MCP Servers}
  {description = Connect any compatible AI platform to Adobe CX Enterprise data and workflows. No coding required.}
  {cta = Explore MCP Servers}
  {image = ../assets/mcp-servers-card.png}

* agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflow instructions that guide agents through CX Enterprise tasks consistently.}
  {cta = Explore Agent Skills}
  {image = ../assets/agent-skills-card.png}

* apis.md
  {title = APIs for Builders}
  {description = Build custom applications and integrations using the same APIs that power Adobe products.}
  {cta = Explore APIs for Builders}
  {image = ../assets/apis-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="mcp-servers.md" title="MCP サーバー">
                        <img class="is-bordered-r-small" src="../assets/mcp-servers-card.png" alt="MCP サーバー"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="mcp-servers.md" title="MCP サーバー">MCP サーバー</a>
                    </p>
                    <p class="is-size-6">互換性のあるあらゆるAI基盤を、Adobe CX Enterpriseのデータおよびワークフローに接続。 コーディングは必要ありません。</p>
                </div>
                <a href="mcp-servers.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">MCP サーバーの探索</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="agent-skills.md" title="エージェントスキル">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="エージェントスキル"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="agent-skills.md" title="エージェントスキル"> エージェントのスキル </a>
                    </p>
                    <p class="is-size-6">Adobeがキュレートしたワークフロー手順により、エージェントは一貫してCX Enterpriseのタスクを進めることができます。</p>
                </div>
                <a href="agent-skills.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> エージェントのスキルを探る</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="apis.md" title="ビルダー用API">
                        <img class="is-bordered-r-small" src="../assets/apis-card.png" alt="ビルダー用API"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        ビルダー</a>の<a href="apis.md" title="ビルダー用API">API
                    </p>
                    <p class="is-size-6">Adobeと同じAPIを使用して、カスタムアプリケーションや統合機能を構築できます。</p>
                </div>
                <a href="apis.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> ビルダー用APIの探索</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->


## エージェント型ツールの比較

| | MCP サーバー | エージェントスキル | ビルダー用API |
| --- | --- | --- | --- |
| 最適な用途 | CX Enterprise アプリケーションユーザー | CX Enterprise アプリケーションユーザーと開発者 | デベロッパー |
| コーディングが必要 | × | × | ○ |
| 設定時間 | Minutes | Minutes | 時間から日 |
| 得られるもの | AI基盤からCX Enterpriseアプリケーションにアクセスし | ガイド付きの反復可能なワークフロー | 完全なプログラム制御 |

## どこから始めてよいかわからない方は、

- AIを使用してCX Enterprise アプリケーションと対話する（アクションを実行し、データを照会し、AIが自然な会話を通じて次に何をすべきかを発見できるようにする）には、[MCP サーバー](mcp-servers.md)が最も柔軟な出発点となります。
- エージェントがCX Enterprise ワークフローに関するAdobeのベストプラクティスに即興で従えるように、[ エージェントスキル ](agent-skills.md)はそのドメインの専門知識を再利用可能な手順にエンコードします。
- CX Enterpriseの特定のワークフローを合理化または自動化する専用アプリケーションを構築するには、[ ビルダー用API](apis.md)を使用すると、何が起こるかを正確に制御できます。

>[!BEGINTABS]

>[!TAB MCP サーバー]

MCP サーバーは、AI プラットフォームとCX Enterpriseアプリケーションを接続するライブワイヤーだと考えてください。 [Adobe CX Enterprise Coworker for AI Platforms](mcp-servers.md#connect-to-your-ai-platform)から始めます。一度つながると、AI基盤でAdobe CX Enterprise Coworkerを使用して、キャンペーンのクエリ、オーディエンスの取得、ジャーニーのステータスの確認などを簡単な言葉で実行できます。コードは必要ありません。 機能しない場合は、[製品MCP サーバー](mcp-servers.md#connect-to-your-ai-platform)に直接接続してください。

**次の場合にMCP サーバーを使用：**

- AIをCX Enterpriseのワークフローに直接統合し
- 既存のAI基盤にCX Enterpriseのデータを組み込むことで
- 探索分析や高度なデータ取得を行っている場合
- プロジェクトを立ち上げることなく、すばやく成果を達成

[MCP サーバーの探索](mcp-servers.md)

>[!TAB  エージェントのスキル ]

担当者のスキルは、Adobeのドメインの専門知識であり、担当者が従うことのできる指示としてエンコードされます。 担当者が適切なステップを見つけられることを期待するのではなく、CX Enterpriseのワークフローに合わせて何をすべきか、確実に、繰り返し、事前に調整すべきことを正確に指示できます。

**次の場合にエージェントのスキルを使用：**

- AIを利用してCX Enterprise アプリケーションで作業する場合は、Adobeのベストプラクティスに従ってください
- 同じタスクを毎回同じように実行する必要があります
- 反復可能なコンテンツやメディア制作ワークフローを運用している

[エージェントのスキルを見る](agent-skills.md)

>ビルダー]の[!TAB API

APIは構成要素です。 開発者は、Adobeの自社製品と同じAPIを使用して、Adobeのデータとオペレーションに直接プログラムでアクセスできます。 これらのツールを利用して、特定のビジネスワークフローを合理化し、組織が必要とするガードレールを備えたカスタマイズされたエクスペリエンスを構築できます。

**次の場合にAPIを使用：**

- 特定のビジネスユースケース向けに、カスタムアプリケーションや統合を構築する場合
- 特定のガードレールとコントロールにより、ワークフローを最適化または自動化する必要があります
- クロードコードまたはカーソルを使用して、完全なアプリケーションを生成します
- CX Enterpriseのデータを

[ビルダー用APIの確認](apis.md)

>[!ENDTABS]

## それらを一緒に使用

これらのツールは連携するように設計されています。 それらを組み合わせることで、Adobe AIを最大限に活用できます。 エージェントスキルは、AI プラットフォームがMCP サーバーをどのように使用するかを導き、エージェントをCX Enterpriseワークフローに適切な軌道に乗せます。 また、スキルは、APIを呼び出す方法とタイミングを判断し、Adobeのベストプラクティスのガードレールをカスタムビルドの自動化に追加することもできます。 ひとつのチャネルだけを選択する必要はありません。

## エージェント型ツールの活用例

CX Enterpriseのワークフローに適したツールをご覧ください。

<!--
CARDS

* ../use-cases/query-audiences.md
  {title = Audience activation at a glance}
  {description = See which audiences are live, where they are flowing, and whether destinations are healthy, without navigating Real-Time CDP.}
  {cta = Check audience activation}

* https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development
  {title = Develop AEM components with AI}
  {description = Use Claude Code or Cursor with Agent Skills to scaffold, code, and refine AEM components guided by Adobe best practices.}
  {cta = Try with Agent Skills}
  {image = ../assets/agent-skills-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app
  {title = Invoke AEM APIs from a web app}
  {description = Build a web application that authenticates users and calls AEM OpenAPIs using OAuth to deliver governed, programmatic access.}
  {cta = Try with APIs}
  {image = ../assets/using-api-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Audience activation at a glance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="オーディエンスのアクティベーション概要">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="オーディエンスのアクティベーション概要"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" title="オーディエンスのアクティベーション概要"> オーディエンスのアクティベーション概要</a>
                    </p>
                    <p class="is-size-6">Real-Time CDPを使わずに、どのオーディエンスがライブなのか、どこを流れているのか、宛先が健全なのかを確認できます。</p>
                </div>
                <a href="../use-cases/query-audiences.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> オーディエンスのアクティブ化を確認</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Develop AEM components with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" title="AIを活用したAEMコンポーネントの開発" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="AIを活用したAEMコンポーネントの開発"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" title="AIを活用したAEMコンポーネントの開発">AIを使用してAEM コンポーネントを開発</a>
                    </p>
                    <p class="is-size-6">Agent SkillsでClaude CodeまたはCursorを使用して、Adobeのベストプラクティスに従って、AEM コンポーネントを基礎モード化、コード化、調整します。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> エージェントのスキルを試す</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Invoke AEM APIs from a web app">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" title="Web アプリからのAEM APIの呼び出し" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/using-api-card.png" alt="Web アプリからのAEM APIの呼び出し"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" title="Web アプリからのAEM APIの呼び出し">Web アプリからAEM APIを呼び出す</a>
                    </p>
                    <p class="is-size-6">OAuthを使用してユーザーを認証し、AEM OpenAPIを呼び出して、管理されたプログラマティックなアクセスを提供するweb アプリケーションを構築します。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">APIで試す</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
