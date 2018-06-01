---

copyright:

  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# プライベート・リソースの所有権の変更

コマンド・ライン・インターフェースを使用してアカウントの所有権を変更できます。 カタログ内にプライベート・リソースを作成してカスタマイズした後、それらのリソースの所有権を他の人に移管することができます。 所有権の移管後は、アカウントからリソースを表示できなくなります。 アカウントの所有権の変更は元に戻せないので、注意してください。
{:shortdesc: .shortdesc}

## カタログ・リソースの所有者の変更方法

リソースの所有者を変更するには、[CLI](/docs/cli/reference/bluemix_cli/bx_cli.html#ibmcloud_commands_settings) で以下のコマンドを使用します。

`ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
