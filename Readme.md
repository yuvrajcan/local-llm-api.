# Local LLM API Service

An asynchronous, containerized REST API that serves local Large Language Models (LLMs) using consumer-grade hardware. 

## Features
* **Local Inference:** Orchestrates 4-bit quantized Llama 3 models locally via Ollama.
* **Token Streaming:** Implements asynchronous token-by-token generation exactly like ChatGPT.
* **Latency Tracking:** Logs every prompt, response, and generation time to a SQLite database.
* **Dockerized:** Fully containerized for instant deployment.

## Tech Stack
* **Framework:** FastAPI, Python 3.11
* **AI Orchestration:** LangChain, Ollama
* **Database:** SQLite
* **Deployment:** Docker

## Quick Start (Run it yourself)
1. Ensure Docker Desktop and Ollama are installed.
2. Clone this repository.
3. Build the image: `docker build -t local-llm-api .`
4. Run the container: `docker run -p 8000:8000 local-llm-api`
5. Access the API documentation at `http://localhost:8000/docs`