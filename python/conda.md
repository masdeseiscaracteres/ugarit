# Conda
## Packages installed by default
Show conda configurations. Useful to identify which channels it is using by default and which packages are installed by default
(e.g. [`add_pip_as_python_dependency`](https://conda.io/docs/user-guide/configuration/use-condarc.html#add-pip-as-python-dependency-add-pip-as-python-dependency) 
specifies whether pip (and others) are included when python is installed):
```
conda config --show
```

## How to create an environment in a specific location
Create an environment called `env1` in `D:\Users\username\.conda\envs\`:
```
conda create -p D:\Users\username\.conda\envs\env1
```

Check results by showing the list of existing environments:
```
conda info --envs
```

## How to create fully isolated environments
Environments created by conda are not fully independent of others. For example, if you do:
```
conda create -c conda-forge -n env1 python=3.5
activate env1
```
`pip list`ing this new environment will show packages in the new environment but also those in the USER_SITE (https://github.com/conda/conda/issues/394).

To create fully isolated environments, set the environment variable: 
```
PYTHONNOUSERSITE=1
```
