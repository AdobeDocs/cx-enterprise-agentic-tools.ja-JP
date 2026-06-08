---
title: エージェントスキル
description: Adobeが監修したワークフローと手引きを活用して、AI エージェントがCX Enterpriseのタスクを一貫して進められるようにします。
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 3%

---


# エージェントスキル

<!-- last-modified: 2026-05-19 -->

Adobe CX Enterpriseの![担当者のスキル &#x200B;](../assets/hero-agent-skills.png)

エージェントスキルは、Adobeがキュレートしたワークフローで、AI エージェントがAdobe CX Enterpriseのタスクを確実に完了するためのステップバイステップの手順を提供します。 各エージェントスキルは、ドメインの専門知識とベストプラクティスをエンコードすることで、エージェントが改善を必要とせずに、一貫した検証済みの結果を生成できるようにします。 エージェントのスキルは、会話をまたいで繰り返し可能なガイド付きの行動を求めるときに理にかなっています。特に、毎回詳細なプロンプトが必要になるタスクでは、これが重要になります。 これらはMCP サーバーとAPIを補完します。エージェントスキルはエージェントの仕組みを定義し、MCP サーバーとAPIは基礎となるアクセスを提供します。

すべてのエージェントスキルは、[Adobe Skills GitHub リポジトリ &#x200B;](https://github.com/adobe/skills)に保持されます。これは、エージェントスキルのドキュメント、インストール、実装の詳細の主要なソースです。

## Adobe CX Enterprise Agent Skills

すべてのエージェントスキルは、[Adobe Skills GitHub リポジトリ &#x200B;](https://github.com/adobe/skills)で管理されます。 そのワークフローのスキルを探るには、以下の機能領域を選択してください。

### アドビアプリケーション

<!--
CARDS

* https://github.com/adobe/skills/tree/main/plugins/aem
  {title = Adobe Experience Manager}
  {description = Agent Skills for Experience Manager development, content, design, and project management across AEM as a Cloud Service, Edge Delivery Services, and AEM 6.5 LTS.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-aem-card.png}

* https://github.com/adobe/skills/tree/main/plugins/adobe-analytics
  {title = Adobe Analytics}
  {description = Agent Skills for KPI monitoring, funnel analysis, and executive reporting workflows in Adobe Analytics.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-analytics-card.png}

* https://github.com/adobe/skills/tree/main/plugins/adobe-cja
  {title = Customer Journey Analytics}
  {description = Agent Skills for performance comparison, dimension analysis, and workspace authoring in Customer Journey Analytics.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-cja-card.png}

* https://github.com/adobe/skills/tree/main/plugins/app-builder
  {title = Adobe App Builder}
  {description = Agent Skills for scaffolding, testing, and deploying custom applications with Adobe App Builder.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-cxenterprise-card.png}

* https://github.com/adobe/skills/tree/main/plugins/creative-cloud
  {title = Creative Cloud}
  {description = Agent Skills for batch photo editing, design from templates, video editing, and social media variants with Creative Cloud.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-creative-cloud.png}

-->

スキルの詳細、インストール方法、ソースコードについては、[Adobe Skills GitHub リポジトリ &#x200B;](https://github.com/adobe/skills)を参照してください。

## エージェントスキルの仕組み

![&#x200B; エージェントスキルの仕組み](../assets/hero-connect-agent-skills.gif)

エージェントスキルとは、AI担当者にAdobeのエージェント型ツールを使用してタスクを完了する方法を伝える一連の指示です。 エージェントがスキルを読み込むと、即興ではなく、そのワークフローに従います。

- 担当者は毎回同じようにタスクを完了します
- ドメインの専門知識は、一度符号化され、会話を超えて再利用されます
- スキルは、複数のエージェント型ツールやアクションを単一のワークフローに連携させることができます

## 基本を学ぶ

エージェントスキルは、使用しているAI クライアントに基づいてインストールされます。 一部のクライアントは、コマンドラインからの直接インストールをサポートしています。

- **クロード コード**: `/plugin install adobe/skills`
- **ノード環境**: `npx skills add adobe/skills`
- **GitHub CLI**: `gh upskill adobe/skills`

他のクライアントでは、スキルファイルをダウンロードしてAI クライアントに直接追加する必要があります。 クライアントによる完全なインストール手順については、GitHub[&#128279;](https://github.com/adobe/skills#installation)のAdobe Skills READMEを参照してください。

### エージェントのスキルの検索

利用可能なスキルの完全なリストについては、[Adobe Skills GitHub リポジトリ &#x200B;](https://github.com/adobe/skills)を参照してください。 各エージェントスキルには、詳細なガイダンス、参照、例を含む`SKILL.md` ファイルが含まれています。

`adobe/skills` パッケージをインストールまたは追加した後、一部のAI クライアントでは、利用可能なすべてのスキルを直接一覧表示できます。

- **クロード コード**: `claude /plugin list`
- **ノード環境**: `npx skills list`
- **GitHub CLI**: `gh upskill list`

## エージェントスキル、MCP サーバー、API間のビルダーの比較

| | エージェントスキル | MCP サーバー | ビルダー用API |
| --- | --- | --- | --- |
| 目的 | ガイド付きワークフローとベストプラクティス | Adobeのデータとワークフローへのアクセス | 直接システム統合 |
| ドメインの専門知識をコード化 | ○ | × | × |
| コーディングが必要 | × | × | ○ |
| 最適な用途 | 繰り返し可能なガイド付きタスク | データクエリとワークフローアクション | カスタムアプリケーション開発 |
