---
title: エージェント型ツールの活用例
description: 実際のビジネスワークフローに適用されたAdobe CX Enterprise Agentic Toolsを示すステップバイステップのウォークスルー。
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# エージェント型ツールの活用例

<!-- last-modified: 2026-05-20 -->

![&#x200B; エージェント ツールの動作](assets/hero-agentic-tools-in-action.png)

Adobe CX Enterpriseの実際のワークフローをステップバイステップで解説します。 各ウォークスルーは、設定が終わる場所から始まり、ツールをつなぎ合わせ、実際のワークフローが完了します。

<!--
CARDS

* use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Surface Customer Journey Analytics comparisons and conversion trends through plain-language questions. Uses the CX Enterprise MCP Gateway.}
  {cta = Start walkthrough}

* use-cases/query-audiences.md
  {title = Query audiences}
  {description = Check Real-Time CDP audience activation status and destination health without navigating the platform UI. Uses the CX Enterprise MCP Gateway.}
  {cta = Start walkthrough}

* use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Get full visibility into active AJO journeys and campaign configuration without opening AJO. Uses the CX Enterprise MCP Gateway.}
  {cta = Start walkthrough}

* use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments using natural language. Uses the AEM Content MCP Server.}
  {cta = Start walkthrough}

* use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Move from analytics insight to published update in one session, without switching tools. Uses the CX Enterprise MCP Gateway and AEM Content MCP Server.}
  {cta = Start walkthrough}

* use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Review AJO journey status, Real-Time CDP audience activation, and CJA performance data in one AI session. Uses the CX Enterprise MCP Gateway.}
  {cta = Start walkthrough}

* use-cases/aem-cloud-manager-mcp.md
  {title = Manage AEM environments with Cloud Manager}
  {description = Check environment health, review pipeline runs, and manage deployments from your AI client. Uses the AEM Cloud Manager MCP Server.}
  {cta = Start walkthrough}
  {image = https://video.tv.adobe.com/v/3480340?format=jpeg}
-->

## よくある質問

+++AI クライアントからAdobe データをクエリする方法を教えてください。

MCP サーバーを使用します。 AI クライアントを関連するAdobe MCP サーバーエンドポイントに接続し、自然言語で質問します。 サーバーは、リクエストをAdobe API呼び出しに変換し、構造化された結果を返します。

開始するには、[MCP サーバー](tools/mcp-servers.md)を参照してください。

+++

+++複数のAdobe アプリケーションを接続するワークフローを構築するにはどうすればよいですか？

単一のAI セッションで複数のMCP サーバーに接続するか、Adobe APIを使用してカスタムマルチアプリケーションオーケストレーションを実行できます。

ビルダー[&#128279;](tools/apis.md)および[MCP サーバー](tools/mcp-servers.md)のAPIを参照してください。

+++

+++担当者をAdobeのベストプラクティスに従わせるにはどうすればよいですか？

エージェントのスキルの使用： エージェントが一貫性のあるタスクを完了できるように、Adobeドメインの専門知識をスキルにコード化します。

[&#x200B; エージェントスキル &#x200B;](tools/agent-skills.md)を参照してください。

+++

+++Adobe MCP サーバーで動作するAI クライアント？

任意のMCP対応クライアント。 Claude Code、Claude.ai、Cursor、ChatGPT、Google GeminiはすべてMCPをサポートしています。 完全なクライアント比較とセットアップリンクについては、[MCP サーバー](tools/mcp-servers.md)を参照してください。

+++
