---
title: エージェント型ツール
description: MCP サーバー、エージェントスキル、ビルダー用APIを比較し、Adobe CX Enterprise ワークフローに適したエージェント型ツールを選択します。
index: false
source-git-commit: 3c29bfeeef3d2cb523724db02448aaa77cdf8900
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 1%

---


# エージェント型ツール

<!-- last-modified: 2026-05-08 -->

あらゆるエージェント型ツールが同じニーズに対応するわけではありません。 MCP サーバーを利用すれば、コーディング不要で、互換性のあるAI クライアントからAdobeデータに自然言語で即座にアクセスできます。 Agent Skillsは、Adobeドメインの専門知識を繰り返し可能なエージェントワークフローに組み込むことで、タスクを常に一貫性のある方法で実行することができます。 開発者は、APIを通じて完全にプログラム制御をおこない、カスタムアプリケーションを構築して統合できます。 このページでは、トレードオフについて解説し、自身の状況に適した出発点を選択できるようにします。

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
| 最適な用途 | AI クライアントユーザー | すべてのユーザー | デベロッパー |
| コーディングが必要 | × | × | ○ |
| 設定時間 | Minutes | Minutes | 時間から日 |
| 得られるもの | AI ツールからのAdobeへのアクセス | ガイド付きの反復可能なワークフロー | 完全なプログラム制御 |
| AI クライアントが必要 | ○ | ○ | オプション |

## どこから始めてよいかわからないものは、

- AIを使用してAdobe CX Enterprise アプリケーションと対話する（アクションを実行し、データを照会し、AIが自然な会話を通じて次に何をすべきかを発見できるようにする）には、[MCP サーバー](mcp-servers.md)が最も柔軟な出発点となります。
- エージェントがAdobe ネイティブのワークフローに即時に従えるように、[ エージェントスキル ](agent-skills.md)はそのドメインの専門知識を再利用可能な手順にエンコードします。
- Adobeの特定のワークフローを合理化または自動化する専用アプリケーションを構築するには、[ ビルダー用API](apis.md)を使用すると、何が起こるかを正確に制御できます。

>[!BEGINTABS]

>[!TAB MCP サーバー]

MCP サーバーは、AI ツールとAdobeの間を接続するライブワイヤーだと考えてください。 一度連携すれば、AIがキャンペーンのクエリ、オーディエンスの取得、ジャーニーのステータスの確認などを行うのに役立ちます。 コードは必要ありません。

**次の場合にMCP サーバーを使用：**

- 既存のAI ツールにAdobeのデータを組み込むことで
- 探索分析や高度なデータ取得を行っている場合
- プロジェクトを立ち上げることなく、すばやく成果を達成

**試してみる：** Claudeにアクティブなジャーニーの要約を依頼します。 ChatGPTからReal-Time CDPのオーディエンスサイズを取得します。 ダッシュボードを開かずにCJAのキャンペーン指標を確認できます。

[MCP サーバーの探索](mcp-servers.md)

>[!TAB  エージェントのスキル ]

担当者のスキルは、Adobeのドメインの専門知識であり、担当者が従うことのできる指示としてエンコードされます。 担当者が適切なステップを見つけられることを期待するのではなく、適切な手順を説明する必要があります。 Adobeワークフロー向けに、信頼性が高く、反復可能で、すでに調整されている。

**次の場合にエージェントのスキルを使用：**

- 同じタスクを毎回同じように実行する必要があります
- 反復可能なコンテンツやメディア制作ワークフローを運用している
- Adobeについて説明しなくても理解できる担当者が必要です

**試してみる：** バッチで一連の写真を編集して、まとまりのある見た目にします。 単一のソースアセットから、プラットフォームに対応したソーシャルコンテンツのバリエーションを生成。 少数のプロンプトで、Adobe Express テンプレートからデザインします。

[エージェントのスキルを見る](agent-skills.md)

>ビルダー]の[!TAB API

APIは構成要素です。 開発者は、Adobeの自社製品と同じAPIを使用して、Adobeのデータとオペレーションに直接プログラムでアクセスできます。 スケジュール、条件、スタックを実行するものを構築するために使用します。

**次の場合にAPIを使用：**

- カスタムアプリケーションやダッシュボードを構築するときに
- Adobeのデータを
- クロードコードまたはカーソルを使用して、完全なアプリケーションを生成します
- 完全な作成、更新、削除コントロールが必要です

**試す：** カスタムキャンペーンダッシュボードを作成します。 データパイプラインの自動化。 Adobe Experience Platformに読み取りと書き込みを行うClaude Codeを使用してアプリケーションを生成します。

[ビルダー用APIの確認](apis.md)

>[!ENDTABS]

## それらを一緒に使用

MCP サーバー、エージェントスキル、APIは補完的なものです。 多くのワークフローは、次の3つを組み合わせています。

- エージェントスキルは、ワークフローを定義し、エージェントをガイドします
- MCP サーバーは、エージェントにAdobe データへの読み取りアクセス権を付与します
- APIは、システムへの直接書き込みやカスタムアプリケーションロジックを必要とするアクションを処理します
