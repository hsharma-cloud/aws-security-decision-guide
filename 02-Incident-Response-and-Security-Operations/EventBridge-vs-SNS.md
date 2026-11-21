# EventBridge vs SNS

## Purpose

Amazon EventBridge and Amazon Simple Notification Service (SNS) are event-driven services that support incident response and security automation. EventBridge routes security events to appropriate AWS services based on rules, while SNS distributes notifications to subscribers to ensure responders are alerted quickly.

| Feature | Amazon EventBridge | Amazon SNS |
|---------|--------------------|------------|
| Primary Purpose | Event Routing | Message Notification |
| Focus | Event-driven automation | Alert distribution |
| Event Filtering | Advanced rule-based filtering | Basic topic subscription |
| Event Sources | AWS Services, SaaS, Custom Applications | Publishers |
| Destinations | Lambda, Step Functions, SQS, SNS, Systems Manager, and more | Email, SMS, Lambda, SQS, HTTP, Mobile Push |
| Fan-out Messaging | Limited | Excellent |
| Scheduling | Yes | No |
| Typical Users | Cloud Architects, Security Engineers | Security Operations, Incident Responders |

## Key Differences

- EventBridge routes events to automate workflows.
- SNS distributes notifications to people and systems.
- EventBridge is designed for orchestration.
- SNS is designed for reliable message delivery.
- EventBridge commonly triggers SNS during security incidents.

## When to Choose EventBridge

Use EventBridge when you need to:

- Automate incident response workflows.
- Route security events based on rules.
- Integrate AWS services and third-party applications.
- Trigger remediation actions.

## When to Choose SNS

Use SNS when you need to:

- Notify responders immediately.
- Send email or SMS alerts.
- Broadcast messages to multiple subscribers.
- Fan out notifications to multiple systems.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Route security events | **Amazon EventBridge** |
| Notify responders | **Amazon SNS** |
| Automate workflows | **Amazon EventBridge** |
| Send email or SMS alerts | **Amazon SNS** |
| Integrate multiple AWS services | **Amazon EventBridge** |
| Broadcast notifications | **Amazon SNS** |
