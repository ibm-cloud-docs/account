---

copyright:

  years: 2023, 2025
lastupdated: "2025-01-28"

keywords: apptio, cost benefit analysis

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Understanding the usage report
{: #understand-reports}

The following tables shows the correlation between the heading titles in your usage CSV report and JSON report fields as well the version of the CSV.

## Understanding your account summary report
{: #export-csv-api-table-account-summary-csv}

The following table shows the correlation between the heading titles in your CSV report and JSON report fields as well the version of the CSV. For more information about JSON report fields, see [Usage Reports: Get account summary](/apidocs/metering-reporting#get-account-summary){: external}. Each row of the **Account Resource Usage** section represents the aggregated usage of a service plan metric for all the resource instances in the account.

You can view other versions of the CSV if you have earlier account summary reports in your account. The CSV version depends on the date that the data is published. The following are the available versions:

- July 2024 to present is [version 1.2](#account-summary-csv-version-1-2)
- March 2024 to June 2024 is [version 1.1](#account-summary-csv-version-1-1)
- October 2023 to March 2024 is [version 1.0](#account-summary-csv-version-1-0)
- February 2023 to October 2023 is [version 0.2](#account-summary-csv-version-0-2)
- Before February 2023 is [version 0.1](#account-summary-csv-version-0-1).

### Account summary CSV version 1.2
{: #account-summary-csv-version-1-2}

The following table is version 1.2 and the most recent CSV version. You get this version if the data that you're viewing is from July 2024 to present.

| CSV Header          | Description                                        |
|---------------------|-------------------------------------------------|
| Account Owner ID    | ID of the account                               |
| Account Name        | Name of the account                             |
| Billing Month       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Currency Rate       | Currency Exchange Rate with USD as the base     |
| Created Time        | Timestamp at which the CSV report was generated |
| Version             | The version number of the account summary CSV   |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-summary-1-2"}
{: #account-owner-id-1-2}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|-------------------------------|-------------|
| Account ID          | `account_id`                  | ID of the account |
| Month               | `month`                       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Country Code        | `billing_country_code`        | Country the requested account is mapped to |
| Currency Code       | `billing_currency_code`       | The currency in which the account is billed |
| Billable Cost       | `resources.billable_cost`     | The billable charges for all cloud resources used in the account |
| Non Billable Cost  | `resources.non_billable_cost` | Non-billable charges for all cloud resources used in the account |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for account usage summary" caption-side="bottom"}
{: tab-group="account-summary-1-2"}
{: #account-id-1-2}
{: tab-title="Account Usage Summary"}

| CSV Header       | JSON Report Fields                                          | Description |
|---------------------|-------------------------------------------------------------|-------------|
| Subscription ID | `subscription.subscriptions.subscription_id`                | The ID of the subscription |
| CA                  | `subscription.subscriptions.charge_agreement_number`        | The charge agreement number of the subscription |
| Type                | `subscription.subscriptions.type`                           | Type of subscription |
| Subscription Amount | `subscription.subscriptions.subscription_amount`            | The credits available in the subscription for the month |
| Start               | `subscription.subscriptions.start` or \n `subscription.subscriptions.terms.start`| Pay-As-You-Go accounts: the date from which the subscription was active \n Subscription accounts: The start date of the term |
| End                 | `subscription.subscriptions.end` or \n `subscription.subscriptions.terms.end`           | Pay-As-You-Go accounts: unavailable \n Subscription accounts: The end date of the term |
| Credits Total       | `subscription.subscriptions.credits_total` or \n `subscription.subscriptions.terms.credits.total`             | Pay-As-You-Go accounts: The total credits available in the  subscription \n Subscription accounts: The total credits available for the term  |
| Credits Starting    | `subscription.subscriptions.terms.credits.starting_balance` | The unused credits in the term at the beginning of the month |
| Credits Used        | `subscription.subscriptions.terms.credits.used`             | The credits used in this month |
| Credits Balance     | `subscription.subscriptions.terms.credits.balance`          | The remaining credits in this term |
| True Up             | `subscription.subscriptions.terms.credits.true_up`          | The credits remaining after the end of the term |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for subscriptions" caption-side="bottom"}
{: tab-group="account-summary-1-2"}
{: #subscription-id-1-2}
{: tab-title="Subscriptions"}

| CSV Header       | JSON Report Fields                     | Description |
|---------------------|-----------------------------------|-------------|
| Offer ID            | `offers.offer_id`                 | The ID of the offer |
| Credits Total       | `offers.credits_total`            | The total credits before applying the offer |
| Offer Template      | `offers.offer_template`           | The template with which the offer was generated |
| Valid From          | `offers.valid_from`               | The date from which the offer is valid |
| Expire Date         | `offers.expires_on`               | The date until the offer is valid |
| Recurring           | `offers.is_recurring`             | Indicates if a cost is recurring |
| Starting Balance    | `offers.credits.starting_balance` | The available credits in the offer at the beginning of the month |
| Used                | `offers.credits.used`             | The credits used in this month |
| Balance             | `offers.credits.balance`          | The remaining credits in the offer |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for offers" caption-side="bottom"}
{: tab-group="account-summary-1-2"}
{: #offer-id-1-2}
{: tab-title="Offers"}

| CSV Header       | JSON Report Fields | Description |
|---------------------|--------------------|-------------|
| Support Cost        | `support.cost`     | The monthly support cost |
| Support Type        | `support.type` \n (`STANDARD` > `Advanced` and \n `PREMIUM` > `Premium`) | The type of support  |
| Support Overage     | `support.overage`  | Additional support cost for the month |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for support summary" caption-side="bottom"}
{: tab-group="account-summary-1-2"}
{: #support-cost-1-2}
{: tab-title="Support Summary"}

| CSV Header  | JSON Report Fields                 | Description |
|----------------|------------------------------------|-------------|
| Service Name   | `resources.resource_name`          | The name of the resource |
| Service ID     | `resources.resource_id`            | The ID of the resource |
| Currency       | `currency_code`                    | The currency for the cost fields in the resources, plans, and metrics |
| Billable       | `resources.billable`               | Indicates if the plan charges are billed to the customer |
| Plan Name      | `resources.plan_name`              | Name of the service plan |
| Plan ID        | `resources.plan_id`                | ID of the service plan |
| Pricing Region | `reports.resources.plans.pricing_region` | Pricing region for the plan |
| Metric         | `resources.usage.metric`           | The ID of the metric |
| Unit           | `resources.usage.unit`             | The unit that qualifies the quantity |
| Quantity       | `resources.usage.quantity`         | The aggregated value for the metric |
| Cost           | `resources.usage.cost`             | The cost incurred by the metric |
| Original Cost  | `resources.usage.rated_cost`       | Pre-discounted cost incurred by the metric |
| Pending        | `resources.pending`            | Pending charge from classic infrastructure |
| Discount (%)   | `resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID    | `resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
| Non Chargeable  | `resources.plans.usage.non_chargeable` |  When set to `true`, the cost is for informational purpose and is not included while calculating the plan charges. |
| Classic Infrastructure Product ID | `resources.plans.usage.additional_properties.classic_infrastructure_product_id`| Product ID of classic infrastructure resource |
| Classic Infrastructure Package ID | `resources.plans.usage.additional_properties.classic_infrastructure_package_id` | Package ID of classic infrastructure resource |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for account resource usage" caption-side="bottom"}
{: tab-group="account-summary-1-2"}
{: #service-name-1-2}
{: tab-title="Account Resource Usage"}


### Account summary CSV version 1.1
{: #account-summary-csv-version-1-1}

You will get CSV version 1.1 if the data that you're viewing is from March 2024 to June 2024.

| CSV Header          | Description                                        |
|---------------------|-------------------------------------------------|
| Account Owner ID    | ID of the account                               |
| Account Name        | Name of the account                             |
| Billing Month       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Currency Rate       | Currency Exchange Rate with USD as the base     |
| Created Time        | Timestamp at which the CSV report was generated |
| Version             | The version number of the account summary CSV   |
{: class="simple-tab-table"}
{: caption="Table 2. Account summary CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-summary-1-1"}
{: #account-owner-id-1-1}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|-------------------------------|-------------|
| Account ID          | `account_id`                  | ID of the account |
| Month               | `month`                       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Country Code        | `billing_country_code`        | Country the requested account is mapped to |
| Currency Code       | `billing_currency_code`       | The currency in which the account is billed |
| Billable Cost       | `resources.billable_cost`     | The billable charges for all cloud resources used in the account |
| Non Billable Cost  | `resources.non_billable_cost` | Non-billable charges for all cloud resources used in the account |
{: class="simple-tab-table"}
{: caption="Table 2. Account summary CSV header titles and JSON report fields for account usage summary" caption-side="bottom"}
{: tab-group="account-summary-1-1"}
{: #account-id-1-1}
{: tab-title="Account Usage Summary"}

| CSV Header       | JSON Report Fields                                          | Description |
|---------------------|-------------------------------------------------------------|-------------|
| Subscription ID | `subscription.subscriptions.subscription_id`                | The ID of the subscription |
| CA                  | `subscription.subscriptions.charge_agreement_number`        | The charge agreement number of the subscription |
| Type                | `subscription.subscriptions.type`                           | Type of subscription |
| Subscription Amount | `subscription.subscriptions.subscription_amount`            | The credits available in the subscription for the month |
| Start               | `subscription.subscriptions.start` or \n `subscription.subscriptions.terms.start`| Pay-As-You-Go accounts: the date from which the subscription was active \n Subscription accounts: The start date of the term |
| End                 | `subscription.subscriptions.end` or \n `subscription.subscriptions.terms.end`           | Pay-As-You-Go accounts: unavailable \n Subscription accounts: The end date of the term |
| Credits Total       | `subscription.subscriptions.credits_total` or \n `subscription.subscriptions.terms.credits.total`             | Pay-As-You-Go accounts: The total credits available in the  subscription \n Subscription accounts: The total credits available for the term  |
| Credits Starting    | `subscription.subscriptions.terms.credits.starting_balance` | The unused credits in the term at the beginning of the month |
| Credits Used        | `subscription.subscriptions.terms.credits.used`             | The credits used in this month |
| Credits Balance     | `subscription.subscriptions.terms.credits.balance`          | The remaining credits in this term |
{: class="simple-tab-table"}
{: caption="Table 2. Account summary CSV header titles and JSON report fields for subscriptions" caption-side="bottom"}
{: tab-group="account-summary-1-1"}
{: #subscription-id-1-1}
{: tab-title="Subscriptions"}

| CSV Header       | JSON Report Fields                     | Description |
|---------------------|-----------------------------------|-------------|
| Offer ID            | `offers.offer_id`                 | The ID of the offer |
| Credits Total       | `offers.credits_total`            | The total credits before applying the offer |
| Offer Template      | `offers.offer_template`           | The template with which the offer was generated |
| Valid From          | `offers.valid_from`               | The date from which the offer is valid |
| Expire Date         | `offers.expires_on`               | The date until the offer is valid |
| Recurring           | `offers.is_recurring`             | Indicates if a cost is recurring |
| Starting Balance    | `offers.credits.starting_balance` | The available credits in the offer at the beginning of the month |
| Used                | `offers.credits.used`             | The credits used in this month |
| Balance             | `offers.credits.balance`          | The remaining credits in the offer |
{: class="simple-tab-table"}
{: caption="Table 2. Account summary CSV header titles and JSON report fields for offers" caption-side="bottom"}
{: tab-group="account-summary-1-1"}
{: #offer-id-1-1}
{: tab-title="Offers"}

| CSV Header       | JSON Report Fields | Description |
|---------------------|--------------------|-------------|
| Support Cost        | `support.cost`     | The monthly support cost |
| Support Type        | `support.type` \n (`STANDARD` > `Advanced` and \n `PREMIUM` > `Premium`) | The type of support  |
| Support Overage     | `support.overage`  | Additional support cost for the month |
{: class="simple-tab-table"}
{: caption="Table 2. Account summary CSV header titles and JSON report fields for support summary" caption-side="bottom"}
{: tab-group="account-summary-1-1"}
{: #support-cost-1-1}
{: tab-title="Support Summary"}

| CSV Header  | JSON Report Fields                 | Description |
|----------------|------------------------------------|-------------|
| Service Name   | `resources.resource_name`          | The name of the resource |
| Service ID     | `resources.resource_id`            | The ID of the resource |
| Currency       | `currency_code`                    | The currency for the cost fields in the resources, plans, and metrics |
| Billable       | `resources.billable`               | Indicates if the plan charges are billed to the customer |
| Plan Name      | `resources.plan_name`              | Name of the service plan |
| Plan ID        | `resources.plan_id`                | ID of the service plan |
| Pricing Region | `reports.resources.plans.pricing_region` | Pricing region for the plan |
| Metric         | `resources.usage.metric`           | The ID of the metric |
| Unit           | `resources.usage.unit`             | The unit that qualifies the quantity |
| Quantity       | `resources.usage.quantity`         | The aggregated value for the metric |
| Cost           | `resources.usage.cost`             | The cost incurred by the metric |
| Original Cost  | `resources.usage.rated_cost`       | Pre-discounted cost incurred by the metric |
| Pending        | `resources.pending`            | Pending charge from classic infrastructure |
| Discount (%)   | `resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID    | `resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
| Non Chargeable  | `resources.plans.usage.non_chargeable` |  When set to `true`, the cost is for informational purpose and is not included while calculating the plan charges. |
| Classic Infrastructure Product ID | `resources.plans.usage.additional_properties.classic_infrastructure_product_id`| Product ID of classic infrastructure resource |
| Classic Infrastructure Package ID | `resources.plans.usage.additional_properties.classic_infrastructure_package_id` | Package ID of classic infrastructure resource |
{: class="simple-tab-table"}
{: caption="Table 2. Account summary CSV header titles and JSON report fields for account resource usage" caption-side="bottom"}
{: tab-group="account-summary-1-1"}
{: #service-name-1-1}
{: tab-title="Account Resource Usage"}

#### Account summary CSV version 1.0
{: #account-summary-csv-version-1-0}

You will get CSV version 1.0 if the data that you're viewing is from October 2023 to March 2024.

| CSV Header          | Description                                        |
|---------------------|-------------------------------------------------|
| Account Owner ID    | ID of the account                               |
| Account Name        | Name of the account                             |
| Billing Month       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Currency Rate       | Currency Exchange Rate with USD as the base     |
| Created Time        | Timestamp at which the CSV report was generated |
{: class="simple-tab-table"}
{: caption="Table 3. Account summary CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-summary-1-0"}
{: #account-owner-id-1-0}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|-------------------------------|-------------|
| Account ID          | `account_id`                  | ID of the account |
| Month               | `month`                       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Country Code        | `billing_country_code`        | Country the requested account is mapped to |
| Currency Code       | `billing_currency_code`       | The currency in which the account is billed |
| Billable Cost       | `resources.billable_cost`     | The billable charges for all cloud resources used in the account |
| Non Billable Cost  | `resources.non_billable_cost` | Non-billable charges for all cloud resources used in the account |
{: class="simple-tab-table"}
{: caption="Table 3. Account summary CSV header titles and JSON report fields for account usage summary" caption-side="bottom"}
{: tab-group="account-summary-1-0"}
{: #account-id-1-0}
{: tab-title="Account Usage Summary"}

| CSV Header       | JSON Report Fields                                          | Description |
|---------------------|-------------------------------------------------------------|-------------|
| Subscription ID | `subscription.subscriptions.subscription_id`                | The ID of the subscription |
| CA                  | `subscription.subscriptions.charge_agreement_number`        | The charge agreement number of the subscription |
| Type                | `subscription.subscriptions.type`                           | Type of subscription |
| Subscription Amount | `subscription.subscriptions.subscription_amount`            | The credits available in the subscription for the month |
| Start               | `subscription.subscriptions.start` or \n `subscription.subscriptions.terms.start`| Pay-As-You-Go accounts: the date from which the subscription was active \n Subscription accounts: The start date of the term |
| End                 | `subscription.subscriptions.end` or \n `subscription.subscriptions.terms.end`           | Pay-As-You-Go accounts: unavailable \n Subscription accounts: The end date of the term |
| Credits Total       | `subscription.subscriptions.credits_total` or \n `subscription.subscriptions.terms.credits.total`             | Pay-As-You-Go accounts: The total credits available in the  subscription \n Subscription accounts: The total credits available for the term  |
| Credits Starting    | `subscription.subscriptions.terms.credits.starting_balance` | The unused credits in the term at the beginning of the month |
| Credits Used        | `subscription.subscriptions.terms.credits.used`             | The credits used in this month |
| Credits Balance     | `subscription.subscriptions.terms.credits.balance`          | The remaining credits in this term |
{: class="simple-tab-table"}
{: caption="Table 3. Account summary CSV header titles and JSON report fields for subscriptions" caption-side="bottom"}
{: tab-group="account-summary-1-0"}
{: #subscription-id-1-0}
{: tab-title="Subscriptions"}

| CSV Header       | JSON Report Fields                     | Description |
|---------------------|-----------------------------------|-------------|
| Offer ID            | `offers.offer_id`                 | The ID of the offer |
| Credits Total       | `offers.credits_total`            | The total credits before applying the offer |
| Offer Template      | `offers.offer_template`           | The template with which the offer was generated |
| Valid From          | `offers.valid_from`               | The date from which the offer is valid |
| Expire Date         | `offers.expires_on`               | The date until the offer is valid |
| Recurring           | `offers.is_recurring`             | Indicates if a cost is recurring |
| Starting Balance    | `offers.credits.starting_balance` | The available credits in the offer at the beginning of the month |
| Used                | `offers.credits.used`             | The credits used in this month |
| Balance             | `offers.credits.balance`          | The remaining credits in the offer |
{: class="simple-tab-table"}
{: caption="Table 3. Account summary CSV header titles and JSON report fields for offers" caption-side="bottom"}
{: tab-group="account-summary-1-0"}
{: #offer-id-1-0}
{: tab-title="Offers"}

| CSV Header       | JSON Report Fields | Description |
|---------------------|--------------------|-------------|
| Support Cost        | `support.cost`     | The monthly support cost |
| Support Type        | `support.type` \n (`STANDARD` > `Advanced` and \n `PREMIUM` > `Premium`) | The type of support  |
| Support Overage     | `support.overage`  | Additional support cost for the month |
{: class="simple-tab-table"}
{: caption="Table 3. Account summary CSV header titles and JSON report fields for support summary" caption-side="bottom"}
{: tab-group="account-summary-1-0"}
{: #support-cost-1-0}
{: tab-title="Support Summary"}

| CSV Header  | JSON Report Fields                 | Description |
|----------------|------------------------------------|-------------|
| Service Name   | `resources.resource_name`          | The name of the resource |
| Service ID     | `resources.resource_id`            | The ID of the resource |
| Currency       | `currency_code`                    | The currency for the cost fields in the resources, plans, and metrics |
| Billable       | `resources.billable`               | Indicates if the plan charges are billed to the customer |
| Plan Name      | `resources.plan_name`              | Name of the service plan |
| Plan ID        | `resources.plan_id`                | ID of the service plan |
| Pricing Region | `reports.resources.plans.pricing_region` | Pricing region for the plan |
| Metric         | `resources.usage.metric`           | The ID of the metric |
| Unit           | `resources.usage.unit`             | The unit that qualifies the quantity |
| Quantity       | `resources.usage.quantity`         | The aggregated value for the metric |
| Cost           | `resources.usage.cost`             | The cost incurred by the metric |
| Original Cost  | `resources.usage.rated_cost`       | Pre-discounted cost incurred by the metric |
| Pending        | `resources.pending`            | Pending charge from classic infrastructure |
| Discount (%)   | `resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID    | `resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
| Non Chargeable  | `resources.plans.usage.non_chargeable` |  When set to `true`, the cost is for informational purpose and is not included while calculating the plan charges. |
| Classic Infrastructure Product ID | `resources.plans.usage.additional_properties.classic_infrastructure_product_id`| Product ID of classic infrastructure resource |
| Classic Infrastructure Package ID | `resources.plans.usage.additional_properties.classic_infrastructure_package_id` | Package ID of classic infrastructure resource |
{: class="simple-tab-table"}
{: caption="Table 3. Account summary CSV header titles and JSON report fields for account resource usage" caption-side="bottom"}
{: tab-group="account-summary-1-0"}
{: #service-name-1-0}
{: tab-title="Account Resource Usage"}

### Account summary CSV version 0.2
{: #account-summary-csv-version-0-2}

You will get CSV version 0.2 if the data that you're viewing is from February 2023 to October 2023.

| CSV Header          | Description                                        |
|---------------------|-------------------------------------------------|
| Account Owner ID    | ID of the account                               |
| Account Name        | Name of the account                             |
| Billing Month       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Currency Rate       | Currency Exchange Rate with USD as the base     |
| Created Time        | Timestamp at which the CSV report was generated |
{: class="simple-tab-table"}
{: caption="Table 4. Account summary CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-summary-0-2"}
{: #account-owner-id-0-2}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|-------------------------------|-------------|
| Account ID          | `account_id`                  | ID of the account |
| Month               | `month`                       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Country Code        | `billing_country_code`        | Country the requested account is mapped to |
| Currency Code       | `billing_currency_code`       | The currency in which the account is billed |
| Billable Cost       | `resources.billable_cost`     | The billable charges for all cloud resources used in the account |
| Non Billable Cost  | `resources.non_billable_cost` | Non-billable charges for all cloud resources used in the account |
{: class="simple-tab-table"}
{: caption="Table 4. Account summary CSV header titles and JSON report fields for account usage summary" caption-side="bottom"}
{: tab-group="account-summary-0-2"}
{: #account-id-0-2}
{: tab-title="Account Usage Summary"}

| CSV Header       | JSON Report Fields                                          | Description |
|---------------------|-------------------------------------------------------------|-------------|
| Subscription ID | `subscription.subscriptions.subscription_id`                | The ID of the subscription |
| CA                  | `subscription.subscriptions.charge_agreement_number`        | The charge agreement number of the subscription |
| Type                | `subscription.subscriptions.type`                           | Type of subscription |
| Subscription Amount | `subscription.subscriptions.subscription_amount`            | The credits available in the subscription for the month |
| Start               | `subscription.subscriptions.start` or \n `subscription.subscriptions.terms.start`| Pay-As-You-Go accounts: the date from which the subscription was active \n Subscription accounts: The start date of the term |
| End                 | `subscription.subscriptions.end` or \n `subscription.subscriptions.terms.end`           | Pay-As-You-Go accounts: unavailable \n Subscription accounts: The end date of the term |
| Credits Total       | `subscription.subscriptions.credits_total` or \n `subscription.subscriptions.terms.credits.total`             | Pay-As-You-Go accounts: The total credits available in the  subscription \n Subscription accounts: The total credits available for the term  |
| Credits Starting    | `subscription.subscriptions.terms.credits.starting_balance` | The unused credits in the term at the beginning of the month |
| Credits Used        | `subscription.subscriptions.terms.credits.used`             | The credits used in this month |
| Credits Balance     | `subscription.subscriptions.terms.credits.balance`          | The remaining credits in this term |
{: class="simple-tab-table"}
{: caption="Table 4. Account summary CSV header titles and JSON report fields for subscriptions" caption-side="bottom"}
{: tab-group="account-summary-0-2"}
{: #subscription-id-0-2}
{: tab-title="Subscriptions"}

| CSV Header       | JSON Report Fields                     | Description |
|---------------------|-----------------------------------|-------------|
| Offer ID            | `offers.offer_id`                 | The ID of the offer |
| Credits Total       | `offers.credits_total`            | The total credits before applying the offer |
| Offer Template      | `offers.offer_template`           | The template with which the offer was generated |
| Valid From          | `offers.valid_from`               | The date from which the offer is valid |
| Expire Date         | `offers.expires_on`               | The date until the offer is valid |
| Recurring           | `offers.is_recurring`             | Indicates if a cost is recurring |
| Starting Balance    | `offers.credits.starting_balance` | The available credits in the offer at the beginning of the month |
| Used                | `offers.credits.used`             | The credits used in this month |
| Balance             | `offers.credits.balance`          | The remaining credits in the offer |
{: class="simple-tab-table"}
{: caption="Table 4. Account summary CSV header titles and JSON report fields for offers" caption-side="bottom"}
{: tab-group="account-summary-0-2"}
{: #offer-id-0-2}
{: tab-title="Offers"}

| CSV Header       | JSON Report Fields | Description |
|---------------------|--------------------|-------------|
| Support Cost        | `support.cost`     | The monthly support cost |
| Support Type        | `support.type` \n (`STANDARD` > `Advanced` and \n `PREMIUM` > `Premium`) | The type of support  |
| Support Overage     | `support.overage`  | Additional support cost for the month |
{: class="simple-tab-table"}
{: caption="Table 4. Account summary CSV header titles and JSON report fields for support summary" caption-side="bottom"}
{: tab-group="account-summary-0-2"}
{: #support-cost-0-2}
{: tab-title="Support Summary"}

| CSV Header  | JSON Report Fields                 | Description |
|----------------|------------------------------------|-------------|
| Service Name   | `resources.resource_name`          | The name of the resource |
| Service ID     | `resources.resource_id`            | The ID of the resource |
| Currency       | `currency_code`                    | The currency for the cost fields in the resources, plans, and metrics |
| Billable       | `resources.billable`               | Indicates if the plan charges are billed to the customer |
| Plan Name      | `resources.plan_name`              | Name of the service plan |
| Plan ID        | `resources.plan_id`                | ID of the service plan |
| Pricing Region | `reports.resources.plans.pricing_region` | Pricing region for the plan |
| Metric         | `resources.usage.metric`           | The ID of the metric |
| Unit           | `resources.usage.unit`             | The unit that qualifies the quantity |
| Quantity       | `resources.usage.quantity`         | The aggregated value for the metric |
| Cost           | `resources.usage.cost`             | The cost incurred by the metric |
| Original Cost  | `resources.usage.rated_cost`       | Pre-discounted cost incurred by the metric |
| Pending        | `resources.pending`            | Pending charge from classic infrastructure |
| Discount (%)   | `resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID    | `resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
{: class="simple-tab-table"}
{: caption="Table 4. Account summary CSV header titles and JSON report fields for account resource usage" caption-side="bottom"}
{: tab-group="account-summary-0-2"}
{: #service-name-0-2}
{: tab-title="Account Resource Usage"}

### Account summary CSV version 0.1
{: #account-summary-csv-version-0-1}

You will get CSV version 0.1 if the data that you're viewing is from before February 2023.

| CSV Header          | Description                                        |
|---------------------|-------------------------------------------------|
| Account Owner ID    | ID of the account                               |
| Account Name        | Name of the account                             |
| Billing Month       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Created Time        | Timestamp at which the CSV report was generated |
{: class="simple-tab-table"}
{: caption="Table 5. Account summary CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-summary-0-1"}
{: #account-owner-id-0-1}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|-------------------------------|-------------|
| Account ID          | `account_id`                  | ID of the account |
| Month               | `month`                       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Country Code        | `billing_country_code`        | Country the requested account is mapped to |
| Currency Code       | `billing_currency_code`       | The currency in which the account is billed |
| Billable Cost       | `resources.billable_cost`     | The billable charges for all cloud resources used in the account |
| Non Billable Cost  | `resources.non_billable_cost` | Non-billable charges for all cloud resources used in the account |
{: class="simple-tab-table"}
{: caption="Table 5. Account summary CSV header titles and JSON report fields for account usage summary" caption-side="bottom"}
{: tab-group="account-summary-0-1"}
{: #account-id-0-1}
{: tab-title="Account Usage Summary"}

| CSV Header       | JSON Report Fields                                          | Description |
|---------------------|-------------------------------------------------------------|-------------|
| Subscription ID | `subscription.subscriptions.subscription_id`                | The ID of the subscription |
| CA                  | `subscription.subscriptions.charge_agreement_number`        | The charge agreement number of the subscription |
| Type                | `subscription.subscriptions.type`                           | Type of subscription |
| Subscription Amount | `subscription.subscriptions.subscription_amount`            | The credits available in the subscription for the month |
| Start               | `subscription.subscriptions.start` or \n `subscription.subscriptions.terms.start`| Pay-As-You-Go accounts: the date from which the subscription was active \n Subscription accounts: The start date of the term |
| End                 | `subscription.subscriptions.end` or \n `subscription.subscriptions.terms.end`           | Pay-As-You-Go accounts: unavailable \n Subscription accounts: The end date of the term |
| Credits Total       | `subscription.subscriptions.credits_total` or \n `subscription.subscriptions.terms.credits.total`             | Pay-As-You-Go accounts: The total credits available in the  subscription \n Subscription accounts: The total credits available for the term  |
| Credits Starting    | `subscription.subscriptions.terms.credits.starting_balance` | The unused credits in the term at the beginning of the month |
| Credits Used        | `subscription.subscriptions.terms.credits.used`             | The credits used in this month |
| Credits Balance     | `subscription.subscriptions.terms.credits.balance`          | The remaining credits in this term |
{: class="simple-tab-table"}
{: caption="Table 5. Account summary CSV header titles and JSON report fields for subscriptions" caption-side="bottom"}
{: tab-group="account-summary-0-1"}
{: #subscription-id-0-1}
{: tab-title="Subscriptions"}

| CSV Header       | JSON Report Fields                     | Description |
|---------------------|-----------------------------------|-------------|
| Offer ID            | `offers.offer_id`                 | The ID of the offer |
| Credits Total       | `offers.credits_total`            | The total credits before applying the offer |
| Offer Template      | `offers.offer_template`           | The template with which the offer was generated |
| Valid From          | `offers.valid_from`               | The date from which the offer is valid |
| Expire Date         | `offers.expires_on`               | The date until the offer is valid |
| Recurring           | `offers.is_recurring`             | Indicates if a cost is recurring |
| Starting Balance    | `offers.credits.starting_balance` | The available credits in the offer at the beginning of the month |
| Used                | `offers.credits.used`             | The credits used in this month |
| Balance             | `offers.credits.balance`          | The remaining credits in the offer |
{: class="simple-tab-table"}
{: caption="Table 5. Account summary CSV header titles and JSON report fields for offers" caption-side="bottom"}
{: tab-group="account-summary-0-1"}
{: #offer-id-0-1}
{: tab-title="Offers"}

| CSV Header       | JSON Report Fields | Description |
|---------------------|--------------------|-------------|
| Support Cost        | `support.cost`     | The monthly support cost |
| Support Type        | `support.type` \n (`STANDARD` > `Advanced` and \n `PREMIUM` > `Premium`) | The type of support  |
| Support Overage     | `support.overage`  | Additional support cost for the month |
{: class="simple-tab-table"}
{: caption="Table 5. Account summary CSV header titles and JSON report fields for support summary" caption-side="bottom"}
{: tab-group="account-summary-0-1"}
{: #support-cost-0-1}
{: tab-title="Support Summary"}

| CSV Header  | JSON Report Fields                 | Description |
|----------------|------------------------------------|-------------|
| Service Name   | `resources.resource_name`          | The name of the resource |
| Service ID     | `resources.resource_id`            | The ID of the resource |
| Currency       | `currency_code`                    | The currency for the cost fields in the resources, plans, and metrics |
| Billable       | `resources.billable`               | Indicates if the plan charges are billed to the customer |
| Plan Name      | `resources.plan_name`              | Name of the service plan |
| Plan ID        | `resources.plan_id`                | ID of the service plan |
| Pricing Region | `reports.resources.plans.pricing_region` | Pricing region for the plan |
| Metric         | `resources.usage.metric`           | The ID of the metric |
| Unit           | `resources.usage.unit`             | The unit that qualifies the quantity |
| Quantity       | `resources.usage.quantity`         | The aggregated value for the metric |
| Cost           | `resources.usage.cost`             | The cost incurred by the metric |
| Original Cost  | `resources.usage.rated_cost`       | Pre-discounted cost incurred by the metric |
| Pending        | `resources.pending`            | Pending charge from classic infrastructure |
| Discount (%)   | `resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID    | `resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
{: class="simple-tab-table"}
{: caption="Table 5. Account summary CSV header titles and JSON report fields for account resource usage" caption-side="bottom"}
{: tab-group="account-summary-0-1"}
{: #service-name-0-1}
{: tab-title="Account Resource Usage"}

### Understanding your instances report
{: #table-account-instance-report}

The following tables show the correlation between the heading titles in your CSV report and API parameters. For more information about JSON report fields, see [Usage Reports: Get resource instance usage in an account](/apidocs/metering-reporting#get-resource-usage-account). Each row of the **Account Instance Usage** section represents an instance usage of a specific metric in a service plan.

Regular account CSV reports are not real time and can be incomplete. Complete CSV reports are generated for previous months that have already been invoiced. In case of potentially inconsistent data in the CSV reports, it's advised to regenerate the CSV after couple of hours. For more accurate and real time usages, it's always recommended to use the JSON APIs.
{: note}

You can view other versions of the CSV if you have earlier instances reports in your account. The CSV version depends on the date that the data is published. The following are the available versions:

- June 2024 to present is [version 1.2](#instances-CSV-version-1-2)
- March 2024 to June 2024 is [version 1.1](#instances-csv-version-1-1)
- October 2023 to March 2024 is [version 1.0](#instances-csv-version-1-0)
- February 2023 to October 2023 is [version 0.2](#instances-csv-version-0-2)
- Before February 2023 is [version 0.1](#instances-csv-version-0-1).

### Instances CSV version 1.2
{: #instances-CSV-version-1-2}

The following table is version 1.2 and the most recent CSV version. You get this version if the data that you're viewing is from June 2024 to present.

| CSV Header       | Description                                     |
|------------------|-------------------------------------------------|
| Account Owner ID | ID of the account                               |
| Account Name     | Name of the account                             |
| Billing Month    | The month in which usages were incurred. Represented in `yyyy-mm` format     |
| Currency Rate    | Currency Exchange Rate with USD as the base     |
| Created Time     | Timestamp at which the CSV report was generated |
| Version          | The version number of the account instance CSV  |
{: class="simple-tab-table"}
{: caption="Table 6. Account instance CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-instance-1-2"}
{: #account-owner-id-instance-1-2}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|------------------------------------|-------------|
| Service Name        | `resources.resource_name`          | The name of the resource |
| Service ID          | `resources.resource_id`            | The ID of the resource |
| Instance Name       | `resources.resource_instance_name` | The name of the resource instance |
| Instance ID         | `resources.resource_instance_id`   | The ID of the resource instance |
| Plan Name           | `resources.plan_name`              | The name of the plan where the instance was provisioned and rated |
| Plan ID             | `resources.plan_id`                | The ID of the plan where the instance was provisioned and rated |
| Region              | `resources.region`                 | The region where instance was provisioned |
| Consumer ID         | `resources.consumer_id`            | The ID of the consumer |
| Resource Group Name | `resources.resource_group_name`    | The name of the resource group |
| Resource Group ID   | `resources.resource_group_id`      | The ID of the resource group |
| CF Org              | `resources.organization_name`      | The name of the CF organization |
| Org ID              | `resources.organization_id`        | The ID of the CF organization |
| CF Space            | `resources.space_name`             | The name of the CF space |
| Space ID            | `resources.space_id`               | The ID of the CF space|
| Currency            | `resources.currency_code`          | The currency for the cost fields in the resources, plans, and metrics |
| Billable            | `resources.billable`               | Validates if a cost is charged to the account |
| Usage Metric        | `resources.usage.metric`           | ID of the metric |
| Usage Unit          | `resources.usage.unit`             | Unit that qualifies the quantity |
| Usage Quantity      | `resources.usage.quantity`         | Aggregated value for the metric |
| Original Cost       | `resources.usage.rated_cost`       | The starting cost of a resource within your account |
| Volume Discount [New]{: tag-new}  | `resources.usage.volume_discount` | This percentage reflects the reduction to the original cost that you receive under a volume based pricing structure |
| Volume Cost [New]{: tag-new} | `resources.usage.volume_cost` | The original cost adjusted for volume based discounts that are applied at the account level |
| Cost [New]{: tag-new} |  `resources.usage.cost`   |  The pre-tax cost after accounting for any applicable discounts |
| Pending             | `resources.pending`            | 	Pending charge from classic infrastructure |
| Discount (%)        | `resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID         | `resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
| Non Chargeable  | `resources.usage.non_chargeable` |  When set to `true`, the cost is for informational purpose and is not included while calculating the plan charges. |
| Classic Infrastructure Product ID | `resources.usage.additional_properties.classic_infrastructure_product_id`  | Product ID of classic infrastructure resource |
| Classic Infrastructure Package ID |`resources.usage.additional_properties.classic_infrastructure_package_id` | Package ID of classic infrastructure resource |
| Parent Resource Instance ID | `resources.parent_resource_instance_id` | Resource instance ID of the parent resource associated with this instance |
| Other Tags          | `resources.tags`                   | Tags that are not of `key:value` format |
{: class="simple-tab-table"}
{: caption="Table 6. Account instance CSV header titles and JSON report fields for account instance usage" caption-side="bottom"}
{: tab-group="account-instance-1-2"}
{: #service-name-instance-1-2}
{: tab-title="Account Instance Usage"}

### Instances CSV version 1.1
{: #instances-csv-version-1-1}

You will get CSV version 1.1 if the data that you're viewing is from March 2024 to June 2024.

| CSV Header       | Description                                     |
|------------------|-------------------------------------------------|
| Account Owner ID | ID of the account                               |
| Account Name     | Name of the account                             |
| Billing Month    | The month in which usages were incurred. Represented in `yyyy-mm` format     |
| Currency Rate    | Currency Exchange Rate with USD as the base     |
| Created Time     | Timestamp at which the CSV report was generated |
| Version          | The version number of the account instance CSV  |
{: class="simple-tab-table"}
{: caption="Table 7. Account instance CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-instance-1-1"}
{: #account-owner-id-instance-1-1}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|------------------------------------|-------------|
| Service Name        | `resources.resource_name`          | The name of the resource |
| Service ID          | `resources.resource_id`            | The ID of the resource |
| Instance Name       | `resources.resource_instance_name` | The name of the resource instance |
| Instance ID         | `resources.resource_instance_id`   | The ID of the resource instance |
| Plan Name           | `resources.plan_name`              | The name of the plan where the instance was provisioned and rated |
| Plan ID             | `resources.plan_id`                | The ID of the plan where the instance was provisioned and rated |
| Region              | `resources.region`                 | The region where instance was provisioned |
| Consumer ID         | `resources.consumer_id`            | The ID of the consumer |
| Resource Group Name | `resources.resource_group_name`    | The name of the resource group |
| Resource Group ID   | `resources.resource_group_id`      | The ID of the resource group |
| CF Org              | `resources.organization_name`      | The name of the CF organization |
| Org ID              | `resources.organization_id`        | The ID of the CF organization |
| CF Space            | `resources.space_name`             | The name of the CF space |
| Space ID            | `resources.space_id`               | The ID of the CF space|
| Currency            | `resources.currency_code`          | The currency for the cost fields in the resources, plans, and metrics |
| Billable            | `resources.billable`               | Validates if a cost is charged to the account |
| Usage Metric        | `resources.usage.metric`           | ID of the metric |
| Usage Unit          | `resources.usage.unit`             | Unit that qualifies the quantity |
| Usage Quantity      | `resources.usage.quantity`         | Aggregated value for the metric |
| Usage Cost          | `resources.usage.cost`             | Cost incurred by the metric |
| Original Cost       | `resources.usage.rated_cost`       | The starting cost of a resource within your account |
| Pending             | `resources.pending`            | 	Pending charge from classic infrastructure |
| Discount (%)        | `resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID         | `resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
| Non Chargeable  | `resources.usage.non_chargeable` |  When set to `true`, the cost is for informational purpose and is not included while calculating the plan charges. |
| Classic Infrastructure Product ID | `resources.usage.additional_properties.classic_infrastructure_product_id`  | Product ID of classic infrastructure resource |
| Classic Infrastructure Package ID |`resources.usage.additional_properties.classic_infrastructure_package_id` | Package ID of classic infrastructure resource |
| Parent Resource Instance ID | `resources.parent_resource_instance_id` | Resource instance ID of the parent resource associated with this instance |
| Other Tags          | `resources.tags`                   | Tags that are not of `key:value` format |
{: class="simple-tab-table"}
{: caption="Table 7. Account instance CSV header titles and JSON report fields for account instance usage" caption-side="bottom"}
{: tab-group="account-instance-1-1"}
{: #service-name-instance-1-1}
{: tab-title="Account Instance Usage"}

### Instances CSV version 1.0
{: #instances-csv-version-1-0}

You will get CSV version 1.0 if the data that you're viewing is from October 2023 to March 2024.

| CSV Header       | Description                                     |
|------------------|-------------------------------------------------|
| Account Owner ID | ID of the account                               |
| Account Name     | Name of the account                             |
| Billing Month    | The month in which usages were incurred. Represented in `yyyy-mm` format     |
| Currency Rate    | Currency Exchange Rate with USD as the base     |
| Created Time     | Timestamp at which the CSV report was generated |
{: class="simple-tab-table"}
{: caption="Table 8. Account instance CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-instance-1-0"}
{: #account-owner-id-instance-1-0}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|------------------------------------|-------------|
| Service Name        | `resources.resource_name`          | The name of the resource |
| Service ID          | `resources.resource_id`            | The ID of the resource |
| Instance Name       | `resources.resource_instance_name` | The name of the resource instance |
| Instance ID         | `resources.resource_instance_id`   | The ID of the resource instance |
| Plan Name           | `resources.plan_name`              | The name of the plan where the instance was provisioned and rated |
| Plan ID             | `resources.plan_id`                | The ID of the plan where the instance was provisioned and rated |
| Region              | `resources.region`                 | The region where instance was provisioned |
| Consumer ID         | `resources.consumer_id`            | The ID of the consumer |
| Resource Group Name | `resources.resource_group_name`    | The name of the resource group |
| Resource Group ID   | `resources.resource_group_id`      | The ID of the resource group |
| CF Org              | `resources.organization_name`      | The name of the CF organization |
| Org ID              | `resources.organization_id`        | The ID of the CF organization |
| CF Space            | `resources.space_name`             | The name of the CF space |
| Space ID            | `resources.space_id`               | The ID of the CF space|
| Currency            | `resources.currency_code`          | The currency for the cost fields in the resources, plans, and metrics |
| Billable            | `resources.billable`               | Validates if a cost is charged to the account |
| Usage Metric        | `resources.usage.metric`           | ID of the metric |
| Usage Unit          | `resources.usage.unit`             | Unit that qualifies the quantity |
| Usage Quantity      | `resources.usage.quantity`         | Aggregated value for the metric |
| Usage Cost          | `resources.usage.cost`             | Cost incurred by the metric |
| Original Cost       | `resources.usage.rated_cost`       | The starting cost of a resource within your account |
| Pending             | `resources.pending`            | 	Pending charge from classic infrastructure |
| Discount (%)        | `resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID         | `resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
| Non Chargeable  | `resources.usage.non_chargeable` |  When set to `true`, the cost is for informational purpose and is not included while calculating the plan charges. |
| Classic Infrastructure Product ID | `resources.usage.additional_properties.classic_infrastructure_product_id`  | Product ID of classic infrastructure resource |
| Classic Infrastructure Package ID |`resources.usage.additional_properties.classic_infrastructure_package_id` | Package ID of classic infrastructure resource |
| Parent Resource Instance ID | `resources.parent_resource_instance_id` | Resource instance ID of the parent resource associated with this instance |
| Other Tags          | `resources.tags`                   | Tags that are not of `key:value` format |
{: class="simple-tab-table"}
{: caption="Table 8. Account instance CSV header titles and JSON report fields for account instance usage" caption-side="bottom"}
{: tab-group="account-instance-1-0"}
{: #service-name-instance-1-0}
{: tab-title="Account Instance Usage"}

### Instances CSV version 0.2
{: #instances-csv-version-0-2}

You will get CSV version 0.2 if the data that you're viewing is from February 2023 to October 2023.

| CSV Header       | Description                                     |
|------------------|-------------------------------------------------|
| Account Owner ID | ID of the account                               |
| Account Name     | Name of the account                             |
| Billing Month    | The month in which usages were incurred. Represented in `yyyy-mm` format     |
| Currency Rate    | Currency Exchange Rate with USD as the base     |
| Created Time     | Timestamp at which the CSV report was generated |
{: class="simple-tab-table"}
{: caption="Table 9. Account instance CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-instance-0-2"}
{: #account-owner-id-instance-0-2}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|------------------------------------|-------------|
| Service Name        | `resources.resource_name`          | The name of the resource |
| Service ID          | `resources.resource_id`            | The ID of the resource |
| Instance Name       | `resources.resource_instance_name` | The name of the resource instance |
| Instance ID         | `resources.resource_instance_id`   | The ID of the resource instance |
| Plan Name           | `resources.plan_name`              | The name of the plan where the instance was provisioned and rated |
| Plan ID             | `resources.plan_id`                | The ID of the plan where the instance was provisioned and rated |
| Region              | `resources.region`                 | The region where instance was provisioned |
| Consumer ID         | `resources.consumer_id`            | The ID of the consumer |
| Resource Group Name | `resources.resource_group_name`    | The name of the resource group |
| Resource Group ID   | `resources.resource_group_id`      | The ID of the resource group |
| CF Org              | `resources.organization_name`      | The name of the CF organization |
| Org ID              | `resources.organization_id`        | The ID of the CF organization |
| CF Space            | `resources.space_name`             | The name of the CF space |
| Space ID            | `resources.space_id`               | The ID of the CF space|
| Currency            | `resources.currency_code`          | The currency for the cost fields in the resources, plans, and metrics |
| Billable            | `resources.billable`               | Validates if a cost is charged to the account |
| Usage Metric        | `resources.usage.metric`           | ID of the metric |
| Usage Unit          | `resources.usage.unit`             | Unit that qualifies the quantity |
| Usage Quantity      | `resources.usage.quantity`         | Aggregated value for the metric |
| Usage Cost          | `resources.usage.cost`             | Cost incurred by the metric |
| Original Cost       | `resources.usage.rated_cost`       | The starting cost of a resource within your account |
| Pending             | `resources.pending`            | 	Pending charge from classic infrastructure |
| Discount (%)        | `resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID         | `resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
| Other Tags          | `resources.tags`                   | Tags that are not of `key:value` format |
{: class="simple-tab-table"}
{: caption="Table 9. Account instance CSV header titles and JSON report fields for account instance usage" caption-side="bottom"}
{: tab-group="account-instance-0-2"}
{: #service-name-instance-0-2}
{: tab-title="Account Instance Usage"}

### Instances CSV version 0.1
{: #instances-csv-version-0-1}

You will get CSV version 0.1 if the data that you're viewing is from before February 2023.

| CSV Header       | Description                                     |
|------------------|-------------------------------------------------|
| Account Owner ID | ID of the account                               |
| Account Name     | Name of the account                             |
| Billing Month    | The month in which usages were incurred. Represented in `yyyy-mm` format     |
| Created Time     | Timestamp at which the CSV report was generated |
{: class="simple-tab-table"}
{: caption="Table 10. Account instance CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-instance-0-1"}
{: #account-owner-id-instance-0-1}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|------------------------------------|-------------|
| Service Name        | `resources.resource_name`          | The name of the resource |
| Service ID          | `resources.resource_id`            | The ID of the resource |
| Instance Name       | `resources.resource_instance_name` | The name of the resource instance |
| Instance ID         | `resources.resource_instance_id`   | The ID of the resource instance |
| Plan Name           | `resources.plan_name`              | The name of the plan where the instance was provisioned and rated |
| Plan ID             | `resources.plan_id`                | The ID of the plan where the instance was provisioned and rated |
| Region              | `resources.region`                 | The region where instance was provisioned |
| Consumer ID         | `resources.consumer_id`            | The ID of the consumer |
| Resource Group Name | `resources.resource_group_name`    | The name of the resource group |
| Resource Group ID   | `resources.resource_group_id`      | The ID of the resource group |
| CF Org              | `resources.organization_name`      | The name of the CF organization |
| Org ID              | `resources.organization_id`        | The ID of the CF organization |
| CF Space            | `resources.space_name`             | The name of the CF space |
| Space ID            | `resources.space_id`               | The ID of the CF space|
| Currency            | `resources.currency_code`          | The currency for the cost fields in the resources, plans, and metrics |
| Billable            | `resources.billable`               | Validates if a cost is charged to the account |
| Usage Metric        | `resources.usage.metric`           | ID of the metric |
| Usage Unit          | `resources.usage.unit`             | Unit that qualifies the quantity |
| Usage Quantity      | `resources.usage.quantity`         | Aggregated value for the metric |
| Usage Cost          | `resources.usage.cost`             | Cost incurred by the metric |
| Original Cost       | `resources.usage.rated_cost`       | The starting cost of a resource within your account |
| Pending             | `resources.pending`            | 	Pending charge from classic infrastructure |
| Discount (%)        | `resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID         | `resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
| Other Tags          | `resources.tags`                   | Tags that are not of `key:value` format |
{: class="simple-tab-table"}
{: caption="Table 10. Account instance CSV header titles and JSON report fields for account instance usage" caption-side="bottom"}
{: tab-group="account-instance-0-1"}
{: #service-name-instance-0-1}
{: tab-title="Account Instance Usage"}

### User tags
{: #acct-instance-user-tags}

For tags that are of `key:value` format, a new column is added for each and every unique `key`, with the `key` as the column name and the `value` as the column value for the corresponding instance usage row. For example, if there are two instances, `i1` and `i2`, with tag `env:prod` on `i1` and tags `env:test` and `team:backend` on `i2`, there would be two additional columns named `env` and `team`. And only the `i1` row will have value `prod` under the `env` column. The `i2` row will have values `test` and `backend` under the `env` and `team` columns. The following table shows the example layout.

| Instance ID | Other tags | `env`  | `team`    |
|-------------|------------|--------|-----------|
| `i1`        |            | `prod` |           |
| `i2`        |            | `test` | `backend` |
{: caption="Table 11. Example of tag layout in the CSV report" caption-side="bottom"}


### Service tags
{: #acct-instance-service-tags}

If the account has [Projects](https://cloud.ibm.com/docs/secure-enterprise?topic=secure-enterprise-understanding-projects) provisioned in it, then all the resource instances that are part of a project will have some service tags attached to them. These service tags are also of `key:value` type and they indicate the `project_id` and `config_id` that the project resource instance belongs to. Similar to the `key:value` user tags, a new column is added for each and every unique service tag `key`, with the `key` as the column name and the `value` as the column value for the corresponding instance usage row.

For example, if there are two instances, `i1` and `i2`, with service tags `project::config_id:123` and `project::project_id:321` on `i1`, and service tags `schematics::config_id:456` and `schematics::project_id:654` on `i2`, there would be four additional columns named `service_tag::project::config_id`, `service_tag::project::project_id`, `service_tag::schematics::config_id` and `service_tag::schematics::project_id`. So, they would have the service tag keys with a prefix `service_tag::` prepended to it, which helps in visual distinction between user tag keys and service tag keys. And eventually, the `i1` row will have values `123` and `321` under the first two columns, and `i2` row will have values `456` and `654` under the next two columns respectively.

The following table shows the example layout.

| Instance ID | Other tags | `env`  | `team`    | `service_tag::project::config_id` | `service_tag::project::project_id` | `service_tag::schematics::config_id` | `service_tag::schematics::project_id` |
|-------------|------------|--------|-----------|--------------------------------------|---------------------------------------|-----------------------------------|------------------------------------|
| `i1`        |            | `prod` |           | `123`                                | `321`                 | | |
| `i2`        |            | `test` | `backend` |                                      |                                       | `456`                             | `654` |
{: caption="Table 12. Example of service tag layout in the CSV report" caption-side="bottom"}

Tags are shown for both active and deleted resources. It might take up to 24 hours to reflect the updated or created tags.
{: note}

## Understanding your enterprise account summary
{: #enterprise-usage-table-account-summary-csv}

The following tables show the correlation between the heading titles in your CSV report and JSON report fields. The usage in the **Enterprise Resource Usage** section is aggregated by each metric of a service plan.

The following are the JSON report section APIs for the different CVS headings:

* Billing Units: [Enterprise Billing Units: List billing units](/apidocs/enterprise-apis/billing-unit?code=go#list-billing-units){: external}
* Credit Pools and Overages: [Enterprise Billing Units: Get credit pools](/apidocs/enterprise-apis/billing-unit?code=go#get-credit-pools){: external}
* Enterprise Usage Summary and Enterprise Resource Usage: [Enterprise Usage Reports API: Get usage reports for enterprise entities](/apidocs/enterprise-apis/resource-usage-reports#get-resource-usage-report){: external}

You can view other versions of the CSV if you have earlier enterprise account summary reports in your account. The CSV version depends on the date that the data is published. The following are the available versions:

- July 2024 to present is [version 1.2](#enterprise-account-summary-csv-version-1-2)
- March 2024 to June 2024 is [version 1.1](#enterprise-account-summary-csv-version-1-1)
- October 2024 to March 2024 is [version 1.0](#enterprise-account-summary-csv-version-1-0)
- February 2023 to October 2024 is [version 0.2](#enterprise-account-summary-csv-version-0-2)
- Before February 2023 is [version 0.1](#enterprise-account-summary-csv-version-0-1).

### Enterprise account summary CSV version 1.2
{: #enterprise-account-summary-csv-version-1-2}

The following table is version 1.2 and the most recent CSV version. You get this version if the data that you're viewing is from July 2024 to present.

| CSV Header         | Description        |
|--------------------|--------------------|
| Entity ID          | ID of the requested entity (`enterprise_id`/`account_group_id`/`account_id`) |
| Entity Type        | Type of the requested entity (enterprise/account_group/account) |
| Billing Month      | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Currency Rate      | Currency Exchange Rate with USD as the base |
| Created Time       | Timestamp at which the CSV report was generated |
| Version            | The version number of the enterprise summary CSV |
{: class="simple-tab-table"}
{: caption="Table 13. Enterprise usage report CSV contents for entity metadata" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-2"}
{: #entity-metadata-1-2}
{: tab-title="Entity Metadata"}

| CSV Header      | Description |
|--------------------|-------------|
| Entity ID          | ID of the hierarchy entity |
| Entity Type        | Type of the hierarchy entity |
| Entity Name        | Name of the hierarchy entity |
| Parent Entity ID   | ID of the parent of this hierarchy entity |
| Parent Entity Name | Name of the parent of the current hierarchy entity |
| Parent Entity Type | Type of the parent of the current hierarchy entity |
| Entity CreatedOn   | Timestamp at which the hierarchy entity was created |
{: class="simple-tab-table"}
{: caption="Table 13. Enterprise usage report CSV contents for entity hierarchy" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-2"}
{: #entity-hierarchy-1-2}
{: tab-title="Entity Hierarchy"}

| CSV Header Header          | JSON Report Fields        | Description        |
|------------------------|---------------------------|--------------------|
| Billing Unit ID        | `resources.id`         | The ID of the DEFAULT billing unit of the requested entity, which is a globally unique identifier (GUID) |
| Billing Unit Name      | `resources.name`       | The name of the billing unit |
| Billing Unit CreatedOn | `resources.created_at` | The creation date of the billing unit |
{: class="simple-tab-table"}
{: caption="Table 13. Enterprise usage report CSV contents for billing units" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-2"}
{: #billing-unit-id-enterprise-1-2}
{: tab-title="Billing Units"}

| CSV Header Header     | JSON Report Fields                        | Description        |
|-------------------|-------------------------------------------|--------------------|
| Credit Pool Type  | `resources.type`                          | The type of credit, either `PLATFORM` or `SUPPORT` |
| Currency Code     | `resources.currency_code`                 | The currency code of the associated billing unit |
| Billing Option ID | `resources.term_credits.billing_option_id`| The ID of the billing option from which the subscription term is derived |
| Category          | `resources.term_credits.category`         | The category of the credit pool. \n For platform credit the valid values are `PLATFORM`, `OFFER`, or `SERVICE` \n For support credit the valid value is `SUPPORT` |
| Start Date        | `resources.term_credits.start_date`       | The start date of the term in ISO format |
| End Date          | `resources.term_credits.end_date`         | The end date of the term in ISO format  |
| Total Credits     | `resources.term_credits.total_credits`    | The total credit available in this term |
| Starting Balance  | `resources.term_credits.starting_balance` | The balance of available credit at the start of the current month |
| Used Credits      | `resources.term_credits.used_credits`     | The amount of credit used during the current month |
| Current Balance   | `resources.term_credits.current_balance`  | The balance of remaining credit in the subscription term |
| True Up           | `resources.term_credits.true_up`          | The credits remaining after the end of the term |
{: class="simple-tab-table"}
{: caption="Table 13. Enterprise usage report CSV contents for credit pools" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-2"}
{: #credit-pool-type-enterprise-1-2}
{: tab-title="Credit Pools"}

| CSV Header Header     | JSON Report Fields       | Description        |
|-------------------|--------------------------|--------------------|
| Credit Pool Type  | `resources.type`         | The type of credit, either `PLATFORM` or `SUPPORT` |
| Currency Code     | `resources.currency_code`| The currency code of the associated billing unit |
| Overage           | `resources.overage.cost` | The number of credits that are used as overage |
{: class="simple-tab-table"}
{: caption="Table 13. Enterprise usage report CSV contents for overages" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-2"}
{: #overages-enterprise-1-2}
{: tab-title="Overages"}

| CSV Header Header      | JSON Report Fields  | Description        |
|--------------------|---------------------|--------------------|
| Entity ID          | `reports.entity_id`         | The ID of the entity |
| Entity Type        | `reports.entity_type`       | The type of the entity  \n Possible values: `enterprise` , `account-group`, or `account` |
| Entity Name        | `reports.entity_name`       | A user-defined name for the entity, such as the enterprise name or account group name |
| Billing Unit ID    | `reports.billing_unit_id`   | The ID of the billing unit  |
| Billing Unit Name  | `reports.billing_unit_name` | The name of the billing unit |
| Country Code       | `reports.country_code`      | The country code of the billing unit |
| Currency Code      | `reports.currency_code`     | The currency code of the billing unit |
| Billable Cost      | `reports.billable_cost`     | Billable charges that are aggregated from all entities in the report |
| Non Billable Cost  | `reports.non_billable_cost` | Non-billable charges that are aggregated from all entities in the report |
{: class="simple-tab-table"}
{: caption="Table 13. Enterprise usage report CSV contents for enterprise usage summary" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-2"}
{: #entity-resource-usage1-1-2}
{: tab-title="Enterprise Usage Summary"}

| CSV Header Header    | JSON Report Fields                       | Description        |
|------------------|------------------------------------------|--------------------|
| Entity ID        | `reports.entity_id`                      | The ID of the entity |
| Entity Type      | `reports.entity_type`                    | The type of the entity. \n Possible values: `enterprise`, `account-group`, or `account` |
| Parent Entity ID | `reports.parent_entity_id`               | The ID of the parent of the requested entity |
| Billing Unit ID  | `reports.billing_unit_id`                | The ID of the billing unit  |
| Currency Code    | `reports.currency_code`                  | The currency code of the billing unit |
| Service Name     | `reports.resources.resource_name`        | The name of the resource |
| Service ID       | `reports.resources.resource_id`          | The ID of the resource |
| Billable         | `reports.resources.plans.billable`       | Whether the plan charges are billed to the customer |
| Plan Name        | `reports.resources.plan_name`            | The name of the plan |
| Plan ID          | `reports.resources.plan_id`              | The ID of the plan |
| Pricing Region   | `reports.resources.plans.pricing_region` | The pricing region for the plan |
| Metric           | `reports.resources.plans.usage.metric`   | The name of the metric |
| Unit             | `reports.resources.plans.usage.unit`     | A unit to qualify the quantity |
| Quantity         | `reports.resources.plans.usage.quantity` | The aggregated value for the metric |
| Cost             | `reports.resources.plans.usage.cost`     | The cost that was incurred by the metric |
| Pending          | `reports.resources.plans.pending`        | Pending charge from classic infrastructure |
| Classic Infrastructure Product ID | `resources.usage.additional_properties.classic_infrastructure_product_id`  | Product ID of classic infrastructure resource |
| Classic Infrastructure Package ID |`resources.usage.additional_properties.classic_infrastructure_package_id` | Package ID of classic infrastructure resource |
{: class="simple-tab-table"}
{: caption="Table 13. Enterprise usage report CSV contents for enterprise resource usage" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-2"}
{: #entity-resource-usage2-1-2}
{: tab-title="Enterprise Resource Usage"}

### Enterprise account summary CSV version 1.1
{: #enterprise-account-summary-csv-version-1-1}

The following table is version 1.1. You get this version if the data that you're viewing is from March 2024 to June 2024.

| CSV Header         | Description        |
|--------------------|--------------------|
| Entity ID          | ID of the requested entity (`enterprise_id`/`account_group_id`/`account_id`) |
| Entity Type        | Type of the requested entity (enterprise/account_group/account) |
| Billing Month      | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Currency Rate      | Currency Exchange Rate with USD as the base |
| Created Time       | Timestamp at which the CSV report was generated |
| Version            | The version number of the enterprise summary CSV |
{: class="simple-tab-table"}
{: caption="Table 14. Enterprise usage report CSV contents for entity metadata" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-1"}
{: #entity-metadata-1-1}
{: tab-title="Entity Metadata"}

| CSV Header      | Description |
|--------------------|-------------|
| Entity ID          | ID of the hierarchy entity |
| Entity Type        | Type of the hierarchy entity |
| Entity Name        | Name of the hierarchy entity |
| Parent Entity ID   | ID of the parent of this hierarchy entity |
| Parent Entity Name | Name of the parent of the current hierarchy entity |
| Parent Entity Type | Type of the parent of the current hierarchy entity |
| Entity CreatedOn   | Timestamp at which the hierarchy entity was created |
{: class="simple-tab-table"}
{: caption="Table 14. Enterprise usage report CSV contents for entity hierarchy" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-1"}
{: #entity-hierarchy-1-1}
{: tab-title="Entity Hierarchy"}

| CSV Header Header          | JSON Report Fields        | Description        |
|------------------------|---------------------------|--------------------|
| Billing Unit ID        | `resources.id`         | The ID of the DEFAULT billing unit of the requested entity, which is a globally unique identifier (GUID) |
| Billing Unit Name      | `resources.name`       | The name of the billing unit |
| Billing Unit CreatedOn | `resources.created_at` | The creation date of the billing unit |
{: class="simple-tab-table"}
{: caption="Table 14. Enterprise usage report CSV contents for billing units" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-1"}
{: #billing-unit-id-enterprise-1-1}
{: tab-title="Billing Units"}

| CSV Header Header     | JSON Report Fields                        | Description        |
|-------------------|-------------------------------------------|--------------------|
| Credit Pool Type  | `resources.type`                          | The type of credit, either `PLATFORM` or `SUPPORT` |
| Currency Code     | `resources.currency_code`                 | The currency code of the associated billing unit |
| Billing Option ID | `resources.term_credits.billing_option_id`| The ID of the billing option from which the subscription term is derived |
| Category          | `resources.term_credits.category`         | The category of the credit pool. \n For platform credit the valid values are `PLATFORM`, `OFFER`, or `SERVICE` \n For support credit the valid value is `SUPPORT` |
| Start Date        | `resources.term_credits.start_date`       | The start date of the term in ISO format |
| End Date          | `resources.term_credits.end_date`         | The end date of the term in ISO format  |
| Total Credits     | `resources.term_credits.total_credits`    | The total credit available in this term |
| Starting Balance  | `resources.term_credits.starting_balance` | The balance of available credit at the start of the current month |
| Used Credits      | `resources.term_credits.used_credits`     | The amount of credit used during the current month |
| Current Balance   | `resources.term_credits.current_balance`  | The balance of remaining credit in the subscription term |
{: class="simple-tab-table"}
{: caption="Table 14. Enterprise usage report CSV contents for credit pools" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-1"}
{: #credit-pool-type-enterprise-1-1}
{: tab-title="Credit Pools"}

| CSV Header Header     | JSON Report Fields       | Description        |
|-------------------|--------------------------|--------------------|
| Credit Pool Type  | `resources.type`         | The type of credit, either `PLATFORM` or `SUPPORT` |
| Currency Code     | `resources.currency_code`| The currency code of the associated billing unit |
| Overage           | `resources.overage.cost` | The number of credits that are used as overage |
{: class="simple-tab-table"}
{: caption="Table 14. Enterprise usage report CSV contents for overages" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-1"}
{: #overages-enterprise-1-1}
{: tab-title="Overages"}

| CSV Header Header      | JSON Report Fields  | Description        |
|--------------------|---------------------|--------------------|
| Entity ID          | `reports.entity_id`         | The ID of the entity |
| Entity Type        | `reports.entity_type`       | The type of the entity  \n Possible values: `enterprise` , `account-group`, or `account` |
| Entity Name        | `reports.entity_name`       | A user-defined name for the entity, such as the enterprise name or account group name |
| Billing Unit ID    | `reports.billing_unit_id`   | The ID of the billing unit  |
| Billing Unit Name  | `reports.billing_unit_name` | The name of the billing unit |
| Country Code       | `reports.country_code`      | The country code of the billing unit |
| Currency Code      | `reports.currency_code`     | The currency code of the billing unit |
| Billable Cost      | `reports.billable_cost`     | Billable charges that are aggregated from all entities in the report |
| Non Billable Cost  | `reports.non_billable_cost` | Non-billable charges that are aggregated from all entities in the report |
{: class="simple-tab-table"}
{: caption="Table 14. Enterprise usage report CSV contents for enterprise usage summary" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-1"}
{: #entity-resource-usage1-1-1}
{: tab-title="Enterprise Usage Summary"}

| CSV Header Header    | JSON Report Fields                       | Description        |
|------------------|------------------------------------------|--------------------|
| Entity ID        | `reports.entity_id`                      | The ID of the entity |
| Entity Type      | `reports.entity_type`                    | The type of the entity. \n Possible values: `enterprise`, `account-group`, or `account` |
| Parent Entity ID | `reports.parent_entity_id`               | The ID of the parent of the requested entity |
| Billing Unit ID  | `reports.billing_unit_id`                | The ID of the billing unit  |
| Currency Code    | `reports.currency_code`                  | The currency code of the billing unit |
| Service Name     | `reports.resources.resource_name`        | The name of the resource |
| Service ID       | `reports.resources.resource_id`          | The ID of the resource |
| Billable         | `reports.resources.plans.billable`       | Whether the plan charges are billed to the customer |
| Plan Name        | `reports.resources.plan_name`            | The name of the plan |
| Plan ID          | `reports.resources.plan_id`              | The ID of the plan |
| Pricing Region   | `reports.resources.plans.pricing_region` | The pricing region for the plan |
| Metric           | `reports.resources.plans.usage.metric`   | The name of the metric |
| Unit             | `reports.resources.plans.usage.unit`     | A unit to qualify the quantity |
| Quantity         | `reports.resources.plans.usage.quantity` | The aggregated value for the metric |
| Cost             | `reports.resources.plans.usage.cost`     | The cost that was incurred by the metric |
| Pending          | `reports.resources.plans.pending`        | Pending charge from classic infrastructure |
| Classic Infrastructure Product ID | `resources.usage.additional_properties.classic_infrastructure_product_id`  | Product ID of classic infrastructure resource |
| Classic Infrastructure Package ID |`resources.usage.additional_properties.classic_infrastructure_package_id` | Package ID of classic infrastructure resource |
{: class="simple-tab-table"}
{: caption="Table 14. Enterprise usage report CSV contents for enterprise resource usage" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-1"}
{: #entity-resource-usage2-1-1}
{: tab-title="Enterprise Resource Usage"}


### Enterprise account summary CSV version 1.0
{: #enterprise-account-summary-csv-version-1-0}

You will get CSV version 1.0 if the data that you're viewing is from October 2024 to March 2024.

| CSV Header         | Description        |
|--------------------|--------------------|
| Entity ID          | ID of the requested entity (`enterprise_id`/`account_group_id`/`account_id`) |
| Entity Type        | Type of the requested entity (enterprise/account_group/account) |
| Billing Month      | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Currency Rate      | Currency Exchange Rate with USD as the base |
| Created Time       | Timestamp at which the CSV report was generated |
{: class="simple-tab-table"}
{: caption="Table 15. Enterprise usage report CSV contents for entity metadata" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-0"}
{: #entity-metadata-1-0}
{: tab-title="Entity Metadata"}

| CSV Header      | Description |
|--------------------|-------------|
| Entity ID          | ID of the hierarchy entity |
| Entity Type        | Type of the hierarchy entity |
| Entity Name        | Name of the hierarchy entity |
| Parent Entity ID   | ID of the parent of this hierarchy entity |
| Parent Entity Name | Name of the parent of the current hierarchy entity |
| Parent Entity Type | Type of the parent of the current hierarchy entity |
| Entity CreatedOn   | Timestamp at which the hierarchy entity was created |
{: class="simple-tab-table"}
{: caption="Table 15. Enterprise usage report CSV contents for entity hierarchy" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-0"}
{: #entity-hierarchy-1-0}
{: tab-title="Entity Hierarchy"}

| CSV Header Header          | JSON Report Fields        | Description        |
|------------------------|---------------------------|--------------------|
| Billing Unit ID        | `resources.id`         | The ID of the DEFAULT billing unit of the requested entity, which is a globally unique identifier (GUID) |
| Billing Unit Name      | `resources.name`       | The name of the billing unit |
| Billing Unit CreatedOn | `resources.created_at` | The creation date of the billing unit |
{: class="simple-tab-table"}
{: caption="Table 15. Enterprise usage report CSV contents for billing units" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-0"}
{: #billing-unit-id-enterprise-1-0}
{: tab-title="Billing Units"}

| CSV Header Header     | JSON Report Fields                        | Description        |
|-------------------|-------------------------------------------|--------------------|
| Credit Pool Type  | `resources.type`                          | The type of credit, either `PLATFORM` or `SUPPORT` |
| Currency Code     | `resources.currency_code`                 | The currency code of the associated billing unit |
| Billing Option ID | `resources.term_credits.billing_option_id`| The ID of the billing option from which the subscription term is derived |
| Category          | `resources.term_credits.category`         | The category of the credit pool. \n For platform credit the valid values are `PLATFORM`, `OFFER`, or `SERVICE` \n For support credit the valid value is `SUPPORT` |
| Start Date        | `resources.term_credits.start_date`       | The start date of the term in ISO format |
| End Date          | `resources.term_credits.end_date`         | The end date of the term in ISO format  |
| Total Credits     | `resources.term_credits.total_credits`    | The total credit available in this term |
| Starting Balance  | `resources.term_credits.starting_balance` | The balance of available credit at the start of the current month |
| Used Credits      | `resources.term_credits.used_credits`     | The amount of credit used during the current month |
| Current Balance   | `resources.term_credits.current_balance`  | The balance of remaining credit in the subscription term |
{: class="simple-tab-table"}
{: caption="Table 15. Enterprise usage report CSV contents for credit pools" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-0"}
{: #credit-pool-type-enterprise-1-0}
{: tab-title="Credit Pools"}

| CSV Header Header     | JSON Report Fields       | Description        |
|-------------------|--------------------------|--------------------|
| Credit Pool Type  | `resources.type`         | The type of credit, either `PLATFORM` or `SUPPORT` |
| Currency Code     | `resources.currency_code`| The currency code of the associated billing unit |
| Overage           | `resources.overage.cost` | The number of credits that are used as overage |
{: class="simple-tab-table"}
{: caption="Table 15. Enterprise usage report CSV contents for overages" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-0"}
{: #overages-enterprise-1-0}
{: tab-title="Overages"}

| CSV Header Header      | JSON Report Fields  | Description        |
|--------------------|---------------------|--------------------|
| Entity ID          | `reports.entity_id`         | The ID of the entity |
| Entity Type        | `reports.entity_type`       | The type of the entity  \n Possible values: `enterprise` , `account-group`, or `account` |
| Entity Name        | `reports.entity_name`       | A user-defined name for the entity, such as the enterprise name or account group name |
| Billing Unit ID    | `reports.billing_unit_id`   | The ID of the billing unit  |
| Billing Unit Name  | `reports.billing_unit_name` | The name of the billing unit |
| Country Code       | `reports.country_code`      | The country code of the billing unit |
| Currency Code      | `reports.currency_code`     | The currency code of the billing unit |
| Billable Cost      | `reports.billable_cost`     | Billable charges that are aggregated from all entities in the report |
| Non Billable Cost  | `reports.non_billable_cost` | Non-billable charges that are aggregated from all entities in the report |
{: class="simple-tab-table"}
{: caption="Table 15. Enterprise usage report CSV contents for enterprise usage summary" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-0"}
{: #entity-resource-usage1-1-0}
{: tab-title="Enterprise Usage Summary"}

| CSV Header Header    | JSON Report Fields                       | Description        |
|------------------|------------------------------------------|--------------------|
| Entity ID        | `reports.entity_id`                      | The ID of the entity |
| Entity Type      | `reports.entity_type`                    | The type of the entity. \n Possible values: `enterprise`, `account-group`, or `account` |
| Parent Entity ID | `reports.parent_entity_id`               | The ID of the parent of the requested entity |
| Billing Unit ID  | `reports.billing_unit_id`                | The ID of the billing unit  |
| Currency Code    | `reports.currency_code`                  | The currency code of the billing unit |
| Service Name     | `reports.resources.resource_name`        | The name of the resource |
| Service ID       | `reports.resources.resource_id`          | The ID of the resource |
| Billable         | `reports.resources.plans.billable`       | Whether the plan charges are billed to the customer |
| Plan Name        | `reports.resources.plan_name`            | The name of the plan |
| Plan ID          | `reports.resources.plan_id`              | The ID of the plan |
| Pricing Region   | `reports.resources.plans.pricing_region` | The pricing region for the plan |
| Metric           | `reports.resources.plans.usage.metric`   | The name of the metric |
| Unit             | `reports.resources.plans.usage.unit`     | A unit to qualify the quantity |
| Quantity         | `reports.resources.plans.usage.quantity` | The aggregated value for the metric |
| Cost             | `reports.resources.plans.usage.cost`     | The cost that was incurred by the metric |
| Pending          | `reports.resources.plans.pending`        | Pending charge from classic infrastructure |
| Classic Infrastructure Product ID | `resources.usage.additional_properties.classic_infrastructure_product_id`  | Product ID of classic infrastructure resource |
| Classic Infrastructure Package ID |`resources.usage.additional_properties.classic_infrastructure_package_id` | Package ID of classic infrastructure resource |
{: class="simple-tab-table"}
{: caption="Table 15. Enterprise usage report CSV contents for enterprise resource usage" caption-side="bottom"}
{: tab-group="enterprise-account-summary-1-0"}
{: #entity-resource-usage2-1-0}
{: tab-title="Enterprise Resource Usage"}

### Enterprise account summary CSV version 0.2
{: #enterprise-account-summary-csv-version-0-2}

You will get CSV version 0.2 if the data that you're viewing is from February 2023 to October 2024.

| CSV Header         | Description        |
|--------------------|--------------------|
| Entity ID          | ID of the requested entity (`enterprise_id`/`account_group_id`/`account_id`) |
| Entity Type        | Type of the requested entity (enterprise/account_group/account) |
| Billing Month      | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Currency Rate      | Currency Exchange Rate with USD as the base |
| Created Time       | Timestamp at which the CSV report was generated |
{: class="simple-tab-table"}
{: caption="Table 16. Enterprise usage report CSV contents for entity metadata" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-2"}
{: #entity-metadata-0-2}
{: tab-title="Entity Metadata"}

| CSV Header      | Description |
|--------------------|-------------|
| Entity ID          | ID of the hierarchy entity |
| Entity Type        | Type of the hierarchy entity |
| Entity Name        | Name of the hierarchy entity |
| Parent Entity ID   | ID of the parent of this hierarchy entity |
| Parent Entity Name | Name of the parent of the current hierarchy entity |
| Parent Entity Type | Type of the parent of the current hierarchy entity |
| Entity CreatedOn   | Timestamp at which the hierarchy entity was created |
{: class="simple-tab-table"}
{: caption="Table 16. Enterprise usage report CSV contents for entity hierarchy" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-2"}
{: #entity-hierarchy-0-2}
{: tab-title="Entity Hierarchy"}

| CSV Header Header          | JSON Report Fields        | Description        |
|------------------------|---------------------------|--------------------|
| Billing Unit ID        | `resources.id`         | The ID of the DEFAULT billing unit of the requested entity, which is a globally unique identifier (GUID) |
| Billing Unit Name      | `resources.name`       | The name of the billing unit |
| Billing Unit CreatedOn | `resources.created_at` | The creation date of the billing unit |
{: class="simple-tab-table"}
{: caption="Table 16. Enterprise usage report CSV contents for billing units" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-2"}
{: #billing-unit-id-enterprise-0-2}
{: tab-title="Billing Units"}

| CSV Header Header     | JSON Report Fields                        | Description        |
|-------------------|-------------------------------------------|--------------------|
| Credit Pool Type  | `resources.type`                          | The type of credit, either `PLATFORM` or `SUPPORT` |
| Currency Code     | `resources.currency_code`                 | The currency code of the associated billing unit |
| Billing Option ID | `resources.term_credits.billing_option_id`| The ID of the billing option from which the subscription term is derived |
| Category          | `resources.term_credits.category`         | The category of the credit pool. \n For platform credit the valid values are `PLATFORM`, `OFFER`, or `SERVICE` \n For support credit the valid value is `SUPPORT` |
| Start Date        | `resources.term_credits.start_date`       | The start date of the term in ISO format |
| End Date          | `resources.term_credits.end_date`         | The end date of the term in ISO format  |
| Total Credits     | `resources.term_credits.total_credits`    | The total credit available in this term |
| Starting Balance  | `resources.term_credits.starting_balance` | The balance of available credit at the start of the current month |
| Used Credits      | `resources.term_credits.used_credits`     | The amount of credit used during the current month |
| Current Balance   | `resources.term_credits.current_balance`  | The balance of remaining credit in the subscription term |
{: class="simple-tab-table"}
{: caption="Table 16. Enterprise usage report CSV contents for credit pools" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-2"}
{: #credit-pool-type-enterprise-0-2}
{: tab-title="Credit Pools"}

| CSV Header Header     | JSON Report Fields       | Description        |
|-------------------|--------------------------|--------------------|
| Credit Pool Type  | `resources.type`         | The type of credit, either `PLATFORM` or `SUPPORT` |
| Currency Code     | `resources.currency_code`| The currency code of the associated billing unit |
| Overage           | `resources.overage.cost` | The number of credits that are used as overage |
{: class="simple-tab-table"}
{: caption="Table 16. Enterprise usage report CSV contents for overages" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-2"}
{: #overages-enterprise-0-2}
{: tab-title="Overages"}

| CSV Header Header      | JSON Report Fields  | Description        |
|--------------------|---------------------|--------------------|
| Entity ID          | `reports.entity_id`         | The ID of the entity |
| Entity Type        | `reports.entity_type`       | The type of the entity  \n Possible values: `enterprise` , `account-group`, or `account` |
| Entity Name        | `reports.entity_name`       | A user-defined name for the entity, such as the enterprise name or account group name |
| Billing Unit ID    | `reports.billing_unit_id`   | The ID of the billing unit  |
| Billing Unit Name  | `reports.billing_unit_name` | The name of the billing unit |
| Country Code       | `reports.country_code`      | The country code of the billing unit |
| Currency Code      | `reports.currency_code`     | The currency code of the billing unit |
| Billable Cost      | `reports.billable_cost`     | Billable charges that are aggregated from all entities in the report |
| Non Billable Cost  | `reports.non_billable_cost` | Non-billable charges that are aggregated from all entities in the report |
{: class="simple-tab-table"}
{: caption="Table 16. Enterprise usage report CSV contents for enterprise usage summary" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-2"}
{: #entity-resource-usage1-0-2}
{: tab-title="Enterprise Usage Summary"}

| CSV Header Header    | JSON Report Fields                       | Description        |
|------------------|------------------------------------------|--------------------|
| Entity ID        | `reports.entity_id`                      | The ID of the entity |
| Entity Type      | `reports.entity_type`                    | The type of the entity. \n Possible values: `enterprise`, `account-group`, or `account` |
| Parent Entity ID | `reports.parent_entity_id`               | The ID of the parent of the requested entity |
| Billing Unit ID  | `reports.billing_unit_id`                | The ID of the billing unit  |
| Currency Code    | `reports.currency_code`                  | The currency code of the billing unit |
| Service Name     | `reports.resources.resource_name`        | The name of the resource |
| Service ID       | `reports.resources.resource_id`          | The ID of the resource |
| Billable         | `reports.resources.plans.billable`       | Whether the plan charges are billed to the customer |
| Plan Name        | `reports.resources.plan_name`            | The name of the plan |
| Plan ID          | `reports.resources.plan_id`              | The ID of the plan |
| Pricing Region   | `reports.resources.plans.pricing_region` | The pricing region for the plan |
| Metric           | `reports.resources.plans.usage.metric`   | The name of the metric |
| Unit             | `reports.resources.plans.usage.unit`     | A unit to qualify the quantity |
| Quantity         | `reports.resources.plans.usage.quantity` | The aggregated value for the metric |
| Cost             | `reports.resources.plans.usage.cost`     | The cost that was incurred by the metric |
| Pending          | `reports.resources.plans.pending`        | Pending charge from classic infrastructure |
{: class="simple-tab-table"}
{: caption="Table 16. Enterprise usage report CSV contents for enterprise resource usage" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-2"}
{: #entity-resource-usage2-0-2}
{: tab-title="Enterprise Resource Usage"}

### Enterprise account summary CSV version 0.1
{: #enterprise-account-summary-csv-version-0-1}

You will get CSV version 0.1 if the data that you're viewing is from before February 2023.

| CSV Header         | Description        |
|--------------------|--------------------|
| Entity ID          | ID of the requested entity (`enterprise_id`/`account_group_id`/`account_id`) |
| Entity Type        | Type of the requested entity (enterprise/account_group/account) |
| Billing Month      | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Created Time       | Timestamp at which the CSV report was generated |
{: class="simple-tab-table"}
{: caption="Table 17. Enterprise usage report CSV contents for entity metadata" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-1"}
{: #entity-metadata-0-1}
{: tab-title="Entity Metadata"}

| CSV Header      | Description |
|--------------------|-------------|
| Entity ID          | ID of the hierarchy entity |
| Entity Type        | Type of the hierarchy entity |
| Entity Name        | Name of the hierarchy entity |
| Parent Entity ID   | ID of the parent of this hierarchy entity |
| Parent Entity Name | Name of the parent of the current hierarchy entity |
| Parent Entity Type | Type of the parent of the current hierarchy entity |
| Entity CreatedOn   | Timestamp at which the hierarchy entity was created |
{: class="simple-tab-table"}
{: caption="Table 17. Enterprise usage report CSV contents for entity hierarchy" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-1"}
{: #entity-hierarchy-0-1}
{: tab-title="Entity Hierarchy"}

| CSV Header Header          | JSON Report Fields        | Description        |
|------------------------|---------------------------|--------------------|
| Billing Unit ID        | `resources.id`         | The ID of the DEFAULT billing unit of the requested entity, which is a globally unique identifier (GUID) |
| Billing Unit Name      | `resources.name`       | The name of the billing unit |
| Billing Unit CreatedOn | `resources.created_at` | The creation date of the billing unit |
{: class="simple-tab-table"}
{: caption="Table 17. Enterprise usage report CSV contents for billing units" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-1"}
{: #billing-unit-id-enterprise-0-1}
{: tab-title="Billing Units"}

| CSV Header Header     | JSON Report Fields                        | Description        |
|-------------------|-------------------------------------------|--------------------|
| Credit Pool Type  | `resources.type`                          | The type of credit, either `PLATFORM` or `SUPPORT` |
| Currency Code     | `resources.currency_code`                 | The currency code of the associated billing unit |
| Billing Option ID | `resources.term_credits.billing_option_id`| The ID of the billing option from which the subscription term is derived |
| Category          | `resources.term_credits.category`         | The category of the credit pool. \n For platform credit the valid values are `PLATFORM`, `OFFER`, or `SERVICE` \n For support credit the valid value is `SUPPORT` |
| Start Date        | `resources.term_credits.start_date`       | The start date of the term in ISO format |
| End Date          | `resources.term_credits.end_date`         | The end date of the term in ISO format  |
| Total Credits     | `resources.term_credits.total_credits`    | The total credit available in this term |
| Starting Balance  | `resources.term_credits.starting_balance` | The balance of available credit at the start of the current month |
| Used Credits      | `resources.term_credits.used_credits`     | The amount of credit used during the current month |
| Current Balance   | `resources.term_credits.current_balance`  | The balance of remaining credit in the subscription term |
{: class="simple-tab-table"}
{: caption="Table 17. Enterprise usage report CSV contents for credit pools" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-1"}
{: #credit-pool-type-enterprise-0-1}
{: tab-title="Credit Pools"}

| CSV Header Header     | JSON Report Fields       | Description        |
|-------------------|--------------------------|--------------------|
| Credit Pool Type  | `resources.type`         | The type of credit, either `PLATFORM` or `SUPPORT` |
| Currency Code     | `resources.currency_code`| The currency code of the associated billing unit |
| Overage           | `resources.overage.cost` | The number of credits that are used as overage |
{: class="simple-tab-table"}
{: caption="Table 17. Enterprise usage report CSV contents for overages" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-1"}
{: #overages-enterprise-0-1}
{: tab-title="Overages"}

| CSV Header Header      | JSON Report Fields  | Description        |
|--------------------|---------------------|--------------------|
| Entity ID          | `reports.entity_id`         | The ID of the entity |
| Entity Type        | `reports.entity_type`       | The type of the entity  \n Possible values: `enterprise` , `account-group`, or `account` |
| Entity Name        | `reports.entity_name`       | A user-defined name for the entity, such as the enterprise name or account group name |
| Billing Unit ID    | `reports.billing_unit_id`   | The ID of the billing unit  |
| Billing Unit Name  | `reports.billing_unit_name` | The name of the billing unit |
| Country Code       | `reports.country_code`      | The country code of the billing unit |
| Currency Code      | `reports.currency_code`     | The currency code of the billing unit |
| Billable Cost      | `reports.billable_cost`     | Billable charges that are aggregated from all entities in the report |
| Non Billable Cost  | `reports.non_billable_cost` | Non-billable charges that are aggregated from all entities in the report |
{: class="simple-tab-table"}
{: caption="Table 17. Enterprise usage report CSV contents for enterprise usage summary" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-1"}
{: #entity-resource-usage1-0-1}
{: tab-title="Enterprise Usage Summary"}

| CSV Header Header    | JSON Report Fields                       | Description        |
|------------------|------------------------------------------|--------------------|
| Entity ID        | `reports.entity_id`                      | The ID of the entity |
| Entity Type      | `reports.entity_type`                    | The type of the entity. \n Possible values: `enterprise`, `account-group`, or `account` |
| Parent Entity ID | `reports.parent_entity_id`               | The ID of the parent of the requested entity |
| Billing Unit ID  | `reports.billing_unit_id`                | The ID of the billing unit  |
| Currency Code    | `reports.currency_code`                  | The currency code of the billing unit |
| Service Name     | `reports.resources.resource_name`        | The name of the resource |
| Service ID       | `reports.resources.resource_id`          | The ID of the resource |
| Billable         | `reports.resources.plans.billable`       | Whether the plan charges are billed to the customer |
| Plan Name        | `reports.resources.plan_name`            | The name of the plan |
| Plan ID          | `reports.resources.plan_id`              | The ID of the plan |
| Pricing Region   | `reports.resources.plans.pricing_region` | The pricing region for the plan |
| Metric           | `reports.resources.plans.usage.metric`   | The name of the metric |
| Unit             | `reports.resources.plans.usage.unit`     | A unit to qualify the quantity |
| Quantity         | `reports.resources.plans.usage.quantity` | The aggregated value for the metric |
| Cost             | `reports.resources.plans.usage.cost`     | The cost that was incurred by the metric |
| Pending          | `reports.resources.plans.pending`        | Pending charge from classic infrastructure |
{: class="simple-tab-table"}
{: caption="Table 17. Enterprise usage report CSV contents for enterprise resource usage" caption-side="bottom"}
{: tab-group="enterprise-account-summary-0-1"}
{: #entity-resource-usage2-0-1}
{: tab-title="Enterprise Resource Usage"}
