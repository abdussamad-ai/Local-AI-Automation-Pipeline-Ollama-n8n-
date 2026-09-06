# Local AI Automation Framework (n8n + Ollama)

![n8n Supported](https://img.shields.io/badge/n8n-v2.37+-orange?logo=n8n)
![Ollama Compatible](https://img.shields.io/badge/Ollama-Llama3.2-blue?logo=ollama)
![License MIT](https://img.shields.io/badge/License-MIT-green)
![100% Free](https://img.shields.io/badge/Cost-0%20USD-brightgreen)

A frameworkless, 100% free, and local AI automation pipeline built using n8n and Ollama (Llama 3.2). Run AI workflows without third-party API costs or credit limits.

## 🏗️ Architecture

```text
[ Input Text ] ──> [ n8n Workflow (Docker) ] ──> [ Ollama AI Engine (Host PC) ] ──> [ Output ]
```

## 🚀 Key Features
- **Zero API Cost:** Powered completely by Ollama running locally.
- **Privacy-First:** Data stays inside your local machine.
- **Offline Capable:** Works without an active internet connection once models are downloaded.

## 🛠️ Quick Start (1-Click Docker Setup)

### 1. Enable Ollama CORS on Host
Run the following PowerShell command to make Ollama accessible to Docker containers:
```powershell
$env:OLLAMA_HOST="0.0.0.0"
$env:OLLAMA_ORIGINS="*"
ollama pull llama3.2
ollama serve
```

### 2. Start n8n
Run docker-compose:
```bash
docker-compose up -d
```
Access n8n at `http://localhost:5678`.

### 3. Import Workflow
1. Open n8n.
2. Click **Workflow** -> **Import from File**.
3. Select `workflow.json`.
4. Execute the pipeline!
