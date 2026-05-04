---

copyright:

  years: 2015, 2026
lastupdated: "2026-05-04"

keywords: payment method, credit card, payment, billing method, pay, pay my bill, billing items, ibm billing,

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Managing payments
{: #linkedusage}

Depending on your account type, you can easily manage your payment methods by using the [Payments](/billing/payments) page in the {{site.data.keyword.cloud}} console or by going to [{{site.data.keyword.IBM}} Billing](https://myibm.ibm.com/billing/).
{: shortdesc}

A valid credit card is required for all Pay-As-You-Go and Subscription accounts. Every month, the credit card is charged with the usage amount that is accumulated during that month. When updates to your payment details and billing address details are approved, they are applied to your account within few days. The contact that is specified in the billing address section receives an email confirming that the updates are applied.

If your account was initially set up with a purchase order (PO) or firm order letter (FOL) that includes a payment method, you can switch to credit card payment. When you change your payment method to credit card, all charges in your account, including subscriptions, support, and usage, are billed to the credit card.
{: note}

You can contact {{site.data.keyword.cloud_notm}} Support to get help with payment-related issues. From the console menu bar, click the **Help** icon ![Help icon](../icons/help.svg "Help") > **Support center**, and then click **Create a case** to get in touch.
{: tip}

## Before you begin
{: #prereqs-payments}

To manage payments, you need to be assigned the operator role or higher on the billing account management service. See [Assigning access to account management services](/docs/iam?topic=iam-account-services) for more information.

## Managing payment methods for new US-based Pay-As-You-Go accounts with credit card billing
{: #manage-paygo-us-account}

If you're a new Pay-As-You-Go account owner that is located in the US and you are paying with a credit card, can you add multiple cards to the account, replace your default card with a saved one, or edit the details of a card. You manage your credit card from the [Payments](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console.

Complete the following steps to add a new payment method to the account:

1. Click **Add payment method**.
2. Enter the card details, and click **Save**. Updates to your card details are reflected immediately.

You can’t enter a PO Box as the billing address.
{: important}

When you add a new credit card, it becomes the default credit card. Recurring payments are charged to the default payment method.

Complete the following steps to edit your active payment method:

1. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Edit** menu.
1. To edit the billing address, click **Edit** and update the billing address.
1. To edit the card details, click **Edit** and update the card number or expiration date.

You can only have one address that's associated with your payment methods. All credit cards in the account will be updated to the same address.
{: note}

Complete the following steps to set a new default payment method:

1. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Set as default**.
2. Confirm that you want to make this payment method the default. The default payment method is charged for recurring payments

## Managing payment methods for all other accounts
{: #manage-other-account}

The steps to update your credit card apply to the following types of accounts:

* New and existing Pay-As-You-Go accounts based in the US with any payment method other than a credit card
* New and existing Pay-As-You-Go accounts not based in the US
* New and existing Subscription accounts worldwide
* Existing Pay-As-You-Go and Enterprise Savings Plan accounts created through {{site.data.keyword.IBM_notm}} sellers

1. Go to the [Payments](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console.
2. In the Add Payment Method section, enter the billing information for your new card, and click **Add credit card**.

Updating a credit card with the billing address details requires a manual review that might take a few days. To view your open change request cases, go to the [{{site.data.keyword.cloud_notm}} Support Center](/unifiedsupport/supportcenter){: external}.

If you are switching the payment method for purchase order or firm order letter to credit card payment, the verification process can take up to 30 minutes while your account information is validated, provided that there are no billing address issues.

American Express can't be used as a payment method for India, Singapore, and South Africa based accounts that are billed in US dollars.
{: note}


###  India-based customers with accounts that are billed in US Dollars
{: #rupees-billing}

Due to current banking regulations, recurring credit card transactions might be unsuccessful for India-based customers with accounts that are billed in US Dollars. You can use one of the following methods to make a payment:
 * [Make a one-time payment](/docs/account?topic=account-linkedusage#makepayment)
 * Request to migrate your account to be billed in India Rupees. To make a request, provide a credit card that is billed in India Rupees on the [Payment Method](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console. Specify that India Rupees are in the **Payment Currency** section. Additional information might be requested through a Support case during the migration process.

### Making a one-time payment
{: #makepayment}

You can use a credit card to make a one-time payment at any time for any amount, whether it's for the full balance or a partial sum. The details that you enter for the one-time payment aren't recorded for future use, and aren't populated with a default amount.

To make a one-time payment, in the {{site.data.keyword.cloud_notm}} console, go to **Manage > Billing and usage**, and select **Payments**. Click **Manual Payment** and complete the fields in the one-time payment section. One-time payments are reviewed and processed each day. The account balance is updated after the payment is accepted. If a late fee is assessed and you have submitted a one-time payment, contact the [{{site.data.keyword.cloud_notm}} Support Center](https://cloud.ibm.com/unifiedsupport/supportcenter){: external}.

## Managing payment methods for purchase orders
{: #manage-po-billing}

If you set up your Enterprise Savings Plan or Pay-As-You-Go account through an {{site.data.keyword.IBM_notm}} seller with a purchase order and firm order letter that includes a payment method, you can manage your payment method using credit card in the {{site.data.keyword.cloud_notm}} console.

### Adding a credit card
{: #add-cc-po}

If your account was initially set up with a purchase order and firm order letter, you can add credit card as your payment method. When you add a credit card, it becomes the payment method for all charges in your account, including subscriptions, support entitlements, and usage.

Before you add a credit card, ensure that you understand the following:

* All entitlements in your account, including subscriptions, support, and additional services, are charged to the credit card.
* You will receive email notifications if there are any issues with your credit card.
* Your billing address must match the address on file with your credit card issuer.

To add a credit card to your account, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Billing and usage**.
2. Click **Payments** in the navigation pane, and then click **Add payment method**.
3. In the **Add payment method** section, enter your billing address and credit card information.
4. Click **Continue**. After the details are updated, click **Submit**.
5. The credit card verification process can take up to 30 minutes while your account information is validated. Wait for the verification process to complete. You might need to log out and log back in to see the changes. 

After your credit card is verified and added to your account, all future charges are automatically billed to this card. From the **Payments** page, you can update the card number or billing address, add more credit cards, change the default card for payments, or delete cards that you no longer need.   

The payment method change applies to all entitlements in your account. You cannot have different payment methods for different services or entitlements within the same account.
{: note}

## Managing your payment method outside of the console
{: #payment-method-ibm}

You might manage your payment method on a separate billing platform. You can easily register, update, or delete a payment method by going to [IBM Billing](https://myibm.ibm.com/billing/) and log in with your IBMid and password. You are also required to enter the temporary passcode that's emailed to you.

To add a payment method, complete the following steps:
1. Go to [ibm.com](http://www.ibm.com){: external} and log in with the same IBMid and password that you use to log in to {{site.data.keyword.cloud_notm}}.
1. Click the **Avatar** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar"), and select **Billing**.
1. Click **Manage payment method**.
1. Enter your payment information, and click **Register**. A temporary passcode is emailed to you after the registration process is complete.

After you register a payment method, when you click **Manage payment method**, you can view the Manage my wallet page to update or delete your payment methods by clicking the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
{: tip}
