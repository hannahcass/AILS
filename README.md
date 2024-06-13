### Install Conda env

conda create --name env_name

## Install Poetry

(Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | py -

## Install torch

poetry run pip install torch==1.12.1+cu116 torchvision==0.13.1+cu116 -f https://download.pytorch.org/whl/torch_stable.html

## Install the rest of required packages

## Check if cuda active

poetry run python -c "import torch; print(torch.cuda.is_available())"

python -c "import torch; print(torch.cuda.is_available())"

## Evaluate results

python .\evaluation_script.py --submission="probs.csv" --target="data_train.csv"
