
# 🧠 Prompt Engineering & Fine-Tuning Playground 

This repository contains a collection of **prompt engineering techniques** for working with large language models (LLMs) such as OpenAI's GPT, Claude, or open-source models like LLaMA and Mistral. It is designed as a reference and hands-on guide for anyone interested in mastering how to structure prompts to get optimal results from LLMs. The repository demonstrates how to **fine-tune** the facebook/bart-large-cnn model on a summarization task using two approaches:

✅ Full Fine-Tuning: Updates all model parameters.
⚡ PEFT (LoRA): Updates a small set of adapter weights with significantly lower compute.
---

## 📦 What's Inside

The repo showcases various methods and examples of prompt engineering, including:

- ✅ **Zero-Shot Prompting**  
  Ask the model to perform a task with no examples — rely purely on instructions.

- ✅ **One-Shot Prompting**  
  Provide **one example** before giving the model a new input to generalize from.

- ✅ **Few-Shot Prompting**  
  Show **multiple examples** to guide the model's output formatting and behavior.



---

## 🛠 How to Use

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/prompt-engineering-playground.git
   cd prompt-engineering-playground

## 🧠 What is PEFT?

**Parameter-Efficient Fine-Tuning (PEFT)** enables training of large language models by modifying and training only a small subset of parameters. **LoRA (Low-Rank Adaptation)** is one such technique that allows fine-tuning with far less memory and compute — making it ideal for faster experimentation.

---

## 📋 Summary of Model & Task

- **Base model**: `facebook/bart-large-cnn`
- **Dataset**: `knkarthick/dialogsum` (via Hugging Face Hub)
- **Metric**: ROUGE (for summarization quality)
- **Platform**: AWS SageMaker Studio or local Jupyter environment

---

## 🚀 Run on AWS SageMaker

### ✅ Requirements

- AWS account with SageMaker Studio enabled
- IAM permissions to start instances (e.g., `ml.m5.2xlarge`)

### 🧾 Steps

1. **Launch Notebook Instance**
   - Open SageMaker Studio
   - Start a `ml.m5.2xlarge` kernel

2. **Clone this Repository**
   ```bash
   git clone https://github.com/mishra123/genai-with-llm.git
3. **Open the Notebook**
   Open ```fine_tuning.ipynb``` in JupyterLab

4. **Run the Code**
    Execute each cell in the Jupyter notebook to:

    ✅ Fine-tune the model using both approaches:

   - Full fine-tuning

   - PEFT with LoRA

    💾 Save model checkpoints:

   - Save locally or to an S3 bucket

    📊 Evaluate and compare:

   - ROUGE scores (ROUGE-1, ROUGE-2, ROUGE-L)

# 💻 Run Locally
✅ Requirements
  - Python 3.8+

  - At least 8 GB RAM 

  - Jupyter Notebook or VS Code

🧾 Steps
 1. **Clone this Repository**
     ```git clone https://github.com/mishra123/genai-with-llm.git```
    
 2. **Create and Activate a Virtual Environment**
  ```
  python3 -m venv .venv
  source .venv/bin/activate  # On Windows: .venv\Scripts\activate
  pip install -r requirements.txt
  pip install notebook
  jupyter notebook fine_tuning.ipynb
```
 3. Run the Notebook
  - Step through the notebook to fine-tune and compare results.
