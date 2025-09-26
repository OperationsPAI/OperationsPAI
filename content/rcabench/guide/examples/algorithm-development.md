---
title: Algorithm Development
weight: 1
---

This guide explains how to develop, package, and integrate custom RCA algorithms with RCABench.

## Algorithm Requirements

### Input Data Types

Algorithms receive three types of observability data:

- **Metrics**: Time-series performance metrics (CPU, memory, response time, etc.)
- **Traces**: Distributed tracing data showing request flows
- **Logs**: Application and infrastructure log messages

### Output Requirements

Algorithms must output results in this JSON format:

```json
{
  "root_cause": "service-name",
  "confidence": 0.85,
  "execution_time": 45.2,
  "algorithm_version": "1.0.0",
  "ranking": [
    {
      "service": "service-a",
      "score": 0.85,
      "reasoning": "High CPU utilization correlation"
    },
    {
      "service": "service-b",
      "score": 0.42,
      "reasoning": "Elevated error rate"
    }
  ],
  "metadata": {
    "model_confidence": 0.78,
    "data_quality": 0.95,
    "anomaly_threshold": 0.7
  }
}
```
