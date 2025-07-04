# installing the jupyter notebook using external package virualenv

**option 1**

## install pip 

```bash
sudo apt install python3 python3-pip
```

## install virtual environment
```bash
sudo apt install python3-virtualenv
```
## create the virtual environment
```bash
virtualenv my-jupyter-env
```

## activate the virtual environment ( in home directory)
```bash
source my-jupyter-env/bin/activate
```
## install jupyter notebook
```bash
pip install jupyter
```

# run the notebook
```bash
jupyter notebook
``` 
## deactivate the virtual environment (optional)
```bash
deactivate
```

**option 2 - using in-built package venv**

## create directory
```bash
mkdir myproject
```
## change the directory
```bash
cd myproject
```
## create a virtual environment

```bash
python3 -m venv .venv
```
> -m is module and the module name is venv from python3 library
> .venv is the hidden directory for the virtual environment

## activate the virtual environment
```bash
source ~/myproject/.venv/bin/activate
```
## to deactivate the virtual environment
```bash
deactivate
```



