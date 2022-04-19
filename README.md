# What GPT Knows about Who is Who

This is the repository for our paper *What GPT Knows About Who is Who*.

Our abstract:

*Coreference resolution -- which is a crucial task for understanding discourse and language at large -- has yet to witness widespread benefits from large language models (LLMs). Moreover, coreference resolution systems largely rely on supervised labels, which are highly expensive and difficult to annotate, thus making it ripe for prompt engineering. In this paper, we introduce a QA-based prompt-engineering method and discern generative, pre-trained LLMs' abilities and limitations toward the task of coreference resolution. Our experiments show that GPT-2 and GPT-Neo can return valid answers, but that their capabilities to identify coreferent mentions are limited and prompt-sensitive, leading to inconsistent results.*


## Environment Setup

### Local environment

You can create the required conda env with:

```bash
conda env create -f corefGPT.yml
```

Then you can start the conda env with:

```bash
conda activate corefGPT
```

To start easily, you can download our processed ECB+ files from [here](https://drive.google.com/file/d/1jQB8lmtfbgN0rWCyeKBfRn81gCCfTcxT/view?usp=sharing) and place them in the root of this directory. Moreover, to experiment with the Streamlining model, you can download our trained model from [here](https://drive.google.com/file/d/1UW9qpKl6gQD8ysvke-lUNMcd-HjhTfr6/view?usp=sharing) and place that locally under Models/Streamline.

### Setting up the right paths

Lastly, when running the notebooks you have to change the lines the prefix the grdrive path with the local path. So this:
```python
local_path = ""

# Change this to "local_path" if you run the notebook locally
root_path = gdrive_dir_path
```

Needs to be changed to this:
```python
local_path = ""

# Change this to "local_path" if you run the notebook locally
root_path = local_path
```

## Model runtimes

Below you will see how long each model took to run on colab:


| Model | GPT2  | GPT-NEO-125M | Multi-pass Sieves  | E2E      | Streamline (Pairwise) |
| :---: | :---: | :---:        | :---:              | :---:    | :---:                 |
| Time  | 3h    | 7.5h         | 5h                 | 2m       | 2h                    |





