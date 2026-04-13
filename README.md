# LLMAssemblyPlanGeneration

This repository contains the code and data accompanying the paper:

**"Out-of-the-Box Assembly Instruction Generation: A Peer Evaluation of Open-Source LLMs"**

---

## 📖 Overview

This study investigates the applicability of pre-trained, general-purpose Large Language Models (LLMs) for generating assembly instructions without fine-tuning. The evaluation focuses on:

- Domain knowledge relevant to manufacturing and assembly  
- Instruction generation quality across different prompting strategies  
- The use of LLMs as evaluators (peer evaluation), including analysis of evaluator behaviour  

All experiments are implemented in a Jupyter Notebook and can be reproduced using the provided data and scripts.

---

## 📂 Repository Structure

- `LLMEvaluation.ipynb`  
  Main Jupyter Notebook containing all experiments, evaluations, and analysis.

- `requirements.txt`  
  Python dependencies required to run the notebook.

- `DomainRelevanceTestResponses/`  
  Raw LLM responses to the domain relevance test questions.

- `DomainRelevanceTestEvaluation/`  
  Evaluator scores for the domain relevance test.

- `PromptingTestResponses/`  
  Generated assembly instructions for all task–prompt combinations.

- `PromptingTestEvaluation/`  
  Peer evaluation scores (clarity, completeness, correctness) for all generated instructions.

- `AssemblyTaskInstructions/`  
  Original assembly manuals used as reference material for the five evaluation tasks.

---

## ⚙️ Setup Instructions

### 1. Clone the repository

git clone https://github.com/harkiransahota/LLMAssemblyPlanGeneration.git  
cd LLMAssemblyPlanGeneration  

---

### 2. Create and activate a virtual environment

#### macOS/Linux

python3 -m venv venv  
source venv/bin/activate  

#### Windows

python -m venv venv  
.\venv\Scripts\activate  

---

### 3. Install dependencies

pip install -r requirements.txt  

---

## 🔑 API Configuration

This project uses the Nebius API to access LLMs.

Create a `.env` file in the project root directory:

NEBIUS_TOKEN=your_access_token_here

Replace `your_access_token_here` with your actual API token.

The notebook automatically loads this variable via `python-dotenv`.

---

## ▶️ Running the Experiments

Start Jupyter Notebook:

jupyter notebook  

Open `LLMEvaluation.ipynb` and execute the cells sequentially to reproduce:

- Domain relevance evaluation  
- Prompting test (assembly instruction generation)  
- Peer evaluation and scoring  
- Aggregation and analysis of results  

---

## 📊 Notes on Reproducibility

- All raw model outputs and evaluation scores are included in this repository.  
- Scores reported in the paper are derived from the provided evaluation files.  
- Preprocessing steps (e.g., removal of formatting artifacts such as `think` tags) are implemented within the notebook.  

---

## 📄 License

Please refer to the individual model licenses where applicable. This repository contains only generated outputs and evaluation data.