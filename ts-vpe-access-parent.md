---

copyright:

  years: 2020, 2025
lastupdated: "2025-07-07"

keywords: troubleshoot lose access parent, access parent region, vpe object

subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}


# Why did I lose access to my public VPE object?
{: #troubleshoot-vpe-access-parent}
{: troubleshoot}

When you create a VPE object, you are the owner of that object. During the object creation, you attach it to a parent region. If you lose access to that parent region, you lose the access to use the endpoint, but you don't lose the access to customize the endpoint.



You lost access to your parent region and now you don't have access to your public VPE object, but you have access to the private VPE object version in the private catalog. 
{: tsSymptoms}
   
The most likely reasons that you might lose access to a parent region is because the region got deleted or the admin of the region removed you from the allowlist. 
{: tsCauses}

There are a couple of different scenarios for fixing this issue. You can contact the admin of the region and try to reinstate your access or you can change the parent to a different region. 

If you didn't share your VPE object with any accounts, you can change the parent. If you shared your object with other accounts and you lost access and the region wasn't deleted, the shared accounts on the object still have access to the endpoint. If this is true, then you can't change the parent region on your object.  

To update the parent region, use the following steps:
1. Go to **Manage** > **Catalogs** > **Private catalogs** in the {{site.data.keyword.cloud_notm}} console, and select **Objects**
1. Select your object from the table. 
1. Click the **Edit** icon ![Edit icon](../icons/icon_write.svg "Edit") from the Details section and update your parent. 
{: tsResolve}
