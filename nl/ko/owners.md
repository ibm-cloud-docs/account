---

copyright:

  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# 개인용 리소스 소유권 변경

명령행 인터페이스를 사용하여 계정 소유권을 변경할 수 있습니다. 카탈로그에서 개인용 리소스를 작성하고 사용자 정의한 후 해당 리소스의 소유권을 다른 사용자에게 전송할 수 있습니다. 소유권을 전송한 후에는 계정에서 리소스를 볼 수 없습니다. 계정 소유권 변경은 취소할 수 없으므로 주의하십시오.
{:shortdesc: .shortdesc}

## 카탈로그 리소스의 소유자를 변경하는 방법

[CLI](/docs/cli/reference/bluemix_cli/bx_cli.html#ibmcloud_commands_settings)를 사용하여 리소스의 소유자를 변경하려면 다음 명령을 사용하십시오.

`ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
