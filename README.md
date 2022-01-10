# MUCIC-MEDDOPROF
Participation of Team MUCIC in MEDDOPROF
# Introduction
Abstract. Technological developments in healthcare industry are generating lots of electronic health records as well as text data which is usually referred as medical text data. Processing medical text data in unstructured form is not only challenging but also has lot of applications. Named entity recognition, the task of extracting named entities and classifying them into predefined categories is an important preprocessing step in the NLP pipeline. Extracting named entities from medical text is very useful for many applications and at the same time very challenging because of the characteristics of medical text data. Considering the gravity of medical text processing, in this paper, we (Team MUCIC) describe the models submitted to ”MEDical DOocu-ments PROFessions recognition” (MEDDOPROF), a first shared task consisting of three Tracks, namely: Track 1: MEDDOPROF-NER, Track 2: MEDDOPROF-CLASS, and Track 3: MEDDOPROF-NORM, in Spanish language. We participated in Track 1 and 2 and proposed two models based on fine-tuning BERT embeddings using i) BertForTokenClassification from transformers and ii) Flair framework, for the automatic detection of Occupations and Professions in medical text. The model using BertForTokenClassification reported micro F1 scores of 0.629 and 0.598 for Track 1 and 2 respectively, while the Flair framework model reported micro F1 scores of 0.8 and 0.764 for Track 1 and 2 respectively. Further, the Flair framework model for MEDDOPROF-NER track became one among the best models.

# Prerequisites
pip install pycorenlp
pip install pyneuroner[gpu]
pip install -q flair
pip install seqeval
python -m spacy download es
python -m spacy download en

# Directory structure
The MUCIC_MEDDOPROF directory includes two jupyter notebook file as follows, meddoprof-final-bert.ipynb (for BERT model) and meddoprof-with-flair-final-code.ipynb (for BERT with Flair model)

# Installation
Each notebook includes comments for each cell in it and easy to replicate.

# Usage
It is suggested to be uploaded in Google Colab or Kaggle notebook and use GPU to execute the code.

# Examples
The code is Easy to be replicated just you need to run the cells one after another. (also check the path for datasets.)

# Input / Output
##converting dataset to conll representation , call the function in notebook as follow:**********
script: brat_to_conll(<Path to directory of dataset files>, <Path to generated conll file with .txt extension>, 'spacy', <intended language>)\n
#Examples\n
brat_to_conll('../input/oldmedoprof/experiments/test', './test.txt', 'spacy', 'es')
brat_to_conll('../input/full-meddoprof-ds/meddoprof-training-set/task1', './train.txt', 'spacy', 'es')

# Evaluation
The model using only Bert reported micro F1 scores of 0.629 and 0.598 for Track 1 and 2 respectively, while the Flair framework model reported micro F1 scores of 0.8 and 0.764
for Track 1 and 2 respectively that obtained second ranks at the MEDDOPROF-NER and CLASS subtasks


# Reference
Workshop overview paper:
  @article{lima2021nlp,
  title={NLP applied to occupational health: MEDDOPROF shared task at IberLEF 2021 on automatic recognition, classification and normalization of professions and occupations from medical texts},
  author={Lima-L{\'o}pez, Salvador and Farr{\'e}-Maduell, Eul{\`a}lia and Miranda-Escalada, Antonio and Briv{\'a}-Iglesias, Vicent and Krallinger, Martin},
  year={2021},
  publisher={Sociedad Espa{\~n}ola para el Procesamiento del Lenguaje Natural}
}
  
 Description of models at ADOP FERT-Automatic Detection of Occupations and Profession in Medical Texts using Flair and BERT:
  @inproceedings{DBLP:conf/sepln/BalouchzahiSS21,
  author    = {Fazlourrahman Balouchzahi and
               Grigori Sidorov and
               Hosahalli Lakshmaiah Shashirekha},
  title     = {{ADOP} FERT-Automatic Detection of Occupations and Profession in Medical
               Texts using Flair and {BERT}},
  booktitle = {Proceedings of the Iberian Languages Evaluation Forum (IberLEF 2021)
               co-located with the Conference of the Spanish Society for Natural
               Language Processing {(SEPLN} 2021), {XXXVII} International Conference
               of the Spanish Society for Natural Language Processing., M{\'{a}}laga,
               Spain, September, 2021},
  series    = {{CEUR} Workshop Proceedings},
  volume    = {2943},
  pages     = {747--757},
  publisher = {CEUR-WS.org},
  year      = {2021},
  url       = {http://ceur-ws.org/Vol-2943/meddoprof\_paper2.pdf}
}

# Contact
frs_b@yahoo.com

# License
Copyright © 2021 for this paper by its authors. Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0).
