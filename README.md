# ztm-ml-notes
Notes on Daniel Bourke + Andrei Neagoi's ML Course.

# Machine Learning 101 
## i. What is the goal of Machine Learning?
Computers were brought into this world to make completing tasks more efficient for humans.

The goal of machine learning is to make computers act more and more like humans. The more they act like humans, the more helpful they are for humans!

## ii. AI/Machine Learning/Data Science
*Artificial Intelligence* - human intelligence exhibited by machines.

**Narrow AI** - Machines can be just as good or even better than humans at certain tasks. Ex: detecting heart disease, playing chess, etc. Narrow AI is only good at one specific task extremely well.

**Artifical General Intelligence (AGI)** - Extremely good at many human tasks (we are approaching this era soon)

**Machine Learning** - a subset of AI. It's an approach to try and achieve AI through systems that want to find patterns through a set of data. Computers can do things without us saying, "do this, then do that". Stanford describes ML as the science of getting machines to act without humans specifying instructions.

**Deep Learning** - Techniques for implementing machine learning. (also: deep neural networks)

**Data Science** - Simply put, analyzing data. There's a lot of overlap w. ML.

## iii. Machine Learning Playground Exercise: https://teachablemachine.withgoogle.com/
### iv. How did we get to Machine Learning?
(Simplified version) We first used spreadsheets like excel to generate data and put it in an excel file to make business decisions. As companies got more idea, we created this idea of relational databases. We needed a better way to organize and understand things from data. Thus, came MySQL: this helped us read, write, and understand data of many different types. Then, in 2000s, we created this idea of "big data" since FB, Google, Twitter needed to store way more precise data for their customers. Then after, NoSQL + MongoDB came along to help us manage even more meta data.

Machine Learning came along to automate and help us make data-driven decisions more efficiently. This was due to the growth in data and the improvements of CPU, GPU, and computation.

![alt text](https://cdn.discordapp.com/attachments/1001013905411276820/1038307441550561290/Screenshot_2022-11-04_at_9.22.46_PM.png
)

### Oversimplified YouTube Recommendation Model: https://ml-playground.com/#

# iv. Types of Machine Learning 
![alt text](https://cdn.discordapp.com/attachments/1001013905411276820/1038338384369811506/Screenshot_2022-11-04_at_11.25.50_PM.png
)

**Supervised learning** - Pre-created categorizations for data. You can do things like classification: (is this an apple or a pear?) (regression, stock prices, etc).. GROUPS EXIST.

 **Unsupervised learning** -  Data that doesn't have labels / groups don't exist. Clustering means we need machine to create these groups. GROUPS DONT EXIST.

**Reinforcement learning** - Teaching machines through trial/error, reward/punishment. Reinforces positive rewards and changes behaviors based on negative rewards. 

# 2) ML and Data Science Framework
Machine Learning comes in three parts: data modeling, data collection, and deployment.

First, create a framework. Then, match it to DS and ML tools. Lastly, we'll learn by doing.

Determine what problem we're trying to solve. (supervised or unsupervised)

What kind of data do we have? (structured or unstructured?)

What does success mean to us? (metrics in where we want our models to be at of an accuracy - somethimg to aim for).

Features - which ones are most useful? Bodyweight is a numerical feature (ex: they're more likely to have heart disease. A ML model algorithm's goal is to turn this data into specific people.

Modeling - Based on our problem and data, which model should we use."

Experimentation - how can we improve? what can we try next?

Experimentation - how can we improve? what can we try next?

## i. Types of ML Problems

First, we should clarify for what types of problems we don't need ML to solve (since AI isn't the answer to everything): when a simple hand-coded instruction-based systen will work. For example, if you want to create your favorite dish, if you already know what you need in order to create the result and how to get there, you shouldn't and it wouldn't make sense to use ML to gather the processes.

Main types of machine learning: supervised learning, unsupervised learning, transfer learning, reinforced learning. These are the most common.

Transfer learning is when a machine is learning what another machine knows.

Learning types:Learning Types

## ii. Types of Data
Structured data - what we see in an excel file, such as rows and columns of different features and records.

Unstructured data - images, natural language text, transcribed phone calls, video calls, etc.

Data Types:

Static Data - Data that doesn't change over time. CSV is one of the most common types of data formats.

Static Data:

Streaming Data - Data that changes over times. For example, say you wanted to predict how stock prices change depending on news headlines, you'd be working with streaming data since news headlines update constantly. Most of the work you do in practice will start with static data. But once your efforts show more results and you learn, you'll soon be working with streaming data.

Streaming Data:

## iii. Types of Evaluation
An evaluation metric is a measure of how well a machine learning algorithm predicts the future. Depending on the task, your evaluation metric may change. Say for example, it's to detect heart disease, you'll want a model that calculates with at least 99% accuracy since that's a very important task. Also, if you're doing ML for companies, it'll also depend on what percentage they are comfortable with the evaluation metric being.

Evaluation Metric:

There are different types of metrics:DIfferent metrics

iv. Features in Data
Features are different forms of data. They refer to forms within structured and unstructured data. For example, if predicting heart disease, features would be variables like body weight, sex, blood pressure, etc. Using feature variables, we can find out the target variables (whether or not someone has heart disease).

Different features of data:

Feature Coverage - How many samples have the same features? Ideally, every sample has the same features

v. Modelling -- Splitting Data
It's important that essentially machines learn concepts and are able to apply them to a multitude of similar situations versus memorizimg concepts and final products -- since that isn't helpful for application and retention.

Splitting Data:

Different features of data

v. Picking Model, Tuning, and Comparison

### 3 Parts to Modelling

Choosing a Model (Training Data):

Tuning Data is essentially adjusting and tuning properties to create the best trained data as possible. ML models have hyperparameters you can adjust. Goal of tuning hyperparameters is to improve the model's performance.

When comparing models, you want to make sure that the training set has a close evaluation to the test set:comparing

Here's how you can tell if data is underfitting, overfitting, or just right (Goldilock's Zone):test sets

Fixes for overfitting / underfitting:

Underfitting & Overfitting Data: All experiments should be conducted on different portions of your data.

Training data set ??? Use this set for model training, 70???80% of your data is the standard. Validation/development data set ??? Use this set for model hyperparameter tuning and experimentation evaluation, 10???15% of your data is the standard. Test data set ??? Use this set for model testing and comparison, 10???15% of your data is the standard. These amounts can fluctuate slightly, depending on your problem and the data you have.

Poor performance on training data means the model hasn???t learned properly and is underfitting. Try a different model, improve the existing one through hyperparameter or collect more data.

Great performance on the training data but poor performance on test data means your model doesn???t generalize well. Your model may be overfitting the training data. Try using a simpler model or making sure your the test data is of the same style your model is training on.

Another form of overfitting can come in the form of better performance on test data than training data. This may mean your testing data is leaking into your training data (incorrect data splits) or you've spent too much time optimizing your model for the test set data. Ensure your training and test datasets are kept separate at all times and avoid optimizing a models performance on the test set (use the training and validation sets for model improvement).

Poor performance once deployed (in the real world) means there???s a difference in what you trained and tested your model on and what is actually happening. Ensure the data you're using during experimentation matches up with the data you're using in production.

## vi. Experimentation + Tools
Machine Learning projects become tool-matching projects. (what have we tried? what else can we try?)

Tools:

Anaconda, the hardware store for ML and DS tools
Jupyter Notebooks, to write Python code and communicate our work. All our projects are done here.
Pandas, Matplot Lib, NumPy; data analysis
Tensor Flow, Scikit Learn, Pytorch; building ML models
