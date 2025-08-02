# 🛰️ Observability Stack

This repository provides a ready-to-run, containerized observability stack using popular open-source tools from Grafana Labs and the CNCF ecosystem. It allows you to collect, store, and visualize **metrics**, **logs**, and **traces** — all in one place.

## 📦 Stack Components

| Component         | Purpose                          | Port        | URL                        |
|-------------------|----------------------------------|-------------|----------------------------|
| **Grafana**       | Dashboards & visualization       | `3000`      | http://localhost:3000     |
| **Prometheus**    | Metrics collection & storage     | `9090`      | http://localhost:9090     |
| **Tempo**         | Distributed tracing backend      | `3200/4317` | http://localhost:3200     |
| **Loki**          | Log aggregation and querying     | `3100`      | http://localhost:3100     |
| **OTel Collector**| Unified telemetry pipeline       | `4317/4318` |                            |

---

## 🧰 What's Included

- `docker-compose.yml`: Defines all services, their ports, and network.
- `otel-collector-config.yaml`: Collects traces, logs, and metrics; exports to Tempo, Loki, Prometheus.
- `tempo.yaml`: Config for Tempo (trace storage).
- `loki-config.yaml`: Config for Loki (log storage).
- `prometheus.yaml`: Config for scraping metrics from the collector and services.

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/hasanfathi/observability-stack.git
cd observability-stack
### ✅ Step 2: Start the Observability Stack

```bash
docker-compose up -d
