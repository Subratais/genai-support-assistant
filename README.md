# Customer Support AI Assistant

This project is a proof-of-concept for building a smart customer support assistant using a large language model and retrieval-based search. It’s designed to run entirely in Google Colab and requires no paid infrastructure.

---

## What It Does

- Uses a public dataset of customer support tweets
- Retrieves relevant past conversations using vector search (ChromaDB)
- Generates responses using the Mistral-7B language model
- Provides a `/generate_response` API using FastAPI
- Makes the API available through a public ngrok link for testing

---

## How to Try It

You can try everything directly in Google Colab.  
Click below to open the notebook:

https://colab.research.google.com/drive/1AMUXz3BUmmCU1iHwfBV63WPMf9WsSlcJ?authuser=1#scrollTo=TWo-vinAD6gN

Once the last cell runs, you’ll get a temporary public API URL (via ngrok), something like: https://xyz.ngrok-free.app/generate_response



Use the `/docs` endpoint to interact with it using Swagger UI.

---

## Sample Input

```json
{
  "query": "I need help resetting my password."
}

## Sample Output

{
  "query": "I need help resetting my password.",
  "answer": "Sure, please go to the password reset page and follow the steps. Let me know if it doesn't work.",
  "top_document": "...",
  "context": "..."
}

## Folder Structure

customer-support-ai-assistant/
├── celonis_customer_support_ai_colab.py  # Main notebook
├── requirements.txt                 # Dependencies
├── README.md 








