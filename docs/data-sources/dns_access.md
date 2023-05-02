---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "adguard_dns_access Data Source - adguard"
subcategory: ""
description: |-
  
---

# adguard_dns_access (Data Source)



## Example Usage

```terraform
### this data source has been DEPRECATED and will be removed in a future release
### Use the `dns` block in the `adguard_config` data source instead
# get the DNS access list
data "adguard_dns_access" "test" {}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Read-Only

- `allowed_clients` (List of String) The allowlist of clients: IP addresses, CIDRs, or ClientIDs
- `blocked_hosts` (List of String) Disallowed domains
- `disallowed_clients` (List of String) The blocklist of clients: IP addresses, CIDRs, or ClientIDs
- `id` (String) Identifier attribute

