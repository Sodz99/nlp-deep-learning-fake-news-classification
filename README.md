# NLP and Deep Learning For Fake News Classification in Python

NLP and Deep Learning For Fake News Classification in Python — NLP project.

## Overview
Business Overview

What is Fake News? Fake news is the deliberate presentation of (typically) false or misleading claims as news, where the claims are misleading by design.

How News and digital media evolved? The news media evolved from newspapers, tabloids, and magazines to a digital form such as online news platforms, blogs, social media feeds, and many news mobile apps. News outlets benefitted from the widespread use of social media/mobile platforms by providing updated news in near real time to its subscribers. It became easier for consumers to acquire the latest news at their fingertips. So, These digital media platforms become very powerful due to their easy accessibility to the world and ability to allow users to discuss and share ideas and debate over issues such as democracy, education, health, research and history.

## Data
In our study we used the Fake news dataset from Kaggle to classify unreliable news articles as Fake news using Deep learning Technique Sequence to Sequence programming. A full training dataset with the following attributes
- id : unique id for a news article
- title: the title of a news article
- author: author of the news article
- text : the text of the article; could be incomplete
- label : a label that marks the article as potentially unreliable ○ 1 : unreliable ○ 0 : reliable

_Data is not included in this repository._

## Approach
1. Data cleaning / Pre-processing (outlier/missing values/categorical) - a. Removing Missing record b. Merge all text together c. Removing special character from text
2. Sequence Data Preparation a. Tokenizing text after preprocessing b. Build Vocabulary to filter text sets: Choose length of maximum vocabulary size c. Sequence data preparation: i. Use vocab ii. Maximum sequence length iii. Padding
3. Word Embedding - This is a step where we convert text data to meaningful numerical vectors. We use a pre-trained glove to convert into a numeric vector.
4. Build Sequence Model - Building Sequence layer with embedding, Dense, Dropout with below sequence layer: a. Simple RNN b. LSTM c. GRU
5. Validate Model Training - Which model will be finalized on the basis of the following a. Confusion matrix b. Accuracy
6. Model comparison - Model comparison in terms of performance, stability and computation time

Modular code overview

Once you unzip the modular_code.zip file you can find the following folders within it.
1. input
2. src
3. output
4. lib
1. The input folder contains all the data that we have for analysis. In our case, it will contain three csv files which are a. submit.csv b. test.csv

c. train.csv It also has another folder called glove which contains the glove embedding file
2. The src folder is the heart of the project. This folder contains all the modularized code for all the above steps in a modularized manner. It further contains the following. a. ML_pipeline b. engine.py

The ML_pipeline is a folder that contains all the functions put into different python files which are appropriately named. These python functions are then called inside the engine.py file

3. The output folder contains two folders. They are : a. models - The models folder contains all the models that we trained for this data saved as reusable files. These models can be easily loaded and used for future use and the user need not have to train all the models from the beginning. b. reports - The report folder contains a csv file which stores all the models trained along with their accuracy and other details.
4. The lib folder is a reference folder. It contains the original ipython notebook that we saw in the videos.

## Tech stack
➔ Language : Python ➔ Libraries : Scikit-learn , Tensorflow , Keras, Glove, Flask, nltk, pandas, numpy

## How to run
```bash
pip install -r modular_code/requirements.txt
python modular_code/src/engine.py
```
Notebooks: [`fakenews_seq_classification.ipynb`](modular_code/lib/fakenews_seq_classification.ipynb)

## Project structure
```
.gitignore
README.md
modular_code/
  lib/
    fakenews_seq_classification.ipynb
  requirements.txt
  src/
    ML_Pipeline/
    engine.py
```

## Credits
Based on a ProjectPro guided project.
