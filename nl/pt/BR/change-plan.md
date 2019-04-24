---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-13"

keywords: change service, upgrade service, service plan

subcollection: account

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Mudando planos de serviço
{: #changing}

É possível mudar o plano de um serviço do {{site.data.keyword.Bluemix}} quando as mudanças de plano estão ativadas para o serviço específico. Você pode desejar mudar seu plano, por exemplo, para fazer upgrade ou reduzir seu plano. É possível mudar seu plano por meio de seu painel da instância de serviço.
{: shortdesc}

Você está procurando detalhes sobre como fazer upgrade de seu tipo de conta? Consulte [Como fazer upgrade ou converter meu tipo de conta?](/docs/account?topic=account-changeacct) para obter mais informações.
{: tip}

É possível mudar os planos de serviços somente para determinados serviços. Se mudanças de plano estiverem ativadas para o serviço, o painel da instância de serviço exibirá uma opção **Plano** na navegação. Cada serviço terá um conjunto diferente de etapas subsequentes se você mudar o seu plano.

1. Clique em **Plano** no painel da instância de serviço. Normalmente, é possível fazer upgrade do plano ou reduzi-lo.
2. Depois de mudar seu plano, deve-se concluir etapas extras. As etapas serão diferentes dependendo do tipo de mudança de plano e do serviço. Por exemplo, se
tiver reduzido o plano, talvez precise remontar seu app. Ou, caso tenha feito upgrade do
plano, talvez seja necessário remontar o app e tomar ações adicionais.

   Para remontar seu app, acesse sua lista de recursos para localizar o app ao qual o serviço está ligado. Clique no ícone Menu ![Ícone Menu](../icons/icon_hamburger.svg) **> Lista de recursos**. No menu do app, selecione **Reiniciar app**.

  Para obter mais informações sobre quaisquer ações necessárias adicionais, consulte a documentação para o serviço.

## Mudando um plano por meio da CLI
{: #changing_command_line}

Como uma alternativa para o console, é possível mudar o plano de um serviço usando a interface da linha de comandos (CLI) do {{site.data.keyword.Bluemix_notm}}.

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

   - Se o serviço não estiver ativado com o RC e for, portanto, baseado no Cloud Foundry, mude seu plano usando o [comando `ibmcloud cf update-service`](/docs/cli/reference/ibmcloud?topic=cloud-cli-cf#cf).

     ```
     ibmcloud cf update-service <service_instance_name> [-p <plan_name>]
     ```
     {:codeblock}
