# EC2

## Overview

EC2 = Elastic Compute Cloud = IaaS

Includes:
* Virtual Machines (EC2)
* Storing Data (EBS)
* Load Balancing (ELB)
* Scaling (ASG)

## Config

* OS (Linux, Win, or Mac)
* CPU
* RAM
* Storage
  * Network Attached (EBS, EFS)
  * Hardware (EC2 Instance Store)
* Network
* Firewall (SG)
* Bootstrap Script (EC2 User Data)
  * Launch commands as root when machine starts
    * Install updates
    * Install software
    * Anything else you can script

## Instance Types

Naming Convention for Instance Types:
* **t2.micro**
  * **t**: instance class (t = general purpose)
  * **2**: generation (AWS improves over time)
  * **micro**: size within the instance class

Examples of instance classes:
* **t2.micro**: 1 vCPU, 1GB Memory, Low/moderate network (AWS Free Tier, 750hrs/mo)
* **t2.xlarge**: 4 vCPU, 16GB Memory, Moderate network
* **r5.16xlarge**: 64 vCPU, 512GB, 20 Gbps, 13600 EBS Mbps
* **c5d.4xlarge**: 16 vCPU, 32GB Memory, Up to 10GBps Network, 4750 EBS Mbps

Instance Types:
* t: general purpose
* c: compute-optimized
  * Batch-processing
  * Media transcoding
  * High-performance web server
  * High-performance computing
  * Machine Learning
  * Gaming Servers
* r, x, z: memory-optimized
  * High-performance relational/non-relational db
  * Distributed web scale cache stores
  * In-memory database for BI
  * Real-time processing of big unstructured data
* i, D, H: storage-optimized
  * OLTP systems
  * Relational and NoSQL dbs
  * Cache for in-memory database (i.e. redis)
  * Data warehousing apps
  * Distributed filesystems

## AMI

Amazon Machine Image (template for OS, app server, and apps)

## Lifecycle

* Start
* Stop
* Terminate (Delete so I can't start again)