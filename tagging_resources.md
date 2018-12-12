---

copyright:

  years: 2018
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:notes: .note}


# Tagging resources
{: #tagging-resources}

A tag is a label that you assign to a resource, and they are useful because it creates a simple way for you to filter through similar resources in your resource list. This means that tags are used organize your resources and easily find them later. To see a full list of tags on your account, go to **Manage > Account**, and select **Tags**. 
{: shortdesc}


## Tagging permissions
{: #tagging-permissions}

Anyone on the account can see the tags on resources and they can use the tags to organize resources in the account. But to attach or remove a tag from a resource, you must have a role on that resource.  To learn more, click [IAM-managed resource](/docs/account/tagging_IAM-managed.html#tagging-IAM), [Resources managed by Cloud Foundry](/docs/account/tagging_cloud-foundry.html#tagging-CF), and [Classic infrastructure resources](/docs/account/tagging_classic-infra.html#tagging-classic-infra). 


## Adding and removing tags on a resource
{: #add-tags}

1. Click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) > **Resource list** to view your list of resources. Find the resource that you want to tag.
2. If your resource doesn't have a tag, click the actions menu ![action menu icon](../icons/action-menu-icon.svg) for the row of the resource > **Add tag**. If you have a tag on a resource and you want to add more, in the Tag column, click the Edit icon ![Edit icon](../icons/edit-tagging.svg) next to the displayed tag. 
3. Type a name for the tag, and press Enter after each tag if you're adding more than one.
4. To remove a tag from the resource, click the `Remove` icon ![Remove icon](../icons/close-tagging.svg) next to the tag. 
5. Save your changes. 

### Tagging rules and limits
{: #limits}

The maximum size of label style tag is 128 characters. The permitted characters are A-Z, 0-9, white space, underscore, hyphen, period, and colon, and tags  are case-insensitive. . Colons turn the tag into a `key:value` pair. You can't use a colon in a tag without creating a `key:value` pair. A comma separates tags, so commas can't be used within the tag name itself.

Some resource types can't be tagged:

- {{site.data.keyword.openwhisk_short}}
- {{site.data.keyword.containershort}}


## Granting access
{: #access}

As the account owner, you might want to delegate some of the responsibility of tagging resources. To do that, you can grant access to other users on the account to add and remove tags from resources. For users on account to add tags to a resource, they be assigned the appropriate access. Access to services that belong to a resource group are managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) access policies, and access to services that belong to a Cloud Foundry org and space are managed by Cloud Foundry org and space roles. For more information, see [IAM-managed resource](/docs/account/tagging_IAM-managed.html#tagging), [Resources managed by Cloud Foundry](/docs/account/tagging_cloud-foundry.html#tagging), and [Classic infrastructure resources](/docs/account/tagging_classic-infra.html#tagging). 


## Tagging for resellers
{: #resell}

If your account is associated with different organizations, any tags they create are visible to other users on your account. For example, if you're a reseller you might have customers who are unrelated working in the same account.

To control tag visibility, circulate tagging guidelines and let users know that tags are visible account-wide. 

Use codes rather than names for clients and accounts and avoid placing sensitive information in tags.
{: tip}


## Searching for tags
{: #search-tags}

You can search for tags using different methods:

- {{site.data.keyword.Bluemix_notm}} search bar that is located in the header
- You can filter your resource list by the tag you are searching for
- On the application detail page, you can locate the tags that are associated with that resource 

The same tag can be attached to multiple resources by different users in the same billing account, and not all users have visibility on all resources on the account.
{: note}

<!-- ### Operators supported by search API
{: #search_operators_search}

The search API supports Lucene query syntax. The query parameters are specified in the body of the request with the query attribute.

For example:

To search all resources named ABC use:

    `"query": “name:ABC”`

To search all cloud foundry resources named ABC use:

    `"query": “family:cloud_foundry AND name:ABC”`

To search all cloud foundry resources that are deployed in either `us-south` or `eu-gb` use:

    `“query": "(region:us-south OR region:eu-gb) AND family:cloud_foundry”`

To search all cloud foundry applications named "My app" in region us-south and not in scope s/b7a27f50-d350-4150-b001-8ca9155fc405 use:

    `“query": “region:(us-south) AND name:\"My app\"” AND type:cf-application AND NOT scope:\"s/b7a27f50-d350-4150-b001-8ca9155fc405\””` -->

<!-- ### Sorting results
{: #sorting_results}

You can apply sorting to lots of properties with a comma-separated string. To sort in ascending or descending order, use the following characters as prefix to the property name:

    `+` or unspecified: Ascending order (smallest index first)
    `-` : Descending order (largest index first)

### Wildcards
{: #wildcards}

The following wildcards can be used in search values:

    `*` : matches any character sequence (including the empty one)
    `?` : matches any single character

To avoid a slow query, don't put the wildcard term at the beginning of a search value.
{: tip} -->
