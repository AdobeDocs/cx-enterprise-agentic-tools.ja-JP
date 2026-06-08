---
title: MCP サーバー
description: モデルコンテキストプロトコルサーバーを使用して、MCP互換のAI クライアントをAdobe CX Enterprise ワークフローに接続します。
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1601'
ht-degree: 2%

---


# MCP サーバー

<!-- last-modified: 2026-05-19 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491323/?captions=jpn&learn=on&enablevpops)

Adobe CX Enterprise MCP サーバーは、互換性のあるAI クライアントに、Adobeデータやワークフローへの直接的で管理されたアクセスを提供します。 接続すれば、AI環境から直接、キャンペーンのパフォーマンスのクエリ、オーディエンスのアクティベーション、ジャーニーのレビュー、コンテンツの管理などをおわかりやすい言葉で行うことができます。 MCP サーバーは、AI クライアントとAdobeの基盤システムの間に配置されているため、企業のアクセス制御とデータガバナンスを維持しながら、自然言語の柔軟性を実現できます。

Adobe MCP サーバーは、オープンなModel Context Protocol標準に従っています。 MCP対応のAI クライアントは、あらゆるAdobe MCP サーバーに接続できます。

## CX Enterprise MCP Gateway

![CX Enterprise MCP Gatewayは、AI クライアントをAdobe CX Enterprise スイート全体のMCP ツールに接続します](../assets/mcp-gateway-hero.gif)

**1つのエンドポイント。 すべてのAdobe CX Enterprise MCP サーバー。**

CX エンタープライズゲートウェイは、AI クライアントを、分析、キャンペーン、コンテンツ、データをまたいでツールにルーティングします。各アプリケーションを個別に接続する必要はありません。 一度接続すると、Adobeの使用権限に基づいて、ライセンスが付与されたツールのみがゲートウェイに表示されます。

>[!BEGINTABS]

>[!TAB CX エンタープライズ アプリケーション ]

組織のAdobe ライセンスに基づいて、各アプリケーションのツールを利用できます。

| アプリケーション | 実行できること |
| --- | --- |
| Adobe Journey Optimizer | [&#x200B; ジャーニー、キャンペーン、チャネル設定の確認](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) |
| Customer Journey Analytics | [&#x200B; レポートのクエリ、データビューの検索、ワークスペースの作成](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) |
| Real-Time CDP | [宛先、アクティベーションステータス、データフローの正常性を確認](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) （クローズド ベータ版） |

>[!TAB Connect]

アプリケーション固有のMCP エンドポイントを使用する場合は、CX Enterprise Gateway エンドポイントを使用します。

```
https://cx-enterprise.adobe.io/mcp
```

>[!NOTE]
>AEMの場合は、ダイレクト AEM エンドポイントを使用します。AEMは、CX Enterprise MCP Gateway経由でルーティングされません。

プロンプトが表示されたらAdobe IDでログインし、Adobe アプリケーションにリンクされているIMS組織を選択します。 間違った組織を選択することは、欠けているツールや認証エラーの最も一般的な原因です。

完全なセットアップ手順については、以下の「[AI クライアントに接続する](#connect-to-your-ai-client)」を参照してください。

>[!ENDTABS]

## Adobe CX Enterprise MCP サーバー

以下に示すサーバーは直接接続され、CX Enterprise MCP Gateway経由でルーティングされません。 AJO、Customer Journey Analytics、およびReal-Time CDP アクセスの場合は、上記の[CX Enterprise MCP Gateway](#cx-enterprise-mcp-gateway)を使用します。

<!--
CARDS

* #cx-enterprise-mcp-gateway
  {title = CX Enterprise MCP Gateway}
  {description = One connection to AJO, CJA, and Real-Time CDP tools. The gateway surfaces only the tools your organization is licensed for.}
  {cta = Connect}
  {image = ../assets/mcp-cxenterprise-card.png}

* https://developer.adobe.com/analytics-mcp/docs/aa/
  {title = Adobe Analytics}
  {description = Tools for report suite discovery, dimension and metric analysis, segment authoring, and workspace creation in Adobe Analytics.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-analytics-card.png}

* https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service
  {title = AEM Content}
  {description = Tools for managing pages, content fragments, assets, and launches in Adobe Experience Manager as a Cloud Service using natural language.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service
  {title = AEM Content (Read-Only)}
  {description = Tools for discovering and querying pages, content fragments, and launches in AEM as a Cloud Service. No write access.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager
  {title = AEM Cloud Manager}
  {description = Tools for managing Cloud Manager programs, environments, pipelines, and repositories from your IDE using natural language.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

-->

### MCP サーバーエンドポイント

| サーバー | エンドポイント | ツール |
| --- | --- | --- |
| [CX Enterprise MCP Gateway](#cx-enterprise-mcp-gateway) | `https://cx-enterprise.adobe.io/mcp` | ・ [Adobe Journey Optimizer tools](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server)<br>・[Customer Journey Analytics tools](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp)<br>・[Real-Time CDP tools](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) |
| [Adobe Analytics](https://developer.adobe.com/analytics-mcp/docs/aa/) | `https://aa-mcp.adobe.io/mcp` | [&#x200B; ツールの表示](https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp) |
| [AEM Cloud Manager](https://experienceleague.adobe.com/ja/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | [&#x200B; ツールの表示](https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp) |
| [AEM コンテンツ &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | [&#x200B; ツールの表示](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) |
| [AEM コンテンツ （読み取り専用） &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | [&#x200B; ツールの表示](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly) |

## AI クライアントに接続します

すべてのAdobe MCP サーバーは、Adobe Identity Management サービス（IMS）でOAuthを使用します。 プロンプトが表示されたら、正しいIMS組織を選択します。 間違ったものを選択することは、認証エラーの最も一般的な原因です。

手動で設定する前に、AI クライアントとAdobe アプリケーションのマネージドコネクタの[Adobe AI Registry](https://developer.adobe.com/ai-registry/?type=connector)を確認してください。 マネージドコネクタで認証を自動的に処理します。 クライアントとアプリケーションでコネクタが使用可能な場合は、以下の手動手順の代わりにそれを使用します。

![Adobe MCP サーバーに接続しているAI エージェント &#x200B;](../assets/hero-connect-mcp-servers.gif)

>[!BEGINTABS]

>[!TAB  クロード.ai]

### ![推奨](../assets/badge-recommended.svg)管理対象コネクタの使用

[Adobe AI レジストリ &#x200B;](https://developer.adobe.com/ai-registry/?type=connector)に移動し、Adobe アプリケーションを検索します。 Claude コネクタが一覧表示されている場合（例：[Adobe Experience Manager コネクタ &#x200B;](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)）、次の手順ではなく、その設定手順に従います。

### カスタムコネクタを使用した接続

Claude.aiは、アカウント設定のカスタムコネクタを介してリモート MCP サーバーをサポートします。

1. **設定/統合**&#x200B;に移動します。
2. 「**カスタムコネクタを追加**」をクリックします。
3. URLとして`https://cx-enterprise.adobe.io/mcp`を入力し、`Adobe CX Enterprise`などの表示名を入力します。
4. **Connect**&#x200B;をクリックし、Adobe IDでログインします。 適切なIMS組織を選択します。

完全なセットアップ：[Claude.ai カスタムコネクタのドキュメント &#x200B;](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB  クロード コード ]

### CLIの使用

`claude mcp add`を実行して、CX Enterprise MCP Gatewayを登録します。 1つの接続で、組織のライセンスに基づいて、AJO、CJA、Real-Time CDP ツールにアクセスできます。

```bash
claude mcp add --transport http adobe-cx-enterprise https://cx-enterprise.adobe.io/mcp
```

### 設定ファイルを編集

サーバーをプロジェクトルート （プロジェクトレベル）の`~/.claude.json` （グローバル）または`.mcp.json`に追加します。

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

CX Enterprise MCP GatewayをCursor `mcp.json`設定ファイルに追加し、**設定 / MCP**&#x200B;を介して接続します。

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

ひとつのゲートウェイエントリから、組織のライセンスに基づいてAJO、CJA、Real-Time CDPにアクセスできます。

追加すると、カーソル設定の&#x200B;**インストール済みMCP サーバー**&#x200B;の下にMCP サーバーが表示されます。 **認証が必要**&#x200B;と表示されているサーバーの横にある&#x200B;**Connect**&#x200B;を選択し、Adobe IDでログインします。 アプリケーションにアクセスできるIMS組織を選択します。

![&#x200B; インストール済みのAdobe MCP サーバーとmcp.json](../assets/screenshots/cursor-mcp-server-configuration.jpg)を示すCursor MCP サーバー設定

完全なセットアップ：[&#x200B; カーソル MCP ドキュメント &#x200B;](https://cursor.com/docs/mcp)

>[!TAB ChatGPT]

### ![推奨](../assets/badge-recommended.svg)管理対象コネクタの使用

[Adobe AI レジストリ &#x200B;](https://developer.adobe.com/ai-registry/?type=connector)に移動し、Adobe アプリケーションを検索します。 ChatGPT コネクタがリストされている場合は、以下の手順ではなく、その設定手順に従います。

### リモート MCP サーバーを使用した接続

ChatGPTは、[開発者モード &#x200B;](https://developers.openai.com/api/docs/guides/developer-mode)を介したリモート MCP サーバーをサポートしています。これは、Pro、Plus、Business、Enterprise、Education プランで利用できます。

1. **ChatGPT設定**&#x200B;で開発者モードを有効にします。
2. **設定/統合**&#x200B;に移動します。
3. 「**カスタムコネクタを追加**」をクリックし、**リモート MCP サーバー**&#x200B;を選択します。
4. URLとして`https://cx-enterprise.adobe.io/mcp`、名前として`Adobe CX Enterprise`を入力します。
5. 認証を&#x200B;**OAuth**&#x200B;に設定します。
6. **Connect**&#x200B;をクリックし、Adobe IDでログインします。 適切なIMS組織を選択します。

完全なセットアップ：[ChatGPT MCP ドキュメント &#x200B;](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB OpenAI Codex CLI]

OpenAI Codex CLIは、TOML設定を介してリモート MCP サーバーをサポートします。

**ファイルの場所を設定：**

- **ユーザーレベル （すべてのプロジェクト）:** `~/.codex/config.toml`
- **プロジェクト範囲：** `.codex/config.toml` （プロジェクトルート内）

CX Enterprise MCP Gatewayを追加します。

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
4. MCP オンボーディングウィザードで、次のように入力します。
   - **サーバー名：** `Adobe CX Enterprise`
   - **サーバーURL:** `https://cx-enterprise.adobe.io/mcp`
5. Authenticationを&#x200B;**OAuth 2.0**&#x200B;に設定し、Adobe IMS認証とトークン URLを使用して設定します。
6. 「**作成**」、「**エージェントに追加**」の順に選択します。

>[!NOTE]
>
>Copilot StudioのMCP サーバー接続は、Power Platformを介して行われます。 組織のデータ損失防止（DLP）ポリシーが適用されます。

完全なセットアップ：[Copilot Studio MCP ドキュメント &#x200B;](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## トラブルシューティング

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

## エージェント型ツールの活用例

実際のビジネスワークフローに適用されるAdobe CX Enterprise MCP サーバーを参照してください。

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use the CX Enterprise MCP Gateway to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use the CX Enterprise MCP Gateway to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* ../use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use the CX Enterprise MCP Gateway to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* ../use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine the CX Enterprise MCP Gateway and AEM Content MCP Server to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* ../use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Use the CX Enterprise MCP Gateway for a unified view of AJO, CJA, and Real-Time CDP campaign health in one AI session.}
  {cta = Start walkthrough}
-->
