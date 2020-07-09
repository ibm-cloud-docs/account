---

copyright:

  years: 2018, 2020
lastupdated: "2020-06-05"

keywords: add tags, tags, full list of tags, how to use tags

subcollection: account

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Working with tags
{: #tag}

Use tags to organize your resources and track usage costs. You can tag related resources and view them throughout your account by filtering by tags from your resource list.  
{: shortdesc}

To see a full list of tags in your account, go to **Manage > Account** in the {{site.data.keyword.cloud}} console, and select **Tags**.

## Tagging rules
{: #limits}

Tags are not case-sensitive, and the maximum length of a tag is 128 characters. The permitted characters are A-Z, 0-9, spaces, underscore, hyphen, period, and colon. The use of a colon formats the tag into a string that isolates two logical parts, like a `key:value` pair. A comma separates multiple tags and can't be used within the tag name itself.

### Sample tags and syntax
{: #sample-and-syntax}

You can use tags to help you organize and manage your resources. Consider writing tags as `key:value` pairs to help organize your development environments, projects, compliance, and optimization throughout your organization. See the following table for some examples of tags that you might want to use.

| Tag | Description |
|----------|---------|
| `env:dev`, `env:test`, `env:stage`, `env:prod` | Use to identify your development environment|
| `project:lw-wizard`, `app:poc-app` | Use to identify a project |
| `dataresidency:germany`, `compliance:hipaa`, `compliance:pii` | Use to define compliance requirements |
| `schedule:24x7`, `maxruntime:12days` | Use to help you automate optimization |
{:caption="Table 1. Tag syntax" caption-side="top"}

## Adding and removing tags on a resource
{: #add-remove}

1. From the {{site.data.keyword.Bluemix_notm}} console, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) > **Resource list** to view your list of resources.
2. Expand the resource type twistie that contains the resource you want to tag. For example, if you want to tag an instance of {{site.data.keyword.cos_full_notm}}, expand **Storage**.  
3. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg) to add or update a tag for the resource.

    * To add a tag, click the **Actions** menu ![Actions icon](../icons/action-menu-icon.svg), select **Add Tags**, and type a name for your tag.
    * To add more tags, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg) next to the displayed tag, and type a name for your tag. Press Enter to continue adding tags.
4. To remove a tag, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg). Then, click the **Remove** icon ![Remove icon](../icons/close-tagging.svg) next to the tag.


## Searching for tags
{: #search-tags}

You can search for tags by using any of the following methods:

  * Try the search bar that is located in the {{site.data.keyword.Bluemix_notm}} console menu bar.
  * You can filter your resource list by the tag you are searching for.
  * From the application detail page, you can locate the tags that are associated with that resource.

The same tag can be attached to multiple resources by different users in the same billing account, and not all users have visibility on all resources on the account.
{: note}


## Tagging for resellers
{: #resell}

Tags are visible to all members of an account. If your account is associated with different organizations, if you're a reseller for example, you might want to recommend your customers not to store information in tags that might disclose sensitive information to others in the same account.

To control tag visibility, circulate tagging guidelines and let users know that tags are visible account-wide.

Use codes rather than names for clients and accounts and avoid placing sensitive information in tags.
{: tip}
