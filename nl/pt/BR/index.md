---

copyright:
  years: 2015, 2019
lastupdated: "2019-08-02"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account, subscription, service bundle

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:row-headers: .row-headers}

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
{: row-headers}
{: class="comparison-table"}
{: caption="Tabela 1. Comparação de contas do {{site.data.keyword.Bluemix_notm}}" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the feature. The column headers identify the account type. To understand which features apply to the account types, navigate to the row, and find the feature that you're interested in."}

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
   * Seus apps Cloud Foundry podem acessar até 256 MB de memória de tempo de execução instantânea e gratuita por mês.
   * É possível provisionar uma instância de qualquer serviço no [catálogo do {{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window} que tenha um plano Lite.
   * Depois de 10 dias sem atividade de desenvolvimento, seus apps serão suspensos. Continue trabalhando em seus apps para acordá-los.
   * Depois de 30 dias sem atividade de desenvolvimento, suas instâncias de serviço com planos Lite são excluídas.

## Conta pré-paga
{: #paygo}

Com uma conta Pré-paga, é possível acessar o catálogo integral do {{site.data.keyword.Bluemix_notm}}, incluindo todos os planos grátis, e você obtém o dobro da memória de tempo de execução grátis, com 512 MB por mês. Você paga somente por serviços faturáveis que você usa, sem contratos de longo prazo ou compromissos. Ao fazer upgrade para uma conta Pré-paga, você recebe um [crédito de $200](#upgrade-lite-account) para ajudá-lo a iniciar.

É possível criar vários grupos de recursos para gerenciar facilmente a cota e visualizar o uso de faturamento para um conjunto de recursos. Seus encargos são baseados em seu uso de cálculo e serviços do {{site.data.keyword.Bluemix_notm}}. Se você usar mais do que os abonos de serviço e o tempo de execução grátis, você receberá uma fatura mensal que fornece detalhes sobre os encargos de recurso.

Além disso, com uma conta Pré-paga, é possível solicitar planos de suporte avançado ou premium para obter ajuda extra com as cargas de trabalho de produção. Saiba mais em [Planos de suporte](/docs/get-support?topic=get-support-support-plans).

## Conta Assinatura
{: #subscription-account}

Com uma conta Assinatura, é possível criar múltiplos grupos de recursos para gerenciar facilmente a cota e visualizar o uso de faturamento para um conjunto de recursos. Você confirma uma quantia de gasto mínimo cada mês e recebe um desconto na assinatura que será aplicado a esse encargo mínimo.

Por exemplo, se você se comprometer a gastar US$ 100 por mês por 6 meses, poderá obter um desconto de 10%. Durante o prazo de assinatura, você obterá US$ 600 de uso, mas pagará apenas US$ 540 por ele. Quanto mais longo o prazo de assinatura, melhor será o desconto.

Seu uso é deduzido de sua quantia total de assinatura. Mesmo que seu uso varie de mês a mês, você terá um faturamento previsível e consistente. Se o seu uso exceder o valor total de assinatura, você será cobrado a taxa não descontada pelo excedente.

Assim como com as contas Pré-pagas, sua conta de Assinatura permite que você solicite planos de suporte avançado ou premium para obter ajuda extra se você precisar. Saiba mais em [Planos de suporte](/docs/get-support?topic=get-support-support-plans).

Se você têm uma conta de Assinatura, é possível criar a maioria dos serviços que estão disponíveis no [catálogo do {{site.data.keyword.Bluemix_notm}}](https://{DomainName}/catalog){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo"). No entanto, alguns serviços usam um plano de precificação específico que requer que você o compre separadamente.

### Assinaturas de pacote configurável de serviços
{: #service-subscriptions}

As assinaturas de pacote configurável de serviços fornecem acesso e crédito a um conjunto de serviços dentro de um domínio específico que são destinados a casos de uso populares. É possível escolher entre os pacotes configuráveis de serviços que abrangem os serviços de IA, análise de dados, {{site.data.keyword.blockchainfull_notm}}, Internet of Things (IoT) e nativos da nuvem. Se as suas necessidades passarem por vários domínios, será possível comprar várias assinaturas de pacote configurável de serviços.

É possível incluir pacotes configuráveis de serviços em qualquer tipo de conta existente, incluindo contas Lite. Nos primeiros 90 dias, você estará limitado a usar os serviços dentro do pacote configurável. Após os 90 dias iniciais, será possível acessar o catálogo integral. As assinaturas de pacote configurável de serviços estão sujeitas aos termos da [Descrição do serviço {{site.data.keyword.Bluemix_notm}}](/docs/overview/terms-of-use?topic=overview-terms).

As assinaturas de pacote configurável de serviços não estão disponíveis por meio do console do {{site.data.keyword.Bluemix_notm}}. Para saber mais e comprar um pacote configurável de serviços, entre em contato com a equipe de [Vendas do {{site.data.keyword.Bluemix_notm}}![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}.
{:tip}

Depois de comprar uma assinatura de pacote configurável de serviços, você receberá um e-mail com um código de assinatura que se aplica para incluir o pacote configurável em sua conta. Para obter mais informações sobre como aplicar códigos de recurso, consulte [Gerenciando assinaturas](/docs/billing-usage?topic=billing-usage-subscriptions). Quando seu pacote configurável de serviços expirar ou você usar todo o crédito, será possível continuar a usar qualquer um dos serviços com o uso cobrado na taxa Pré-paga.

## Fazendo upgrade de sua conta
{: #upgrade-lite-account}

Quando você estiver pronto para levar sua conta para o próximo nível, será possível [fazer upgrade de sua conta Lite](/docs/account?topic=account-upgrading-account) para uma conta Pré-paga ou de Assinatura. O upgrade de sua conta desbloqueia o catálogo integral do {{site.data.keyword.Bluemix_notm}}, fornece recursos gratuitos extras e muito mais.

Depois de fazer upgrade de sua conta Lite para uma conta Pré-paga, você obterá um crédito promocional de US$ 200 que será automaticamente aplicado à sua conta. Seu crédito de US$ 200 será válido por 30 dias e seu uso será deduzido automaticamente do valor de crédito. O crédito não pode ser usado com ofertas de terceiros e pode não estar disponível para todas as contas.

Se você já tem uma conta Pré-paga ou de Assinatura, também é possível converter sua conta em um tipo diferente. Para obter mais informações, veja [Fazendo upgrade de sua conta](/docs/account?topic=account-upgrading-account).
