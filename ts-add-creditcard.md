---

copyright:

  years: 2026
lastupdated: "2026-05-04"

keywords: troubleshoot billing, credit card, payment method, credit card verification, purchase order to credit card

subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I add a credit card to my account?
{: #ts-add-cc}
{: troubleshoot}

You're trying to add a credit card to your account, but the option is not available or you receive an error.
{: shortdesc}

When you try to add a credit card on the [Payments](/billing/payments) page, you either don't see the option or you receive an error message when you try to save your credit card information.
{: tsSymptoms}

This issue can occur for several reasons:
{: tsCauses}

* Your account might not have the required permissions to manage payment methods.
* The billing address you entered doesn't match the address on file with your credit card issuer.
* Your credit card information contains errors or is incomplete.
* Your account is managed through a separate billing platform.

To resolve this issue, try the following steps:
{: tsResolve}

1. Verify that you have the Operator role or higher on the Billing account management service. See [Assigning access to account management services](/docs/iam?topic=iam-account-services) for more information.

2. Ensure that the billing address you enter exactly matches the address on file with your credit card issuer, including:
   * Street address
   * City
   * State or province
   * Postal code
   * Country

3. Verify that all required credit card fields are completed:
   * Card number
   * Expiration date
   * Security code (CVV)
   * Cardholder name

4. Check if your payments are managed outside of the console. If you see a message indicating that your payments are managed through {{site.data.keyword.IBM_notm}} Billing, go to [{{site.data.keyword.IBM_notm}} Billing](https://myibm.ibm.com/billing/){: external} to add your credit card.

5. If you continue to experience issues, contact {{site.data.keyword.cloud_notm}} Support by calling 1-866-325-0045 and selecting the third option, or create a case from the [Support Center](/unifiedsupport/supportcenter){: external}.
