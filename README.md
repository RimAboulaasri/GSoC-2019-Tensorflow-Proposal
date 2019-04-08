### Project Proposal<br>Google Summer of Code 2019

# GitHub Issues Classification and Clustering

## TensorFlow 2.0

# Index
1. [Introduction](#introduction)
2. [Synopsis](#synopsis)
3. [Project](#project)
4. [Timeline](#timeline)
 
<div style="page-break-after: always;"></div>

# 1. Introduction 

## Personal Information
|   |   |
|---|---|
| **Full Name** | Rim Aboulaasri |
| **Education**   | 1st Year MSc in Agronomics Student<br>Statistics and Data Science Applied to Life Sciences<br>AgroCampus Ouest Rennes, France  |
| **Email**  | [rim.aboulaasri@agrocampus-ouest.fr](mailto:rim.aboulaasri@agrocampus-ouest.fr)<br>[rim.aboulaasri@gmail.com](mailto:rim.aboulaasri@gmail.com) |
| **Phone**  | +33 6 13 89 86 69 |
| **Github** | <https://github.com/RimAboulaasri> |
| **Programming Languages**| Python and R |
| **Timezone** | Central European Summer Time (GMT +001) |
| **Address** | 9 Residence Saint Jean Baptiste de la Salle <br>35000 Rennes - France|

## About Me

<p style="text-align:justify";> Hello, my name is Rim Aboulaasri and I study Statistics and Data Science applied to Life Sciences. I was born and grew up in Morocco before moving to France to pursue my higher education. I am interested in biology, genetics, machine learning and food technology. 

My favorite programming languages are Python and R. I think Python is a great language since it has a simple syntax and doesn’t require any memory management. Besides, it is one of the most frequently used languages in machine learning. I also enjoy working with R because it offers very useful modules and packages for data analysis.

I have recently worked on several data science and machine learning projects such as : </div> <br>


+ Sensometrics data analysis about Portuguese wines using <b>FactoMineR</b>
+ Prediction of Facebook accounts authenticity using <b>ScikitLearn</b> and <b>Pandas</b> 
+ Horse locomotion characterization using <b>FactoMineR</b> and <b>Shiny</b></p>

<div style="page-break-after: always;"></div>

### Why a TensorFlow GSoC Project ?

<p style="text-align:justify";> For the last decade, Artificial Intelligence has been growing really fast in many different fields. 
Data science and machine learning have a wide range of applications in both our everyday life but also for scientific research. As a part of biology courses, I have studied neural communication, and have always  been interested in this topic, especially when it comes to neural networks involved in deep learning. Since then, I have wanted to develop my machine learning skills and increase my knowledge about deep learning. That's why I have chosen to apply to this topic. I would be very proud to have Tensorflow be my first open-source contribution. As an enthusiastic knowledge seeker, I think that GSoC is a great opportunity for me to learn more about text classification and I am looking forward to work on such a powerful tool.</p>

### How much time will I be able to contribute to this project ?
<p style="text-align:justify";>I will be working 20 to 25 hours per week from the beginning of the project until June 11th. Then, I will be able to devote 35 to 40 hours per week to the project until September 2nd.</p>

### Other commitments during summer
<p style="text-align:justify";>I will be taking my final exams from June 6th to June 11th during which I will be little more busy than usual. Apart from that I do not have any commitments for next summer.</p>

### Preferred medium for communication
<p style="text-align:justify";>I am reachable via Email, Skype, FaceTime or any other similar medium of communication. My preferred languages for communication are English and French.</p>

# 2. Synopsis

<p style="text-align:justify";>Tensorflow is one of the most popular deep learning frameworks in the world. Thanks to its community driven development, thousands of people can collaborate on this project to make it even better. Unfortunately, since TensorFlow is growing really fast it also happens to have some issues. One of the ways to report those, is submitting tickets on the TensorFlow GitHub page. Even if this functionality is handy for developers, it stays quite difficult to distinguish issues priority and occurrence since they’re not sorted and grouped, which can lead to redundancy.

As a part of my Data Science degree, I would love to contribute to TensorFlow and help the community focus on the most important issues of the project by developing a GitHub issues classification and clustering tool.</p>

<!-- <div style="page-break-after: always;"></div> -->

## Benefits to Community

<p style="text-align:justify";> If my proposal is selected by TensorFlow teams, it will help the community to get more productive by organizing reported issues and gathering similar topics. Thanks to this project, TensorFlow maintainers will have a better overview of the important number of tickets and it will also make their tasks a little bit easier going through them. This will then have the effect to handle issues more efficiently and to reduce their processing time. Moreover, listing recurrent issues in a FAQ page on GitHub will help the TensorFlow community to get answers to these issues more quickly.</p>

# 3. Project 

## Objectives

+ <p style="text-align:justify";>Create a tool to classify thousands of GitHub open and closed issues about Tensorflow 2.0.</p>
+ <p style="text-align:justify";>Use machine learning algorithms to cluster them into thematic buckets.</p>
+ <p style="text-align:justify";>Facilitate TensorFlow maintainers tasks by spotting duplicated tickets and add the most common issues to a FAQ page in the TensorFlow GitHub.</p> 

## Milestones

<p style="text-align:justify";>I already have draft a road map to conduct this project:</p>



**1. Data retrieval**

+ <p style="text-align:justify";>First task would be to retrieve open and closed TensorFlow repository’s issues from GitHub using their API. Issues will be stored in JSON format.</p>


**2. Data pre-processing**

+ <p style="text-align:justify";>Second part of the project would consist of data pre-processing. This part can be done by using TensorFlow Transform library. It would also involve Normalization and Lemmatization.

	+ Data normalization would consist of transforming to lower-case, maybe removing punctuation marks and useless data about issues (to be defined) and also deleting « stop words ». I think that, in this case the most important data to keep, to train and test ML algorithms are issues titles and their bodies. 
	+ Lemmatization can be done by using Python tools such as <b>NLTK</b>  or <b>Tree Tagger</b> .</p>

<!-- <div style="page-break-after: always;"></div> -->

**3. Word embedding**

+ <p style="text-align:justify";>The representation of words by scalar vectors can be carried out by using `Keras.layers.embedding` method or by implementing a <b>Word2Vec</b>  model in TensorFlow.</p>


**4. Model building**

+ <p style="text-align:justify";>Fourth part would consist of building several models in order to compare their performance on our data set.

	+ In an unsupervised learning context, issues clustering would be based on K-means clustering method applied to issues bodies and titles and could involve auto-encoders. 
		- K-means clustering is a quiet simple method that is commonly used in unsupervised machine learning.
	+ I also thought of building Convolutional Neural Networks (CNN), Recurrent Neural Networks (RNN) with Keras. 
		- Indeed, CNN usually obtain good results on text classification tasks. They are great for learning the structure of the input data and they are known to be faster to train than RNN. 
		- On another side, RNN are interesting models because they can take sequences as inputs.</p>


**5. Model training**

+ <p style="text-align:justify";> This step would consist of creating validation sets and training built models.</p>

**6. Models deployments and prediction**

+ <p style="text-align:justify";> This step would be based on algorithms comparison. This process would go through performance evaluation by calculating and plotting (using matplotlib Python library) several metrics such as the accuracy, the logarithmic loss, the F1 score or the confusion matrix … for each model.</p>


**7. Fix eventual Model Training issues** 

+ <p style="text-align:justify";>Machine learning models involved in this project will probably be subject of over-fitting or maybe under-fitting. Those issues can be detected by comparing the accuracy of each model on training data and accuracy achieved on the validation data set. There are several solutions to reduce over-fitting such as : 

	+ adding more training data 
	+ using weight-regularization 
	+ adding dropout layers in neural networks
	+ reducing network’s capacity / architecture complexity 
	+ using batch-normalization</p>

**8. Updating issues on GitHub**

+ <p style="text-align:justify";> Once all the issues have been sorted and clustered, I will have to update them using GitHub's API. It will consist of gathering all the similar topics and clustering them in different categories.</p>

## Deliverables

+ <p style="text-align:justify";>Working Python tool to classify and cluster TensorFlow issues on GitHub.</p>
+ <p style="text-align:justify";>Complete documentation set to use the Python tool.</p>
+ <p style="text-align:justify";>Analytic charts comparing used machine learning algorithms for text classification and clustering.</p>


## Future Goals

+ <p style="text-align:justify";>Explore the possibility of visualizing data and issues clusters by using R or Python modules.</p>


<div style="page-break-after: always;"></div>


# 4. Timeline

| <center>Duration</center> | <center>Task</center> |
|---|---|
| April 9th  | <center>**Project Proposal Submission Deadline**<center> |
| March 9th - May 5th | <up><li>Learn more about word embedding with Word2Vec .</li><li>Read Documentation and learn more the use of Auto-encoders for text classification. </li><li>Learn more about RNN such as LSTM, BLSTM and GRU neural networks and comparing their performances.|
| May 6th - May 27th | <center>**Community Bonding**</center><up><li>Get Involved with TensorFlow community.</li><li> Get to know more my mentors.</li><li>Learn about other TensorFlow projects .</li><li> Ask for some advice about text classification to TensorFlow team members such as Laurence Moroney.</li><li>Learn about other TensorFlow projects .</li><li>Get familiar with various TensorFlow tools.</li></up>
| May 27th - June 24th | <center>**Coding Period Start**</center><up><li>**Do Tasks 1, 2 and 3**<up><li>Retrieve and pre-process data.</li><li>Implement words embedding.</li></up><li>Begin to think about eventual classification buckets themes.</li></up>|
| June 24th - June 28th | <center>**First Evaluations**</center><up><li>Submit documented code for tasks 1, 2 and 3 to the git repository.</li></up>|
| June 28th - July 22nd | <center> **Coding Period continues**</center><up><li>**Improve first repository version**<up><li>Use first evaluation feedbacks to optimize or correct previous tasks.</li></up></li><li>**Do tasks 4, 5 and 6**<up><li>Build K-mean, Auto-encoder, RNN and CNN models.</li><li>Train and deploy them</li></up>|
| June 24th - June 28th | <center>**Second Evaluation**</center><up><li>Submit documented code for tasks 1 to 6 to the git repository.</li></up>|
| July 22nd - July 26th | <center> **Coding Period continues**</center><up><li>**Improve second repository version**<up><li>Use second evaluation feedbacks to optimize or correct previous tasks.</li></up></li><li>**Do tasks 7 and 8**<up><li>Try to detect overfitting or under-fitting issues.</li><li>Reduce them with existing methods</li></up>|
| August 19th - August 26th | <center>**Final Submission**</center><up><li>Submit final code with complete documentation to the git repository.</li></up>|