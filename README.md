# 🤖 AI Web Scraper with LLM Parsing

This project is an advanced, AI-enhanced web scraping tool built using **Selenium**, **LangChain**, **Ollama**, and **Streamlit**. It scrapes live DOM content from any website, processes it, and then uses LLMs to **extract specific information based on your custom instructions**.

## ⚙️ Features

- 🌍 Web scraping using **Selenium**
- 🔎 DOM extraction + cleaning
- 🧠 Custom **LLM-based content parsing** via `llama3` (Ollama)
- ✨ LangChain prompt templates
- 📋 Clean, interactive UI built with **Streamlit**
- 🔐 Proxy support (Bright Data / Luminati ready)

---

## 🧠 How It Works

1. Enter a URL
2. The scraper grabs the full DOM content (via Selenium)
3. You provide a description of what you want to extract (e.g. "List all product names and prices")
4. Ollama + LangChain parses only that specific info from the DOM chunks
5. Clean, structured data is returned—no fluff.

---

## 📁 Project Structure

```bash
.
├── main.py                # Streamlit entry point
├── scrape.py              # Core scraping logic
├── .env                   # Environment variables (not committed)
├── requirements.txt       # Python dependencies
├── .gitignore             # Git exclusions
├── README.md              # This file
└── ai/                    # Your virtual environment (ignored)

```
## 🔧 Setup Instructions

1. Clone the Repo
   
```bash

git clone https://github.com/yourusername/ai-web-scraper.git
cd ai-web-scraper

```

2. Set Up Virtual Environment


```bash

python -m venv ai
source ai/bin/activate      # macOS/Linux
ai\Scripts\activate         # Windows

```

3. Install Dependencies

```bash

pip install -r requirements.txt

```

4. Configure .env

```bash

AUTH=brd-customer-<your-credentials>
SBR_WEBDRIVER=https://brd-customer-<your-auth>@brd.superproxy.io:9510

```

5. Run Ollama (locally)
   
   Make sure you have Ollama installed and running locally with llama3 model:

```bash

ollama run llama3

```

5. Run the App

```bash

streamlit run main.py

```
  1. Enter the target website URL.
  
  2. View the cleaned DOM content.
  
  3. Enter your parse instructions (e.g., “Extract all H1 headings and image URLs”).
  
  4. Get precise, structured results from llama3.



