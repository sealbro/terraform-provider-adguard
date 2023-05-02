---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "adguard_user_rules Resource - adguard"
subcategory: ""
description: |-
  
---

# adguard_user_rules (Resource)



## Example Usage

```terraform
# manage user rules
# NOTE: there can only be 1 (one) `adguard_user_rules` resource
# specifying multiple resources will result in errors
resource "adguard_user_rules" "test" {
  rules = [
    "! line 1 bang comment",
    "# line 2 respond with 127.0.0.1 for localhost.org (but not for its subdomains)",
    "127.0.0.1 localhost.org",
    "# line 4 unblock access to unblocked.org and all its subdomains",
    "@@||unblocked.org^",
    "# line 6 block access to blocked.org and all its subdomains",
    "||blocked.org^"
  ]
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `rules` (List of String) List of user rules

### Read-Only

- `id` (String) Identifier attribute
- `last_updated` (String) Timestamp of the last Terraform update of the client

## Import

Import is supported using the following syntax:

```shell
# User rules can be imported by specifying the ID as `1`
# NOTE: there can only be 1 (one) `adguard_user_rules` resource, hence the hardcoded ID
terraform import adguard_user_rules.test "1"
```