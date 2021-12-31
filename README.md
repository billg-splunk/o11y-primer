# o11y-primer (Observability Primer)

## Introduction
The goal of this primer is to provide some basic information on observability, with practical examples.

It's not meant to completely tackle the topic of observability. There are many better references for that out there.

It is meant to teach about some of the concepts around observability (i.e. Docker, Kubernetes, various clouds, different deployment types, etc.), offer some example commands and configurations, and provide some specific examples on how it can be used.

Since I work at Splunk some of my examples will be based on using Splunk Observability Cloud but they could be easily adapted for other solutions, especially if they are built on using [Open Telemetry](https://opentelemetry.io/) for getting data in. Most Splunk-specific information will be in the Splunk section.

It will forever be a "work in progress". And any examples are meant to be just that. Use at your own risk.

## Contents

* [Observability Overview](0100-Observability_Overview/README.md)
* [Docker](0200-Docker/README.md)
* [Kubernetes](0300-Docker/README.md)
* [Collector](0400-Collector/README.md)
  * [Deploying the OTel Collector](0400-Collector/0410-DeployingOTelCollector/README.md)
* [Applications](0500-Applications/README.md)
  * [Instrumententing an Application](0500-Applications/0510-InstrumentingAnApplication/README.md)
  * [Examples for Different Languages](0500-Applications/0520-ExamplesForDifferentLanguages/README.md)
* [AWS](0600-AWS/README.md)
* [GCP](0700-GCP/README.md)
* [Azure](0800-Azure/README.md)
* [Deployment Types](0900-Deployments/README.md)
* CI/CD
* [Splunk Observability](2100-Splunk/README.md)
  * [Splunk OTel Collector (Distribution)](2100-Splunk/2110-SplunkOTelCollector/README.md)
  * [Splunk Metrics](2100-Splunk/2120-SplunkMetrics/README.md)
  * [Splunk Traces](2100-Splunk/2130-SplunkTraces/README.md)
  * [Splunk Logs](2100-Splunk/2140-SplunkLogs/README.md)
  * [Splunk Administration](2100-Splunk/2150-Administration/README.md)
