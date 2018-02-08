---



copyright:

  years: 2016, 2018
lastupdated: "2017-10-13"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}} Standard Account Limited Release
{: #betaintro}

O {{site.data.keyword.Bluemix}} Standard Account Limited Release introduz uma nova conta grátis, que oferece uma nova maneira de trabalhar no {{site.data.keyword.Bluemix_notm}} Público. Uma conta Padrão nunca expira, ao contrário de uma avaliação de 30 dias do {{site.data.keyword.Bluemix_notm}}. É possível continuar a trabalhar em seus aplicativos {{site.data.keyword.Bluemix_notm}} sem quaisquer preocupações sobre restrições de tempo. 
{:shortdesc}

Os usuários nas regiões do Reino Unido e do sul dos EUA são elegíveis para uma conta Padrão. Se você não estiver em nenhuma dessas regiões, ainda será possível criar uma conta Padrão pedindo um convite a um amigo ou entrando em contato com nossa equipe de vendas em sales@bluemix.net. Como um proprietário da conta Padrão, é possível convidar amigos e colegas para participar.  

## Introdução à conta {{site.data.keyword.Bluemix_notm}} Standard
{: #standardaccount}

Você pode estar imaginando o que é diferente em uma conta Padrão em comparação com uma conta para teste. As tabelas a seguir resumem os principais detalhes sobre uma conta Padrão do {{site.data.keyword.Bluemix_notm}}. 

|O que há de novo em uma conta Padrão? |    
|-----------------|
| A conta nunca expira. |
| Os aplicativos Cloud Foundry podem acessar até 256 MB de memória de tempo execução instantânea
grátis. |
| É possível acessar planos Lite grátis para serviços Watson em demanda, como Conversation, Internet of Things Platform, Cloudant NoSQLDB. Para obter mais informações, veja [O que está disponível](/docs/pricing/standard_account.html#whatsavailable). |
| Seus aplicativos serão suspensos se não houver atividade de desenvolvimento por 10 dias. |
| Suas instâncias de serviço serão excluídas após 30 dias de inatividade. |
{:caption="Tabela 1. O que há de novo em uma conta Standard" caption-side="top"}

|O que não está mudando quando uma conta para teste é convertida? | 
|-----------------|
|A conta é grátis -- você não precisa de um cartão de crédito. |
|É possível continuar usando suas instâncias do plano Lite. |
|Sua organização, os espaços e as configurações de acesso de membro da equipe associada permanecem
os mesmos. Uma organização pode ser transferida para a sua nova conta. |
|O nível do Suporte {{site.data.keyword.Bluemix_notm}} permanece o mesmo. |
{:caption="Tabela 2. O que não muda" caption-side="top"}

**Nota**: se a sua conta para teste não for convertida, você verá uma mensagem explicando o motivo. É possível que você tenha mais de uma organização em sua conta para teste ou apps existentes que não pode ser transferida. É possível tomar a ação apropriada e, então, tentar
converter a conta novamente.

Quando você possui uma conta Padrão, é possível convidar membros da equipe para colaborar em sua organização e espaços, visualizar seu uso, criar espaços, atualizar seu perfil de conta e gerenciar sua organização.

## Planos Lite
{: #liteplans}
   
Os planos Lite, que também estão disponíveis em uma conta de Pagamento por uso, são estruturados como uma cota grátis. É possível trabalhar em seus projetos sem preocupações, sem o risco de gerar
uma conta acidental. A cota pode operar por um período de tempo específico, por exemplo, por um mês
ou em uma base de uso único. Aqui estão alguns exemplos de cotas do plano Lite:

<ul>
<li>Número máximo de dispositivos registrados.</li>
<li>Número máximo de ligações de aplicativos.</li>
<li>Limite de armazenamento de dados criptografados, por exemplo, 1 GB.</li>
<li>Capacidade de rendimento provisionada.</li>
</ul> 

Em uma conta Padrão, é possível usar qualquer coisa no catálogo do {{site.data.keyword.Bluemix_notm}} que tenha um plano Lite. Os planos Lite são fáceis
de localizar. Por padrão, quando você acessa o catálogo, todos os serviços com um plano Lite são exibidos e identificados com uma tag Lite ![Tag Lite](../icons/Lite.svg). Selecione um serviço para
visualizar os detalhes da cota para o plano Lite associado.

## O que está disponível em uma conta Padrão?
{: #whatsavailable}

Com uma conta Standard, os seus apps do Cloud Foundry podem acessar até um máximo de 256 MB de memória de tempo de execução instantânea. Se você exceder a cota alocada, será possível parar alguns dos apps para liberar a memória de tempo de execução. Também é possível trabalhar com um cluster do Kubernetes com 2 CPU e 4 GB de RAM. 

É possível usar qualquer serviço no catálogo {{site.data.keyword.Bluemix_notm}} que tiver um plano Lite. No entanto, é possível provisionar somente uma instância por plano Lite. Durante o Standard Account Limited Release, os seguintes serviços oferecem um plano Lite:

<ul>
<li>{{site.data.keyword.prf_hublong}}</li>
<li>{{site.data.keyword.mobilepushfull}}</li>
<li>{{site.data.keyword.cloudantfull}}</li>
<li>{{site.data.keyword.conversationfull}}</li>
<li>{{site.data.keyword.iot_full}}</li>
<li>{{site.data.keyword.languagetranslatorfull}}</li>
<li>{{site.data.keyword.personalityinsightsfull}}</li>
<li>{{site.data.keyword.toneanalyzerfull}}</li>
</ul>

Alguns serviços não estão disponíveis em todas as regiões do {{site.data.keyword.Bluemix_notm}}. Para obter mais informações, veja [Serviços por região](/docs/services/services_region.html#services_region).

Mais serviços serão incluídos nesta lista, portanto, fique ligado!

### Limites de cota

Quando os limites de cota forem atingidos, seu aplicativo será interrompido ou seu serviço
será desativado. Se o plano Lite especificar que a cota será fornecida mensalmente, o uso do recurso será
reconfigurado no primeiro dia de cada mês, quando você poderá voltar a trabalhar com o serviço. Quando você estiver se aproximando de um limite de cota ou estiver no limite de cota, você receberá um e-mail de notificação. 

É possível fornecer uma instância por Plano Lite. 

**Nota**: essas limitações se aplicam apenas a uma conta Padrão. A qualquer momento, é possível fazer upgrade para uma conta de Pagamento por uso ou de Assinatura. Você paga
somente pelo que usar, além dos abonos grátis. Para obter mais informações sobre as contas Pagamento por uso e
Assinatura, veja [Tipos de conta](/docs/accounts/account-types.html).

## Recursos de eficiência
{: #devactivity}

Para ajudar a gerenciar seus recursos, incluímos recursos de eficiência que se baseiam na atividade de desenvolvimento e no uso.

### Suspensão automática do app

Seus apps serão suspensos após de 10 dias de inatividade de desenvolvimento. Isso ajudará
quando você desejar trabalhar em um novo app, porque não atingirá o limite de cota de memória
de 256 MB. 

Para acordar seus apps, comece a trabalhar neles novamente na linha de comandos do
Cloud Foundry ou no console do {{site.data.keyword.Bluemix_notm}}. 
 
 Aqui está uma lista de todos os comandos que acordarão seu app:
  * cf push
  * cf restate
  * cf restart
  * cf ssh
  * cf scale
  * cf stop
  * cf start
  * cf create-route
  * cf map-route
  * cf unmap-route
  * cf delete-route
  * cf enable-ssh
  * cf disable-ssh

Para obter detalhes de uso do comando, consulte [Comandos do Cloud Foundry](/docs/cli/reference/cfcommands/index.html).

 **Nota**: se o seu aplicativo já estiver ativado para SSH, não será possível usar os comandos `cf enable-ssh` e `cf disable-sh` para acordar seu aplicativo. 

### Coleta de Lixo

Os serviços de seu plano Lite serão excluídos se não houver nenhuma atividade neles por 30 dias. Isso significa que você não terá que excluir instâncias inativas quando quiser criar uma nova. 
 
## Participando do Standard Account Limited Release
{: #lgainvitation}

É possível pedir um convite a um amigo com uma conta Padrão ou entrar em contato com nossa equipe de vendas em sales@bluemix.net. Adoraríamos que você experimentasse!

Se você receber um convite de um amigo ou de um vendedor do {{site.data.keyword.Bluemix_notm}}, seu convite exclusivo será enviado para o endereço de e-mail fornecido. Ao receber o convite, preencha as instruções no e-mail para se registrar para uma conta Padrão. 
