---

copyright:
  years: 2021
lastupdated: "2021-08-09"

keywords: catalog, private catalogs, visibility, filter catalog, config rules, security, compliance, catalog filtering, restrict

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}

# Governing what software users can install based on provider  
{: #catalog-scc-rules}

As the account owner or administrator, you can use the {{site.data.keyword.compliance_full}} to create config rules to govern what software users can install based on whether it's provided by IBM, third parties, or an open source community. 
{: shortdesc}

After you create a rule, you can monitor for configuration changes by attaching the rule to a scope, such as an account group, specific accounts, or an entire enterprise. You can further investigate noncompliant resources by reviewing your evaluation results. 

## Creating configuration rules
{: #catalog-rule-cfg}

1. Rule details: name and description
1. Target:

   * Service: Catalog Management
   * Resource kind: account-settings
1. Definition: Use the JSON editor to set configuration properties for the rule. Example: Install only IBM software, boolean, true
1. Enforcement: On

## Attaching config rules to scopes
{: #catalog-attach-scope}

## Viewing your config rules
{: #catalog-rule-view}


 



