In this repo, you will get a Deep Neural Network model built using Tensorflow module.
BUSINESS CASE:
Given a data from an audiobook app. Logically it relates to the audio version of books only. Each customer in the database has made a purchase at least once. We have to create a machine learning algorithm based on our data that can predict if a customer will buy again from the audiobook company.

In the dataset available in the resources no column headers is included as we don't want any text in the data while training the model. Each row represents a person.
-> The first column is ID, we won't use it in our algorithm.
-> The second column is overall book length, sum of the length of all purchases
-> The third column is average book length, sum of the length of all purchases divided by the number of purchases
-> The fourth and fifth column are overall price paid and average price paid, similar to the book length (Price variable is almost always a good predictor
-> The sixth column is review, a boolean that shows if a customer shows engagement with the platform
-> The seventh column is review out of 10. For those who did not leave a review, we will calculate the average as the empty cell can be problematic. (pre processing trick)
   For our ML algorithm,
     review = 8.91; status quo
     review > 8.91; above average "feelings"
     review < 8.91; below average "feelings"
-> The eighth column is total minutes listened, a measure of engagement.
-> The ninth column is completion, the total minutes listened divided by the total length of books a person has purchased, assuming that a person has not re-listened a book
-> The tenth column is support requests, a numerical that shows the total number of support requests a person has opened.
-> The eleventh column is measuring the difference between the last time a person interacted with the platform and their purchase date, higher the value, the better

The data gathered represents two years of engagement and a six months of observation where if a customer converted the target will have a boolean 1 and 0 is s/he did not converted in that 6 months duration

THE BUSINESS CASE ACTION PLAN:
1) Pre process the data
   Balance the dataset
   Divide the dataset in training, validation, and test (prevent overfitting)
   Save the data in a tensor friendly format (save in .npz file format)
2) Create the machine learning algorithm


The dataset is from the Udemy Course: Complete Data Science Training: Mathematics, Statistics, Python, Advanced Statistics in Python, Machine Learning, Deep Learning by 365 Careers
