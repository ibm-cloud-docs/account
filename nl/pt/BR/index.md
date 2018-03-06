---

copyright:

  years: 2015, 2018
lastupdated: "2018-02-15"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Tipos de Conta
{: #accounts}

É possível começar a construir no {{site.data.keyword.Bluemix}} de graça. Temos três tipos de contas diferentes que você pode escolher: Lite, Pré-paga e de Assinatura. É possível usar qualquer um dos tipos de contas para começar a usar o {{site.data.keyword.Bluemix_notm}} - basta escolher aquele que se ajuste melhor às suas necessidades.
{:shortdesc}

## Comparação de conta
{: #compare}

A tabela a seguir fornece uma comparação das contas Lite, Pré-paga e de Assinatura. Para obter mais detalhes sobre cada conta, veja as seções a seguir.

|  | Lite  | Pré-paga | Inscrição |
|--------------------|--------------------|--------------------|--------------------|
| **Acesso à memória do Cloud Foundry grátis** | 256 MB | 512 MB | 512 MB |
| **Acesso aos [Planos de serviços Lite ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/catalog/?search=label:lite){: new_window}** | ![Feature available](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Acesso a todos os planos grátis** |  | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Acesso ao catálogo integral** |  | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Sem restrições de tempo** | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Custo zero garantido** | ![Recurso disponível](../icons/icon_enabled.svg) |  |  |
| **Precificação negociada** |  |  | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Melhor para aprendizado ou construção de POCs** | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |  |
| **Adequado para casos de uso de produção** |  | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
{: caption="Tabela 1. Comparação de contas do {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

## Conta Lite
{: #liteaccount}

Inscreva-se para uma conta Lite grátis para construir apps e explorar serviços com planos grátis selecionados que são denominados Lite e exibidos com uma tag Lite ![Lite tag](../icons/Lite.svg) no console do {{site.data.keyword.Bluemix_notm}}. Sua conta Lite não expira e seu cartão de crédito não é necessário.

Você tem acesso a um único grupo de recursos que é criado e denominado `Default`. Todas as suas instâncias de serviços que são gerenciadas pelo {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) são incluídas automaticamente nesse grupo de recursos. É possível atualizar o nome desse grupo de recursos a qualquer momento. Consulte [Renomeando um grupo de recursos](/docs/account/resourcegroups.html#renaming-a-resource-group) para obter as etapas detalhadas.

Cada grupo de recursos é livre. Ao criar uma conexão entre um serviço gerenciado pelo IAM e um aplicativo Cloud Foundry, crie um alias, que é uma instância de serviço, que conta para sua cota. Consulte [O que é um alias?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

### O que está disponível?

Você pode estar querendo saber o que é oferecido em uma conta Lite. Confira a lista a seguir de recursos-chave:

   * A conta é grátis, nenhum cartão de crédito é necessário.
   * A conta nunca expira.
   * É possível usar uma organização em uma região do {{site.data.keyword.Bluemix_notm}}.
   * Suporte básico do {{site.data.keyword.Bluemix_notm}} de graça. O suporte básico é fornecido para ambientes de não produção ou cargas de trabalho em que severidades tradicionais não são usadas e tempos de resposta específicos não são estipulados.
   * Você recebe notificações por e-mail sobre o status da conta e limites de cota.
   * Seus apps Cloud Foundry podem acessar até 256 MB de memória instantânea de tempo execução grátis.
   * É possível trabalhar com um cluster do Kubernetes com 2 CPUs e 4 GB de RAM.
   * É possível provisionar uma instância de qualquer serviço no catálogo do [{{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window} que tenha um plano Lite.
   * Depois de 10 dias sem atividade de desenvolvimento, seus apps são suspensos. É possível começar a trabalhar em novos apps sem ter que se preocupar com atingir os limites de cota de memória.
   * Depois de 30 dias sem atividade de desenvolvimento, suas instâncias de serviço com planos Lite são excluídas. Dessa forma, você não precisa gerenciar a exclusão de instâncias inativas antes de criar novas.

### Fazendo upgrade de sua conta

Quando você estiver pronto para crescer, faça upgrade para uma conta pré-paga e pague somente o que você usar além dos abonos grátis. Acesse **Gerenciar** > **Faturamento e uso** > **Faturamento** no console e clique em **Incluir cartão de crédito**. 

## Contas faturáveis
{: #billableacts}

A tabela a seguir lista os diferentes tipos de contas e seus métodos de cobrança.

|Tipo de conta |	Como sou cobrado? |
|------------------|-----------------------|
|Pré-paga |	Os encargos baseiam-se no uso do cálculo e serviços do {{site.data.keyword.Bluemix_notm}} |
|Inscrição | É possível obter um desconto mensal com base em um compromisso de gasto mínimo mensal |
| {{site.data.keyword.Bluemix_dedicated_notm}} | Contrato anual |
|{{site.data.keyword.Bluemix_local_notm}} |	Contrato anual |
{:caption="Tabela 2. Contas e encargos faturáveis do {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

Se você vincular sua conta faturável do {{site.data.keyword.Bluemix_notm}} a uma conta do SoftLayer, iniciando no primeiro do próximo mês, seus encargos combinados serão incluídos na fatura do {{site.data.keyword.Bluemix_notm}}. Para obter mais informações, veja [Visualizando créditos](/docs/billing-usage/viewing_usage.html#credits).
{: tip}

### Conta pré-paga

Com uma conta pré-paga, é possível criar múltiplos grupos de recursos para gerenciar facilmente a cota e visualizar o uso de faturamento para um conjunto de recursos. Você é elegível para abonos grátis de tempo de execução e serviço. Se usar mais do que o abono grátis, você receberá uma fatura mensal do {{site.data.keyword.Bluemix_notm}}. A fatura será em dólares dos Estados Unidos (USD) e detalhará os encargos do recurso.

Em muitos países e regiões, é possível inscrever-se para uma conta pré-paga no console do {{site.data.keyword.Bluemix_notm}}. Depois de fornecer suas informações de faturamento e de cartão de crédito, aceite os termos e condições e envie sua solicitação de conta. Em seguida, seu cartão de crédito será validado. Você também receberá um e-mail de confirmação sobre as informações da conta. Alguns minutos após o recebimento do e-mail de confirmação, é possível retornar ao console para continuar a construção de seus apps. 

Se a sua solicitação on-line não puder ser processada para seu país ou região, entre em contato com o [Suporte do {{site.data.keyword.Bluemix_notm}}](https://ibm.biz/bluemixsupport){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg). Após efetuar login no Portal de serviço do {{site.data.keyword.Bluemix_notm}}, clique em **contatar suporte** e selecione a opção **Faturamento, Conta ou Login**.

É possível converter a sua conta pré-paga em uma conta de assinatura a qualquer momento. Entre em contato com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg) para obter mais detalhes.
{: tip}

### Conta Assinatura

Com uma conta Assinatura, é possível criar múltiplos grupos de recursos para gerenciar facilmente a cota e visualizar o uso de faturamento para um conjunto de recursos.

Você confirma uma quantia de gasto mínimo cada mês e recebe um desconto na assinatura que será aplicado a esse encargo mínimo. Você
também paga por qualquer uso que exceda a quantia mínima de gasto.

Para se inscrever para uma conta de Assinatura e para obter mais informações sobre taxas e descontos de assinatura, deve-se entrar em contato com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg)

### Conta do {{site.data.keyword.Bluemix_dedicated_notm}}

Com o {{site.data.keyword.Bluemix_dedicated_notm}}, deve-se inscrever-se para um prazo mínimo de um ano que inclui:

   * Conectividade VPN de volta para a sua infraestrutura
   * Ambiente completamente redundante em um data center do {{site.data.keyword.BluSoftLayer_notm}}
   * Todos os tempos de execução suportados (IBM Java Liberty, Node.js e tempos de execução de software livre integrados)
   * Todos os serviços dedicados selecionados e todos os serviços públicos do {{site.data.keyword.Bluemix_notm}}
   * Suporte {{site.data.keyword.Bluemix_notm}} padrão

Também é possível pedir itens opcionais, tais como
o SoftLayer DirectLink ou opções de suporte premium. Entre em contato com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg) para obter informações adicionais.

O que é pago todos os meses durante esse prazo baseia-se nos serviços dedicados que você deseja, além de uma conta Assinatura que fornece acesso a todos os serviços públicos. Os encargos de uso dos serviços no {{site.data.keyword.Bluemix_notm}} Público são calculados com base no contrato da conta da assinatura. Você recebe
uma fatura para os serviços usados, além desse contrato de
assinatura. Entre em contato com o representante de conta designado da IBM ou com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg) para iniciar seu contrato.

### Conta do {{site.data.keyword.Bluemix_local_notm}}

Com o {{site.data.keyword.Bluemix_local_notm}}, deve-se inscrever por um prazo mínimo de um ano que inclui:

   * Uma capacidade de entrega denominada retransmissão que permite que a IBM se conecte à implementação local e
entregue atualizações de forma automática e consistente.
   * Todos os tempos de execução suportados (IBM Java Liberty, Node.js e tempos de execução de software livre integrados)
   * Todos os serviços locais que você selecionou e acesso a todos os serviços públicos do {{site.data.keyword.Bluemix_notm}}
   * Suporte {{site.data.keyword.Bluemix_notm}} padrão

O que é pago todos os meses durante esse prazo é baseado nos serviços locais que você deseja, além de uma conta Assinatura que fornece acesso a todos os serviços públicos. Os encargos de uso dos serviços no {{site.data.keyword.Bluemix_notm}} Público são calculados com base no contrato da conta da assinatura. Você recebe
uma fatura para os serviços usados, além desse contrato de
assinatura. Entre em contato com o representante de conta designado da IBM ou com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg) para iniciar seu contrato.

## Conta para teste
{: #trial}

As contas para teste estão disponíveis em todas as regiões. Com uma avaliação grátis de 30 dias, é possível ir diretamente e iniciar a construção dos apps e explorar serviços no {{site.data.keyword.Bluemix_notm}}.

Ao inscrever-se para uma avaliação grátis com o ID do {{site.data.keyword.Bluemix_notm}}, sua conta recebe os recursos a seguir gratuitamente:

  * Máximo de 2 GB de memória
  * 10 serviços
  * 1 certificado SSL

Você também tem acesso a um único grupo de recursos que é criado e denominado `Default`. Todas as suas instâncias de serviço gerenciado pelo IAM são automaticamente incluídas nesse grupo de recursos. É possível atualizar o nome desse grupo de recursos a qualquer momento. Consulte [Renomeando um grupo de recursos](/docs/account/resourcegroups.html#renaming-a-resource-group) para obter as etapas detalhadas.

Cada grupo de recursos é livre. Ao criar uma conexão entre um serviço gerenciado pelo IAM e um aplicativo Cloud Foundry, crie um alias, que é uma instância de serviço, que conta para sua cota. Consulte [O que é um alias?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

### O que acontece quando minha avaliação grátis termina?
{: #trialend}

Quando sua avaliação grátis expira 30 dias após sua inscrição, os apps em sua conta são interrompidos. Não é possível se inscrever para outra conta do {{site.data.keyword.Bluemix_notm}}, mas ainda é possível acessar sua conta e quaisquer contas para as quais você é convidado.

Para reiniciar seus apps, converta sua conta para uma conta faturável fornecendo informações de cartão de crédito para uma conta pré-paga ou criando uma conta de assinatura. Será possível então continuar usando os abonos de cálculo e serviço grátis. Você pagará apenas pelo uso de serviços, contêineres e tempos de execução não incluídos no abono mensal grátis.

  * Para fazer upgrade para uma conta pré-paga, acesse **Gerenciar** > **Faturamento e uso** > **Faturamento** no console e clique em **Incluir cartão de crédito**.
  * Para se inscrever para uma conta de Assinatura, entre em contato com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg).

Se você não converter sua conta após a expiração da avaliação grátis, seus apps e serviços serão removidos após 30 dias. No entanto, sua conta não será excluída e será possível efetuar login e fazer upgrade para uma conta faturável a qualquer momento. Além disso, você recebe notificações por e-mail para lembrá-lo de criar uma conta faturável e evitar perder suas configurações de app e configurações de serviço. Se preferir não receber notificações do {{site.data.keyword.Bluemix_notm}}, será possível cancelar a assinatura a qualquer momento.

Se você converter sua conta, seus abonos grátis serão limitados aos abonos normalmente fornecidos por serviço. Os
abonos não são mais de uso ilimitado oferecidos por muitos dos serviços IBM durante a
avaliação grátis.

