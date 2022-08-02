# UniK-QA: Unified Representations of Structured and Unstructured Knowledge for Open-Domain Question Answering

[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/unified-open-domain-question-answering-with/knowledge-base-question-answering-on-1)](https://paperswithcode.com/sota/knowledge-base-question-answering-on-1?p=unified-open-domain-question-answering-with)
<br>
[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/unified-open-domain-question-answering-with/open-domain-question-answering-on)](https://paperswithcode.com/sota/open-domain-question-answering-on?p=unified-open-domain-question-answering-with)
[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/unified-open-domain-question-answering-with/open-domain-question-answering-on-natural)](https://paperswithcode.com/sota/open-domain-question-answering-on-natural?p=unified-open-domain-question-answering-with)

This repo contains code for our paper (UniK-QA is pronounced as *unique-QA*):

[UniK-QA: Unified Representations of Structured and Unstructured Knowledge for Open-Domain Question Answering](https://arxiv.org/pdf/2012.14610.pdf)
<br>
Barlas Oguz*, Xilun Chen*, Vladimir Karpukhin, Stan Peshterliev, Dmytro Okhonko, Michael Schlichtkrull, Sonal Gupta, Yashar Mehdad, Scott Yih
<br>
(*Equal Contribution)
<br>
**Meta AI**

## Getting the Data

After cloning the repo, run the following in the root directory of the repo to fetch the WebQSP data:
```
wget https://dl.fbaipublicfiles.com/UniK-QA/data.tar.xz
tar -xvf data.tar.xz
```

## Reproducing the WebQSP experiment



Follow the interactive Jupyter notebook `UniK-QA on WebQSP.ipynb` to reproduce our experiment on WebQSP.

- The script will first convert the KB relations into text sentences.
- [DPR](https://github.com/facebookresearch/DPR) is then run to select the most relevant relations for each question.
- Next, the input to the [FiD](https://github.com/facebookresearch/FiD) reader is created for each question using the most relevant relations retrieved by DPR.
- Finally, a FiD model can be trained using the UniK-QA input. Our trained FiD checkpoint can be downloaded [here](https://dl.fbaipublicfiles.com/UniK-QA/fid_checkpoint.tar.xz). (Our model was trained in late 2020, so you may need to check out an older version of FiD.)

## License
UniK-QA is CC-BY-NC 4.0 licensed, as found in the LICENSE file.
