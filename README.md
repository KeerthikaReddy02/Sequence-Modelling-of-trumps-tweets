# Deep Learning Sequence Modeling

## Requirements

- [uv](https://docs.astral.sh/uv/)
- Python 3.13 or newer

Install `uv` using the instructions for your operating system in the
[official installation guide](https://docs.astral.sh/uv/getting-started/installation/).

## Set up the project

From the project directory, run:

```shell
uv sync
```

This creates the project environment and installs the dependencies recorded in
`uv.lock`. To keep the lockfile unchanged while syncing, use `uv sync --locked`.

## Run

Run the project command with:

```shell
uv run dl-seq-modeling
```

The command is defined in `pyproject.toml`. `uv run` runs it in the project environment.

## Add dependencies

Add a runtime dependency with:

```shell
uv add package-name
```

For example:

```shell
uv add requests
```

`uv add` updates `pyproject.toml` and `uv.lock`.

## Project structure

The project structure is as follows:
- data - Folder to process the data
- src - Contains the main source code
    - config.py - Python script to define the hyperparameters
    - dataset.py - Python script to set up the dataset and dataloaders
    - predict.py - Inference/prediction script for tweets
    - train.py - Unified training and validation loop
    - models - Has all the model definitions - gru, lstm, transformers
- notebooks
    - exploration.ipynb - Notebook for EDA and quick prototyping