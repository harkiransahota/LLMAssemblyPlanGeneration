# LLMAssemblyPlanGeneration
CODE REPOSITORY

This repository contains the code accompanying the paper:
"Out-of-the-box Assembly Plan Generation: A Peer Evaluation of Open-Source LLMs"

## About

The paper investigates how well pre-trained, general-purpose Large Language Models (LLMs) can be applied directly—without further training—to generate structured assembly instructions from minimal input such as part lists and basic constraints.

This Jupyter Notebook contains the code for the tests and evaluations conucted in the study, including:

- Domain relevance tests by asking 10 general manufacturing questions and scoring responses.

- Quality evaluation of assembly instruction generation from top-performing LLMs using different assembly tasks and prompting strategies.


## Repository Contents

notebook.ipynb: Jupyter Notebook with the code for tests and evaluations.

requirements.txt: Python dependencies to create the virtual environment.

domain_relevance_responses/: LLM responses to the domain relevance test questions.

domain_relevance_evaluations/: Evaluations and scoring of the domain relevance test responses.

prompt_test_responses/: LLM-generated assembly instructions for the prompt (assembly generation) test.

prompt_test_evaluations/: Evaluations of the prompt test assembly instructions.

manufacturer_manuals/: Original assembly manuals for the 5 assembly tasks used in the prompt test, provided for reference and manual verification of generated instructions.

## Instructions to set up the environment and run the notebook.

Getting Started

Follow these steps to run the code locally:

### 1. Clone the repository
git clone https://github.com/harkiransahota/LLMAssemblyPlanGeneration.git

cd LLMAssemblyPlanGeneration

### 2. Create and activate a virtual environment

  #### macOS/Linux:

python3 -m venv venv

source venv/bin/activate


  #### Windows:

python -m venv venv

.\venv\Scripts\activate

### 3. Install dependencies
pip install -r requirements.txt

### 4. Set up the Nebius API token

Create a .env file in the project root folder with the following content:

NEBIUS_TOKEN=your_access_token_here


Replace your_access_token_here with your actual Nebius token.

The notebook will automatically load this environment variable using a package like python-dotenv.

### 5. Run the Jupyter Notebook
jupyter notebook


Open the notebook file and run the cells to reproduce the tests and evaluations.
