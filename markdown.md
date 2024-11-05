# What is it?
Using repeated examinations of inputs and outputs to try and derive the underlying algorithm.
Chicken alalogy: ML tool repeatedly tries to make chicken, until it determines a good recipie. 

# The Framework

1. Data Collection
2. Data Modeling
   1. Problem Definition - Supervised/Unsupervised?
   2. Data - Structured? Unstructured?
   3. Evaluation - What Defines Success for us?
   4. Features - What do we already know about the data? "Body Weight" is a numerical features that can be used to predict Heart disease. The Goal of ML is to determine the patterns these features express. 
   5. Modeling - What machine modeling model should I use?
   6. Experiments (Back to 'Problem Definition') 
3. Deployment (Back to 'Data Collection')

# 1. Problem Definition: When Shouldn't I Use it?
1. Will a simple, hand-coded system work? Use the simpler thing. 

# What types of machine learning are there?
## Supervised
   1. Data
   2. Labels
   3. Use data to try and predict a label
   4. Repeat
   
### Classification - 
- Binary("Does this person have cancer?")
- Multiclass Classification ("What kind of Dog is this?")
### Regression - "How much will this house cost"?
- Has data, but no labels. The ML Algorithm finds the labels. (e.g, grouping customers)
- "Clustering"; putting similar groups of things together. 
### Transfer learning
- Uses infor from one ML algorithm to help another one.

### Reinforcement learning
- Think, a computer teaching itself to play chess by playing games over and over. 
- While cool, has fewer practical applications. 
  
Using the above, you can better figure out which model you should use. 

# 2. Data
Structured Data: CSV/DB/Etc The more data, the better. 
Streaming Data: Think News headlines, or other  live feeds for new data. 
For this, we could get the data, feed it to Jupyter, and use Pandas to analyze it. 

# 3. Evaluation - What defines success for us? ("97% accuracy!")
Depends on the type of problem being solved. Possible Evaluation Metrics: "Mean Absolute Error", "Precision at K", "Mean squared error". 

# 4. Features - "What do we already know about the data"?
Could be columns in structured data, i.e., "**Feature Variables"**. **Numerical Features**, **Derived Features (Custom Column)**, **Categorical features**. Creating new Features ("Who visited the doctor in the last year, based on the year of latest visit?") = "Feature Engineering"

In unstructured data, there are also features. An ML Algorithm trying to identify dogs might notice that there are usually 4 limbs, 2 eyes, a tail, etc. 

Generally, Features that appear in most sample items are the most useful. Insuring most items have the expected features is called **"Feature Coverage"**

# 5. Modeling Part 1 - 3 Sets, i.e., "Train, Validate, Test"
Based on our problem and data, which machine learning model should we use?
1. Choosing and Training a model
2. Tuning a Model
3. Model Comparison

# Generalization: The Most Important Concept in ML
If I repeatedly take practice exams until I understand the material, my success in my final exam is a result of how well I've generalized my knowledge from the other exams. 
If al the exams were identical, I wouldnt be learning anything: I'd just be memorizing the answers. This shoudl be avoided, mainly via the "3 Steps". Obviosly, the final "Testing" data split can't be exposed to the model while it is being trained or tuned. 

# Modeling
- Iterative, Start small, try simpler models before more complex ones.

# Tuning
- We've traid a little data, now lets use the "Validation Data" split to improve our results. 
- Many models have many "dials". Neural Networks let you tweak the number of "Layers"
- Hyperparameters? 

# Model Comparison
- "Final Exam"; evaluate Model against the unseen test data. 
- Determines how well the model is "generalized"
- Looking for "Goldilocks" zone; **Underfitted** data isnt precice enough, **Overfitted** data seems like it knows the pattern too well (perhaps it just memorized the data? Did your training data leak into the Final Data?)
- If a model is poorly fitted, you can use a more complex model, reduce the features, train longer, increase hyperparameters. You can also collect more data. Try a less advanced model. 
- Ensure your comparing apples to apples when comparing the performance of different models. Did they use the same training data? What is the time/energy cost for each to arrive at their decisions?
- Well fited Models are well Generalized
- Consider all parts of a models perfomance--speed, accuracy. Consider the bigger picture.

# 6. Experimentation 
- Try a different model?
- Vary the Inputs?

# Tools
What tools are we using?
- Anaconda (Hardware Store)
- matplotlib
- numpy
- pandas
- scikitlearn
- dmlc XGBoost
