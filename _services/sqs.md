---
title: 'SQS (Simple Queue Service)'
date: 2024-01-03
weight: 3
---

SQS-compatible message queuing powered by [ElasticMQ](https://github.com/softwaremill/elasticmq). Create queues, send and receive messages, manage message visibility.

## Features

- Full SQS API compatibility
- Standard and FIFO queue support
- In-memory message storage
- Message delay and visibility timeout
- Dead letter queue support
- REST-SQS interface on port 9325

## Quick Start

```bash
# Start SQS
docker compose up -d sqs

# Create a queue
aws --endpoint=http://localhost:9324 sqs create-queue --queue-name my-queue

# Send a message
aws --endpoint=http://localhost:9324 sqs send-message \
    --queue-url http://localhost:9324/queue/my-queue \
    --message-body "Hello World"

# Receive messages
aws --endpoint=http://localhost:9324 sqs receive-message \
    --queue-url http://localhost:9324/queue/my-queue
```

## Access

- **SQS API**: `http://localhost:9324`
- **REST UI**: `http://localhost:9325`
