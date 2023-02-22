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
<br />
![Figure 1](https://i.postimg.cc/dD57xq2J/Screenshot-2023-02-21-215328.jpg)
![Figure 2](https://i.postimg.cc/0rkMn6Jt/Screenshot-2023-02-21-215352.jpg)

The model is trained with Gensim Word2Vec model with the tokenized lines of code, and I tested the model to check similar words. <br />
For example, I examined the closest words to **“for”** which is a common word used in python code. The results show that the top three closest words to **""for"** are **"to"**, **"not"**, **"f"**.<br />
![Figure 3](https://i.postimg.cc/zbjL5N4S/Screenshot-2023-02-21-215422.jpg)

I also tested the model on **"if"** which is another very common word used in python code. The results show that the top three closest words to **""if"** are **"in"**, **"to"**, **"f"**.<br />
![Figure 4](https://i.postimg.cc/YLCvCVHc/Screenshot-2023-02-21-215436.jpg)

In addition, the results for the similarity between **"math"** and **"numpy"** gave a score of approximately 0.3. <br />

As an extension, I used the model to find the 50 most common identifiers in Python from the frequencies in the python txt file which you can see below. <br />
np: 4721
plt: 3864
ax: 2673
fig: 1659
X: 1301
y: 1206
x: 1059
axs: 766
def_gen: 709
ax1: 539
random_st: 504
ax2: 462
print: 441
t: 375
A: 316
Y: 283
rng: 280
D_arr_0p5: 271
__all__: 268
X_train: 249
n_samples: 240
Z: 238
len: 226
X_test: 219
D_arr_like_0p5: 217
iris: 215
data: 206
clf: 190
i8: 188
s: 184
re: 180
time: 179
y_train: 175
i: 159
b_: 157
int: 156
__name__: 152
y_test: 142
i4: 138
z: 135
_: 128
xx: 128
N: 128
ax3: 127
float: 127
os: 126
b: 126
a: 120
ax0: 118
c: 116

Using the Python2Vec model, I then calculated the similarity between each pair of the 50 most common identifiers and highlighted interesting patterns. 
The most similar and most dissimilar words can be shown in the figure below. <br />
![Figure 5](https://i.postimg.cc/J79ZFWgx/Screenshot-2023-02-21-235150.jpg)

### Discussions



### References
1. https://github.com/tech-srl/code2vec
2. https://github.com/nalmadi/CS421-project2
3. Uri Alon, Meital Zilberstein, Omer Levy, and Eran Yahav. 2019. Code2vec: learning distributed representations of code. Proc. ACM Program. Lang. 3, POPL, Article 40 (January 2019), 29 pages. https://doi.org/10.1145/3290353