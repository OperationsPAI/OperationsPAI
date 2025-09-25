---
title: Getting Started
date: 2024-02-17
weight: 1
---

## 📋 Prerequisites

### ⚙️ Hardware Requirements

| Component   | Requirement                        |
| ----------- | ---------------------------------- |
| **CPU**     | 4+ cores                           |
| **Memory**  | 8GB+ RAM                           |
| **Storage** | 20GB+ available SSD storage        |
| **OS**      | Linux (Ubuntu 20.04+ or CentOS 8+) |

### 💻 Software Requirements

- **Docker** (>= 20.10)
- **Kubernetes** (>= 1.25) or **kind/minikube** for local development
- **kubectl** (compatible with your cluster version)
- **Go** (>= 1.23) for development
- **Python** (>= 3.10) for SDK usage

## 🚀 Quick Start

{{% steps %}}

### 🛠️ Local Development Setup

{{% steps %}}

#### 📥 Clone Repository

```bash
# Clone the repository
git clone <repository-url>
cd rcabench
```

#### ▶️ Start Services

```bash
# Start all services with Docker Compose
make local-debug

# This will start:
# - MySQL database
# - Redis cache
# - Jaeger tracing
# - BuildKit daemon
# - RCABench API server
```

#### ✅ Verify Installation

```bash
# Check if all services are running
docker ps

# Test API access
curl http://localhost:8082/health

# Access Swagger documentation
open http://localhost:8082/swagger/index.html
```

{{% /steps %}}

### 🐍 Setup Python Environment

```bash
# Install RCABench SDK
pip install rcabench

# Or install from source
cd sdk/python
pip install -e .
```

### 🔌 Connect to RCABench

```python
from rcabench import RCABenchSDK
import time

# Initialize SDK
sdk = RCABenchSDK("http://localhost:8082")

# Verify connection
health = sdk.health_check()
print(f"RCABench status: {health}")
```

### 📊 List Available Resources

```python
# List available algorithms
algorithms = sdk.algorithm.list()
print("Available algorithms:")
for algo in algorithms:
    print(f"  - {algo['name']}: {algo['description']}")

# List available datasets
datasets = sdk.dataset.list()
print("Available datasets:")
for dataset in datasets:
    print(f"  - {dataset['name']}: {dataset['description']}")
```

### ⚡ Inject a CPU Stress Fault

```python
# Define fault injection request
fault_request = [{
    "duration": 300,  # 5 minutes
    "faultType": 5,   # CPU stress fault
    "injectNamespace": "default",
    "injectPod": "target-service-pod",
    "spec": {
        "CPULoad": 80,    # 80% CPU load
        "CPUWorker": 2    # 2 worker threads
    },
    "benchmark": "my-app"
}]

# Execute fault injection
print("Injecting CPU stress fault...")
injection_result = sdk.injection.execute(fault_request)
print(f"Fault injection started: {injection_result}")

# Wait for fault to take effect
time.sleep(60)
```

### 🔍 Run RCA Algorithm

```python
# Define algorithm execution request
algorithm_request = [{
    "benchmark": "my-app",
    "algorithm": "random-walk",  # Example algorithm
    "dataset": "live-data",
    "parameters": {
        "threshold": 0.7,
        "window_size": 300
    }
}]

# Execute algorithm
print("Running RCA algorithm...")
algorithm_result = sdk.algorithm.execute(algorithm_request)
print(f"Algorithm execution started: {algorithm_result}")

# Wait for algorithm to complete
time.sleep(120)

# Get results
results = sdk.algorithm.get_results(algorithm_result['task_id'])
print(f"Root cause analysis results: {results}")
```

{{% /steps %}}

## Next

Let's customize your new site:

{{< cards >}}
{{< card url="../guide/project-structure" title="Project Structure" icon="document-duplicate" >}}
{{< card url="../guide/configuration" title="Configuration" icon="adjustments-vertical" >}}
{{< /cards >}}

```

```
