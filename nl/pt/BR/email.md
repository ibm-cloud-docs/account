---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-28"

keywords: notifications, email notifications, IBM Cloud notifications, notification preferences

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# Configurando preferências de e-mail
{: #email-prefs}

Dependendo do seu tipo de conta do {{site.data.keyword.Bluemix}}, é possível escolher se deseja receber notificações por e-mail sobre eventos não planejados e eventos planejados da plataforma {{site.data.keyword.Bluemix}} ou notificações por e-mail de infraestrutura sobre eventos não planejados, manutenção e anúncios. Também é possível escolher configurar assinaturas de notificação para eventos de infraestrutura clássica.
{: shortdesc}

## Configurando notificações de plataforma
{: #setting-platform-notifications}

Se você for um proprietário da conta Lite, será possível escolher se deseja receber notificações por e-mail sobre eventos não planejados da plataforma {{site.data.keyword.Bluemix}}, como indisponibilidades e eventos planejados, como manutenção. Ao configurar notificações da plataforma do {{site.data.keyword.Bluemix_notm}}, você recebe notificações por e-mail que estão associadas somente à plataforma {{site.data.keyword.Bluemix_notm}}. Você não recebe notificações por e-mail sobre eventos que estão associados a serviços do {{site.data.keyword.Bluemix_notm}}.

É possível configurar notificações por e-mail da plataforma somente para seu perfil, não para a conta. Ou seja, se você alternar para outra conta, quaisquer atualizações de notificação da plataforma que você fizer terão o escopo definido para seu perfil e não para a conta para a qual alternou.

Ao selecionar para receber eventos de plataforma não planejados, você obtém e-mails somente sobre problemas que podem causar uma indisponibilidade (Sev. 1). A qualquer momento, é possível ver todos os eventos planejados e não planejados por meio da página [Status ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/status){: new_window}.

1. Acesse o ícone Avatar ![Ícone Avatar](../icons/i-avatar-icon.svg) &gt; **Perfil e configurações**.
2. Clique em **Notificações**.
3. Selecione se deseja receber notificações da plataforma para cada uma das categorias que você deseja atualizar.

  Por padrão, todas as notificações da plataforma {{site.data.keyword.Bluemix_notm}} estão desativadas.
  {: tip}

4. Clique em **Salvar**.

## Configurando notificações de infraestrutura

Se você for um proprietário da conta Pré-paga ou de Assinatura, será possível escolher se deseja receber notificações por e-mail de infraestrutura do {{site.data.keyword.Bluemix_notm}} sobre eventos não planejados, manutenção e anúncios. As notificações de infraestrutura têm o escopo definido para a conta para a qual você alternou. É possível alternar para outra conta e gerenciar notificações para essa conta.

1. Acesse o ícone Avatar ![Ícone Avatar](../icons/i-avatar-icon.svg) &gt; **Perfil e configurações**.
2. Clique em **Notificações**.
3. Selecione se deseja receber notificações de infraestrutura para cada uma das categorias que você deseja atualizar.

  Por padrão, todas as notificações de infraestrutura do {{site.data.keyword.Bluemix_notm}} estão ativadas.
  {: tip}

4. Clique em **Salvar**.

## Configurando notificações do usuário
{: #setting-user-notifications}

A configuração de notificações do usuário está disponível somente para recursos de infraestrutura clássica. Se você for um proprietário da conta, será possível configurar assinaturas de notificação para usuários em sua conta. As assinaturas são para um conjunto específico de serviços do desenvolvedor, como o {{site.data.keyword.autoscaling}} e o Raid Alert Monitoring. Quando o usuário está inscrito em um serviço, ele recebe e-mail sobre esse serviço.  

Os usuários em sua conta recebem notificações para os tipos de eventos operacionais importantes a seguir:

  * Problemas ou indisponibilidades de infraestrutura não planejados: problemas que podem causar uma indisponibilidade com base em determinadas condições para clientes específicos.
  * Serviço planejado ou manutenção planejada: manutenção que é necessária para manter a infraestrutura em operação no status ideal.
  * Vulnerabilidades de segurança: a área afetada é isolada. Uma correção é criada para fechar a vulnerabilidade e os testes são executados na correção para assegurar que nenhuma função indireta seja afetada.
  * Casos de suporte abertos: alerta os usuários de casos que são abertos em sua conta.

A sincronização da notificação varia dependendo se o evento é planejado ou não planejado. A política de infraestrutura do {{site.data.keyword.BluSoftlayer_notm}} é solucionar problemas o mais rápido possível para remover ou minimizar o risco de problemas adicionais que possam ter um impacto maior. Às vezes, mesmo a manutenção planejada é executada com somente uma notificação avançada.

Para configurar notificações de assinatura para seus usuários, conclua as etapas a seguir:

  1. Acesse **Gerenciar > Conta** e selecione **Notificações**.
  2. Selecione um serviço na tabela.
  3. Na coluna Inscrito, selecione **Sim** para o usuário que deseja receber notificações.

    Para localizar facilmente o usuário que você está procurando, clique em **Filtrar** e filtre por nome, sobrenome ou nome do usuário.
    {: tip}
