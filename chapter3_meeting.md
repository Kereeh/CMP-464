Cross Validation 
k = 3
S1 | S2 | S3

Model 1: train on S1 + S2 and test on S3
Model 2: train S2 + S3 and test on S1
Model 3: train S1 + S3 and test on S2

1. You have more test cases
2. More Training Data

SGDClassifier with hinge loss function
-> linear support vector machine model
-> wants the distance of a data point from the linear line to be as far as possible

