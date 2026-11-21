# SNS vs SQS

## Purpose

Amazon Simple Notification Service (SNS) and Amazon Simple Queue Service (SQS) are messaging services that support reliable and scalable communication between applications. SNS is designed to publish messages to multiple subscribers simultaneously, while SQS stores messages in a queue until they are processed by consumers. Together, they improve the reliability and resilience of security automation and incident response workflows.

| Feature | Amazon SNS | Amazon SQS |
|---------|------------|------------|
| Primary Purpose | Publish/Subscribe Messaging | Message Queue |
| Communication | Push | Pull |
| Delivery | Immediate | Consumer-controlled |
| Message Storage | No | Yes |
| Fan-out | Yes | No |
| Message Ordering | Standard | Standard or FIFO |
| Typical Use Case | Notifications and alerts | Reliable processing and buffering |
| Typical Users | Operations, Security Teams | Developers, Automation Engineers |

## Key Differences

- SNS **pushes** messages to subscribers.
- SQS **stores** messages until they are processed.
- SNS enables one-to-many communication.
- SQS decouples applications for reliable processing.
- SNS and SQS are commonly used together for resilient event-driven architectures.

## When to Choose SNS

Use SNS when you need to:

- Notify multiple subscribers immediately.
- Send email, SMS, or HTTP notifications.
- Fan out events to multiple AWS services.
- Alert incident responders.

## When to Choose SQS

Use SQS when you need to:

- Buffer workloads.
- Decouple applications.
- Ensure reliable message processing.
- Prevent message loss during traffic spikes.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Send notifications immediately | **Amazon SNS** |
| Queue messages for processing | **Amazon SQS** |
| Fan out a message to multiple consumers | **Amazon SNS** |
| Buffer workloads | **Amazon SQS** |
| Alert responders | **Amazon SNS** |
| Build resilient asynchronous applications | **Amazon SQS** |
