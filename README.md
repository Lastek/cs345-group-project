# cs345-group-project

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
