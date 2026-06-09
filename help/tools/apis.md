---
title: ビルダー用API
description: Adobe CX Enterprise APIを使用して、カスタムアプリケーションと統合を構築します。
last-substantial-update: 2026-06-02T00:00:00Z
index: false
source-git-commit: 8f499ad7baf1b5d08dfac90511d0c76e8372c08b
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 11%

---


# ビルダー用API

<!-- last-modified: 2026-06-02 -->

![Adobe CX Enterprise API](../assets/hero-apis.png)

Adobe CX Enterprise APIでは、開発者とAIを活用したコーディングエージェンティックツールが、Adobeのデータとワークフローに直接アクセスできます。 カスタムアプリケーションの構築や統合の自動化、Adobeの機能の自社システムへの組み込みに利用できます。 APIは、システム統合を完全にプログラム制御する必要がある場合や、Adobeデータを基にアプリケーションを構築する場合に最適な選択肢です。 Adobe ワークフローへのエージェント駆動型の会話型アクセスについては、[MCP サーバー](mcp-servers.md)を参照してください。

## Adobe CX Enterprise API

>[!BEGINTABS]

>[!TAB Adobe Analytics]

レポート、データフィード、計算指標、セグメント管理。

[APIを探索](https://developer.adobe.com/analytics-apis/docs/2.0/)

>[!TAB Adobe Commerce]

カタログ、カート、注文、顧客、プロモーション用のRESTおよびGraphQL API。

[APIを探索](https://developer.adobe.com/commerce/webapi/)

>[!TAB Adobe Experience Platform]

データセット、スキーマ、プロファイル、ID、クエリ、セグメント化のCRUD操作。

[APIを探索](https://developer.adobe.com/experience-platform-apis/)

>[!TAB Adobe Journey Optimizer]

ジャーニーのオーケストレーション、キャンペーン管理、コンテンツテンプレート、オファーの決定。

[APIを探索](https://developer.adobe.com/journey-optimizer-apis/)

>[!TAB AEM as a Cloud Service]

Adobe Experience Managerのコンテンツ、アセット、ワークフロー管理API。

[APIを探索](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/apis-and-extensions)

>[!TAB Audience Manager]

オーディエンスの管理とアクティベーションのワークフロー。

[APIを探索](https://developer.adobe.com/audience-manager/)

>[!TAB  クライアント SDK]

モバイル SDK、エッジ SDK、アプリ内メッセージ。

[APIを探索](https://developer.adobe.com/client-sdks/home/)

>[!TAB Customer Journey Analytics]

Adobe Analyticsのデータアクセス、レポート、CJAのインサイトのワークフロー。

[APIを探索](https://developer.adobe.com/cja-apis/docs/)

>[!TAB データ収集]

Edge Networkデータの収集、リアルタイムのイベント収集、ストリーミングデータの配信。

[APIを探索](https://developer.adobe.com/data-collection-apis/docs/)

>[!TAB Developer Console]

API プロジェクトの設定、認証、資格情報管理。

[APIを探索](https://developer.adobe.com/developer-console/docs/guides/)

>[!TAB イベント]

イベント駆動型の統合、webhook、自動化トリガー:

[APIを探索](https://developer.adobe.com/events/docs/)

>[!TAB プライバシー]

プライバシーワークフロー、データガバナンス、データ主体のリクエスト：

[APIを探索](https://experienceleague.adobe.com/ja/docs/experience-platform/privacy/home)

>[!TAB ユーザー管理]

ユーザー管理、ID管理、エンタープライズアカウントの自動化。

[APIを探索](https://developer.adobe.com/umapi/)

>[!ENDTABS]

## APIを使用した構築

![Adobe CX Enterprise APIに接続するIDE](../assets/hero-connect-apis.gif)

Claude Code、Cursor、OpenAI Codexなどのコーディングエージェントは、Adobe CX Enterprise APIを使用した構築に適しています。 プロジェクトにOpenAPI仕様を追加すると、エージェントは手動での配線なしでエンドポイントを発見し、リクエストを作成し、API動作の理由を確認できます。 まず、Adobe Developer Consoleの認証済み資格情報と、プロジェクトに追加されたAPI ドキュメントの2つが必要です。

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
