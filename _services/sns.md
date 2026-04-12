---
title: 'SNS (Simple Notification Service)'
date: 2024-01-04
weight: 4
---

Local SNS implementation powered by [s12v/sns](https://github.com/s12v/sns). Create topics, manage subscriptions, and publish messages locally.

## Features

- SNS API compatibility
- Topic creation and management
- Subscription management (HTTP/HTTPS endpoints)
- Publish messages to topics
- Persistent configuration via mounted volumes

## Quick Start

```bash
# Start SNS
docker compose up -d sns

# Create a topic
aws --endpoint=http://localhost:9911 sns create-topic --name my-topic

# List topics
aws --endpoint=http://localhost:9911 sns list-topics

# Publish a message
aws --endpoint=http://localhost:9911 sns publish \
    --topic-arn arn:aws:sns:eu-west-1:000000000000:my-topic \
    --message "Hello from FakeWS"
```

## Access

- **SNS API**: `http://localhost:9911`
