# Regions, AZs, and Edge

## Regions
AWS has regions all around the world.

They are named, like **us-east-1**, **eu-west-2**, etc.

Where should you put your application? Consider:
* **Compliance**: Data governance and legal requirements
* **Proximity**: Close to customers; less latency
* **Availability**: Are the services in the region you need
* **Pricing**: It varies region to region

## Availability Zones (AZs)
There are 2-6 AZs in each region (usually 3).

Each AZ is one or more datacenters with redundant power, network, and connectivity. They are isolated from each other AZ to be isolated from disasters. But they are connected with high-bandwidth, low-latency networks.

## Edge Locations (Points of Presence)
There are >200 Edge Locations in more than 80 cities (across more then 40 countries).

Edge Locations help deliver content to end users with lower latency.