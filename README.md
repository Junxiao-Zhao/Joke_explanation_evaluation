# Joke Explanation Evaluation

## Introduction
In this project, we evaluate the performance of multiple open-source LLMs on the joke explanation task, inspired by the challenge of understanding complex, pun-filled conversations from a special interests-based community forum that is difficult even for humans to decipher. We aim to address the problem of how well LLMs can explain jokes by effectively understanding and articulating humor. We used the "Joke Explanation" dataset from Hugging Face. We chose to use GPT-4-turbo to generate ground-truth explanations since the original explanations from the dataset are inadequate. We explored the differences in performance with multiple models (LLama2 7b - chat, LLama3 8b - instruct, Mistral8 7b - instruct, and Gemma 7b - instruct) in zero-shot, one-shot, and five-shot scenarios. In terms of evaluation methods, we combined two directions, manual scoring and automatic scoring, to evaluate the performance of the models in different dimensions. The experiments revealed variations in in-context learning capabilities, with LLama 3 showing superior performance, highlighting strengths and limitations that can inform future LLM developments.

## Structure
```
Joke_explanation_evaluation/
│
├── evaluation.ipynb            # evaluate the explanations with bert score and sentence transformers
├── gemma.ipynb                 # generate the explanation using Gemma model
├── humanloop.ipynb             # generate the explanation using gpt4-turbo
├── llama2.ipynb                # generate the explanation using the Llama2 model
├── llama3.ipynb                # generate the explanation using the Llama3 model
├── mixtral.ipynb               # generate the explanation using the Mixtral model
│
├── data/                       # Data files containing evaluations, jokes, and training sets
│   ├── eval-gemma.csv          # Explanation results for GEMMA model
│   ├── eval-Llama2.csv         # Explanation results for Llama2 model
│   ├── eval-llama3.csv         # Explanation results for Llama3 model
│   ├── eval-Mistral.csv        # Explanation results for Mistral model
│   ├── gpt4turbo_explained_full.csv # Full dataset with explanations from GPT-4 Turbo
│   ├── jokes.csv               # Dataset containing jokes
│   ├── test.csv                # Evaluation dataset
│   └── train.csv               # Incontext-learning dataset
│
├── eval/                       # Consolidated folder for all evaluation results and related files
│   ├── all-MiniLM-L6-v2.png    # Graphical representation of MiniLM-L6-v2 evaluations
│   ├── all-MiniLM-L6-v2.xlsx   # Detailed data for MiniLM-L6-v2 evaluations
│   ├── all-mpnet-base-v2.png   # Graphical representation of MPNet-base-v2 evaluations
│   ├── all-mpnet-base-v2.xlsx  # Detailed data for MPNet-base-v2 evaluations
│   ├── bertscore.png           # Graphical representation of BERTScore evaluations
│   ├── bertscore.xlsx          # Detailed data for BERTScore evaluations
│   ├── human_eval_table.csv    # Human evaluation scores in CSV format
│   ├── human_eval_table.pdf    # Human evaluation scores in PDF format
│   ├── human_eval_table.tex    # Human evaluation scores in LaTeX format
│   ├── median_table.csv        # Median scores in CSV format
│   ├── median_table.pdf        # Median scores in PDF format
│   ├── median_table.tex        # Median scores in LaTeX format
│   ├── qualitative.pdf         # Qualitative analysis in PDF format
│   └── qualitative.tex         # Qualitative analysis in LaTeX format
```