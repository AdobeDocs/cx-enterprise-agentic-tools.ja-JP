---
title: Adobe CX Enterprise Agentic Tools
description: MCP サーバー、エージェントスキル、APIを使用して、AI エージェントと開発ツールをAdobe CX Enterpriseの機能に接続します。
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 2%

---


# Adobe CX Enterprise Agentic Tools

<!-- last-modified: 2026-05-08 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491235/?learn=on&enablevpops)

**Adobe CX Enterprise**&#x200B;のデータ、ワークフロー、オートメーションにAIを直接接続します。 互換性のあるAI クライアントや開発ツールから、**平易な言語**&#x200B;でキャンペーンのクエリ、オーディエンスのアクティブ化、ジャーニーの管理を行うことができます。

<!--
CARDS

* tools/mcp-servers.md
  {title = MCP Servers}
  {description = Connect any MCP-compatible AI client to Adobe CX Enterprise workflows. Query data, analyze campaigns, and access audiences without leaving your AI tool.}
  {cta = Explore MCP Servers}
  {image = assets/mcp-servers-card.png}

* tools/agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflows that guide agents through CX Enterprise tasks. Domain expertise encoded once, applied consistently.}
  {cta = Explore Agent Skills}
  {image = assets/agent-skills-card.png}

* tools/apis.md
  {title = APIs for Builders}
  {description = Build custom Adobe CX Enterprise applications using agentic coding tools like Claude Code and Cursor.}
  {cta = Explore APIs for Builders}
  {image = assets/apis-card.png}
-->

## あらゆる部門に対応するエージェント型ツール

>[!BEGINTABS]

>[!TAB  ビジネスリーダー]

Adobeのエージェンティックツールのビジネス価値と、それがAdobeへの投資をどのように拡大するのかを理解します。

- 担当者は、チームを交代させることなく、マーケティングとオペレーションのワークフローを加速させます
- アクセス制御、監査証跡、Human-in-the-loop ワークフローは最初から組み込まれています
- エージェンティックツールは、Adobeのサーフェスだけでなく、互換性のあるあらゆるAI クライアントで動作します
- ユーザーのデータは、ユーザーの権限によって管理された環境に保持されます

[実際のウォークスルー](agentic-tools-in-action.md)を参照して、今日これらのエージェント型ツールでチームが何をしているのかを確認してください。

>[!TAB  ビジネスユーザー]

エージェンティックツールが、どのようにAdobeの日々のワークフローを加速するのかをご確認ください。

- [MCP サーバー](tools/mcp-servers.md)を使用して、AI クライアントを数分でAdobe データに接続します
- 一般的な[&#x200B; キャンペーン &#x200B;](use-cases/analyze-campaign-performance.md)、[&#x200B; オーディエンス &#x200B;](use-cases/query-audiences.md)、[&#x200B; ジャーニー](use-cases/manage-ajo-journeys.md)のタスクについて、順を追って説明します
- 既に使用しているAI環境で作業する

>[!TAB  ビルダーと開発者]

Adobe CX Enterpriseの機能をカスタムアプリケーションやエージェントに統合できます。

- 機能領域ごとにビルダー[&#128279;](tools/apis.md)のAPIを参照し、開発環境の[MCP サーバー](tools/mcp-servers.md)に接続します
- Adobe APIと共に、[Claude Code](https://docs.anthropic.com/en/docs/claude-code/mcp)や[Cursor](https://cursor.com/docs/mcp)などのAI支援コーディングツールを使用します
- [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)で認証と資格情報を設定します
- サポートされているAI クライアントとセットアップ手順の完全なリストについては、[MCP サーバー](tools/mcp-servers.md)を参照してください

>[!TAB 管理者]

アクセスを管理し、承認済みのエージェント型ツールを管理し、組織全体の監視を維持しましょう。

- [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)を介したMCP サーバーおよびAPIの認証を構成します
- Identity Management System （IMS）組織レベルの権限を設定して、エージェント型ツールにアクセスできるユーザーとチームを制御します
- 組織での使用を承認されたAI クライアントとMCP サーバーを定義し、適用します
- 使用状況の監視、監査証跡の確認、エージェンティックアクティビティがコンプライアンス要件を満たしていることを確認します

認証設定については[MCP サーバー](tools/mcp-servers.md)、資格情報およびプロジェクト管理については[Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)を参照してください。

>[!ENDTABS]

## エージェント型ツールの活用例

Adobe CX Enterpriseのエージェント型ツールの実際をご覧ください。 各チュートリアルでは、設定から成果までの実際のビジネスシナリオを取り上げ、AI クライアントの接続方法、求めるべき事項、そして返される結果を正確に提示します。

<!--
CARDS

* use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use the CX Enterprise MCP Gateway to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use the CX Enterprise MCP Gateway to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use the CX Enterprise MCP Gateway to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine CJA and AEM MCP Servers to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Connect AJO, CJA, and Real-Time CDP in one AI session for a unified view of campaign health.}
  {cta = Start walkthrough}
-->

## Adobeの業界トレンド

| リソース | 見つかる内容 |
| --- | --- |
| [Adobe AI レジストリ &#x200B;](https://developer.adobe.com/ai-registry/?type=mcp) | 利用可能なMCP サーバーとエージェントスキルの完全カタログ |
| [Adobe API カタログ &#x200B;](https://developer.adobe.com/apis) | Adobe CX Enterprise API リファレンスの完全版 |
| [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) | API プロジェクトの設定と認証 |
| [Experience League](https://experienceleague.adobe.com/ja/docs/experience-cloud-ai/experience-cloud-ai/home) | Adobeのアプリケーションに関するドキュメントとチュートリアル |
