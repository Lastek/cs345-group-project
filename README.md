# cs345-group-project
## Models
<a href="https://drive.google.com/drive/folders/1-MHkMswFc7CxYdtASQorc5PKhktiUBAx?usp=sharing"> Link to Models </a>


## Setup

Create environment from env.yml:\
`conda env create -f env.yml`

If you choose to rename the environment:\
`conda rename -n steamgames <new_name>`

If you have any issues try updating conda:\
`conda update -n base conda`

For faster conda package solver:

```shell
conda update -n base conda
conda install -n base defaults::conda-libmamba-solver
conda config --set solver libmamba
```

## Automatic commit preparation using pre-commit hooks:
Make sure your conda environment is active in the terminal and run:\
`pre-commit install`

This will clean the notebook before a commit is made.

To override and commit without cleaning add the `--no-verify` flag:\
`git commit -m "example" ---no-verify`

Be careful as it will skip ALL other hooks you may have.

To manually run the nb-clean pre-commit hook:
`pre-commit run nb-clean`


## Prepping notebook for commit (manual)

Standard cleaning:\
`nb-clean clean notebook.ipynb`

Keep original copy before cleaning:\
`nb-clean clean < original.ipynb > cleaned.ipynb`

Clean notebook but leave cell metadata:\
`nb-clean check --preserve-notebook-metadata notebook.ipynb`

To remove empty cells add `-e` flag.

To preserve cell outputs use `-o` flag.

More info about <a href="https://github.com/srstevenson/nb-clean">nb-clean</a>

