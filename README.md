# VerbCLIP
This repository contains the code for the paper "VerbCLIP: Improving Verb Understanding in Vision-Language Models
with Compositional Structures" to be presented at the [3rd Workshop on Advances in Language and Vision Research (ALVR)](https://alvr-workshop.github.io).  

### Pre-requisites
Install the dependencies in `requirements.txt` using the following command:
```bash
pip install -r requirements.txt
```
> Note: When running the VALSE experiment, you have to install the spaCy model separately using the following command (if not already installed):
```bash
python -m spacy download en_core_web_sm
```

### pre-computed embeddings
To make the experiments reproducible and efficient, we provide the embeddings used. 
The embeddings are stored in pickle files, each containing a dictionary where the keys are the strings (either texts or IDs of images) and the values are the embeddings.
__Matrix embeddings__ are also provided in the same format.
Since the files are too large, we have to make them accessible through Google Drive.

The embeddings are organized per experiment. Simply download the embeddings for the experiment you want to run and put them in `experiments/{experiment}/embeddings` (create the directory if it does not exist).

Download links are provided below.
 - __VALSE__ embeddings can be downloaded from [here](https://drive.google.com/file/d/10iSkdGmowjhe7hF6zdTV-uOZ9lwQA8hK/view?usp=drive_link).
 - __VL_Checklist__ embeddings can be downloaded from [here](https://drive.google.com/file/d/1XE71kfnkk9bDGC0RPWJlzd2q2-AGEQMu/view?usp=drive_link).
 - __SVO_Probes__ embeddings can be downloaded from [here](https://drive.google.com/file/d/1To9M95xom1dHAHgtF5X9LiLhalJX9YCj/view?usp=drive_link).

After adding the embeddings, the directory structure should look like this: 
```
experiments
└───valse
│   └───embeddings
│       │   img_emb_14.pkl
│       │   ...
│   ...
└───vl_checklist
│   └───embeddings
│       │   img_emb_14.pkl
│       │   ...
│   ...
└───svo_probes
│   └───embeddings
│       │   img_emb_14.pkl
│       │   ...
│   ...
```

### Running the experiments
To run the experiments, simply run the Jupyter notebook in the `experiments/{experiment}` directory, where `experiment` is one of `valse`, `vl_checklist`, or `svo_probes`.

Any comments or questions are welcome. Please feel free to open an issue or contact us directly.