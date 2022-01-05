# SG

## Overview

Security Groups are how traffic is permitted into or out of EC2 instances


Security Group rules can reference by IP or by Security Group

## How they work

* They only contain allow rules
* They can reference by
  * IP
  * Security Group
* Can be attached to multiple instances
* Locked down to a region/VPC combo
* Live "outside" the EC2
* Good to maintain one SG for SSH access
* Diagnosing issues
  * Timeouts > Often lead to SG issue
  * Connection Refused > Often an app issue

## Typical Ports

* 22 = SSH
* 21 = FTP (22 = SFTP)
* 80 = HTTP (443 = HTTPS)
* 3389 = RDP