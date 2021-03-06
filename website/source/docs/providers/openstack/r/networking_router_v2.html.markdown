---
layout: "openstack"
page_title: "OpenStack: openstack_networking_router_v2"
sidebar_current: "docs-openstack-resource-networking-router-2"
description: |-
  Manages a V2 router resource within OpenStack.
---

# openstack\_networking\_router_v2

Manages a V2 router resource within OpenStack.

## Example Usage

```
resource "openstack_networking_router_v2" "router_1" {
  region = ""
  name = "my_router"
  external_gateway = "f67f0d72-0ddf-11e4-9d95-e1f29f417e2f"
}
```

## Argument Reference

The following arguments are supported:

* `region` - (Required) The region in which to obtain the V2 networking client.
    A networking client is needed to create a router. If omitted, the
    `OS_REGION_NAME` environment variable is used. Changing this creates a new
    router.

* `name` - (Optional) A unique name for the router. Changing this
    updates the `name` of an existing router.

* `admin_state_up` - (Optional) Administrative up/down status for the router
    (must be "true" or "false" if provided). Changing this updates the
    `admin_state_up` of an existing router.

* `external_gateway` - (Optional) The network UUID of an external gateway for
    the router. A router with an external gateway is required if any compute
    instances or load balancers will be using floating IPs. Changing this
    updates the `external_gateway` of an existing router.

* `tenant_id` - (Optional) The owner of the floating IP. Required if admin wants
    to create a router for another tenant. Changing this creates a new router.

## Attributes Reference

The following attributes are exported:

* `region` - See Argument Reference above.
* `name` - See Argument Reference above.
* `admin_state_up` - See Argument Reference above.
* `external_gateway` - See Argument Reference above.
* `tenant_id` - See Argument Reference above.
