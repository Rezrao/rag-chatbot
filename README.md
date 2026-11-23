# rag-chatbot

Ask questions across multiple PDFs without switching between documents. This Python RAG chatbot provides a Gradio interface for local PDF question answering with models from Ollama or Hugging Face.

## Features

- Process multiple PDFs as input for a chat session.
- Ask questions about your documents through a Gradio web interface.
- Use models from Ollama or Hugging Face.
- Run locally or use the Kaggle notebook with an Ngrok tunnel.

## Installation

Install [uv](https://docs.astral.sh/uv/) and, if you plan to use Ollama models, [Ollama](https://ollama.com/). Model downloads require network access; local model execution also needs enough memory for the selected model.

Replace `YOUR-USERNAME` below with the owner of your standalone repository.

```bash
git clone https://github.com/YOUR-USERNAME/rag-chatbot.git
cd rag-chatbot
uv sync --locked
```

Alternatively, use the included Docker Compose setup:

```bash
docker compose up --build
```

To download the source archive once the standalone repository has a `v0.1.0` release, use:

```bash
curl -L https://github.com/YOUR-USERNAME/rag-chatbot/archive/refs/tags/v0.1.0.tar.gz -o rag-chatbot-v0.1.0.tar.gz
```

## Usage

From the project directory, start the interface on localhost:

```bash
uv run python -m rag_chatbot --host localhost
```

Open `http://localhost:7860/`, provide your PDFs, and ask questions about their contents.

You can also start the application with the included script:

```bash
bash ./scripts/run.sh
```

For access through an Ngrok tunnel, install and configure Ngrok first, then run:

```bash
bash ./scripts/run.sh --ngrok
```

**An Ngrok tunnel exposes the interface beyond your machine.** Use the localhost command when you only need access from your own browser.

## License

Licensed under Apache-2.0. This project is based on [datvodinh/rag-chatbot](https://github.com/datvodinh/rag-chatbot). Retain the upstream license and applicable attribution notices when redistributing its code.

## Related projects

Other repositories listed as projects from the same author:

- [EngHirsi/fabric-sdk-node](https://github.com/EngHirsi/fabric-sdk-node): A Node.js SDK project for Hyperledger Fabric.
- [P-Adomako/sre-checklist](https://github.com/P-Adomako/sre-checklist): A checklist repository for site reliability engineering.
- [masna3icom-source/docker-vpn-pptp](https://github.com/masna3icom-source/docker-vpn-pptp): A Docker-based PPTP VPN project.

