# What GPT Knows about Who is Who

This is the repository for our paper *What GPT Knows About Who is Who*.

Our abstract:

*Coreference resolution – which is a crucial task for understanding discourse and language at large – has yet to witness widespread benefits from large language models (LLMs). More- over, coreference resolution systems largely rely on supervised labels, which are highly ex- pensive and difficult to annotate, thus making it ripe for prompt engineering. In this paper, we introduce a QA-based prompt-engineering method and discern generative, pre-trained LLMs’ abilities and limitations toward the task of coreference resolution. Our experiments show that GPT-2 and GPT-Neo can return valid answers, but that their capabilities to identify coreferent mentions are limited and prompt- sensitive, leading to inconsistent results*


## Environment Setup

### Option 1) Colab
The most easy way to run the notebooks from this project is our [Gdrive version of this project](https://drive.google.com/drive/folders/1pBpo-uD_HFropodUNIFH3nmh37blK9hF?usp=sharing).

You only need to add a shortcut of this folder to your own drive, which makes sure it all the paths used match and work.

### Option 2) Local environment

You can create the required conda env with:

```bash
conda env create -f corefGPT.yml
```

Then you can start the conda env with:

```bash
conda activate corefGPT
```

You will need to download the "Data" and "Results" folders from [our drive](https://drive.google.com/drive/folders/1pBpo-uD_HFropodUNIFH3nmh37blK9hF?usp=sharing) and place them in the root of this directory


And you will need to download the "models" folder from [Models/Streamline from our drive](https://drive.google.com/drive/folders/1VvoF_6IGiN4_o-8xpFLO1TQ6h1-nRwl_) and place that locally under Models/Streamline, so the path is Models/Streamline/models.

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





