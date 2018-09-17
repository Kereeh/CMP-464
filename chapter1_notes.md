---
title: Chapter 1 - The Machine Learning Landscape
description: Notes and Exercises for Chapter 1
---

What
Machine Learning is the science of programming computers so they can learn from data

Why
1. Instead of manually fixing code, ML algorithm can do it simpler and better
2. ML techniques provide different perspective in finding solutions than traditional problems
3. ML provides insight to large datasets

Types
1. Supervised, Unsupervised, Semisupervised, Reinforcement Learning - how much human supervision there is
2. Online vs Batch Learning
3. Instance-based vs Model-based learning

Supervised Learning - training data fed to the algorithm has labels
    1. Classification such as spam filters
    2. Predicting a target numeric value given a set of features (predictors) - regression task
    a. kNN
    b. Linear Regression
    c. Logistic Regression
    d. Support Vector Machines
    e. Decision Trees and Random Forest
    f. Neural Networks

Unsupervised Learning - training data is unlabeled
    a. Clustering - try to detect groups based on similar features(?)
        1. k-Means
        2. Hierarchical Cluster Analysis
        3. Expectation Maximization
    b. Visulation and dimensionality reduction - outputs a 2d or 3d representation of data that can be plotted - easy to understand patterns visualy. 
        1. Principal Component Analysis
        2. Kernel PCS
        3. Locally-Linear Embedding
        4. t-distributed Stochastic Neighbor Embedding
    c. Association rule learning - dig into large amounts of data and discover interesting relations betewen attributes (how different is this with clustering?)
        1. Apriori
        2. Eclat

Semisupervised Learning - a lot of unlabelled data with a little bit of labeled data.
    Example is how google photos is able to identify people in images with a litle bit of labeling from the user
    Deep belief networks are based on unsupervised components called restricted Blotzzmann machines

Reinforcement Learning - a learning system where an [agent] observes the environment, select and performs action, and get [rewards] in return or [penalties] for mistakes. It then learns by itself what the best strategy [policy] is to get the most reward over time. 

Batch Learning - system is unable to learn incrementally - must be trained with ALL of data (no split between test and train set) and is typically done offline. Takes a lot of time and commputing resources because it will train on the ful lset of data. 

Online Learning - opposite of batch learning where the system learns incrementally by feeding it [mini-batches] of data. This is faster and cheaper than batch learning. Best used for systems that receive data as continuous flow with the need to adapt and change rapidly. 
Learning Rate is an important parameter of this system - it is how fast they should adapt to the changing data. Don't necessarily want a super fast one nor a super slow one. 

Approaches to Generalization:
Instance-based Learning is when the system learns the examples by heart(??) then generalizes to new cases using a similary measure.

Model-based learning is building a model given the examples, and use that to make [predictions]

Challenges of Machine Learning
1. Insufficient Quantity of Training Data
2. Nonrepresentative Training Data
3. Poor Quality Data
4. Irrelevant Features
5. Overfitting the Training Data
6. Underfitting the Training Data

TESTING AND VALIDATING
Splitting data into two sets: training and test set. Train your model on the training set, and test using test set. The error rate on new set is called [generalization error] or [out-of-sample error], and then evaluating the model on the test set. This gives us information on whether or not we overfit or underfit in the training set. 

A second holdout set of data called the validation set - where you train multiple models with various hyperparameters and select which ones perform on the validation set. 

NO FREE LUNCH

Summary
1. ML is a system where machines laern from data instead of explicitly list the code rules
2. There are many types of ML systems
3. ML project includes gathering data in a training set, then feeding training set to a learning algorithm. 
4. Data needs to be sufficient and relevant; model needs to be neither too simple nor too complicated. 

Exercises
1. How would you define Machine Learning?
    It is a way for machines to learn and improve itself based on data.
2. Can you name four types of problems where it shines?
    Spam filter using classification
    Training AI systems such as the Dota Bot with Reinforcement learning
    Predicting stock market or election results (can this count as 2)
3. What is a labeled training set?
    Dataset with column headers
4. What are two most common supervised tasks?
    Classification in spam filters
    Regression task by predicting a numerical value based on a given set of features
5. Can you name the four common unsupervised tasks?
    Clustering
    Visualization
    Dimensionality Reduction
    Association Rule Learning
6. What type of Machine Learning Algorithm would you used to allow a robot to walk in various unkown terrains?
    Reinforcement learning, where the robot loses points everytime it bumps into a wall, and gains points for not losing points.
7. What type of algorithm would you use to segment your customers into multiple groups?
    Unsupervised Learning using clustering
8. Would you frame the problem of spam detection as a supervised or unsupervised learning problem?
    If there are no labels of spam and ham, then it would be an unsupervised learning problem.
    We could then look at the data, and then label them ourselves, and then it would become a supervised learning
