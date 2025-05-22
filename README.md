# Exno.6-Prompt-Engg
# Date:
# Register no.
# Experiment 6: Python Code for Multi-AI Tool Integration

## 🚀 Aim
To develop Python code that is compatible with multiple AI tools and platforms, enabling automation of tasks such as interacting with APIs, comparing AI-generated outputs, and generating actionable insights.

---

## 🧠 Algorithm

1. **Import Required Libraries**
   - Use Python libraries such as `requests`, `json`, and `pandas`.

2. **Configure API Access**
   - Set up API keys and base URLs for multiple AI platforms (e.g., OpenAI, Google Gemini, Claude, Microsoft Copilot).

3. **Define the Prompt and Task**
   - Select a common task (e.g., summarization or Q&A) and standardize the prompt for consistency.

4. **Send Requests to AI Tools**
   - Send HTTP POST requests using the prompt to each tool's endpoint.

5. **Parse and Normalize Responses**
   - Convert all responses into a structured format (e.g., JSON or DataFrame) for easy comparison.

6. **Analyze and Compare Outputs**
   - Compare based on:
     - ✅ Accuracy
     - 🔄 Coherence
     - ✨ Simplicity
     - ⏱️ Speed
     - 🤝 User Experience

7. **Generate Actionable Insights**
   - Print or store comparative results to help select the best AI tool for specific tasks.

---

## 🖥️ Example Code Snippet

```python
import requests
import json

def call_openai(prompt):
    url = "https://api.openai.com/v1/completions"
    headers = {
        "Authorization": "Bearer YOUR_OPENAI_API_KEY",
        "Content-Type": "application/json"
    }
    data = {
        "model": "text-davinci-003",
        "prompt": prompt,
        "max_tokens": 150
    }
    response = requests.post(url, headers=headers, json=data)
    return response.json()["choices"][0]["text"]

# Example usage
prompt = "Summarize the basics of blockchain technology."
response_openai = call_openai(prompt)
print("OpenAI Response:", response_openai)
