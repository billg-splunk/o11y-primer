# O11y Primer Overview

Observability is all about answering the unknown unknowns.

Monitoring told us when a system is working and when it isn't.
Observability helps us understand why it isn't working.

Monitoring is a collection of logs, metrics and traces.
Observability helps you use that data to understand what's happening.

Monitoring is about failures.
Observability is about understanding the overall behavior of a system.

Monitoring is about system down.
Observability is about system "a little slower", and how we isolate why.

## Where can I buy Observability?

Observability is not a product. It's a way to work. It's preparation to understand your system, so when (not if) there is a problem you are ready. It's about knowing problems will happen, and having the processes to deal with that. It's about looking at the right data at the right time, not being constantly alerted.

## So do I need logs, metrics and traces

Some day maybe we will be able to stop worrying about the inputs and just worry about the outcomes. But in the short-term we need to bring in the kinds of data that can help our systems be more observable. Today that foundation is based on logs/events, metrics and traces.

Metrics: Answer "Do I have a problem?"
Traces: Answer "Where is the problem?"
Logs: Answer "Why is the problem happening?"

Detect -> Troubleshoot -> Root Cause

### Metrics

Metrics are numbers that describe a process or activity over time. They are really easy to process quickly, which makes them well-suited to be analyzed quickly and answer when I have a problem.

Examples of metrics sources:
* CPU (cpu utiolization), Memory (memory utilization), and Disk (utilization)
* Infrastructure Metrics from AWS CloudWatch, Azure Monitor, and GCP StackDriver
* Web Tracking scripts (Synthetics, Google Analytics)
* Agents (Collectors, Instrumentation)
* Business (Revenue, bounce rate, cart abandonment)

### Traces

Traces are maps of a user's journey -- the pages they hit, the functions they run, the systems they run on, etc. When traces run long or are erroneous, the metadata can help us isolate what is in common with those journeys that are problematic. Maybe a single host or containers are causing the issues, or a specific store or type of customer is facing the issues.

### Events or Logs

Logs are structu
