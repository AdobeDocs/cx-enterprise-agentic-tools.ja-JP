---
title: ビルダー用API
description: Adobe CX Enterprise APIを使用して、カスタムアプリケーションと統合を構築します。
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 3%

---


# ビルダー用API

<!-- last-modified: 2026-06-02 -->

![Adobe CX Enterprise API](../assets/hero-apis.png)

Adobe CX Enterprise APIでは、開発者とAIを活用したコーディングエージェンティックツールが、Adobeのデータとワークフローに直接アクセスできます。 カスタムアプリケーションの構築や統合の自動化、Adobeの機能の自社システムへの組み込みに利用できます。 APIは、システム統合を完全にプログラム制御する必要がある場合や、Adobeデータを基にアプリケーションを構築する場合に最適な選択肢です。 Adobe ワークフローへのエージェント駆動型の会話型アクセスについては、[MCP サーバー](mcp-servers.md)を参照してください。

## Adobe CX Enterprise API

Adobe CX Enterprise APIは、Adobe Experience Platform、Journey Optimizer、Customer Journey Analyticsなどの製品を支える中核となるデータとオペレーションを公開します。 各APIはAPI ファーストの設計に従っており、開発者とAI支援のコーディングエージェンティックツールが、Adobe Adobeの社内で使用するのと同じ機能に、プログラミング可能な方法で直接アクセスできます。 カスタムアプリケーションの構築、ワークフローの自動化、Adobeデータの自社システムへの統合に役立ちます。

<!--
CARDS

* https://developer.adobe.com/audience-manager/
  {title = Audience Manager}
  {description = Audience management and activation workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aam-card.png}

* https://developer.adobe.com/client-sdks/home/
  {title = Client SDKs}
  {description = Mobile SDKs, edge SDKs, and in-app messaging.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/cja-apis/docs/
  {title = Customer Journey Analytics}
  {description = Analytics data access, reporting, and CJA insights workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cja-card.png}

* https://developer.adobe.com/data-collection-apis/docs/
  {title = Data Collection}
  {description = Edge Network data ingestion, real-time event collection, and streaming data delivery.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/developer-console/docs/guides/
  {title = Developer Console}
  {description = API project setup, authentication, and credential management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/events/docs/
  {title = Events}
  {description = Event-driven integrations, webhooks, and automation triggers.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://experienceleague.adobe.com/ja/docs/experience-platform/privacy/home
  {title = Privacy}
  {description = Privacy workflows, data governance, and data subject requests.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/experience-platform-apis/
  {title = Adobe Experience Platform}
  {description = CRUD operations for datasets, schemas, profiles, identities, queries, and segmentation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/journey-optimizer-apis/
  {title = Adobe Journey Optimizer}
  {description = Journey orchestration, campaign management, content templates, and offer decisioning.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-ajo-card.png}

* https://developer.adobe.com/analytics-apis/docs/2.0/
  {title = Adobe Analytics}
  {description = Reporting, data feeds, calculated metrics, and segment management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-analytics-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/apis-and-extensions
  {title = AEM as a Cloud Service}
  {description = Content, asset, and workflow management APIs for Adobe Experience Manager.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aem-card.png}

* https://developer.adobe.com/commerce/webapi/
  {title = Adobe Commerce}
  {description = REST and GraphQL APIs for catalog, cart, orders, customers, and promotions.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-commerce-card.png}

* https://developer.adobe.com/umapi/
  {title = User Management}
  {description = User management, identity administration, and enterprise account automation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}
-->

## ビルダーとMCP サーバーのAPI

システム統合を完全に制御する必要がある場合や、カスタムアプリケーションを構築する場合は、APIを使用します。 AI エージェントにAdobeワークフローを直接操作してもらいたい場合は、MCP サーバーを使用します。

| | API | MCP サーバー |
| --- | --- | --- |
| 直接システム統合 | ○ | 時々 |
| エージェントにも使いやすいオーケストレーション | 制限付き | ○ |
| 生データへのアクセス | ○ | 通常は抽象化 |
| カスタムアプリケーション開発 | プライマリの使用例 | セカンダリ |
| AIを活用したワークフロー | 対応 | プライマリの使用例 |

## ビルダー向けAPIの基本を学ぶ

![Adobe CX Enterprise APIに接続するIDE](../assets/hero-connect-apis.gif)

Adobe CX Enterprise APIを構築する前に、Adobe Developer Consoleの認証済み資格情報と、コーディングエージェントがAdobe APIを確実に使用できるようにプロジェクトに追加されたAPI ドキュメントの2つの機能が必要です。

### Adobe Developer ConsoleでのAPI資格情報の設定

すべてのAdobe CX Enterprise API アクセスは[Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)を通じて管理されます。 プロジェクトを作成し、アプリケーションに必要なAPIを追加し、資格情報を生成します。

1. ログインして[Adobe Developer Consoleでプロジェクト &#x200B;](https://developer.adobe.com/developer-console/docs/guides/projects/)を作成します。
2. [必要なAdobe CX Enterprise アプリケーションのAPI](https://developer.adobe.com/developer-console/docs/guides/services/)を追加します。
3. [認証タイプ &#x200B;](https://developer.adobe.com/developer-console/docs/guides/authentication/)を選択してください。 自動ワークフローには&#x200B;**OAuth サーバー間**&#x200B;を使用し、ユーザー向けアプリケーションには&#x200B;**OAuth Web App**&#x200B;を使用します。
4. 認証情報を生成。 アプリケーションで使用するクライアント ID、クライアント秘密鍵、およびトークンエンドポイントをメモします。

ほとんどのAdobe CX Enterprise APIには、アプリケーションのライセンスが必要です。 Developer Console プロジェクトでAPIが使用できない場合は、Adobe担当者にお問い合わせください。

### プロジェクトにAdobe API コンテキストを追加する

AI コーディングエージェントは、プロジェクトに適切な参照資料を追加すると、Adobe APIを確実に検出して使用できます。 これは、OpenAPI仕様を公開するあらゆるAdobe CX Enterprise APIで機能します。

**1. API仕様を検索**

上記の[Adobe CX Enterprise API](#adobe-cx-enterprise-apis)を参照するか、[Adobe Developer API カタログ &#x200B;](https://developer.adobe.com/apis)に直接移動します。

**2. OpenAPI仕様をダウンロード**

プロジェクトに`/specs` ディレクトリを作成します。 [developer.adobe.com](https://developer.adobe.com/apis)のAPI参照ページからOpenAPI YAMLをダウンロードし、そこに保存します。 ソース URLとダウンロード日を記録する`README.md`を追加します。

```
/specs/README.md
/specs/aem-assets.openapi.yaml
```

>[!TIP]
>チェックイン済みのスナップショットは、コーディングエージェントに安定した再現可能な動作を提供し、APIの変更をGit履歴に表示します。

**3. API インデックスを生成**

このプロンプトをコーディングエージェントに貼り付け、`<API-SPEC-FILE>`をファイル名に置き換えます。

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and generate /docs/<API-SPEC-FILE>.api.md.

Create a concise API index for AI coding agents. For each operation include: operationId, HTTP method, path, purpose, authentication requirements, required inputs, response shape, common error responses, pagination behavior, asynchronous behavior, and deprecation status.

Do not invent endpoints, parameters, request bodies, response fields, or behavior not present in the OpenAPI specification.
```

**4. エージェントの指示を生成**

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and /docs/<API-SPEC-FILE>.api.md.

Generate AGENTS.md. Instructions should:
- Treat the OpenAPI specification as the source of truth.
- Use the API index as a navigation guide.
- Never invent endpoints, parameters, response fields, or status codes.
- Prefer documented operationIds.
- Avoid deprecated or experimental APIs unless explicitly requested.
- Follow authentication requirements defined in the specification.
- Use the local OpenAPI snapshot for implementation decisions.
```

**5.**&#x200B;を確認

生成されたファイルのみを使用して、コーディング担当者に簡単なタスクを完了するように依頼します。

```
Write a function that takes an AEM asset ID and returns the asset title and description. Use only /specs/aem-assets.openapi.yaml and /docs/aem-assets.api.md.
```

エージェントが動作を発明せずに正しく完了した場合、設定は完了します。

**推奨されるプロジェクト構造**

```
project/
├── specs/
│   ├── README.md
│   └── aem-assets.openapi.yaml
├── docs/
│   └── aem-assets.api.md
└── AGENTS.md
```

**スペックを最新の状態に保つ**

Adobeが新しいAPI バージョンを公開する場合：新しいスナップショットを`/specs`にダウンロードし、`README.md`で日付を更新し、インデックスと`AGENTS.md`を再生成します。
