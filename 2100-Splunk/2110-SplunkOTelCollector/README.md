# Splunk OTel Collector

Splunk's distribution of the Open Telemetry Collector provides a unified way to receive, process, and export metric, trace, and log data for the Splunk Observability Cloud.

The distribution can be used with other back-ends other than Splunk's, but it has been designed to be supported by Splunk and offer convenience functionality specific to Splunk.

Splunk Observability Cloud also works with other collectors other than Splunk's distribution; however Splunk only formally supports using the Splunk distribution.

## Components

[The components](https://github.com/signalfx/splunk-otel-collector/blob/main/docs/components.md) bundled with Splunk's distribution are summarized on the github page linked. Perhaps the most important components are:

* Receivers
  * General / multi-type
    * **receiver_creator**: Instantiates other receivers based on whether observed endpoints match a rule.
    * **otlp**: Standard receiver for OTLP format (metrics, logs and traces)
    * **splunk_hec**: Receives logs and metrics in Splunk HEC format. 
  * Metrics
    * **hostmetrics**: Collects host data (CPU, memory, disk, etc.)
    * **simpleprometheus**: Wrapper around the prometheus receiver. Scrapes metrics from a single target.
    * **smartagent**: Allows users to utilize existing SignalFx Smart Agent monitors as OTel Collector metric receivers. It assumes you have a properly configured functional SmartAgent release bundle on the system
    * **signalfx**: Receives metrics and events (logs) in SFx proto format to forward on (i.e. as a gateway)
  * Traces
    * **sapm**: Receives traces from other collectors or the SignalFx Smart Agent (i.e. as a gateway). Builds on Jaeger proto.
    * **jaeger**: Receives traces in the Jaeger format. Protocols are defined in configuration.
    * **zipkin**: Receives traces in Zipkin (v1 and v2) format.
  * Logs
    * **fluentforward**: Used to send log data from fluentd to Splunk Observability Cloud
* Processors
  * ...
* Exporters
  * **sapm** (traces), **signalfx** (metrics, trace metadata, and events), and **splunk_hec** (logs for Log Observer and Splunk) are the current way data is sent to Splunk Observability Cloud today.
  * At some point Splunk Observability Cloud will support **otlp**, at which time the default pipelines will be updated.