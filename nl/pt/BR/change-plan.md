---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-30"

keywords: change service, upgrade service, service plan, pricing plan

subcollection: account

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Mudando planos de serviço
{: #changing}

É possível mudar o plano de precificação de um serviço {{site.data.keyword.Bluemix}} quando as mudanças no plano estão ativadas para o serviço específico. Você pode desejar mudar o plano, por exemplo, fazer upgrade ou reduzir seu plano. É possível mudar o plano de precificação do serviço no painel da instância de serviço.
{: shortdesc}

Você está procurando detalhes sobre como fazer upgrade de seu tipo de conta? Consulte [Fazendo upgrade de sua conta](/docs/account?topic=account-upgrading-account) para obter mais informações.
{: tip}

É possível mudar os planos de serviços somente para determinados serviços. Se mudanças de plano estiverem ativadas para o serviço, o painel da instância de serviço exibirá uma opção **Plano** na navegação. Cada serviço terá um conjunto diferente de etapas subsequentes se você mudar o seu plano.

1. No console do {{site.data.keyword.Bluemix_notm}}, clique no ícone Menu ![Ícone Menu](../icons/icon_hamburger.svg) > **Lista de recursos** para visualizar sua lista de recursos. Clique no serviço que você deseja atualizar.
1. Clique em **Plano** no painel da instância de serviço. Selecione o plano para o qual você deseja mudar e clique em **Salvar**.

    Alguns serviços têm planos que não são selecionáveis na página Plano. Geralmente, esses planos não são selecionáveis porque requerem assistência da equipe de Vendas ou requerem uma migração antes que seja possível mudar os planos. Veja a documentação para o serviço para obter informações sobre as próximas etapas requeridas.

1. Depois de mudar seu plano, deve-se concluir etapas extras. As etapas serão diferentes dependendo do tipo de mudança de plano e do serviço. Por exemplo, se
tiver reduzido o plano, talvez precise remontar seu app. Ou, caso tenha feito upgrade do
plano, talvez seja necessário remontar o app e tomar ações adicionais.

   Para remontar seu app, acesse sua lista de recursos para localizar o app ao qual o serviço está ligado. Clique no ícone Menu ![Ícone Menu](../icons/icon_hamburger.svg) **> Lista de recursos**. No menu do app, selecione **Reiniciar app**.

  Para obter mais informações sobre quaisquer ações necessárias adicionais, consulte a documentação para o serviço.

## Mudando um plano por meio da CLI
{: #changing_command_line}

Como uma alternativa para o console, é possível mudar o plano de precificação de um serviço usando a interface da linha de comandos (CLI) do {{site.data.keyword.Bluemix_notm}}.

1. Verifique se o serviço está ativado com o controlador de recurso.

   ```
   ibmcloud catalog service <service_name>
   ```
   {:codeblock}

   Se o serviço estiver ativado com o controlador de recurso (RC), ele listará `RC Compatible true`. Tome nota do ID do plano para o qual você deseja mudar.

   ```
   RC Compatible      true
   RC Provisionable   true
   IAM Compatible     true
   Children   Name                      Kind         ID
              lite                      plan         4bcd3fgh-3cf2-47c0-93d4-d2f2289eac28
              standard                  plan         264d0450-996d-4bcd-894d-fc7018dacf1e
    ```

1. Mude o plano para a sua instância de serviço.

   - Se o serviço estiver ativado com o RC, mude seu plano usando o [comando `ibmcloud resource service-instance-update`](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource).

     ```
     ibmcloud resource service-instance-update <service_instance_name> --service-plan-id <plan_id>
     ```
     {: codeblock}

   - Se o serviço não estiver ativado para RC e, portanto, se basear no Cloud Foundry, mude seu plano usando o [comando `ibmcloud cf update-service`](/docs/cli?topic=cloud-cli-ibmcloud_commands_services#ibmcloud_service_update).

     ```
     ibmcloud cf update-service <service_instance_name> [-p <plan_name>]
     ```
     {:codeblock}
