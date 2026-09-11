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


2. Environment Setup
Create a .env file in the root directory of your project and add your OpenRouter API key:

Kod hissəsi
OPENROUTER_API_KEY=your_openrouter_api_key_here
💻 Usage
Run the following Python script to execute your first request and print the completion:

Python
import os
from dotenv import load_dotenv
from openai import OpenAI

# Load environment variables
load_dotenv()

# Initialize OpenRouter Client
client = OpenAI(
    api_key=os.getenv("OPENROUTER_API_KEY"),
    base_url="[https://openrouter.ai/api/v1](https://openrouter.ai/api/v1)"
)

# Active free-tier model selection
MODEL_NAME = "google/gemini-2.0-flash-lite-preview-02-05:free"

# Send completion request
response = client.chat.completions.create(
    model=MODEL_NAME,
    messages=[
        {"role": "system", "content": "You are a helpful and concise assistant."},
        {"role": "user", "content": "Explain API in one simple sentence."}
    ]
)

# Output response
print("Bot Response:")
print(response.choices[0].message.content)
