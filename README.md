# Machine Learning Specialization. Washington University

- I was curiouos about TuriCreate and Graphlab, so i thought maybe this courses could help to check it out in action and also reinforcing knowledge. Let's give it a try.


![alt](pics/intro.png)
https://www.coursera.org/specializations/machine-learning



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