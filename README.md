# 🔵 Cane · AI Assistant for SOC Analysts

> *Cane*: the support an analyst leans on.

An **AI assistant** that helps an analyst make sense of alerts and techniques: a **RAG over
MITRE ATT&CK** with a tool-using agent, an **MCP** server and an **n8n** workflow. I build it
locally, measure it, deploy it, **attack** it and **secure** it, and evaluate it with a 5-block
framework (data, models, cloud, DevSecOps and governance).

## What it demonstrates
- Building a useful AI system end to end (not just a notebook prototype).
- **Securing** every surface: prompt injection, data leakage, tool abuse — from the model to deployment.
- **Evaluating** rigorously: golden dataset, baseline and documented failure modes.
- Deploying with **Docker, Kubernetes and Terraform** and monitoring it in production.

## Planned structure

```
cane/
├── src/cane/     RAG, agent and API
├── tests/        tests
├── evals/        golden dataset, baseline, FAILURE_MODES.md
├── mcp_server/   MCP server exposing the tools
├── workflows/    n8n export (no secrets)
├── infra/        Docker, Kubernetes and Terraform
└── docs/         architecture, adr/ and security/
```

## Status
🗓️ **Starts December 2026** (day 58 of my AI learning plan). Until then this repository holds only
this README: the first piece is the semantic ATT&CK index in a vector database. Folders are created
as the project progresses.

## ⚠️ Security
API keys go in **environment variables**, never in the code. The n8n workflow is exported **without
secrets**. No model weights or large datasets in the repo (see [`.gitignore`](./.gitignore)).

---

<sub>Built by [@0x0128](https://github.com/0x0128) · part of my AI security portfolio.</sub>
