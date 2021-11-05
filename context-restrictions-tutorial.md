---

copyright:
  years: 2021
lastupdated: "2021-11-05"

keywords: network-level access, network security strategy

subcollection: account
content-type: tutorial
account-plan: lite 
completion-time: 20m

---

{:shortdesc: .shortdesc}
{:screen: .screen}  
{:codeblock: .codeblock}  
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'}
{:video: .video}


# Leveraging context-based restrictions to secure your resources
{: #context-restrictions-tutorial}
{: toc-content-type="tutorial"}
{: toc-completion-time="20m"}

This tutorial walks you through how to use context-based restrictions as an extra layer of protection to your resources. By completing this tutorial, you learn how to create network zones and rules that define access restrictions to specific resources based on context in addition to IAM identity.
{: shortdesc}

The tutorial uses a fictitious account owner named Xander. Xander has already set-up access for managers that need the `administrator` role on account management services by using IAM policies. 

Xander trusts his team to manage their personal and service credentials properly, but he wants to make sure they are protected even if credentials are mismanaged. Because Xander knows the IP addresses that the team uses, Xander can restrict access to the policy management service based on the network location of the access requests. This way, policy creation is restricted to the IP addresses he defines. Since both IAM access and context-based restrictions must allow access, context-based restrictions offer protection even in the face of compromised or mismanaged credentials.

## Create a network zone
{: #tutorial-networkzone-new}
{: step}

First, create a new network zone for the team. 

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Context-based restrictions**
2. Go to **Network zones** and then click **Create**. 
3. Name the network zone `management-team-zone`
4. Enter the IP addresses the team must use:
    1. Team members in Austin use the following IP addresses: 4.4.4.1-4.4.4.99
    1. An Austin team member in another building uses the following subnet: 204.17.5.0/24
    1. A remote team member uses the following IP address: 3.3.3.56
5. Click **Next**.
6. Review the details of the network zone.
7. Click **Create**.


## Create a rule
{: #tutorial-context-rules}
{: step}

Now, Xander can use the network zone that he created in a rule. 

1. Go to **Rules** and click **Create**. 
2. Name the rule `Management team context` and click **Continue**. 
3. To restrict access to the creation of IAM access management policies, select **Account management** and then select **IAM AM Policy**. 
4. Click **Continue**.
5. Xander has specified public endpoints in his network zone, so he keeps the endpoint type toggle switch set to **Yes**, which allows requests from any endpoint type. 
6. Select the network zone `management-team-zone`.
7. Click **Add** to include your context configuration in the rule.
8. Then, click **Create**.

Xander is now restricting policy management requests to the IP addresses and endpoint type his management team uses. Since the management team has the right access policies, and they use allowed IP addresses, they are authenticated to execute policy management operations. All policy management requests that come from IP addresses and endpoint types that do not match the conext Xander defined are denied.

## Next steps
{: #tutorial-context-step-next}

 You can also use network zones to restrict access at the account level. For more information, see [Allowing specific IP addresses](/docs/account?topic=account-ips&interface=ui).
