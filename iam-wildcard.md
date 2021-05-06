---

copyright:

  years: 2019, 2020

lastupdated: "2020-05-06"

keywords: access, users, service IDs, access group, IAM, policy, characters, wildcard, operators, asterisk, question mark, *, ?, JSON document, policy document

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:term: .term}

# Assigning access by using wildcard policies
{: #wildcard}

When you're assigning access to certain IAM-enabled services, you can use advanced operators in a [policy](#x2853407){: term} to grant access to resources that satisfy specific naming conventions. By using wildcard policies, you can reduce the number of policies that are required for managing access to some resources.
{:shortdesc}

To assign access, you need the administrator role on the resource. For more information, see [IAM access](/docs/account?topic=account-userroles).

## JSON policy document
{: #policy-js}

Most access policies are stored in {{site.data.keyword.cloud}} as JSON documents. When you use the `stringEquals` operator in a policy, an exact string match is performed between the query and the target string. When you use the `stringMatch` operator, a case-sensitive string match is performed between the pattern and the target string using either an asterisk (`*`), question mark (`?`), or both. An asterisk (`*`) represents any sequence of zero or more characters in the string, and a question mark (`?`) represents any single character. See the following examples:

  * `*dev*` matches any string that contains `dev`
  * `dev*` matches any string that begins with `dev`
  * `*dev` matches any string that ends with `dev`

Refer to the documentation for the specific service that you are assigning access to for details about the supported operators for specific attributes for that service.
{: note}

### Using an asterisk (`*`) as a wildcard
{: #policy-doc-asterisk} 

The following example shows how you might create a policy that gives a user access to manage all {{site.data.keyword.messagehub}} topics that start with `dev` in a particular account. 

```
{
    "type": "access",
    "subjects": [
        {
            "attributes": [
                {
                    "name": "iam_id",
                    "value": "IBMid-12345"
                }
            ]
        }
    ],
    "roles": [
        {
            "role_id": "crn:v1:bluemix:public:iam::::serviceRole:Manager"
        }
    ],
    "resources": [
        {
            "attributes": [
                {
                    "name": "accountId",
                    "value": "d727f71e99b14534b3267fab8cc9b09a"
                },
                {
                    "name": "serviceName",
                    "value": "messagehub"
                },
                {
                    "name": "resourceType",
                    "value": "topic"
                },
                {
                    "name": "resource",
                    "operator": "stringMatch",
                    "value": "dev*"
                }
            ]
        }
    ]
}
```
{: codeblock}

### Using a question mark (`?`) as a wildcard
{: #policy-doc-multiwildcards} 

The following example shows how you can create a policy that gives a user access to edit any {{site.data.keyword.messagehub}} topic that ends in `81` with two characters before the numerical characters in a particular account. 

```
{
    "type": "access",
    "subjects": [
        {
            "attributes": [
                {
                    "name": "iam_id",
                    "value": "IBMid-12345"
                }
            ]
        }
    ],
    "roles": [
        {
            "role_id": "crn:v1:bluemix:public:iam::::serviceRole:Writer"
        }
    ],
    "resources": [
        {
            "attributes": [
                {
                    "name": "accountId",
                    "value": "d727f71e99b14534b3267fab8cc9b09a"
                },
                {
                    "name": "serviceName",
                    "value": "messagehub"
                },
                {
                    "name": "resourceType",
                    "operator": "stringEquals"
                    "value": "topic",
                },
                {
                    "name": "resource",
                    "operator": "stringMatch",
                    "value": "*??81"
                }
            ]
        }
    ]
}
```
{: codeblock}



