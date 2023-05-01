# DATA 245 Project
# Building SDG Classifier: Monitor the Process of the SDGs using Machine Learning
![](images/SDGs.png)

 Angel Ren 016729557  
 Bertha Tam 012313600  
 Johnny Qiu 016237780  
 Manyu Zhang 016718858  
 Yuan Pan 016102138

***
## Abstract

***
## Dataset
We have selected the OSDG Community Dataset containing SDG labels being validated by Community Platform scientists. It contains text passages extracted from reports, policy papers, and abstracts of publications.The dataset is usually updated once every three months, and we used the newest version published on Apr 2023.

Each text passage has approximately 90 words. The SDG labels were validated by over 1,400 Community Platform scientists. The dataset is usually updated once every three months, and we used the newest version published on Apr 1st, 2023 .

https://zenodo.org/record/5550238

![](images/dataset.jpg)
***
## Methodology
While each text can be related to multiple SDGs, each data instance was assigned a single SDG from the dataset. To better address this multi-label classification problem, we generated a new labeled dataset from our original dataset. We used TF-IDF to convert the texts to vectors and applied k-means clustering with a hyperparameter k of 16. After examining the word clouds generated from the clustering, we manually assigned SDG labels to those clusters and generated a 15 labeled dataset from the metadata.

With two different labeled datasets on hand, we trained five multi-classification classifiers and compared their performance using accuracy, F1 score and confusion matrix. Finally, we selected the better model and tested it on new text scripts.

![](images/Framework.png)

