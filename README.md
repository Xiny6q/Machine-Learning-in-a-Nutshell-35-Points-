Download link :https://programming.engineering/product/machine-learning-in-a-nutshell-35-point

# Machine-Learning-in-a-Nutshell-35-Points-
Machine Learning in a Nutshell [35 Points]
Name, Surname, ID Number

Problem 3.1 Machine Learning in a Nutshell [35 Points]

For this exercise you will use a dataset, divided into training set and validation set (download them in Moodle). The first row is the vector x and the second row the vector y.

Based on this data, we want to learn a function mapping from x values to y values, of the form y = T (x ).

Please upload the code you developed in the corresponding section in Moodle.

Supervised vs Unsupervised Learning [2 Points]

Briefly explain the diﬀerences between supervised and unsupervised learning. Is the above a supervised or unsupervised learning problem? Why?

Regression vs Classification [2 Points]

Supervised learning is typically divided into regression and classification tasks. Briefly explain what are the diﬀerences between regression and classification.

Name, Surname, ID Number

Linear Least Squares [4 Points]

Consider the training set above to calculate features (x) of the form [sin 2i x ]i=0…n 1. Compute the feature values when n is 2, 3 and 9 (i.e., when using 2, 3 and 9 features). Use the linear least squares (LLS) method to predict output values y for input values x 2 f0, 0.01, 0.02, . . . , 6g using the diﬀerent numbers of features. Attach a single plot showing the three resulting predictions when using 2, 3 and 9 features (i.e., having x and y as axes).

d) Training a Model [2 Points]

1

N

yitrue

predicted

2

The root mean square error (RMSE) is defined as RMSE =

i=1

yi

, where N is the

N

¨

P

number of data points. Using the LLS algorithm implemented in the previous exercise, train a diﬀerent model for each of the number of features between 1 and 9, i.e., [1,2,3…,9]. For each of these models compute the corresponding RMSE for the training set. Attach a plot where the x-axis represents the number of features and the y-axis represents the RMSE.

Name, Surname, ID Number

Model Selection [4 Points]

Using the models trained in the previous exercise, compute the RMSE of each of these models for the validation set.

Compare in one plot the RMSE on the training set and on the validation set. How do they diﬀer? Can you explain what is the reason for these diﬀerences? (Hint: remember the plot from Exercise c) ) What is the number of features that you should use to achieve a proper modeling?

Name, Surname, ID Number

Cross Validation [8 Points]

K-fold cross validation is a common approach to estimate the test error when the dataset is small. The idea is to randomly divide the training set into K diﬀerent datasets. Each of these datasets is then used as validation set for the model trained from the remaining K 1 datasets. The resulting vector of errors E = [e1…eK ] can now be used to compute a distribution (typically by fitting a Gaussian distribution). When K is equal to the number of data points, K-fold cross validation takes the name of leave-one-out cross validation (LOO).

Apply LOO using only the training set and compute the mean/variance of the RMSE for the learned models. Repeat for the models with the number of features between 1 and 9, i.e., [1,2,3…,9]

Attach a plot showing the mean/variance (as a distribution) of the RMSE computed using LOO and having on the x-axis the number of features and on the y-axis the RMSE. Which is the optimal number of features now? Discuss the results obtained and compare against model selection using train/validation set.

g) Kernel Functions [2 Points]

A kernel function k xi , xj is given by the inner product of two feature vectors. Write out the kernel function for the previous set of features where n = 3.

Name, Surname, ID Number

Kernel Regression [6 Points]

The kernel function in the previous question required explicit definition of the type and number of features,

which is often diﬃcult in practice. Instead, we can use a kernel that defines an inner product in a (possibly infinite dimensional) feature space.

Using the training set and an exponential squared kernel k x i , x j

= exp

1

kx i x j k2 with = 0.15,

2

predict output values y for input values x

2 f

0,0.01,…,6

g

. Attach a plot of your results.

T

K

1

(Hint: use standard kernel regression: f (x ) = k

y with K i j = k

x i , x j

and ki = k (x , x i )).

Compute the RMSE on the validation set for the kernel regression model. Compare it with the RMSE of the best LLS model you found.

Name, Surname, ID Number

Derivation [5 Points]

Explain the concept of ridge regression and why/when it is used. Derive its final equations presented during

the lecture.

(Hint: remind that for normal linear regression the cost function is J = 1 PN ( f (x i ) yi )2 )

2 i=1

(Hint 2: use matrix notation)

6
