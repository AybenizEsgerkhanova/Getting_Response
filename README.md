# OpenRouter API — Getting Response Task

This project demonstrates how to interact with Large Language Models (LLMs) by sending requests and parsing responses using the **OpenRouter API** and the official `openai` Python SDK.

---

## 🚀 Features

* Full integration with OpenRouter API (`base_url="https://openrouter.ai/api/v1"`).
* Secure API key management using environment variables via `.env`.
* Configurable system instructions and user prompt handling.
* Correct response object extraction (`response.choices[0].message.content`).

---

## 🛠️ Prerequisites & Installation

### 1. Install Required Packages

Install the necessary Python libraries using `pip`:

```bash
pip install openai python-dotenv
