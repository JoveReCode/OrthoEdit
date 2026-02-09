# OrthoEdit
- Code for [``OrthoEdit: Principled and Stable Knowledge Editing via Orthogonal Subspace Projection``]


## Requirements
- pytorch==1.12.1
- einops==0.8.1
- higher==0.2.1
- hydra-core==1.2.0
- transformers==4.48.0
- datasets==4.4.1
- spacy==3.8.11
- scipy==1.15.3
- scikit-learn==1.0.2
- nltk==3.7

## Run
#### 1. Run editing
    python3 -m experiments.evaluate     --alg_name=OrthoEdit     --model_name=meta-llama/Meta-Llama-3-8B-Instruct     --hparams_fname=Llama3-8B.json --ds_name=mcf --dataset_size_limit=5000   --num_edits=100 --downstream_eval_steps=0

#### 2. Summarize the results
    python summarize.py --dir_name=OrthoEdit --runs=run_<run1>,run_<run2>

## Acknowledgment
Our code is based on  [``MEMIT``](https://github.com/kmeng01/memit.git) and [``AlphaEdit``](https://github.com/jianghoucheng/AlphaEdit.git).
