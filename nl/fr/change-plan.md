---



copyright:

  years: 2017, 2019
lastupdated: "2019-02-13"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Changement des plans de service
{: #changing}

Vous pouvez changer le plan d'un service {{site.data.keyword.Bluemix}} si les changements de plan sont activés pour le service spécifique. Vous pouvez être amené à changer de plan, par exemple, pour mettre à niveau ou réduire votre plan. Vous pouvez effectuer cette action à partir de votre tableau de bord d'instance de service.
{: shortdesc}

Recherchez-vous plus de détails sur la mise à niveau de votre type de compte ? Voir [Comment mettre à niveau ou modifier mon type de compte ?](/docs/account/account_faq.html#changeacct) pour plus d'informations.
{: tip}

Vous pouvez changer les plans de service pour certains services uniquement. Si le changement de plan est possible pour le service, le tableau de bord de l'instance du service affiche l'option **Plan** dans la navigation. Chaque service propose un ensemble différent d'étapes à suivre si vous changez de plan.

1. Cliquez sur **Plan** dans le tableau de bord d'instance de service. En général, vous pouvez mettre à niveau votre plan ou passer à un plan de niveau inférieur.
2. Après avoir changé de plan, vous devez effectuer des étapes supplémentaires. Celles-ci varient selon le type de changement de plan et le service. Par exemple, si vous êtes passé à un plan de niveau inférieur, il se peut que vous deviez reconstituer votre application. Ou bien, si vous avez mis à niveau votre plan, vous devrez peut-être reconstituer votre application et effectuer d'autres opérations.

   Pour reconstituer votre application, accédez à votre liste de ressources pour trouver l'application à laquelle le service est lié. Cliquez sur l'icône Menu ![Icône Menu](../icons/icon_hamburger.svg) **> Liste de ressources**. Dans le menu de l'application, sélectionnez **Redémarrer l'application**.

  Pour plus d'informations sur les autres fonctions requises, consultez la documentation relative au service.

## Changement d'un plan via l'interface de ligne de commande
{: #changing_command_line}

Vous pouvez changer le plan d'un service non seulement en utilisant la console mais également en utilisant l'interface de ligne de commande (CLI) {{site.data.keyword.Bluemix_notm}}.

1. Vérifiez que le service est activé via le contrôleur de ressources.

   ```
   ibmcloud catalog service <service_name>
   ```
   {:codeblock}

   Si le service est activé via le contrôleur de ressources, la mention `RC Compatible true` s'affiche. Notez l'ID du plan que vous souhaitez désormais utiliser.

   ```
   RC Compatible      true
   RC Provisionable   true
   IAM Compatible     true
   Children   Name                      Kind         ID
              lite                      plan         4bcd3fgh-3cf2-47c0-93d4-d2f2289eac28
              standard                  plan         264d0450-996d-4bcd-894d-fc7018dacf1e
    ```

1. Changez de plan pour votre instance de service.

   - Si le service est activé via le contrôleur de ressources, changez votre plan en utilisant la commande [`ibmcloud resource service-instance-update`](/docs/cli/reference/ibmcloud/cli_resource_group.html#ibmcloud_commands_resource).

     ```
     ibmcloud resource service-instance-update <service_instance_name> --service-plan-id <plan_id>
     ```
     {: codeblock}

   - Si le service n'est pas est activé via le contrôleur de ressources mais dépend de Cloud Foundry, changez de plan en utilisant la commande [`ibmcloud cf update-service`](/docs/cli/reference/ibmcloud/cf_index.html#cf).

     ```
     ibmcloud cf update-service <service_instance_name> [-p <plan_name>]
     ```
     {:codeblock}
