# HW 2 - Housing data analisys

## ECGR 5105 - Summer 2024

#### Joshua Ayers

#### SID: 801083470

#### Professor: Vinit Katariya

#### Github: https://github.com/Jayers0/HW2_ECGR5105

## Problem 1

## A)

The following code is an implementation of the required functions for logistic regresion
The sigmoid opperatot is used as the gradient mediating funtion to avoid exploding and diminishing gradients
The mathmatical formula is shown in the formula below: 

$$
\sigma(z) = \frac{1}{1+e^{-z}}

$$


The next formula is the log cost function and is an expantion of the log cost function. 

$$
J(\theta) = \frac{1}{m}\sum^{m}_{i=1}Err(h_{\theta}(x^{(i)}),y^{i})

$$


Note that the $y^{(i)} \neq y^i $ but rather denotes the item of the dataset by the indicies $i:i\in S : S \text{ is a dataset} \land m =\text{the cardonality of S}$. 
$$
$$
The $Err(h(\theta),y)$ function shown above is the logarithmic nonlinear function that represents the Euclidian cost function ($h(\theta)$).
It is equal to the following mathmatical expression:

$$

Err(h_\theta(x),y) = (1-y)\log(1-h_{\theta}(x))-y\log(h_\theta(x))$$
For the purposes of this assignment I will use the sigmoid opperator($\sigma$) as the cost function($h(x)$) both becuase it was the example used in class and because it has no distrabution bias.

The next formula is the gradient decent algorithum. This function is a composite of the partial dirivative of the log cost funtion in all dimentions ($\text{gradient denoted as }\nabla$) in respect to the independednt variable. As shown below where F is a hypothetical cost funtion

$$
a_{n+1}=a_{n}-\gamma_{n}\nabla F(a_{n})

$$

Finally the logicstic regresion combines the all of the logistics cost function the sigmoid and the gradient decent and the gradient decent algorithum.

After testing at learning rates 0.01, 0.05, 0.1 for 1000 epochs. None of the models converged.

### Q1-A: Identify the best parameters for your linear regression model, based on the above input variables. 
The best parameters IE those with the strongest positive or negative corolation too the data is the number of stories and the furnishing status however for part 1A the relavant data will be "stories".

## B)

Using the same gradient decent algorithum defined in part 1a i loaded the specalized features
Implemnt the normalizatiom

## Problem 2

Using the same gradient decent algorithum I used the normalized and standardized the inputs
Implemnt the normalization and standardization function.

$$
N(X)=\frac{X_i-\left \lceil{x}\right \rceil }{\left \lceil{x}\right \rceil - \lfloor{X}\rfloor}

$$

$$
standardize = S(X)=\frac{X_i-average(x)}{std(X)}

$$

## A

I took the data from part 1a and passed it through the standardize function. This function didnt converge however on a purely 

## B


## problem 3

Emplement of the regularized gradient decenct algorithum.

$$
J(\theta) = \frac{1}{2m} \left[ \sum_{i=1}^{m} (h_\theta(x^{(i)}) - y^{(i)})^2 + \lambda \sum_{j=1}^{n} \theta_j^2 \right]

$$

$$
\theta_j := \theta_j - \alpha \left( \frac{1}{m} \sum_{i=1}^{m} (h_\theta(x^{(i)}) - y^{(i)}) x_j^{(i)} + \frac{\lambda}{m} \theta_j \right)

$$

### A)

The standardization is data is betterin terms of its performance as you can see both have lower loss. thouhg there seems to be overfitting ocuring as the training loss is lower than validation loss

### B)

As with before the standardization outperforms the normalization having lower training and validation loss however both for 3a and 3b both seem to have issues with overfitting
