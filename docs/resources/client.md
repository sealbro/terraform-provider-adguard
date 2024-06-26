---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "adguard_client Resource - adguard"
subcategory: ""
description: |-
  
---

# adguard_client (Resource)



## Example Usage

```terraform
# manage a client
resource "adguard_client" "test" {
  name = "Test Client"
  ids  = ["192.168.100.15", "test-client"]
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `ids` (Set of String) Set of identifiers for this client (IP, CIDR, MAC, or ClientID)
- `name` (String) Name of the client

### Optional

- `blocked_services` (Set of String) Set of blocked services for this client
- `blocked_services_pause_schedule` (Attributes) Sets periods of inactivity for filtering blocked services. The schedule contains 7 days (Sunday to Saturday) and a time zone. (see [below for nested schema](#nestedatt--blocked_services_pause_schedule))
- `filtering_enabled` (Boolean) Whether to have filtering enabled on this client. Defaults to `false`
- `ignore_querylog` (Boolean) Whether to write to the query log. Defaults to `false`
- `ignore_statistics` (Boolean) Whether to be included in the statistics. Defaults to `false`
- `parental_enabled` (Boolean) Whether to have AdGuard parental controls enabled on this client. Defaults to `false`
- `safebrowsing_enabled` (Boolean) Whether to have AdGuard browsing security enabled on this client. Defaults to `false`
- `safesearch` (Attributes) (see [below for nested schema](#nestedatt--safesearch))
- `tags` (Set of String) Set of tags for this client
- `upstreams` (List of String) List of upstream DNS server for this client
- `upstreams_cache_enabled` (Boolean) Whether to enable DNS caching for this client's custom upstream configuration. Defaults to `false`
- `upstreams_cache_size` (Number) The upstreams DNS cache size, in bytes
- `use_global_blocked_services` (Boolean) Whether to use global settings for blocked services. Defaults to `true`
- `use_global_settings` (Boolean) Whether to use global settings on this client. Defaults to `true`

### Read-Only

- `id` (String) Internal identifier for this client
- `last_updated` (String) Timestamp of the last Terraform update of the client

<a id="nestedatt--blocked_services_pause_schedule"></a>
### Nested Schema for `blocked_services_pause_schedule`

Optional:

- `fri` (Attributes) Paused service blocking interval for `Friday` (see [below for nested schema](#nestedatt--blocked_services_pause_schedule--fri))
- `mon` (Attributes) Paused service blocking interval for `Monday` (see [below for nested schema](#nestedatt--blocked_services_pause_schedule--mon))
- `sat` (Attributes) Paused service blocking interval for `Saturday` (see [below for nested schema](#nestedatt--blocked_services_pause_schedule--sat))
- `sun` (Attributes) Paused service blocking interval for `Sunday` (see [below for nested schema](#nestedatt--blocked_services_pause_schedule--sun))
- `thu` (Attributes) Paused service blocking interval for `Thursday` (see [below for nested schema](#nestedatt--blocked_services_pause_schedule--thu))
- `time_zone` (String) Time zone name according to IANA time zone database. For example `America/New_York`. `Local` represents the system's local time zone.
- `tue` (Attributes) Paused service blocking interval for `Tueday` (see [below for nested schema](#nestedatt--blocked_services_pause_schedule--tue))
- `wed` (Attributes) Paused service blocking interval for `Wednesday` (see [below for nested schema](#nestedatt--blocked_services_pause_schedule--wed))

<a id="nestedatt--blocked_services_pause_schedule--fri"></a>
### Nested Schema for `blocked_services_pause_schedule.fri`

Optional:

- `end` (String) End of paused service blocking schedule, in HH:MM format
- `start` (String) Start of paused service blocking schedule, in HH:MM format


<a id="nestedatt--blocked_services_pause_schedule--mon"></a>
### Nested Schema for `blocked_services_pause_schedule.mon`

Optional:

- `end` (String) End of paused service blocking schedule, in HH:MM format
- `start` (String) Start of paused service blocking schedule, in HH:MM format


<a id="nestedatt--blocked_services_pause_schedule--sat"></a>
### Nested Schema for `blocked_services_pause_schedule.sat`

Optional:

- `end` (String) End of paused service blocking schedule, in HH:MM format
- `start` (String) Start of paused service blocking schedule, in HH:MM format


<a id="nestedatt--blocked_services_pause_schedule--sun"></a>
### Nested Schema for `blocked_services_pause_schedule.sun`

Optional:

- `end` (String) End of paused service blocking schedule, in HH:MM format
- `start` (String) Start of paused service blocking schedule, in HH:MM format


<a id="nestedatt--blocked_services_pause_schedule--thu"></a>
### Nested Schema for `blocked_services_pause_schedule.thu`

Optional:

- `end` (String) End of paused service blocking schedule, in HH:MM format
- `start` (String) Start of paused service blocking schedule, in HH:MM format


<a id="nestedatt--blocked_services_pause_schedule--tue"></a>
### Nested Schema for `blocked_services_pause_schedule.tue`

Optional:

- `end` (String) End of paused service blocking schedule, in HH:MM format
- `start` (String) Start of paused service blocking schedule, in HH:MM format


<a id="nestedatt--blocked_services_pause_schedule--wed"></a>
### Nested Schema for `blocked_services_pause_schedule.wed`

Optional:

- `end` (String) End of paused service blocking schedule, in HH:MM format
- `start` (String) Start of paused service blocking schedule, in HH:MM format



<a id="nestedatt--safesearch"></a>
### Nested Schema for `safesearch`

Optional:

- `enabled` (Boolean) Whether Safe Search is enabled. Defaults to `false`
- `services` (Set of String) Services which SafeSearch is enabled.

## Import

Import is supported using the following syntax:

```shell
# Client can be imported by specifying the name
terraform import adguard_client.test "Test Client"
```
