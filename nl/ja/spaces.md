---

copyright:

  years: 2018
lastupdated: "2018-04-13"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}

# スペースの決定
{: #determinespaces}

組織内で、スペースは、追加レベルの境界適用および抽象化を提供します。

スペースは、組織内で、ユーザーがアプリおよびサービスを開発して実行することができる予約済みの領域です。 スペースは、1 つの組織内にいくつでも作成可能であり、スペースへのアクセス権限を持つユーザーを制御することができます。 詳しくは、『[スペース](/docs/account/orgs_spaces.html#orgsspacesusers)』を参照してください。

定義する予定のスペースの数が多い場合は、スペース管理を支援するアプリケーションを作成できます。 スペースの数が 60 を超える場合は、別の組織を定義することも検討してください。

## 単一組織と複数組織のスペースの対比
{: #spaceconsiderations}

単一組織体系を採用すると、組織内に定義したスペースによって、分離と抽象化のレベルが提供されます。 スペースを定義する際には、以下のガイダンスを考慮してください。

* 1 回だけプロビジョンと構成を要求するサービスをホストするスペースを組織に定義します。
* デリバリー・ライフサイクルに基づいてスペースを定義します。
  例えば、開発中のアプリ用に 1 つ以上のスペース、テスト・フェーズのアプリ用に 1 つ以上のスペース、実動アプリケーション用に 1 つ以上のスペースを定義することができます。
* デリバリー・ライフサイクル境界が不十分な場合は、LOB およびデリバリー・フェーズごとに 1 つ以上のスペースを定義することで、分離を強化することが可能です。
* 異なるユーザー・グループに対して境界を適用する必要があるかどうかを決めます。
  例えば、開発者は、アプリケーションを開発した後、それをテストすることはできません。 アプリケーションをテストするには、別のユーザー集合が必要です。 このシナリオでは、アプリケーション開発者用スペースとアプリケーション・テスター用スペースの 2 つを作成します。 その後、各ユーザー集合に、適切なスペースへのアクセス権限を付与します。

複数組織体系を実装すると、LOB またはデリバリー・ライフサイクル、あるいはその両方で各組織を分離することができます。 その後、会社内の同じ部門によって
デリバリーされるアプリまたはプロジェクトの数に基づいて複数のスペースを定義することができます。 組織内のスペースを計画する際には、以下のガイダンスを考慮してください。

* 1 回だけプロビジョンと構成を要求するサービスをホストするスペースを組織に定義します。
* アプリケーションごと、関連アプリのグループごと、または特定プロジェクトのスペースを定義します。
* 異なるユーザーに境界を適用する必要がある場合は、各ユーザー集合ごとにスペースを定義します。 スペースで開発者役割が付与されたユーザーは、そのスペースでプロビジョンされて実行中のすべてのリソースと {{site.data.keyword.Bluemix_notm}} サービスへの全アクセス権限を持ちます。 ユーザーがリソースのすべては制御できないようにセキュリティーを強化する必要がある場合は、異なるスペースを定義することを検討してください。 これらのどのスペース内でも、該当スペースで実行中のアプリで使用される {{site.data.keyword.Bluemix_notm}} サービスをプロビジョンできます。

## スペースの命名、制約事項、および管理
{: #spaceadmin}

クラウド組織にさまざまなスペースを定義する際には、以下のガイダンスを考慮してください。

* 命名規則を定義して適用します。 例えば、組織のロケーションおよびクラウドのタイプに関する情報をスペース名に含めるという命名規則を定義します。 スペース名は、作成後に変更可能です。 スペース名が変更されたら、すべてのスペース・チーム・メンバーにその変更を通知してください。
* スペースに適用される制約事項を定義します。 例えば、各スペースで開発、管理、デプロイが可能なアプリのタイプを定義します。
* スペースの管理者を特定します。 複数のユーザーにスペース管理を委任すると有効です。
