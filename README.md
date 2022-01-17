# knowledge-distillation-seq
This repository implements sequence-level knowledge distillation (Kim and Rush 2016)

## Quick Start:
1. Installation
```
git clone https://github.com/OpenNMT/OpenNMT-py
cd OpenNMT-py
pip install -e .
mkdir th-en/run
```

2. Download dataset
* `th-en dataset`: [thai-english](https://sites.google.com/site/iwsltevaluation2015/mt-track) dataset for machine translation task, which can be found in 2015-01 folder. We then process it with [Sentencepiece Tokenizer](https://github.com/google/sentencepiece).

3. Run
Create three .yaml files inside OpenNMT directory for teacher, student and distilled networks, where the first two have a dataset path generated from sentencepiece tokenizer and distilled config file has a dataset path generte from trained teacher network. Instead of shell file I prefer notebook format, so to train all three networks run the following.
```
$ run OpenNMT-py.ipynb
```
