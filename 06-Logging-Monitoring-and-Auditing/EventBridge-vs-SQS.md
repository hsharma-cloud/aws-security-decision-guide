# Amazon EventBridge vs Amazon SQS

## Purpose

Amazon EventBridge and Amazon Simple Queue Service (SQS) are messaging services, but they solve different problems. EventBridge is an event bus that routes events between producers and consumers based on rules, enabling event-driven architectures. Amazon SQS is a fully managed message queue that stores messages until they are processed by consumers, enabling reliable asynchronous communication and workload decoupling.

| Feature | Amazon EventBridge | Amazon SQS |
|---------|--------------------|------------|
| Primary Purpose | Event Routing | Message Queue |
| Communication Model | Event Bus | Queue |
| Message Storage | No | Yes |
| Event Filtering | Advanced Rule-Based Filtering | No |
| Message Ordering | No Guarantee | FIFO Available |
| Message Retention | No | Up to 14 Days |
| Supports Multiple Targets | Yes | Single Consumer Group (per message) |
| Best For | Event-Driven Automation | Asynchronous Processing |
| Typical Users | Developers & Security Engineers | Application Developers |

## Key Differences

- EventBridge **routes events** to targets based on matching rules.
- SQS **stores messages** until they are processed.
- EventBridge does not retain events for later processing.
- SQS provides durable message storage and retry capabilities.
- EventBridge is ideal for automation, while SQS is ideal for decoupling applications and buffering workloads.

## When to Choose EventBridge

Use EventBridge when you need to:

- Build event-driven architectures.
- Route AWS service events.
- Trigger Lambda functions automatically.
- Integrate SaaS applications.
- Filter events before delivery.

## When to Choose SQS

Use Amazon SQS when you need to:

- Queue messages for later processing.
- Decouple microservices.
- Handle traffic spikes.
- Guarantee message delivery.
- Retry failed message processing.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Trigger a Lambda function when an EC2 instance terminates | **Amazon EventBridge** |
| Queue orders for asynchronous processing | **Amazon SQS** |
| Route AWS service events | **Amazon EventBridge** |
| Buffer workloads during traffic spikes | **Amazon SQS** |
| Build event-driven automation | **Amazon EventBridge** |
| Ensure reliable message processing | **Amazon SQS** |
