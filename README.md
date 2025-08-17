Machine Learning Lab 01: Iris Classification with K-Nearest Neighbors (KNN)

Objective
This lab's primary goal was to introduce fundamental concepts in machine learning by using the classic Iris dataset. The key tasks included:
* Loading and exploring a dataset using Python libraries like Pandas and Scikit-learn.
* Visualizing data relationships to gain insights into feature and class distributions.
* Building and evaluating a basic machine learning classifier, specifically the K-Nearest Neighbors (KNN) algorithm.
* Understanding how a model's performance can be affected by key hyperparameters, such as the value of 'k'.

Steps and Key Activities
Environment Setup: We started by importing essential libraries including pandas for data manipulation, seaborn and matplotlib for visualization, and various modules from scikit-learn for machine learning tasks.
Data Exploration: The Iris dataset was loaded and converted into a Pandas DataFrame. We then used seaborn.pairplot to visualize the relationships between the four features (sepal length, sepal width, petal length, petal width) and observe how the three Iris species (setosa, versicolor, virginica) are distributed.

Model Building:
The dataset was split into a training set (80%) and a test set (20%) to ensure we could evaluate the model's performance on unseen data.
A K-Nearest Neighbors classifier was trained using four different values for k (1, 3, 5, and 7).
The model's accuracy was calculated for each value of k to see how it affected performance.

Results and Observations
The model's performance was excellent, achieving perfect accuracy for k=1, k=3, and k=5. For k=7, the accuracy was still very high at 0.97.

Model Performance: The high accuracy across the board confirms that the Iris dataset is a well-suited problem for a simple, distance-based algorithm like KNN. The perfect scores for smaller k values indicate that the data is very clean and the species are well-separated.

Effect of k: The slight drop in accuracy at k=7 is an interesting and important observation. While a larger k can help smooth out noise, in this specific case, it may have caused the model to consider a 'neighbor' from a different species that was located on the edge of its cluster, leading to a single incorrect prediction. This demonstrates the trade-off in choosing k: a value that is too large can sometimes over-generalize and pull in less-relevant data points.

Data Characteristics: The pairplot visualization clearly showed distinct clusters for each species, which explains why the KNN classifier performed so well. The clean separation between the groups made it straightforward for the model to correctly classify most of the test data points.
