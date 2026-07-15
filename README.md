# 🤖 SLM-Agent

### Fine-Tuning Small Language Models into Intelligent AI Agents using LoRA/QLoRA & Model Context Protocol (MCP)

> An end-to-end framework for fine-tuning Small Language Models (SLMs) into production-ready AI agents capable of **tool selection**, **parameter extraction**, **multi-step reasoning**, and **external tool execution** through the **Model Context Protocol (MCP)**.

---

## 🚀 Project Highlights

- 🧠 Fine-tuned SLM using **LoRA / QLoRA**
- 🔧 Model Context Protocol (MCP) integration
- 🤖 Automatic Tool Selection
- 📌 Structured Parameter Extraction
- 🔄 Multi-step Tool Calling
- 📊 Automated Evaluation Pipeline
- 📈 Experiment Tracking using Weights & Biases
- ⚡ FastAPI Inference Server
- 🐳 Dockerized Deployment
- 📦 Modular & Production-Oriented Codebase

---

# 🎯 Motivation

Large Language Models are powerful but expensive to deploy and operate.

This project explores how **Small Language Models (SLMs)** can be transformed into capable AI agents by fine-tuning them to:

- Understand user intent
- Choose the correct external tool
- Extract structured parameters
- Execute tools via MCP
- Generate grounded responses

The goal is to build lightweight, efficient, and deployable AI agents without relying on massive proprietary models.

---

# 🏗️ System Architecture

```

                          User
                            │
                            ▼
                  Fine-Tuned SLM Agent
                            │
        ┌───────────────────┴────────────────────┐
        ▼                                        ▼
 Tool Selection                          Parameter Extraction
        │                                        │
        └───────────────────┬────────────────────┘
                            ▼
                     MCP Client
                            │
            ┌───────────────┴────────────────┐
            ▼                                ▼
      File Reader Tool                 Web Search Tool
            │                                │
            └───────────────┬────────────────┘
                            ▼
                     Tool Responses
                            │
                            ▼
                  Final AI Response

```

---

# ✨ Features

## Agentic AI

- Tool Calling
- Multi-step Reasoning
- Tool Selection
- Parameter Extraction
- MCP Integration

## Fine-Tuning

- LoRA
- QLoRA
- Hugging Face Transformers
- PEFT

## Backend

- FastAPI
- Async Python
- REST APIs

## Evaluation

- Tool Selection Accuracy
- Parameter Extraction Accuracy
- Task Completion Rate
- Hallucination Detection
- Response Quality Metrics

## Deployment

- Docker
- Docker Compose

---

# 📂 Project Structure

```

SLM-Agent/

│

├── config/
│ └── training_config.yaml

├── scripts/
│ ├── setup.py
│ ├── train_model.py
│ ├── evaluate_model.py
│ ├── inference_demo.py
│ └── chat.py

├── src/
│ ├── data/
│ ├── training/
│ ├── inference/
│ └── tools/

├── docker-compose.yml
├── docker-compose-agent.yml
├── docker-compose-mcp.yml

├── requirements.txt

└── README.md

```

---

# ⚙️ Tech Stack

## AI / Machine Learning

- Python
- Hugging Face Transformers
- PEFT
- LoRA
- QLoRA
- BitsAndBytes

## Agent Framework

- Model Context Protocol (MCP)
- Function Calling
- Tool Routing

## Backend

- FastAPI
- REST APIs
- AsyncIO

## Experiment Tracking

- Weights & Biases

## Deployment

- Docker
- Docker Compose

---

# 🔄 Workflow

```

Dataset

│

▼

Data Preparation

│

▼

LoRA / QLoRA Fine-Tuning

│

▼

Evaluation

│

▼

Inference Server

│

▼

SLM Agent

│

▼

Tool Selection

│

▼

MCP Client

│

▼

External Tool Execution

│

▼

Response Generation

```

---

# 🚀 Quick Start

## Clone Repository

```bash
git clone https://github.com/madhavvyas03/SLM-Agent.git

cd SLM-Agent
```

---

## Create Virtual Environment

Windows

```bash
python -m venv .venv

.venv\Scripts\activate
```

Linux / macOS

```bash
python3 -m venv .venv

source .venv/bin/activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Configure Training

Modify

```
config/training_config.yaml
```

to customize

- Learning Rate
- Batch Size
- Epochs
- LoRA Rank
- LoRA Alpha

---

# 🏋️ Training

```bash
python scripts/train_model.py \
--config config/training_config.yaml
```

---

# 📊 Evaluation

```bash
python scripts/evaluate_model.py \
--model-path ./models/model-agent-final \
--run-benchmarks
```

---

# 💬 Interactive Chat

```bash
python scripts/chat.py
```

---

# ⚡ Run Inference Server

```bash
python src/inference/server.py
```

---

# 🐳 Docker Deployment

Build

```bash
docker compose build
```

Run

```bash
docker compose up
```

Run Detached

```bash
docker compose up -d
```

---

# 📈 Evaluation Metrics

The evaluation framework measures:

| Metric | Description |
|---------|-------------|
| Tool Selection Accuracy | Correct tool prediction |
| Parameter Extraction Accuracy | Correct argument extraction |
| Task Completion Rate | End-to-end execution success |
| Hallucination Rate | Incorrect or fabricated outputs |
| Response Quality | Overall answer quality |
| Execution Success Rate | Successful MCP execution |

---

# 🔌 Supported Tools

Current MCP integrations include:

- 📄 File Reader
- 🌐 Web Search

The architecture is modular and can be extended with additional MCP-compatible tools.

---

# 📊 Weights & Biases

The project supports experiment tracking through **Weights & Biases**, logging:

- Training Loss
- Validation Loss
- Learning Rate
- Tool Accuracy
- Hallucination Rate
- Response Quality
- Hardware Utilization

---

# 📈 Results

The fine-tuned model successfully learns to:

- Select the appropriate external tool
- Extract structured parameters
- Execute MCP tool calls
- Perform multi-step reasoning
- Recover from tool failures
- Generate grounded responses

---

# 🛠️ Customization

Adding a new tool only requires:

1. Register the tool in `mcp_client.py`
2. Add training examples in `dataset_builder.py`
3. Regenerate the dataset
4. Fine-tune the model

The modular architecture makes it straightforward to integrate additional MCP-compatible services.

---

# 🔮 Future Improvements

- Multi-Agent Collaboration
- Long-Term Memory
- Retrieval-Augmented Generation (RAG)
- Streaming Responses
- Kubernetes Deployment
- CI/CD Pipeline
- Additional MCP Tool Integrations
- Quantized Inference Optimization

---

# 📚 References

- LoRA: https://arxiv.org/abs/2106.09685
- PEFT: https://github.com/huggingface/peft
- Hugging Face Transformers: https://huggingface.co/docs/transformers
- Model Context Protocol: https://modelcontextprotocol.io
- Weights & Biases: https://wandb.ai

---

# 👨‍💻 Author

**Madhav Vyas**

B.Tech. Computer Science & Applied Mathematics  
Indraprastha Institute of Information Technology Delhi (IIIT Delhi)

---

## ⭐ Star this Repository

If you found this project useful or interesting, consider giving it a ⭐ to support the project.
