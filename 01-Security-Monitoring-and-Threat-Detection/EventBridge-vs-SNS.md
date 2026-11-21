# EventBridge vs SNS

## Purpose

Amazon EventBridge and Amazon Simple Notification Service (SNS) are event-driven services that enable communication between applications and AWS services. EventBridge is designed for event routing and application integration, while SNS is designed for message delivery and notification to subscribers.

| Feature | Amazon EventBridge | Amazon SNS |
|---------|--------------------|------------|
| Primary Purpose | Event Routing | Message Notification |
| Focus | Event-driven integration | Publish/Subscribe messaging |
| Event Filtering | Advanced | Basic |
| Event Sources | AWS Services, SaaS, Custom Applications | Publishers |
| Destinations | 20+ AWS services, APIs, SaaS | Email, SMS, Lambda, SQS, HTTP, Mobile Push |
| Fan-out Messaging | Limited | Yes |
| Scheduling | Yes | No |
| Typical Users | Application Developers, Cloud Architects | Developers, Operations Teams |

## Key Differences

- EventBridge routes **events** based on rules.
- SNS delivers **messages** to subscribers.
- EventBridge is designed for application integration.
- SNS is designed for notifications and fan-out messaging.
- EventBridge can trigger SNS when notifications are required.

## When to Choose EventBridge

Use EventBridge when you need to:

- Route AWS events between services.
- Build event-driven architectures.
- Integrate SaaS applications.
- Trigger automated workflows.

## When to Choose SNS

Use SNS when you need to:

- Send notifications.
- Broadcast messages to multiple subscribers.
- Deliver alerts through email, SMS, or mobile push.
- Fan out messages to multiple endpoints.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Route application events | **Amazon EventBridge** |
| Send notifications | **Amazon SNS** |
| Build event-driven workflows | **Amazon EventBridge** |
| Broadcast messages | **Amazon SNS** |
| Integrate AWS and SaaS services | **Amazon EventBridge** |
| Notify multiple subscribers | **Amazon SNS** |
