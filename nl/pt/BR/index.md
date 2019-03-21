---

copyright:
  years: 2015, 2019
lastupdated: "2019-02-13"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Tipos de Conta
{: #accounts}

O {{site.data.keyword.Bluemix_notm}} tem três tipos de conta diferentes: Lite, Pré-paga e Assinatura. Você obtém uma conta Lite grátis assim que se inscreve. Pré-paga e Assinatura são nossas opções de conta faturáveis, cada uma oferecendo recursos diferentes. Compare cada conta e escolha a que melhor se adéqua às suas necessidades.
{:shortdesc}


## Comparando contas
{: #compare}

A tabela a seguir fornece uma comparação das contas Lite, Pré-paga e de Assinatura. Para obter mais detalhes sobre cada conta, consulte as seções a seguir.

|                                         | Lite               | Pagamento por uso      | Inscrição       |
|-----------------------------------------|--------------------|--------------------|--------------------|
| **Acesso à memória do Cloud Foundry grátis** | 256 MB             | 512 MB             | 512 MB             |
| **Acesso aos [Planos de serviços Lite ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/catalog/?search=label:lite){: new_window}** | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Acesso a todos os planos grátis**            |                    | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Acesso ao catálogo completo do {{site.data.keyword.Bluemix_notm}}** |  | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Acesso a múltiplas regiões do Cloud Foundry** |               | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Sem restrições de tempo** | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Custo zero garantido**                | ![Recurso disponível](../icons/icon_enabled.svg) |  |         |
| **Precificação com desconto**                  |                    |                    | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Melhor para provas de conceito de aprendizado ou construção** | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |  |
| **Adequado para casos de uso de produção**        |                    | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
{: caption="Tabela 1. Comparação de contas do {{site.data.keyword.Bluemix_notm}}" caption-side="top"}


## Conta Lite
{: #liteaccount}

Inscreva-se para uma conta Lite para começar a construir seus apps e explorar serviços com planos Lite grátis selecionados, que são exibidos com uma tag Lite ![Tag Lite](../icons/Lite.svg) no console do {{site.data.keyword.Bluemix_notm}}. Sua conta Lite não expira e seu cartão de crédito não é necessário.

Você tem acesso a um único grupo de recursos que é criado e denominado `Default`. Todas as instâncias de seu serviço que forem gerenciadas pelo Identity and Access Management (IAM) do {{site.data.keyword.Bluemix_notm}} serão incluídas automaticamente nesse grupo de recursos. É possível atualizar o nome desse grupo de recursos a qualquer momento. Consulte [Renomeando um grupo de recursos](/docs/resources?topic=resources-rgs#rename_rgs) para obter as etapas detalhadas.

Cada grupo de recursos é livre. Ao criar uma conexão entre um serviço gerenciado pelo IAM e um app Cloud Foundry, você cria um alias, que é uma instância de serviço, que conta para sua cota. Veja [Gerenciando conexões](/docs/resources?topic=resources-connect_app).
{: tip}

### O que está disponível?
{: #lite-account-features}

Confira a lista a seguir de recursos-chave que estão disponíveis em uma conta Lite:

   * A conta é grátis, nenhum cartão de crédito é necessário.
   * A conta nunca expira.
   * É possível usar uma organização em uma região do {{site.data.keyword.Bluemix_notm}}.
   * Suporte básico do {{site.data.keyword.Bluemix_notm}} de graça. O suporte básico é fornecido para ambientes de não produção ou cargas de trabalho em que severidades tradicionais não são usadas e tempos de resposta específicos não são estipulados.
   * Você recebe notificações por e-mail sobre o status da conta e limites de cota.
   * Seus apps Cloud Foundry podem acessar até 256 MB de memória instantânea de tempo execução grátis.
   * É possível provisionar uma instância de qualquer serviço no [catálogo do {{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window} que tenha um plano Lite.
   * Depois de 10 dias sem atividade de desenvolvimento, seus apps serão suspensos. Continue trabalhando em seus apps para acordá-los.
   * Depois de 30 dias sem atividade de desenvolvimento, suas instâncias de serviço com planos Lite são excluídas.

### Fazendo upgrade de sua conta Lite
{: #upgrade-lite-account}

É possível fazer upgrade para uma conta Pré-paga ou conta de Assinatura. Para obter mais informações, consulte [Como fazer upgrade ou converter meu tipo de conta?](/docs/account?topic=account-changeacct)

Você obterá um crédito promocional de US$ 200 após fazer upgrade para uma conta Pré-paga e o crédito será automaticamente aplicado à sua conta. Seu crédito de US$ 200 é válido por 30 dias e é automaticamente aplicado à sua fatura. O crédito não pode ser usado com ofertas de terceiros.

## Conta pré-paga
{: #paygo}

Com uma conta pré-paga, é possível criar múltiplos grupos de recursos para gerenciar facilmente a cota e visualizar o uso de faturamento para um conjunto de recursos. Seus encargos são baseados em seu uso de cálculo e serviços do {{site.data.keyword.Bluemix_notm}}. Você é elegível para abonos grátis de tempo de execução e serviço. Se você usar além do abono grátis, receberá uma fatura mensal do {{site.data.keyword.Bluemix_notm}}. A fatura será em dólares dos Estados Unidos (US$) e fornecerá detalhes sobre os encargos do recurso.

Além disso, com uma conta Pré-paga, é possível pedir itens opcionais, como opções de suporte avançado ou premium. Entre em contato com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg) para obter informações adicionais.


### Fazendo upgrade de sua conta Pré-paga
{: #upgrade-to-subscription}

Para fazer upgrade da conta Pré-paga para uma conta de Assinatura, entre em contato com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo").

## Conta Assinatura
{: #subscription-account}

Com uma conta Assinatura, é possível criar múltiplos grupos de recursos para gerenciar facilmente a cota e visualizar o uso de faturamento para um conjunto de recursos. Você se compromete com um valor de gasto mínimo a cada mês e recebe um desconto de assinatura que é aplicado a esse encargo mínimo. Será cobrada uma taxa sem desconto por qualquer uso que exceda o seu valor total de assinatura. Para visualizar sua assinatura, acesse **Gerenciar > Faturamento e uso** e selecione **Assinaturas**.

Se você tiver uma conta de assinatura, será possível criar a maioria dos serviços disponíveis no [catálogo do {{site.data.keyword.Bluemix_notm}}](https://cloud.ibm.com/catalog/){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo"). No entanto, alguns serviços usam um plano de precificação específico que requer que você o compre separadamente.

### Conta do {{site.data.keyword.Bluemix_dedicated_notm}}
Com o {{site.data.keyword.Bluemix_dedicated_notm}}, é necessário inscrever-se para um prazo mínimo de um ano que inclui:

   * Conectividade VPN de volta para a sua infraestrutura
   * Ambiente completamente redundante em um data center do {{site.data.keyword.BluSoftlayer_notm}}
   * Todos os tempos de execução suportados ({{site.data.keyword.runtime_liberty_short}}, {{site.data.keyword.runtime_nodejs_short}} e os tempos de execução de software livre integrados)
   * Todos os serviços dedicados que você selecionou e todos os serviços públicos do {{site.data.keyword.Bluemix_notm}}
   * Suporte {{site.data.keyword.Bluemix_notm}} padrão

Também é possível pedir itens opcionais, como {{site.data.keyword.BluDirectLink}} ou opções de suporte avançado ou premium. Entre em contato com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg) para obter informações adicionais.

O que é pago todos os meses durante esse prazo baseia-se nos serviços dedicados que você deseja, além de uma conta Assinatura que fornece acesso a todos os serviços públicos. Os encargos de uso dos serviços no {{site.data.keyword.Bluemix_notm}} Público são calculados com base no contrato da conta da assinatura. Você recebe
uma fatura para os serviços usados, além desse contrato de
assinatura. Entre em contato com o representante de conta designado da IBM ou com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg) para iniciar seu contrato.
