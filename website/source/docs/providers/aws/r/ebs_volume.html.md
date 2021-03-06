---
layout: "aws"
page_title: "AWS: aws_ebs_volume"
sidebar_current: "docs-aws-resource-ebs-volume"
description: |-
  Provides an Elastic IP resource.
---

# aws\_ebs\_volume

Manages a single EBS volume.

## Example Usage

```
resource "aws_ebs_volume" "example" {
    availability_zone = "us-west-1a"
    size = 40
}
```

## Argument Reference

The following arguments are supported:

* `availability_zone` - (Required) The AZ where the EBS volume will exist.
* `encrypted` - (Optional) If true, the disk will be encrypted.
* `iops` - (Optional) The amount of IOPS to provision for the disk.
* `size` - (Optional) The size of the drive in GB.
* `snapshot_id` (Optinal) A snapshot to base the EBS volume off of.
* `type` - (Optional) The type of EBS volume.
* `kms_key_id` - (Optional) The KMS key ID for the volume.
