# Machine Learning Specialization. Washington University

- I was curiouos about TuriCreate and Graphlab, so i thought maybe this courses could help to check it out in action and also reinforcing knowledge. Let's give it a try.


![alt](pics/intro.png)
https://www.coursera.org/specializations/machine-learning

![alt](pics/overview.png)

- 1st course: General approach.

![alt](pics/course1.png)

- 2nd course: Regression


-----------------------
-----------------------

# **Personal notes:**



# Graphlab

- It seems to work like pandas but storing info in hard drive instead of memory, also it has its own ml algorithms and displaying tools.


![alt](pics/graphlab.png " ")
![alt](pics/graphlab2.png " ")


# ML course metrics

**Classification accuracy** => fraction of items correctly classified.

- To recommender systems we don't need what an user doesn't like.
- Maybe it is better to focus on how quickly can we discover the relatively few liked items (imbalanced class problem)

**Recall** => how many of the items I really like were actually recommended to me. It measures how much the recommender system covers what I really like.

**Precision** => from all the recommended items available, what fraction I really like. It measures how much I am going to waste my time on products I don't like.

- You can maximize recall just recommending everything, then recall tends to 1, but then precision tends to 0.

- Ideal perfect recommender: All the products I like and only the products I like. Everything I don't like was never shown to me => Precision=Recall=1 (obviously not possible)

![alt](pics/auc1.png)
Another: When you know specifically the number of items you have to recoomend, then use it at k==items you have.


# Classification error and accuracy (my way)

- error = (# of mistakes) / (total #) = 1 - accuracy ; error € [0,1], the lowest the better.


- accuracy = (# of correct) / (total #) ; accuracy €[0,1]. The hightest the better.

What's good accuracy?

For binary classification in a balance dataset half the time it predicts right by default => accuracy = 0.5, so do it better.

- For k classess accuracy = 1/k by default.

Then, is 90% accuracy good? It depends. If 90% of sent emails are spam, just saying all mails are spam you get 90% of accuracy.

- Check out:

    - Is there class imbalance?
    - How does it compare to a simple, baseline approach?
    - What accuracy range do I need? What is good enough?

False positives, false negatives, and confusion matrices.

------------------------

![alt](pics/classification_matrix.png)

![alt](pics/classification_example.png)

![alt](pics/classification_example2.png)

--------------

**- Precision** = positive predictive value = TP / (TP+FP)

    - Fraction of relevant instances among retrieved instances.

**- Recall** = sensitivity = TP/ (TP + FN)

    - Fraction of the total amount of relevant instances that were actually retrieved.

Example:

A ML algorithm identifies 8 dogs in a picture where there are 12 dogs and some cats. Of the identified dogs, 5 are really dogs (TP), and there are 3 cats identified as dogs (FP)

Precision = 5/8 
From all dogs identified, just 5 were actually dogs

Recall= 5/12
From all the dogs, just 5 were identified

![alt](./pics/precission_recall.png " ")
*Internet picture.*

In the picture we see: 
- 1 TP
- 2 FP
- 7 TN
- 0 FN


**- Classification accuracy**.

Accuracy = nº of correct predictions / total of predictions = (TP+FN)/ total of samples

If 98% of samples are type A, our model can easily get 98% of training accuracy, so it's important to have a well balanced system if we'll trust this metric

**- Confusion matrix**.

        n=165       Predicted NO    Predicted YES

        Actual NO       50              10

        Actual YES      5               100

- TP    :   Predicted YES and actual output was YES.
- TN    :   Predicted   NO and the actual output was NO.
- FP    :   Predicted   YES   and the actual output was NO (the prediction is false).
- FN    :  Predicted NO  and the actual output was  YES.

**- AUC**:

Axis Y: TP rate
Axis X: FP rate

TP rate =   sensitivity =   TP / (FN+TP)
FP rate =   specificity =   FP / (FP+TN)

**- F1 score**:

F1  =   2   /   (1/precision + 1/recall)

It tries to find a balance between both metrics

**- MSE**:

Is the average of the square difference between the Original Values and the Predicted Values. Due to the ², higher errors are highlighted and we can work them out.

**- When using each metric**:

https://medium.com/usf-msds/choosing-the-right-metric-for-machine-learning-models-part-1-a99d7d7414e4


# Bias

![alt](pics/bias.png)
- Models with less bias tend to need more data to perform well, but do better with sufficient data.


# NN basics

- NN basic
![alt](pics/nn_basics1.png)

**Layers:**

![alt](pics/nn1.png)
![alt](pics/nn2.png)
![alt](pics/nn3.png)
![alt](pics/nn4.png)
![alt](pics/nn5.png)