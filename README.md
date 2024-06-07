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
│   ├── test.csv                # Test dataset
│   └── train.csv               # Training dataset
│
├── eval/                       # Consolidated folder for all evaluation results and related files
│   ├── all-MiniLM-L6-v2.png    # Graphical representation of MiniLM-L6-v2 evaluations
│   ├── all-MiniLM-L6-v2.xlsx   # Detailed data for MiniLM-L6-v2 evaluations
│   ├── all-mpnet-base-v2.png   # Graphical representation of MPNet-base-v2 evaluations
│   ├── all-mpnet-base-v2.xlsx  # Detailed data for MPNet-base-v2 evaluations
│   ├── bertscore.png           # Graphical representation of BERTScore evaluations
│   ├── bertscore.xlsx          # Detailed data for BERTScore evaluations
│   ├── median_table.csv        # Median scores in CSV format
│   ├── median_table.pdf        # Median scores in PDF format
│   └── median_table.tex        # Median scores in LaTeX format
```