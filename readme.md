# Dataquest.IO guided projects

# Introduction

In the completion of the Dataquest.IO Data Scientist in Python path, there were
a number of guided projects to work on real, small data sets. The guided projects
were intended to showcase a student's abilities and work style.

The purpose of this repo is to house and collate all the guided projects
I've worked on, as well as give a brief overview of each, and the skills and
technologies used. Not all the projects contain what I would call flourish. Many
I simply aimed to complete the written objectives. Towards the completion of the
certificate, I decided to test my skills and went further than what was required

Note: LLMs were used for parts of this, see [Disclaimer](#disclaimer)

# History

Some of the projects originally lived in their own repos. I realised at the
completion it was cleaner to contain them all in one.
As a result, the commit history of individual projects has not
been preserved in this repo

# Portfolio projects

## 1. [Classifying Heart Disease](./heart_disease/pipeline_full.ipynb)

This project was about building a classifier to predict heart disease from some
initial screening tests using logistic regression. I decided to teach myself
the `pipeline` syntax of `sklearn` and perform recursive feature elimination with
cross validation to build a model. This pipeline was then used to perform a hyperparameter
optimisation. The end result was a model that was that achieved a higher accuracy and precision
than what was available from the baseline model.

## 2. [Predicting Gym Attendance](./gym_attendance/simple.ipynb)

This project was to build a model to predict gym attendance at any given time point in a year
using stochastic gradient descent regression. It allowed me to demonstrate
the value of doing some thorough data inspection and cleaning, the holiday data column was broken,
so I reconstructed it using what information I could glean about the location of the gym.

I used a GridSearch with cross validation for hyperparameter optimisation, but demonstrated that
performing clever feature engineering increases the accuracy of the model substantially more
than increasing the size of the hyperparameter space.

## 3. [Predicting Employee productivity using decision trees](./decision_trees/main.ipynb)

This project was to take some productivity data from a clothing manufacturer in
Bangladesh, and build a decision tree to predict whether a given shift and team of workers would be productive.
This was the first project where I built a pipeline to make use of selectively turning on or off a feature in a
hyperparameter search. I also used `dtreeviz` for the visualisation of the decision trees.

## 4. [Predicting listing gains in Indian IPO market](./indian_ipo_tensorflow/main.ipynb)

This was the first project using Tensorflow and building neural networks. I split
the data by time, to see how well it could predict the future. Unfortunately the split date
was around March 2020, just as COVID was spreading around the world. Unsurprisingly, the model did
not predict COVID and had generally poor accuracy.

## 5. [Credit card customer segmentation](./credit_card/simple.ipynb)

This project involved taking customer data from a credit card company and using K-Means algorithm to work out
appropriate customer demographics for advertising campaigns. The work determined 3 primary clusters, containing most
customers and 3 smaller clusters for more niche customer profiles.

# Other Projects

## 1. [Building spam filter using naive bayes](./spam_filter/simple.ipynb)

Using a labeled SMS data set, built a naive bayes filter to classify messages as spam or not with 98% accuracy.

## 2. [Lottery addiction](./lottery/simple.ipynb)

Using some probability and basic functions, writing some trivial code to display odds of winning a lottery

## 3. [Finding best markets to advertise in for an e-learning company](./e-learning/simple.ipynb)

Analysing the results of a freeCodeCamp survey, using demographics and reported income levels

## 4. [Northwinds Traders](./northwinds_sql/main.ipynb)

Using SQL to extract insights from customer, employee and sales data about the performance of the company

## 5. [Predicting forest fires](./forest_fires/main.ipynb)

Aim of the project was to see if using meterological data and indicators from Fire Weather Index (FWI) could be used
to predict the total area burned in a forest fire. Several models were attempted, but using linear models to model
the behaviour of a non-linear process did not yield models worth implementing.

## 6. [Predicting insurance costs](./insurance/simple.ipynb)

Looking at patient demographics and health indicators, and insurance charges. Trying to predict what the cost of a
patient would be.

## 7. [Winning Jeopardy](./jeopardy/simple.ipynb)

Looking at historical answers and values for questions in Jeopardy, determine if there's any topic reuse that should
guide what an aspiring player should study.

# Disclaimer

Part of doing this work was working out how I can work with LLMs in a workflow, and
establishing what parts of the work they are good at doing, and what parts I would
be better at doing. Typically, the prompts involved specifying the type of graph
or visualisation I wanted and tweaking the colours, presentation for me. It was faster
than memorising all of matplotlib and seaborn documentation. The LLMs used were

1. ChatGPT-4o
2. Deepseek
3. Jetbrains AI (forwards to ChatGPT-4o)
4. Local LLMs running on 4090 (various models and quantisations)

The general finding I have made is that LLMs are great at some specific discrete tasks, and if
you construct your prompts correctly and specifically enough it is faster than
writing the code yourself. There are definitely cases where repeated reprompting and
editing was likely slower than simply reading the documentation and doing it myself. Finding
the boundary of when to take one approach vs the other was the intent of using them.

As with the rapid progression and evolution of these models, that boundary point
is constantly shifting. The learnings I made about what the models could do at
the time of writing could be invalidated with the next release of a model. Still,
there are limits based upon the training data available. Constructing prompts to specify
exactly what versions of different libraries are in use yields better results, and can
avoid situations where the code generated relies on deprecated function.

