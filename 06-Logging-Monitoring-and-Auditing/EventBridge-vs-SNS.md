# Amazon EventBridge vs Amazon SNS

## Purpose

Amazon EventBridge and Amazon Simple Notification Service (SNS) are event-driven messaging services, but they are designed for different communication patterns. EventBridge routes and filters events from AWS services, SaaS applications, and custom applications to multiple targets based on rules. Amazon SNS is a publish/subscribe (Pub/Sub) messaging service that immediately pushes messages to multiple subscribers such as email, SMS, Lambda functions, HTTP endpoints, or Amazon SQS queues.

| Feature | Amazon EventBridge | Amazon SNS |
|---------|--------------------|------------|
| Primary Purpose | Event Routing | Publish/Subscribe Messaging |
| Trigger Type | Events | Messages |
| Event Filtering | Advanced Rule-Based Filtering | Subscription Filtering |
| AWS Service Integration | Extensive | Moderate |
| Supports SaaS Integrations | Yes | No |
| Fan-Out Messaging | Limited | Excellent |
| Delivery Model | Event Routing | Push Notifications |
| Best For | Event-Driven Automation | Notifications and Fan-Out Messaging |
| Typical Users | Developers & Security Engineers | Operations & Application Teams |

## Key Differences

- EventBridge routes **events** based on rules.
- SNS distributes **messages** to multiple subscribers.
- EventBridge supports advanced event pattern matching.
- SNS provides low-latency fan-out messaging.
- EventBridge is commonly used for automation, while SNS is commonly used for notifications.

## When to Choose EventBridge

Use EventBridge when you need to:

- Build event-driven architectures.
- Route AWS service events.
- Integrate SaaS applications.
- Trigger Lambda functions automatically.
- Filter events before processing.

## When to Choose SNS

Use SNS when you need to:

- Send email or SMS notifications.
- Notify multiple subscribers simultaneously.
- Fan out messages to several systems.
- Broadcast operational alerts.
- Deliver messages to SQS queues or Lambda functions.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Trigger a Lambda function when an EC2 instance stops | **Amazon EventBridge** |
| Send an email alert to administrators | **Amazon SNS** |
| Filter AWS events before routing | **Amazon EventBridge** |
| Broadcast a message to multiple subscribers | **Amazon SNS** |
| Build event-driven workflows | **Amazon EventBridge** |
| Deliver operational notifications | **Amazon SNS** |
