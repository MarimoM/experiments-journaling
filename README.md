# LLM Experimentation: Optimizing a Journaling Agent

This repository contains the code for experiments for the [article](https://dev.to/margarita_sliachina/llm-experimentation-optimizing-my-journaling-agent-3bnf).

## 🧪 The Experiment
The idea is to compare different prompting strategies and models to find the most reliable method for structured data extraction.
- Case Study: An "AI Journaling Assistant" that categorizes messy, conversational journal entries.
- Goal: To reliably extract a JSON object containing topics, sentiment, and a summary.

### The Variants
I compare four distinct variants:
- Instruction-Based Prompt + gpt-4o-mini
- Instruction-Based Prompt + gpt-4o
- Schema-Enforced (Tool Calling) + gpt-4o-mini
- Schema-Enforced (Tool Calling) + gpt-4o

### The Metrics
To measure success, we used a multi-layered evaluation strategy:
- `is_valid` (Rule-Based): Checks for syntactically correct JSON.
- `topics_correctness_regex` (Rule-Based): Checks if all expected topics are present.
- `summary_quality` (LLM-as-a-Judge): Evaluates the subjective quality of the summary.
- Cost & Latency: Tracked automatically by Langfuse.

## 🚀 How to Run This Project

**1. Prerequisites**

You will need API keys for:
   - Langfuse (Cloud)
   - OpenAI
     
**2. Setup**
   - Open the `Experiments_Journaling_Assistant.ipynb` notebook in Google Colab or a local Jupyter environment.
   - Install the required libraries by running the `pip install` cells at the beginning of the notebook.
   - Fill in your API keys in the setup cell.
     
**3. Run Cells From JupyterNotebook**

### Have fun!
