---

copyright:
  years: 2024

lastupdated: "2024-11-11"

keywords: pricing, global catalog api

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Getting dynamic pricing
{: #getting-pricing-api}

As a seller, reseller, or a user that wants to pull pricing programmatically, you may want to get pricing dynamically so that you can quote true prices and do cost predictions on what a service or software is going to cost. To do this, you can leverage the Global Catalog API to get that dynamic pricing. To use the API, you need to have the correct [authentication](/apidocs/resource-catalog/global-catalog#authentication).
{: shortdesc}

## Getting pricing
{: #getting-pricing}

You can use the [Global Catalog API](/apidocs/resource-catalog/global-catalog#intro) to find regional pricing for a service but you need to know the object's ID. For each object of the service, there is a different ID. The best way to find the ID is to use the Global Catalog UI. As an example, with the following steps, we'll find the deployment plan ID for Cloud Object Storage.

1. Go to the [Global Catalog](https://globalcatalog.cloud.ibm.com/){: external} and click **Global Catalog Search**.
1. Search for `Cloud Object Storage` and select **Object Storage** from the results. The service we want will have the display name `Object Storage` and the name `object-storage-group`.
1. From the navigation menu, select **Cloud Object Storage** > **Standard** > **Premium Global Deployment**.
1. Select the **Overview** tab to view the deployment ID. For Cloud Object storage, it is `744bfc56-d12c-4866-88d5-dac9139e0e5d:global`.

Now that you know the ID for the object, you can use the following steps to get pricing.

You can use {{site.data.keyword.cloud-shell_full}} to enter commands. For more information, see [Working in Cloud Shell](/docs/cloud-shell?topic=cloud-shell-shell-ui).
{: tip}

1. Run the following command to call the Global Catalog pricing API for the global deployment plan ID.

   ```sh
   curl --request GET
   --url 'https://globalcatalog.cloud.ibm.com/api/v1/744bfc56-d12c-4866-88d5-dac9139e0e5d:global/pricing'
   --header 'accept: application/json'
   ```
   {: codeblock}
   {: curl}

   The response includes the list of pricing deployment regions. Look for `deployment_regions` in the response. For Cloud Object Storage, you'll find that the available regions are `us-south`, `us-east`, and `eu-de`.
1. Call the pricing API again, but this time add the query parameter `deployment_regions` and specify one of the regions that is contained within the list. For this example, we'll use `us-south`.

   ```sh
   curl --request GET
   --url 'https://globalcatalog.cloud.ibm.com/api/v1/744bfc56-d12c-4866-88d5-dac9139e0e5d:global/pricing?deployment_region=us-south'
   --header 'accept: application/json'
   ```
   {: codeblock}
   {: curl}

1. Repeat step three as needed to get pricing for all regions.


### Example response
{: #example-response}

The following is an example response for the curl command from the previous steps. For more information, see [Understanding JSON fields](#understanding-json-fields).

```
{
  "deployment_id": "744bfc56-d12c-4866-88d5-dac9139e0e5d:global",
  "deployment_location": "global",
  "deployment_region": "us-south",
  "origin": "pricing_catalog",
  "type": "paygo",
  "url": "https://globalcatalog.cloud.ibm.com/api/v1/744bfc56-d12c-4866-88d5-dac9139e0e5d:global/pricing?deployment_region=us-south",
  "i18n": {},
  "starting_price": {},
  "effective_from": "2024-09-01T00:00:00Z",
  "effective_until": "9999-12-31T00:00:00Z",
  "metrics": [
    {
      "part_ref": "",
      "metric_id": "COSSTDBAND",
      "tier_model": "Step Tier",
      "resource_display_name": "Standard bandwidth",
      "charge_unit_display_name": "GIGABYTE",
      "charge_unit_name": "STANDARD_BANDWIDTH",
      "charge_unit": "GIGABYTE",
      "charge_unit_quantity": 1,
      "amounts": [
        {
          "country": "USA",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "USD",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "EURO",
          "currency": "EUR",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.080997165
            },
            {
              "quantity_tier": 150000,
              "price": 0.06299779500000001
            },
            {
              "quantity_tier": 999999999,
              "price": 0.044998425
            }
          ]
        },
        {
          "country": "ARG",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "CAN",
          "currency": "CAD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.12269699999999999
            },
            {
              "quantity_tier": 150000,
              "price": 0.095431
            },
            {
              "quantity_tier": 999999999,
              "price": 0.068165
            }
          ]
        },
        {
          "country": "AUS",
          "currency": "AUD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.13348164599999998
            },
            {
              "quantity_tier": 150000,
              "price": 0.103819058
            },
            {
              "quantity_tier": 999999999,
              "price": 0.07415647
            }
          ]
        },
        {
          "country": "ISA",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "BOL",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "BRA",
          "currency": "BRL",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.45585000000000003
            },
            {
              "quantity_tier": 150000,
              "price": 0.3545500000000001
            },
            {
              "quantity_tier": 999999999,
              "price": 0.25325000000000003
            }
          ]
        },
        {
          "country": "ASEAN",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "CHE",
          "currency": "CHF",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.07711649999999999
            },
            {
              "quantity_tier": 150000,
              "price": 0.059979500000000005
            },
            {
              "quantity_tier": 999999999,
              "price": 0.042842500000000006
            }
          ]
        },
        {
          "country": "CHL",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "NZL",
          "currency": "NZD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.146412882
            },
            {
              "quantity_tier": 150000,
              "price": 0.113876686
            },
            {
              "quantity_tier": 999999999,
              "price": 0.08134049
            }
          ]
        },
        {
          "country": "COL",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "DNK",
          "currency": "DKK",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.6043995
            },
            {
              "quantity_tier": 150000,
              "price": 0.4700885000000001
            },
            {
              "quantity_tier": 999999999,
              "price": 0.33577750000000006
            }
          ]
        },
        {
          "country": "ECU",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "GBR",
          "currency": "GBP",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.069068727
            },
            {
              "quantity_tier": 150000,
              "price": 0.053720121
            },
            {
              "quantity_tier": 999999999,
              "price": 0.038371515
            }
          ]
        },
        {
          "country": "HKG",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "IDN",
          "currency": "IDR",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 1389.195
            },
            {
              "quantity_tier": 150000,
              "price": 1080.4850000000001
            },
            {
              "quantity_tier": 999999999,
              "price": 771.7750000000001
            }
          ]
        },
        {
          "country": "IND",
          "currency": "INR",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 7.5412125
            },
            {
              "quantity_tier": 150000,
              "price": 5.865387500000001
            },
            {
              "quantity_tier": 999999999,
              "price": 4.1895625
            }
          ]
        },
        {
          "country": "JPN",
          "currency": "JPY",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 13.104449999999998
            },
            {
              "quantity_tier": 150000,
              "price": 10.192350000000001
            },
            {
              "quantity_tier": 999999999,
              "price": 7.28025
            }
          ]
        },
        {
          "country": "KOR",
          "currency": "KRW",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 119.8917
            },
            {
              "quantity_tier": 150000,
              "price": 93.24910000000001
            },
            {
              "quantity_tier": 999999999,
              "price": 66.60650000000001
            }
          ]
        },
        {
          "country": "MEX",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "NOR",
          "currency": "NOK",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.945603
            },
            {
              "quantity_tier": 150000,
              "price": 0.7354690000000002
            },
            {
              "quantity_tier": 999999999,
              "price": 0.525335
            }
          ]
        },
        {
          "country": "PER",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "SWE",
          "currency": "SEK",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.9217664999999999
            },
            {
              "quantity_tier": 150000,
              "price": 0.7169295
            },
            {
              "quantity_tier": 999999999,
              "price": 0.5120925
            }
          ]
        },
        {
          "country": "TWN",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "VEN",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
        {
          "country": "ZAF",
          "currency": "ZAR",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 1.608147
            },
            {
              "quantity_tier": 150000,
              "price": 1.2507810000000001
            },
            {
              "quantity_tier": 999999999,
              "price": 0.8934150000000001
            }
          ]
        }
```
{: codeblock}

#### Understanding JSON fields
{: #understanding-json-fields}

The following table shows the response body fields and their descriptions. For more information, see the [Global Catalog API documentation](/apidocs/resource-catalog/global-catalog).

| JSON field                 | Description |
|----------------------------|-------------|
| `deployment_id`            | The deployment object ID this pricing is from. |
| `deployment_location`      | The deployment location this pricing is from. Such as `global`. |
| `deployment_region`        | This is the region where the deployment plan is to retrieve plan pricing for a global deployment. For this example it is `us-south`.  |
| `origin`                   | Where the pricing data comes from. For this example, it's `pricing_catalog` and is designated by the Pricing Source in the Global Catalog UI. |
| `type`                     | Type of plan. Valid values are `free`, `trial`, `paygo`, `bluemix-subscription`, and `ibm-subscription`. For more information, see [Account types](/docs/account?topic=account-accounts). |
| `url`                      | The url for the artifact. This is the url that you can use to get pricing. |
| `starting_price`           | Plan-specific starting price information. |
| `effective_from`           | The start date for the available pricing. |
| `effective_until`          | The end date for the available pricing. |
| `metrics`                  | Specifications of resources or operations that determine usage for pricing. |
| `part_ref`                 | The IBM assigned part reference number for the metric. |
| `metric_id`                | The metric ID or part number. |
| `tier_model`               | The tier model. For example, `Granular Tier`, `Step Tier`, `Simple Tier`, `Linear Tier`, and `Graduated Tier`. For more information, see [How you're charged](/docs/account?topic=account-charges#charges-services). |
| `resource_display_name`    | Display name of the resource. This is how the metric appears in the catalog. |
| `charge_unit_display_name` | Display name of the charge unit. Unit friendly display name for the `charge_unit`. |
| `charge_unit_name`         | An assigned name for the charge unit. This is the ID that is used to measure usages for the metric. |
| `charge_unit`              | This is the chargable unit. For this example, it's `GIGABYTE`. |
| `charge_unit_quantity`     | The chargable unit quantity. In the example response, the charge unit is 1, which means you are charged for each gigabyte used. |
| `amounts`                  | The pricing per metric by country and currency. |
| `country`                  | Country for which this object's price is applicable. |
| `currency`                 | Currency for the prices. |
| `quantity_tier`            | Level of usage for that price in that tier. |
| `price`                    | Price per unit for this tier. Since the `charge_unit_quantity` is `1`, and the `charge_unit` is `GIGABYTE`, you are charged for each gigabyte. Also, since this is step tier pricing model, you're charged .09 USD for each gigabyte, up to 50,000, and .07 USD for units between 50,000 and 150,000. |
{: caption="Example response JSON fields" caption-side="bottom"}
