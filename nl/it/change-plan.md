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


# Modifica dei piani di servizio
{: #changing}

Puoi modificare il piano di prezzi di un servizio {{site.data.keyword.Bluemix}} se le modifiche del piano sono abilitate per lo specifico servizio. Potresti voler modificare il piano, ad esempio, per eseguire un upgrade del tuo piano o per ridurlo. Puoi modificare il piano di prezzi del servizio dal dashboard dell'istanza del servizio.
{: shortdesc}

Stai cercando dettagli sull'upgrade del tuo tipo di account? Per ulteriori informazioni, vedi [Upgrade del tuo account](/docs/account?topic=account-upgrading-account).
{: tip}

Puoi modificare i piani di servizio solo per specifici servizi. Se per il servizio sono abilitate le modifiche del piano, il dashboard dell'istanza del servizio visualizza un'opzione **Piano** nel riquadro di navigazione. Se modifichi
il tuo piano, ogni servizio prevede una procedura diversa a cui devi attenerti.

1. Dalla console {{site.data.keyword.Bluemix_notm}}, fai clic sull'icona Menu ![Icona Menu](../icons/icon_hamburger.svg) > **Elenco risorse** per visualizzare il tuo elenco di risorse. Fai clic sul servizio che vuoi aggiornare.
1. Fai clic su **Piano** nel dashboard dell'istanza del servizio. Seleziona il piano a cui vuoi passare e fai clic su **Salva**.

    Alcuni servizi dispongono di piani non selezionabili dalla pagina Piano. Normalmente, questi piani non sono selezionabili perché richiedono assistenza dal team delle vendite o è necessario eseguire una migrazione prima di poter modificare i piani. Consulta la documentazione del servizio per informazioni sui passi successivi necessari.

1. Dopo che hai modificato il tuo piano, devi completare dei passi supplementari. Tale procedura varia a
seconda del tipo di modifica del piano e del servizio. Ad esempio, se hai ridotto il tuo piano, è possibile
che tu debba preparare nuovamente la tua applicazione. Nel caso invece in cui tu abbia eseguito l'upgrade del tuo piano, potresti dover preparare di nuovo la tua applicazione ed eseguire delle altre azioni.

   Per preparare di nuovo la tua applicazione, vai all'elenco risorse per trovare l'applicazione a cui è associato il servizio. Fai clic sull'icona Menu ![Icona Menu](../icons/icon_hamburger.svg) **> Elenco risorse**. Nel menu delle applicazioni, seleziona **Riavvia applicazione**.

  Per ulteriori informazioni su tutte le altre azioni necessarie, vedi la documentazione del servizio.

## Modifica di un piano tramite la CLI
{: #changing_command_line}

Come alternativa alla console, puoi modificare il piano di prezzi di un servizio utilizzando la CLI (command-line interface) {{site.data.keyword.Bluemix_notm}}.

1. Verifica se il servizio è abilitato con il controller delle risorse.

   ```
   ibmcloud catalog service <service_name>
   ```
   {:codeblock}

   Se il servizio è abilitato con il controller delle risorse (RC), viene elencato `RC Compatible true`. Prendi nota dell'ID del piano che vuoi modificare.

   ```
   RC Compatible      true
   RC Provisionable   true
   IAM Compatible     true
   Children   Name                      Kind         ID
              lite                      plan         4bcd3fgh-3cf2-47c0-93d4-d2f2289eac28
              standard                  plan         264d0450-996d-4bcd-894d-fc7018dacf1e
    ```

1. Modifica il piano per la tua istanza del servizio.

   - Se il servizio è abilitato RC, modifica il tuo piano utilizzando il [comando `ibmcloud resource service-instance-update`](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource).

     ```
     ibmcloud resource service-instance-update <service_instance_name> --service-plan-id <plan_id>
     ```
     {: codeblock}

   - Se il servizio non è abilitato RC ed è pertanto basato su Cloud Foundry, modifica il tuo piano utilizzando il [comando `ibmcloud cf update-service`](/docs/cli?topic=cloud-cli-ibmcloud_commands_services#ibmcloud_service_update).

     ```
     ibmcloud cf update-service <service_instance_name> [-p <plan_name>]
     ```
     {:codeblock}
