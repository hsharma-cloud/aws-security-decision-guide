# AWS Chatbot vs SNS

## Purpose

AWS Chatbot and Amazon Simple Notification Service (SNS) both support operational awareness and incident response but serve different roles. AWS Chatbot delivers AWS notifications and enables operational interactions within collaboration platforms such as Slack and Microsoft Teams, while Amazon SNS is a messaging service that distributes notifications to subscribers across multiple communication channels.

| Feature | AWS Chatbot | Amazon SNS |
|---------|-------------|------------|
| Primary Purpose | ChatOps Integration | Notification Service |
| Focus | Team collaboration | Message delivery |
| Delivers to | Slack, Microsoft Teams | Email, SMS, HTTP, Lambda, SQS, Mobile Push |
| Interactive Commands | Yes | No |
| Uses SNS Topics | Yes | N/A |
| Supports AWS CLI Commands | Yes | No |
| Best For | Operational collaboration | Notification distribution |
| Typical Users | Operations Teams, Incident Responders | Applications, Security Teams |

## Key Differences

- AWS Chatbot integrates AWS notifications into collaboration platforms.
- SNS delivers notifications to subscribers through multiple endpoints.
- Chatbot relies on SNS topics to receive notifications.
- SNS is the messaging backbone, while Chatbot provides the collaboration interface.
- Together they improve communication during security incidents.

## When to Choose AWS Chatbot

Use AWS Chatbot when you need to:

- Receive AWS alerts in Slack or Microsoft Teams.
- Collaborate during incidents.
- Execute approved AWS CLI commands from chat.
- Improve operational visibility.

## When to Choose SNS

Use SNS when you need to:

- Send notifications to multiple subscribers.
- Deliver alerts by email or SMS.
- Trigger Lambda or SQS.
- Build event-driven notification systems.

## Quick Decision

| If you need to... | Choose |
|-------------------|--------|
| Send alerts to Slack or Teams | **AWS Chatbot** |
| Notify multiple subscribers | **Amazon SNS** |
| Collaborate during incidents | **AWS Chatbot** |
| Send email or SMS alerts | **Amazon SNS** |
| Execute AWS commands from chat | **AWS Chatbot** |
| Build notification workflows | **Amazon SNS** |
