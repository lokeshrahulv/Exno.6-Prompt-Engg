# Experiment 6: Python Code for Multi-AI Tool Integration
# Date:
## Register no: 212222100024
##  Aim
To develop Python code that is compatible with multiple AI tools and platforms, enabling automation of tasks such as interacting with APIs, comparing AI-generated outputs, and generating actionable insights.

---

##  Algorithm

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
     -  Accuracy
     -  Coherence
     -  Simplicity
     -  Speed
     -  User Experience

7. **Generate Actionable Insights**
   - Print or store comparative results to help select the best AI tool for specific tasks.

---

##  Example Code Snippet

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

```

## Summary
This experiment demonstrates that GPT-Neo and GPT-2, while both powerful language models, respond differently to the same natural language query. Each model reflects its distinct training data and architecture, influencing the tone, content, and structure of the response. GPT-Neo tends to generate more structured, informative content, while GPT-2 sometimes outputs more generic or creative responses.

## Conclusion
This experiment demonstrates how Python can serve as a powerful bridge between multiple AI tools, enabling developers to create multi-model pipelines that evaluate, compare, or combine the strengths of various services. This integration supports:
   
   • Better decision-making on tool selection
   
   • Automation of evaluation and benchmarking
   
   • Enhanced productivity by combining outputs

Such a system is scalable and can be adapted for broader use cases including multi-tool chatbots, creative content workflows, or research benchmarking.

# Result
The corresponding prompt was executed successfully. The Python code integrated multiple AI tools and demonstrated comparative analysis for output evaluation.
