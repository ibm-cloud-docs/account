---

copyright:
  years: 2021
lastupdated: "2021-02-17"

keywords: account best practices, best practices account, security best practice

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:term: .term}

**WIP**
# Best practices for securing your account
{: #bp-secure-account}

Take time to review the suggested best practices to lower you security risks for all production, staging, and test servers in your cloud infrastructure. This list is an excellent starting point to increase the security of your cloud infrastructure. Go through the lists and follow the links to improve the security of your account.
{: shortdesc}


## What makes a good resource group strategy?
{: #security-strategy}

- Identity and access management
- Networking
- Server hardening
- Data protection

## Identity and access management
{: #bp-security-iam}

IAM enables you to securely authenticate users for platform services and control access to resources.
- IAM users are attached to access groups
  - [Setting up access groups](/docs/account?topic=account-groups)
- IAM policies are attached to groups and roles no individual users
  - [Managing access to resources](/docs/account?topic=account-assign-access-resources)
- attach users to resource groups
  - [Managing resource groups](/docs/account?topic=account-rgs)
- **Overall Best practices:**
  - [Best practices for organizing resources and assigning access](/docs/account?topic=account-account_setup)

## Networking
{: #bp-security-networking}

Customize settings to ensure protection against unwanted access to your applications, networks, and workloads.
- Enable encryption on all databases
  - [Key Protect Integration](/docs/cloud-databases?topic=cloud-databases-key-protect)
- Consider using source NAT settings on your gateway device to lower potential attack surface of your devices
  - [Virtual Private Endpoints](/docs/cloud-databases?topic=cloud-databases-vpes)
  - [Creating a VPN gateway](/docs/vpc?topic=vpc-vpn-create-gateway)
- For any Virtual Serves on your VPC, ensure all network interfaces have at least one VPC security group attached
  - [Using security groups](/docs/vpc?topic=vpc-using-security-groups)
- Certify that DDOS and WAF protection is enabled on all network devices
  - DDOS - [Dealing with Distributed Denial of Service attacks](/docs/cis?topic=cis-distributed-denial-of-service-ddos-attack-concepts)
  - WAF - [WAF actions and CIS rule set](/docs/cis?topic=cis-waf-settings)
  - **Best practice** - [Managing CIS for optimal security](/docs/cis?topic=cis-manage-your-ibm-cis-for-optimal-security)


## Server hardening
{: #bp-security-server-hardening}

Boost your servers protection by removing unnecessary components and access. 
- Limit root/admin access to minimal amount of users including backup personal
  - what is this saying? is this just about account access? or is there specific server access?
  - [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access)
  - [Managing access for CIS](/docs/cis?topic=cis-iam-and-cis)
  - [About data encryption for VPC](/docs/vpc?topic=vpc-vpc-encryption-about#vpc-customer-managed-encryption)
  - [Setting up network ACLs](/docs/vpc?topic=vpc-using-acls)
- Ensure operating system is up to date with the latest security patches
  - not sure what this one is. I'm thinking it falls in the categories of monitoring and auditing
  - [{{site.data.keyword.monitoringlong_notm}}: Getting started tutorial](/docs/monitoring?topic=monitoring-getting-started)
- Check whether authentication and authorization events are logged in each server
  - [Managing events in your account](/docs/activity-tracker?topic=activity-tracker-manage_events)
- Review running services and disable those that are not required
  - [Searching for resources](/docs/overview?topic=overview-ui#search)
- If public network access is not required, disable public network interfaces or IP addresses
  - not sure where to find this
- Change Default ports where possible and reasonable
  - not sure what this means by default ports or where the user would do this
  - [Working with health checks](/docs/vpc?topic=vpc-alb-health-checks)
- Ensure that all ports not required for your application are closed on the OS level firewall
  - [Security in your VPC](/docs/vpc?topic=vpc-security-in-your-vpc)
  - [Working with health checks](/docs/vpc?topic=vpc-alb-health-checks)
  - [Setting up network ACLs](/docs/vpc?topic=vpc-using-acls)
- If Security Groups are available on your host level firewall, ensure that Security Groups are activated and configured
  - [Using security groups](/docs/vpc?topic=vpc-using-security-groups)


## Data protection
{: #bp-security-data-protection}

Safeguard your information from corruption, compromise, or loss. 
- Confirm that all attached and unattached data disks are encrypted
  - [Key Protect Integration](/docs/cloud-databases?topic=cloud-databases-key-protect)
  - [Managing data encryption](/docs/vpc?topic=vpc-vpc-encryption-managing)
- Restrict network access for all databases to a specific IP range 
  - [Allowing specific IP addresses](/docs/account?topic=account-ips)



## Next steps
{: #bp-account-security-next-steps}

Check out [Getting started with Security and Compliance Center](/docs/security-compliance?topic=security-compliance-getting-started).

