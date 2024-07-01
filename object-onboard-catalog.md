---

copyright:
  years: 2021, 2022
lastupdated: "2022-12-06"

subcollection: account

keywords: objects, private catalog, onboarding, vpe objects, vpe

---

{{site.data.keyword.attribute-definition-list}}


# Create Virtual Private Endpoints for your private catalog
{: #object-onboard-catalog}

To create a Virtual Private Endpoint (VPE), you first need to create a private catalog to centrally manage access to your VPEs. VPEs are created by using a JSON object, which represents any publishable entity on your account that isn't a product.
{: shortdesc}

For information about creating a private catalog, see [Creating a private catalog for your objects](/docs/account?topic=account-restrict-by-user-object&interface=ui#catalog-all-object).

## Before you begin
{: #onboard-object-prereq}

1. Make sure you're assigned the Editor role on the catalog management service to create a private catalog and add an object.
1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.


## Creating your VPE
{: #create-object-ui}
{: ui}

To create and add a VPE to your private catalog, use the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, select **Private catalogs**.
1. Select the private catalog where you want to add your VPE.
   You can only add VPEs to Virtual Private Endpoint catalogs. You can't add VPEs to a product catalog or a preset configuration catalog.
   {: note}

1. To add a VPE to your private catalog, click **Add**.
1. Enter your endpoint's Display name and unique Programmatic name. Choose a Parent region and click **Add**.

Make sure that this VPE is visible to the service ID that you plan to use during your service registration. For more information see, [Onboard your Service ID](/docs/get-coding?topic=get-coding-vpe-onboarding-platform#service-ID-onboarding).
{: note}

## Creating your VPE by using the CLI
{: #create-object-cli}
{: cli}

To create and add a VPE to your private catalog, use the following steps:

1. Create a new filter.
   ```bash
   ibmcloud catalog object create vpe [--catalog CATALOG] [--crn CRN] [--endpoint-type TYPE] [--fqdn FQDN] [--name NAME] [--region REGION]
   ```
   {: codeblock}

   If you have multiple values for the `fqdn` flag, you can list the values separated by a comma. For example, `--fdqn "example.com, example2.com"`.

For more information about this command, enter:
```bash
ibmcloud catalog object help create vpe
```
{: codeblock}

## Next steps
{: #next-steps-object}

After you added a VPE object to your private catalog, you need to [validate your object's data format](/docs/get-coding?topic=get-coding-vpe-onboarding-platform#validate-vpe-object).
