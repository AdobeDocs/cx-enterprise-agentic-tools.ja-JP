---
title: MCP サーバー
description: モデルコンテキストプロトコルサーバーを使用して、MCP互換のAI クライアントをAdobe CX Enterprise ワークフローに接続します。
index: false
last-substantial-update: 2026-06-09T00:00:00Z
source-git-commit: 8f499ad7baf1b5d08dfac90511d0c76e8372c08b
workflow-type: tm+mt
source-wordcount: '2078'
ht-degree: 3%

---


# MCP サーバー

<!-- last-modified: 2026-06-09 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

Adobe CX Enterprise MCP サーバーは、互換性のあるAI クライアントに、Adobeデータやワークフローへの直接的で管理されたアクセスを提供します。 接続すれば、AI環境から直接、キャンペーンのパフォーマンスのクエリ、オーディエンスのアクティベーション、ジャーニーのレビュー、コンテンツの管理などをおわかりやすい言葉で行うことができます。 MCP サーバーは、AI クライアントとAdobeの基盤システムの間に配置されているため、企業のアクセス制御とデータガバナンスを維持しながら、自然言語の柔軟性を実現できます。

Adobe MCP サーバーは、オープン [&#x200B; モデル コンテキスト プロトコル &#x200B;](https://modelcontextprotocol.io/docs/getting-started/intro)標準に従います。 MCP対応のAI クライアントは、あらゆるAdobe MCP サーバーに接続できます。

## CX Enterprise MCP サーバー

![CX Enterprise MCPは、AI クライアントをAdobe CX Enterprise スイート全体のツールに接続します](../assets/mcp-gateway-hero.gif)

エンドポイントと機能を表示するアプリケーションを選択します。

>[!BEGINTABS]

>[!TAB CX エンタープライズ MCP]

**1つのエンドポイント。 複数のCX エンタープライズ アプリケーション。**

接続すると、AI クライアントは、組織のライセンスに基づいてCX エンタープライズアプリケーションにアクセスできます。 組織を有効にするには、[cxo-mcp-feedback@adobe.com](mailto:cxo-mcp-feedback@adobe.com)にメールを送信してアクセスをリクエストしてください。

```
https://cx-enterprise.adobe.io/mcp
```

| CX Enterprise アプリケーション | 実行できること |
| --- | --- |
| Adobe Analytics | レポートスイートの検出、セグメントのオーサリング、ワークスペースの作成 |
| Adobe Experience Platform | データセットの発見、スキーマの閲覧、サンドボックスの管理 |
| Adobe Journey Optimizer | ジャーニー、キャンペーン、チャネル設定の確認 |
| Adobe Journey Optimizer B2B edition | B2B ジャーニー、アカウントプログラム、購買グループ、パーソナライゼーションの管理 |
| Customer Journey Analytics | レポートのクエリ、データビューの確認、ワークスペースの作成 |
| Real-Time CDP | オーディエンスのアクティベーションステータス、宛先の健全性、データフローの健全性の確認 |

>[!NOTE]
>
>各CX Enterprise アプリケーションへのアクセスは、組織の使用権限とAdobe Admin Consoleでのユーザーの権限に基づいています。 組織のCX Enterprise MCPを有効にするには、[cxo-mcp-feedback@adobe.com](mailto:cxo-mcp-feedback@adobe.com)に電子メールを送信します。

>[!TAB Experience Manager]

Adobe Experience Managerには、異なるワークフロー用に複数のMCP サーバーがあります。

| MCP サーバー | エンドポイント | 実行できること |
| --- | --- | --- |
| [AEM （コードモード） &#x200B;](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/aem` | 自然言語のルックアップ、読み取り、書き込み、削除により、AEMにREST API アクセスを直接実行できます |
| [AEM Cloud Manager](https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | プログラム、環境、パイプライン、リポジトリの管理 |
| [AEM コンテンツ &#x200B;](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | ページ、コンテンツフラグメント、アセット、ローンチの管理 |
| [AEM コンテンツ （読み取り専用） &#x200B;](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | 書き込みアクセスなしで、ページ、コンテンツフラグメント、ローンチを発見、クエリできます |
| AEM Document Authoring | `https://mcp.adobeaemcloud.com/adobe/mcp/da` | 文書オーサリングでのファイル、バージョン履歴、メディア参照の管理 |
| [AEM Experience Governance](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/mcp-servers/experience-governance-mcp-server) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-governance` | ブランドガイドラインやコンプライアンスルールに照らしてコンテンツや画像を評価する |
| [AEM Experience Production](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/experience-production/overview) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-production` | AIを活用したコンテンツ概要により、AEMページを大規模に変革、作成できます |

>[!NOTE]
>
>各AEM環境へのアクセスは、組織のAEM Cloud Serviceの使用権限と、その環境でのユーザーの権限によって異なります。

>[!TAB Experience Platform]

| MCP サーバー | エンドポイント | 実行できること |
| --- | --- | --- |
| Adobe Marketing Agent | `https://aep-ai-ama.adobe.io/mcp` | AEPアプリケーションをまたいで、オーディエンス分析、AEP診断、AJO B2B ジャーニーの構築を連携できます |

>[!NOTE]
>
>アクセス権は、組織のAdobe Experience Platform使用権限とユーザーの権限によって異なります。

>[!TAB Marketo Engage]

| MCP サーバー | エンドポイント | 実行できること |
| --- | --- | --- |
| [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/mcp-server) | `https://marketo-mcp.adobe.io/mcp` | プログラム、キャンペーン、リード、スマートリスト、メール、フォームを管理する |

>[!NOTE]
>
>Marketo Engage MCPは、Adobe IMSではなく、Marketoネイティブのサービス資格情報を使用します。 認証設定については、[Marketo Engage MCP Server ドキュメント &#x200B;](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/mcp-server)を参照してください。 アクセスは、Marketo Engage サブスクリプションとAPI ユーザーの権限によって異なります。

>[!TAB Target]

Adobe Target MCPはパブリックベータ版です。 現在利用可能なすべてのツールは読み取り専用です。 書き込みツールは、一般公開に向けて計画されています。

| MCP サーバー | エンドポイント | 実行できること |
| --- | --- | --- |
| [Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/mcp/target-mcp) | `https://targetmcp.adobe.io/mcp` | アクティビティ、オファー、オーディエンス、mbox、パフォーマンスレポートの確認 |

>[!NOTE]
>
>アクセスは、Adobe Targetの使用権限とユーザーの権限によって異なります。

>[!TAB Workfront]

| MCP サーバー | エンドポイント | 実行できること |
| --- | --- | --- |
| Adobe Workfront | `https://mcp.prod.us-west-2.aws.wfk8s.com/mcp/v1/workfront` | 作業、プロジェクト、プランニングレコード、インサイト、コンテンツ承認を管理できます |

>[!NOTE]
>
>アクセス権は、Adobe Workfront ライセンスとユーザーの権限によって異なります。

>[!ENDTABS]

## AI クライアントに接続します

すべてのAdobe MCP サーバーは、Adobe Identity Management サービス（IMS）でOAuthを使用します。 プロンプトが表示されたら、正しいIMS組織を選択します。 間違ったものを選択することは、認証エラーの最も一般的な原因です。

手動で設定する前に、AI クライアントとAdobe アプリケーションのマネージドコネクタの[Adobe AI Registry](https://developer.adobe.com/ai-registry/?type=connector)を確認してください。 マネージドコネクタで認証を自動的に処理します。 クライアントとアプリケーションでコネクタが使用可能な場合は、以下の手動手順の代わりにそれを使用します。

次の手順では、例としてCX Enterprise MCP エンドポイントを使用します。 同じプロセスがAdobe MCP サーバーにも適用されます。接続するサーバーのエンドポイント URLをスワップします。

![Adobe MCP サーバーに接続しているAI エージェント &#x200B;](../assets/hero-connect-mcp-servers.gif)

>[!BEGINTABS]

>[!TAB  クロード.ai]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="推奨"> マネージド コネクタを使用

[Adobe AI レジストリ &#x200B;](https://developer.adobe.com/ai-registry/?type=connector)に移動し、Adobe アプリケーションを検索します。 Claude コネクタが一覧表示されている場合（例：[Adobe Experience Manager コネクタ &#x200B;](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)）、次の手順ではなく、その設定手順に従います。

### カスタムコネクタを使用した接続

Claude.aiは、アカウント設定のカスタムコネクタを介してリモート MCP サーバーをサポートします。

1. **設定/統合**&#x200B;に移動します。
2. 「**カスタムコネクタを追加**」をクリックします。
3. サーバーエンドポイントをURL （CX Enterprise MCPの場合は`https://cx-enterprise.adobe.io/mcp`など）として入力し、選択した表示名を入力します。
4. **Connect**&#x200B;をクリックし、Adobe IDでログインします。 適切なIMS組織を選択します。

完全なセットアップ：[Claude.ai カスタムコネクタのドキュメント &#x200B;](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB  クロード コード ]

### CLIの使用

`claude mcp add`を実行して、Adobe MCP サーバーを登録します。 サーバー名とURLを、接続するサーバーの値に置き換えます。 この例では、CX Enterprise MCPを使用します。

```bash
claude mcp add --transport http adobe-cx-enterprise https://cx-enterprise.adobe.io/mcp
```

### 設定ファイルを編集

サーバーをプロジェクトルート （プロジェクトレベル）の`~/.claude.json` （グローバル）または`.mcp.json`に追加します。 キーとURLを、接続するサーバーの値に置き換えます。

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

Adobe MCP サーバーはOAuthを使用します。 Claude Codeは、ツールを初めて呼び出したときに、Adobe IDでの認証を求めるプロンプトを表示します。 プロンプトが表示されたら、正しいIMS組織を選択します。

完全なセットアップ：[Claude Code MCP ドキュメント &#x200B;](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB  カーソル ]

Adobe MCP サーバーをCursor `mcp.json`設定ファイルに追加し、**Settings > MCP**&#x200B;経由で接続します。 キーとURLを、接続するサーバーの値に置き換えます。 この例では、CX Enterprise MCPを使用します。

- **グローバル （すべてのプロジェクト）:** `~/.cursor/mcp.json`
- **プロジェクトレベル：** `.cursor/mcp.json` （プロジェクトルート内）

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

追加すると、カーソル設定の&#x200B;**インストール済みMCP サーバー**&#x200B;の下にMCP サーバーが表示されます。 **認証が必要**&#x200B;と表示されているサーバーの横にある&#x200B;**Connect**&#x200B;を選択し、Adobe IDでログインします。 アプリケーションにアクセスできるIMS組織を選択します。

![&#x200B; インストール済みのAdobe MCP サーバーとmcp.json](../assets/screenshots/cursor-mcp-server-configuration.jpg)を示すCursor MCP サーバー設定

完全なセットアップ：[&#x200B; カーソル MCP ドキュメント &#x200B;](https://cursor.com/docs/mcp)

>[!TAB ChatGPT]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="推奨"> マネージド コネクタを使用

[Adobe AI レジストリ &#x200B;](https://developer.adobe.com/ai-registry/?type=connector)に移動し、Adobe アプリケーションを検索します。 ChatGPT コネクタがリストされている場合は、以下の手順ではなく、その設定手順に従います。

### リモート MCP サーバーを使用した接続

ChatGPTは、[開発者モード &#x200B;](https://developers.openai.com/api/docs/guides/developer-mode)を介したリモート MCP サーバーをサポートしています。これは、Pro、Plus、Business、Enterprise、Education プランで利用できます。

1. **ChatGPT設定**&#x200B;で開発者モードを有効にします。
2. **設定/統合**&#x200B;に移動します。
3. 「**カスタムコネクタを追加**」をクリックし、**リモート MCP サーバー**&#x200B;を選択します。
4. サーバーエンドポイントをURL （CX Enterprise MCPの場合は`https://cx-enterprise.adobe.io/mcp`など）として入力し、選択した表示名を入力します。
5. 認証を&#x200B;**OAuth**&#x200B;に設定します。
6. **Connect**&#x200B;をクリックし、Adobe IDでログインします。 適切なIMS組織を選択します。

完全なセットアップ：[ChatGPT MCP ドキュメント &#x200B;](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB OpenAI Codex CLI]

OpenAI Codex CLIは、TOML設定を介してリモート MCP サーバーをサポートします。

**ファイルの場所を設定：**

- **ユーザーレベル （すべてのプロジェクト）:** `~/.codex/config.toml`
- **プロジェクト範囲：** `.codex/config.toml` （プロジェクトルート内）

セクション名とURLを、接続するサーバーの値に置き換えます。 この例では、CX Enterprise MCPを使用します。

```toml
[mcp_servers.adobe-cx-enterprise]
url = "https://cx-enterprise.adobe.io/mcp"
enabled = true
```

Adobe MCP サーバーはOAuthを使用します。 Codex CLIは、初回使用時にOAuth フローを自動的に処理します。 プロンプトが表示されたら、正しいIMS組織を選択します。

完全なセットアップ：[OpenAI Codex CLI MCP ドキュメント &#x200B;](https://developers.openai.com/codex/mcp)

>[!TAB  コパイロット スタジオ ]

Microsoft Copilot Studioは、Power Platform カスタムコネクタを自動的に作成するMCP オンボーディングウィザードを使用して、リモート MCP サーバーに接続します。

1. Copilot Studioでエージェントを開きます。
2. **ツール** ページに移動します。
3. **ツールを追加/新規ツール/モデルコンテキストプロトコル**&#x200B;を選択します。
4. MCP オンボーディングウィザードで、サーバーの詳細を入力します。 例えば、CX Enterprise MCPの場合は次のようになります。
   - **サーバー名：** `Adobe CX Enterprise`
   - **サーバーURL:** `https://cx-enterprise.adobe.io/mcp`
5. Authenticationを&#x200B;**OAuth 2.0**&#x200B;に設定し、Adobe IMS認証とトークン URLを使用して設定します。
6. 「**作成**」、「**エージェントに追加**」の順に選択します。

>[!NOTE]
>
>Copilot StudioのMCP サーバー接続は、Power Platformを介して行われます。 組織のデータ損失防止（DLP）ポリシーが適用されます。

完全なセットアップ：[Copilot Studio MCP ドキュメント &#x200B;](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## エージェント型ツールの活用例

実際のビジネスワークフローに適用されるAdobe CX Enterprise MCP サーバーを参照してください。

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use CX Enterprise MCP to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use CX Enterprise MCP to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* ../use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use CX Enterprise MCP to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* ../use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine CX Enterprise MCP and AEM Content MCP Server to find underperforming content and update it in one session.}
  {cta = Start walkthrough}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="キャンペーンのパフォーマンスを分析">
                        <img class="is-bordered-r-small" src="../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="キャンペーンのパフォーマンスを分析"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/analyze-campaign-performance.md" title="キャンペーンのパフォーマンスを分析"> キャンペーンパフォーマンスの分析</a>
                    </p>
                    <p class="is-size-6">CX Enterprise MCPを使用して、あらゆるAI クライアントからCustomer Journey Analyticsの指標とインサイトを可視化します。</p>
                </div>
                <a href="../use-cases/analyze-campaign-performance.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> チュートリアルを開始</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="オーディエンスの照会">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="オーディエンスの照会"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" title="オーディエンスの照会"> オーディエンスのクエリ </a>
                    </p>
                    <p class="is-size-6">CX Enterprise MCPを使用して、平易な言語プロンプトを使用してReal-Time CDPのオーディエンスと宛先データをクエリします。</p>
                </div>
                <a href="../use-cases/query-audiences.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> チュートリアルを開始</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Review AJO journeys">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-ajo-journeys.md" title="AJO ジャーニーのレビュー">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png" alt="AJO ジャーニーのレビュー"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-ajo-journeys.md" title="AJO ジャーニーのレビュー">AJO ジャーニーのレビュー</a>
                    </p>
                    <p class="is-size-6">CX Enterprise MCPを使用して、AI クライアントからAJOのジャーニー、キャンペーンステータス、ジャーニー条件にアクセスします。</p>
                </div>
                <a href="../use-cases/manage-ajo-journeys.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> チュートリアルを開始</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Manage AEM content with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-aem-content.md" title="AIを活用したAEMコンテンツの管理">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="AIを活用したAEMコンテンツの管理"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-aem-content.md" title="AIを活用したAEMコンテンツの管理">AIを使用したAEM コンテンツの管理</a>
                    </p>
                    <p class="is-size-6">AEMの自然言語を使用して、ページとコンテンツフラグメントを検索、更新、公開できます。</p>
                </div>
                <a href="../use-cases/manage-aem-content.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> チュートリアルを開始</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Optimize content based on performance data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/optimize-content-with-performance-data.md" title="パフォーマンスデータに基づくコンテンツの最適化">
                        <img class="is-bordered-r-small" src="../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png" alt="パフォーマンスデータに基づくコンテンツの最適化"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/optimize-content-with-performance-data.md" title="パフォーマンスデータに基づくコンテンツの最適化"> パフォーマンスデータに基づいてコンテンツを最適化</a>
                    </p>
                    <p class="is-size-6">CX Enterprise MCPとAEM Content MCP Serverを組み合わせることで、パフォーマンスの低いコンテンツを特定し、1回のセッションで更新できます。</p>
                </div>
                <a href="../use-cases/optimize-content-with-performance-data.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> チュートリアルを開始</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## もっと手伝いが必要ですか？

MCP接続には、認証、組織の選択、アプリケーションレベルの権限が含まれます。 何かが期待どおりに機能しない場合は、これらの手順で最も一般的な原因を説明します。

+++Adobe組織の切り替え

Adobe ユーザーが複数のIMS組織に属しており、間違った組織のツールやデータが表示されている場合は、MCP サーバーを切断し、ブラウザーでAdobe セッションからログアウトしてから、再接続します。 ログイン時に組織を選択するよう求められます。

Adobe CX Enterprise MCP サーバーは、ユーザーアカウントが複数のアクセス権を持っている場合でも、一度に1つのIMS組織に対してのみ認証できます。

+++

+++サンドボックス、レポートスイート、環境、またはその他のセッションリソースの指定

一部のAdobe CX Enterprise MCP サーバーでは、結果を返す前にリソースを指定する必要があります。 アプリケーションによっては、サンドボックス、プログラム、環境、レポートスイート、データビューなどがあります。

アクセスできるリソースがわからない場合は、AI クライアントに問い合わせます。 例：「使用可能なサンドボックスのリスト」または「どのレポートスイートにアクセスできますか？」 Adobe CX Enterprise MCP サーバーは、多くの場合、ユーザーが利用できるリソースの完全なリストを返します。

セッションリソースを設定したら、どのリソースを使用するかをAI クライアントに伝えることで、いつでも切り替えることができます。

+++

+++権限とアクセスのエラー

AI クライアントは、OAuthを使用して、Adobeユーザーアカウントの代理として行動します。 Adobe アプリケーションにログインするときに適用される同じ権限とアクセス制御は、MCP サーバーを使用するときに適用されます。

アクションが失敗するか、結果が返されない場合は、Adobe Admin Consoleおよび関連するCX Enterprise アプリケーションで、ユーザーが必要な権限を持っていることを確認します。 アクセス権を調整する必要がある場合は、Adobe システム管理者にお問い合わせください。

+++

+++セッションを失った後の再認証

Adobe CX Enterprise MCP サーバーは、OAuthを使用してAdobe ユーザーアカウントを認証します。 認証状態が失われると、再認証するまで、それ以上のツール呼び出しは成功しません。

再認証するには：AI クライアントのMCP サーバー設定を開き、Adobe CX Enterprise MCP サーバーエントリを選択して再接続します。 Adobe IDで再度ログインするよう求められます。

+++
