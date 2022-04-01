---

copyright:

  years: 2022

lastupdated: "2022-04-01"

keywords: software onboarding, controls, requirements, security, compliance, partners 

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Formatting controls in your readme file
{: #catalog-format-controls}

When you onboard your product to a private catalog, the security and compliance controls that are in your readme file are scanned, validated, and included in your product's information. After you share your product or publish to your account, users can view your controls. 
{: shortdesc}

## Control format
{: #catalog-control-format}

During the onboarding process, controls that are in your readme file and formatted correctly are moved to the Security and compliance table in your private catalog. To include controls with your product's information, make sure that the controls are listed in one table with: 
- a Profile column
- an ID column

You can include more columns in the readme file's control table; however, this information might be overwritten or excluded. 

### Examples
{: #catalog-controls-example}

The following example tables show how you can format your controls in your readme file. 

```markdown
| Profile | ID |
|---------|----|
| NIST | SC-7(3) |
```
{: codeblock}

```markdown
| Profile | Category | ID      | Description |
|---------|----------|---------|-------------|
| NIST | [SC-7](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#/control?version=4.0&number=SC-7) | SC-7(3) | Limit the number of external network connections to the system. |
```
{: codeblock}
