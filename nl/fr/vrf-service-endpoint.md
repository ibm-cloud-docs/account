---

copyright:
  years: 2019
lastupdated: "2019-07-01"

keywords: VRF, virtual routing and forwarding, service endpoint, private network

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Activation de VRF et des noeuds finaux de service
{: #vrf-service-endpoint}

Par défaut, vous vous connectez aux ressources de votre compte via le réseau public d'{{site.data.keyword.Bluemix}}. Vous pouvez activer la fonction VRF (Virtual Routing and Forwarding) pour déplacer le routage IP de votre compte et l'ensemble de ses ressources sur une table de routage distincte. Si VRF est activée, vous pouvez activer les noeuds finaux de service {{site.data.keyword.Bluemix_notm}} pour vous connecter directement aux ressources sans utiliser le réseau public.
{:shortdesc}

Pour activer la fonction VRF et le noeud final de service {{site.data.keyword.Bluemix_notm}}, vous avez besoin d'un compte facturable.

## Activation de VRF
{: #vrf}

VRF permet à plusieurs instances d'une table de routage d'exister dans un routeur et de fonctionner simultanément. Lorsque vous activez VRF, une table de routage distincte est créée pour votre compte et des connexions vers et depuis les ressources de votre compte sont acheminées séparément sur le réseau {{site.data.keyword.Bluemix_notm}}. VRF est activée au niveau du compte, donc toutes les ressources sont affectées par ce changement de mise en réseau. Pour plus d'informations sur la technologie VRF et son incidence sur le routage réseau de votre compte, voir [Virtual routing and forwarding on {{site.data.keyword.Bluemix_notm}}](/docs/resources?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud).

L'activation de VRF modifie de manière permanente la mise en réseau pour votre compte. Veillez à bien en mesurer l'impact sur votre compte et les ressources associées. Après avoir activé la fonction VRF, il est impossible de la désactiver.
{: important}

Pour activer VRF, créez un cas de support avec votre demande.

1. Dans la console, accédez à **Support** et cliquez sur **Créer un cas**.
1. Sélectionnez **Account and access** comme type de support.
1. Dans la zone **Subject**, entrez `Private networking question`.
1. Dans la zone **Description**, entrez le message suivant, en remplaçant _enter your account number_ par votre numéro de compte {{site.data.keyword.Bluemix_notm}}.

   `We are requesting that account *enter your account number* is moved to its own VRF. We understand the risks and approve the change. Please reply back with the scheduled window(s) of time where this change will be made so we can prepare for the migration.`

L'équipe d'ingénierie réseau d'{{site.data.keyword.Bluemix_notm}} contactera le propriétaire du cas pour planifier la conversion à VRF des réseaux de votre compte. Lors du processus de conversion, les connexions aux ressources dans votre compte peuvent être instables en raison de la perte de paquet. La conversion prend environ 15 à 30 minutes selon la complexité de votre compte. S'il existe des connexions {{site.data.keyword.BluDirectLink}} dans votre compte, l'opération peut prendre plus de temps.


## Activation des noeuds finaux de service
{: #service-endpoint}

Lorsque les noeuds finaux de service {{site.data.keyword.Bluemix_notm}} sont activés dans votre compte, vous pouvez choisir d'exposer un noeud final de réseau privé lorsque vous créez une ressource. Vous pouvez ensuite vous connecter directement à ce noeud final via le réseau privé {{site.data.keyword.Bluemix_notm}} au lieu du réseau public. Comme les ressources qui utilisent les noeuds finaux de réseau privé ne comportent pas d'adresse IP routable sur Internet, les connexions à ces ressources sont encore plus sécurisées. Pour plus d'informations, voir [Noeuds finaux de service pour connexions de réseau privé](/docs/resources?topic=resources-service-endpoints).

Pour pouvoir activer des noeuds finaux de service, la fonction VRF doit être activée pour votre compte.
{: note}

Pour activer les noeuds finaux de service à partir de l'interface de ligne de commande, vous devez disposer de la version 0.13 ou ultérieure de l'[interface de ligne de commande {{site.data.keyword.Bluemix_notm}}](/docs/cli?topic=cloud-cli-getting-started).

1.  Vérifiez si les noeuds finaux de service sont déjà activés dans votre compte.

    ```
    ibmcloud account show
    ```
    {: codeblock}

    Si la section `Service Endpoint Enabled` a la valeur `false` comme illustré dans l'exemple suivant, les noeuds finaux de service ne sont pas activés.

    ```
    Retrieving account Mia Example's Account of m.example@example.com...
    OK

    Account ID:                   abc123d0bc2edefthyufffc9b5ca318   
    Currently Targeted Account:   true   
    Linked Softlayer Account:     0123456   
    Service Endpoint Enabled:     false  
    ```
    {: screen}
1. Activez les noeuds finaux de service en exécutant la commande suivante.

   ```
   ibmcloud account update --service-endpoint-enable true
   ```
   {: codeblock}

   Cette modification peut prendre quelques minutes pour entrer en vigueur. Une fois la commande terminée, vous pouvez exécuter à nouveau la commande `ibmcloud account show` pour vérifier.

    Si la fonction VRF n'est pas activée pour votre compte, l'exécution de cette commande vous invite à créer un cas pour procéder à son activation. Entrez `y` pour créer le cas de support. Une fois la fonction VRF activée dans le compte, exécutez à nouveau cette commande pour activer la connectivité de noeud final de service dans votre compte.

    ```
    Service Endpoint is not available in linked Softlayer Account 1008967.
    Enable VRF(Virtual Routing and Forwarding) first to proceed.
    Learn more about VRF here - https://cloud.ibm.com/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html.

    Do you want to open a ticket to enable it?[y/N]> y
    Ticket 70729615 was opened successfully. Follow the link https://control.softlayer.com/support/tickets/70729876 to check the details and track the status of the ticket. You will be required to login to view this ticket.
    Account ID:    1008967
    Ticket:        Private Network Question
    ```
    {: screen}


Une fois les noeud finaux de service activés, vous pouvez créer des ressources qui se connectent via le réseau privé {{site.data.keyword.Bluemix_notm}}. Pour obtenir la liste des services qui prennent en charge les noeuds finaux de service et d'autres informations, voir [Configuration des noeuds finaux de réseau privé](/docs/resources?topic=resources-private-network-endpoints).
