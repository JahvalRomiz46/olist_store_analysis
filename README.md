# Olist Store Dashboard

## Setup Environment - Anaconda

```
conda create --name submission-env python=3.12.7
conda activate submission-env
pip install -r requirements.txt
```

## Setup Environment - Shell/Terminal

```
mkdir submission-env
cd submission-env
pipenv install
pipenv shell
pip install -r requirements.txt
```

## Run steamlit app

```
cd dashboard
streamlit run dashboard.py
```
