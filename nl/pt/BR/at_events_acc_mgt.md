---

copyright:
  years: 2016, 2018

lastupdated: "2018-10-31"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# {{site.data.keyword.cloudaccesstrailshort}} eventos  
{: #at_events}

Como um responsável pela segurança, auditor ou gerenciador, é possível usar o serviço {{site.data.keyword.cloudaccesstrailfull}} para controlar como os usuários e aplicativos interagem com a conta do {{site.data.keyword.Bluemix}}. 
{:shortdesc}

Por exemplo, quando um usuário ou aplicativo efetuar login no {{site.data.keyword.Bluemix_notm}}, usando uma senha, uma chave de API e um código de autenticação ou uma senha, um evento do {{site.data.keyword.cloudaccesstrailshort}} será gerado para cada tentativa. 

O serviço {{site.data.keyword.cloudaccesstrailfull_notm}} registra atividades iniciadas pelo usuário que mudam o estado de um serviço no {{site.data.keyword.Bluemix_notm}}. Para obter mais informações, consulte  [ Sobre o  {{site.data.keyword.cloudaccesstrailshort}} ](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov ).

Para começar a monitorar as ações do usuário, veja [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla). 

## Eventos para gerenciar contas
{: #account}

A tabela a seguir lista o método de API que gera um evento quando eles são chamados:

<table>
  <caption>Ações que geram eventos</caption>
  <tr>
    <th>Ações</th>
	  <th>Descrição</th>
  </tr>
  <tr>
    <td>billing.account.create</td>
	  <td>Um evento será gerado quando você provisionar uma conta e depois que o ID da conta for designado para a conta.</td>
  </tr>
  <tr>
    <td>billing.account.update</td>
	  <td>Um evento é gerado quando você atualiza informações sobre a conta.</td>
  </tr>
  <tr>
    <td>billing.account.active</td>
	  <td>Um evento será gerado quando você verificar a conta ou quando um evento for gerado quando a conta ficar no estado ativo.</td>
  </tr>
  <tr>
    <td>billing.account.subscription.create</td>
	  <td>Um evento será gerado quando você criar uma <a href="/docs/account/index.html#subscription-account">conta da assinatura</a>.</td>
  </tr>
</table>



## Eventos para gerenciar usuários
{: #users}

A tabela a seguir lista o método de API que gera um evento quando ele é chamado:

<table>
  <caption>Ações que geram eventos</caption>
  <tr>
    <th>Ações</th>
	  <th>Descrição</th>
  </tr>
  <tr>
    <td>billing.account.user.create</td>
	  <td>Um evento é gerado quando você envia um convite para um usuário participar de uma conta. </br>O proprietário da conta é o único usuário na conta que pode executar essa ação.</td>
  </tr>
  <tr>
    <td>billing.user.active</td>
	  <td>Um evento é gerado quando você ativa o usuário na conta. </br>Quando o usuário verifica seu endereço de e-mail, o evento é gerado.</td>
  </tr>
  <tr>
    <td>billing.account.user.delete</td>
	  <td>Um evento é gerado quando você remove um usuário da conta. </br>O proprietário da conta é o único usuário na conta que pode executar essa ação.</td>
  </tr>
</table>

## Eventos para gerenciar organizações
{: #org}

A tabela a seguir lista o método de API que gera um evento quando ele é chamado:

<table>
  <caption>Ação que gera eventos</caption>
  <tr>
    <th>Ações</th>
	  <th>Descrição</th>
  </tr>
  <tr>
    <td>billing.account.org.create</td>
	  <td>Um evento é gerado quando você inclui uma organização na conta.</td>
  </tr>
</table>

## Onde procurar os eventos
{: #ui}

Os eventos do {{site.data.keyword.cloudaccesstrailshort}} estão disponíveis no {{site.data.keyword.cloudaccesstrailshort}} **Domínio da conta de Dallas** que está disponível no {{site.data.keyword.Bluemix_notm}}. Para obter mais informações, consulte [Visualizando eventos de conta](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events).

Os eventos do {{site.data.keyword.cloudaccesstrailshort}} são encaminhados automaticamente para o serviço {{site.data.keyword.cloudaccesstrailshort}} na mesma região em que a ação acontece.
