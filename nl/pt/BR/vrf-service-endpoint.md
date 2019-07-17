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

# Ativando o VRF e os terminais em serviço
{: #vrf-service-endpoint}

Por padrão, você se conecta aos recursos em sua conta por meio da rede pública do {{site.data.keyword.Bluemix}}. É possível ativar o roteamento virtual e o encaminhamento (VRF) para mover o roteamento de IP para sua conta e todos os seus recursos em uma tabela de roteamento separada. Se o VRF estiver ativado, será possível, então, ativar os terminais em serviço do {{site.data.keyword.Bluemix_notm}} para se conectarem diretamente aos recursos sem usar a rede pública.{:shortdesc}

Para ativar o roteamento virtual e o encaminhamento e o terminal em serviço do {{site.data.keyword.Bluemix_notm}}, você precisa de uma conta faturável.

## Ativando o VRF
{: #vrf}

O VRF permite que múltiplas instâncias de uma tabela de roteamento existam em um roteador e trabalhem simultaneamente. Quando você ativa o VRF, uma tabela de roteamento separada é criada para sua conta e as conexões de e para os recursos de sua conta são roteadas separadamente na rede do {{site.data.keyword.Bluemix_notm}}. O VRF é ativado no nível de conta, portanto, todos os recursos são afetados por essa mudança de rede. Para obter mais informações sobre a tecnologia VRF e como ela afeta o roteamento da rede da sua conta, consulte [Roteamento virtual e encaminhamento no {{site.data.keyword.Bluemix_notm}}](/docs/resources?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud).

A ativação do VRF altera permanentemente a rede para sua conta. Certifique-se de entender o impacto para sua conta e recursos. Depois de ativar o VRF, ele não pode ser desativado.
{: important}

Para ativar o VRF, crie um caso de suporte com sua solicitação.

1. No console, acesse **Suporte** e clique em **Criar um caso**.
1. Selecione **Conta e acesso** como o tipo de suporte.
1. No campo **Assunto**, insira `Pergunta de rede privada`.
1. No campo **Descrição**, insira a mensagem a seguir, substituindo _insira seu número da conta_ pelo seu número da conta do {{site.data.keyword.Bluemix_notm}}.

   `Estamos solicitando que a conta *insira o número da sua conta* seja movida para seu próprio VRF. Entendemos os riscos e aprovamos a mudança. Responda de volta com a(s) janela(s) planejada(s) de tempo em que essa mudança será feita para que possamos nos preparar para a migração.`

A equipe de engenharia de rede do {{site.data.keyword.Bluemix_notm}} irá acessar o proprietário do caso para planejar um tempo para que a rede de sua conta seja convertida em VRF. Durante o processo de conversão, as conexões com os recursos em sua conta podem ser instáveis devido à perda de pacote. A conversão leva aproximadamente de 15 a 30 minutos, dependendo da complexidade de sua conta. Se sua conta tiver conexões anteriores do {{site.data.keyword.BluDirectLink}}, poderá levar mais tempo.


## Ativando terminais em serviço
{: #service-endpoint}

Quando os terminais em serviço do {{site.data.keyword.Bluemix_notm}} são ativados em sua conta, é possível optar por expor um terminal de rede privada ao criar um recurso. Em seguida, é possível se conectar diretamente a esse terminal por meio da rede privada do {{site.data.keyword.Bluemix_notm}} em vez da rede pública. Como os recursos que usam terminais de rede privada não têm um endereço IP roteável pela Internet, as conexões com esses recursos são mais seguras. Para obter mais informações, consulte [Terminais em serviço para conexões de rede privada](/docs/resources?topic=resources-service-endpoints).

Antes de poder ativar os terminais em serviço, o VRF deve ser ativado para sua conta.
{: note}

Para ativar os terminais em serviço a partir da CLI, é necessária a versão 0.13 ou mais recente da [CLI do {{site.data.keyword.Bluemix_notm}}](/docs/cli?topic=cloud-cli-getting-started).

1.  Verifique se os terminais em serviço já estão ativados em sua conta.

    ```
    ibmcloud account show
    ```
    {: codeblock}

    Se `Terminal em serviço ativado` for `false`, conforme mostrado no exemplo a seguir, os terminais em serviço não serão ativados.

    ```
    Recuperando a conta de m.example@example.com do exemplo da conta Mia...
    OK

    ID da conta:                  abc123d0bc2edefthyufffc9b5ca318   
    Conta atualmente direcionada:   true   
    Conta do Softlayer vinculada:     0123456   
    Terminal em serviço ativado:     false  
    ```
    {: screen}
1. Ative os terminais em serviço ao executar o comando a seguir.

   ```
   ibmcloud account update--service-endpoint-enable true
   ```
   {: codeblock}

   Pode levar alguns minutos para que essa mudança entre em vigor. Após a conclusão do comando, é possível executar o comando `ibmcloud account show` novamente para verificar.

    Se o VRF não estiver ativado para sua conta, a execução desse comando solicitará que você crie um caso para ativá-lo. Insira `y` para criar o caso de suporte. Após o VRF ser ativado na conta, execute o comando novamente para ativar a conectividade do terminal em serviço em sua conta.

    ```
    O terminal em serviço não está disponível na conta do Softlayer vinculada 1008967.
    Primeiro ative o VRF (Virtual Routing and Forwarding) para continuar.
    Saiba mais sobre o VRF aqui: https://cloud.ibm.com/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html.

    Deseja abrir um chamado para ativá-lo?[y/N]> y
    O chamado 70729615 foi aberto com êxito. Siga o link https://control.softlayer.com/support/tickets/70729876 para verificar os detalhes e rastrear o status do chamado. Você será solicitado a efetuar login para visualizar este chamado.
    ID da conta:    1008967
    Chamado:        Questão sobre rede privada
    ```
    {: screen}


Depois que os terminais em serviço são ativados, é possível criar recursos que se conectam por meio da rede privada do {{site.data.keyword.Bluemix_notm}}. Para obter uma lista de serviços que suportam terminais em serviço e mais informações, consulte [Configurando terminais de rede privada](/docs/resources?topic=resources-private-network-endpoints).
