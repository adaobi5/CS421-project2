# CS421-project2

**Project 2: Python2Vec**
Forked from https://github.com/nalmadi/CS421-project2

Table of Contents
=================
  * [Abstract](#abstract)
  * [Results](#results)
  * [Discussions](#discussions)
  * [References](#references)

### Abstract
This project implemented a Python2Vec model using a Word2Vec model trained with Python code. The project involves mining public software repositories for Python code, cleaning the data, and training a Word2Vec model with the collected source code. The model will then be tested with real-life data to determine the similarity of identifiers in code. I used knowledge of mining software repositories and data cleaning, and created a Jupyter Notebook (python-2vec.ipynb) to complete the necessary steps to create a Python2Vec model.

### Results
The python-2vec notebook takes in a list of the following Github repositories **Matplotlib**, **Sckit-Learn**, **Numpy**, **Scipy**, **Flask**, **Requests**, and **Scrapy**.
The code automatically crawls through these repositiories looking for Python code (files that end in .py), and aggregates them into a single txt file (python_files.txt). The lines and words are counted, and everything is tokenized before it is trained using the Gensim Word2Vec model.

The results below are a result of the trained Python2Vec model of the 7 Github repositories, which were aggregated into the txt file (python_files.txt).
<br />
This file contained 1,439,996 lines and thus 5,978,486 words. 
![Figure 1](https://i.postimg.cc/dD57xq2J/Screenshot-2023-02-21-215328.jpg)
![Figure 2](https://i.postimg.cc/0rkMn6Jt/Screenshot-2023-02-21-215352.jpg)




### Discussions



### References
1. https://github.com/tech-srl/code2vec
2. https://github.com/nalmadi/CS421-project2
3. Uri Alon, Meital Zilberstein, Omer Levy, and Eran Yahav. 2019. Code2vec: learning distributed representations of code. Proc. ACM Program. Lang. 3, POPL, Article 40 (January 2019), 29 pages. https://doi.org/10.1145/3290353