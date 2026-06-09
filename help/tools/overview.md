---
title: エージェント型ツール
description: MCP サーバー、エージェントスキル、ビルダー用APIを比較し、Adobe CX Enterprise ワークフローに適したエージェント型ツールを選択します。
last-substantial-update: 2026-06-08T00:00:00Z
index: false
source-git-commit: 94c7d3c6b0542b6e27d8775f78acf40a1b1cae91
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 1%

---


# エージェント型ツール

<!-- last-modified: 2026-06-08 -->

あらゆるエージェンティックツールが同じニーズに対応するわけではありません。 それぞれが何をするのか、いつ使用するのか、どのように始めるべきかを検討し、状況に適した出発点を選択できるようにします。

<!--
CARDS

* mcp-servers.md
  {title = MCP Servers}
  {description = Connect any compatible AI client to Adobe CX Enterprise data and workflows. No coding required.}
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
                    <a href="mcp-servers.md" title="MCP サーバー" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-servers-card.png" alt="MCP サーバー"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="mcp-servers.md" target="_blank" rel="referrer" title="MCP サーバー">MCP サーバー</a>
                    </p>
                    <p class="is-size-6">互換性のあるあらゆるAI クライアントを、Adobe CX Enterpriseのデータおよびワークフローに接続できます。 コーディングは必要ありません。</p>
                </div>
                <a href="mcp-servers.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">MCP サーバーの探索</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="agent-skills.md" title="エージェントスキル" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="エージェントスキル"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="agent-skills.md" target="_blank" rel="referrer" title="エージェントスキル"> エージェントのスキル </a>
                    </p>
                    <p class="is-size-6">Adobeが監修したワークフロー手順により、一貫してCX エンタープライズのタスクをガイドします。</p>
                </div>
                <a href="agent-skills.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> エージェントのスキルを探る</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="apis.md" title="ビルダー用API" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-card.png" alt="ビルダー用API"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        ビルダー</a>の<a href="apis.md" target="_blank" rel="referrer" title="ビルダー用API">API
                    </p>
                    <p class="is-size-6">Adobeと同じAPIを使用して、カスタムアプリケーションや統合機能を構築できます。</p>
                </div>
                <a href="apis.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
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
| 最適な用途 | CX Enterprise アプリケーションユーザー | CX Enterprise アプリケーションのユーザーと開発者 | デベロッパー |
| コーディングが必要 | × | × | ○ |
| 設定時間 | Minutes | Minutes | 時間から日 |
| 得られるもの | AI クライアントからのCX エンタープライズアプリケーションへのアクセス | ガイド付きの反復可能なワークフロー | 完全なプログラム制御 |

## どこから始めてよいかわからないものは、

- AIを使用してCX エンタープライズ アプリケーションと対話する（アクションを実行し、データを照会し、AIが自然会話を通じて次に何をすべきかを見つけられるようにする）には、[MCP サーバー](mcp-servers.md)が最も柔軟な出発点となります。
- エージェントがCX Enterprise ワークフローに関するAdobeのベストプラクティスに即興で従えるように、[ エージェントスキル ](agent-skills.md)はそのドメインの専門知識を再利用可能な手順にエンコードします。
- ユーザー向けの特定のCX エンタープライズ ワークフローを合理化または自動化する集中型アプリケーションを構築するには、[ ビルダー向けAPI](apis.md)を使用すると、何が起こるかを正確に制御してプログラム可能な直接の制御が可能になります。

>[!BEGINTABS]

>[!TAB MCP サーバー]

MCP サーバーは、AI クライアントとCX エンタープライズアプリケーション間のライブワイヤーだと考えてください。 AIを活用すれば、キャンペーンのクエリ、オーディエンスの取得、ジャーニーのステータスの確認などを平易な言語で実行できます。コードを記述する必要はありません。

**次の場合にMCP サーバーを使用：**

- AIをCX企業ワークフローに直接統合し
- 顧客体験に関する企業データは、すでに使用しているAI クライアント内に保持する必要があります
- 探索分析や高度なデータ取得を行っている場合
- プロジェクトを立ち上げることなく、すばやく成果を達成

[MCP サーバーの探索](mcp-servers.md)

>[!TAB  エージェントのスキル ]

担当者のスキルは、Adobeのドメインの専門知識であり、担当者が従うことのできる指示としてエンコードされます。 担当者が適切なステップを見つけるのを期待する代わりに、スキルがCX Enterpriseのワークフローに対して、何をすべきか、確実に、繰り返し、既に調整されているかを正確に伝えます。

**次の場合にエージェントのスキルを使用：**

- AI クライアントを介してCX Enterprise アプリで作業を実行する場合は、Adobeのベストプラクティスに従います
- 同じタスクを毎回同じように実行する必要があります
- 反復可能なコンテンツやメディア制作ワークフローを運用している

[エージェントのスキルを見る](agent-skills.md)

>ビルダー]の[!TAB API

APIは構成要素です。 開発者は、Adobeの自社製品と同じAPIを使用して、Adobeのデータとオペレーションに直接プログラムでアクセスできます。 これらのツールを利用して、特定のビジネスワークフローを合理化し、組織が必要とするガードレールを備えたカスタマイズされたエクスペリエンスを構築できます。

**次の場合にAPIを使用：**

- 特定のビジネスユースケース向けに、カスタムアプリケーションや統合を構築する場合
- 特定のガードレールとコントロールにより、ワークフローを最適化または自動化する必要があります
- クロードコードまたはカーソルを使用して、完全なアプリケーションを生成します
- CX企業データを別のシステムに統合する必要があります

[ビルダー用APIの確認](apis.md)

>[!ENDTABS]

## それらを一緒に使用

これらのツールは連携するように設計されています。 それらを組み合わせることで、Adobe AIを最大限に活用できます。 エージェントスキルは、AI クライアントがMCP サーバーをどのように使用するかを導き、エージェントをCX エンタープライズワークフローに適切な軌道に乗せます。 また、スキルは、APIを呼び出す方法とタイミングを判断し、Adobeのベストプラクティスのガードレールをカスタムビルドの自動化に追加することもできます。 ひとつのチャネルだけを選択する必要はありません。
