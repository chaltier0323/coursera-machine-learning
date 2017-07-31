## Question 1
Suppose m=4 students have taken some class, and the class had a midterm exam and a final exam. You have collected a dataset of their scores on the two exams, which is as follows:

| midterm exam | (midterm exam)^2 | final exam |
|--------------|------------------|------------|
| 89           | 7921             | 96         |
| 72           | 5184             | 74         |
| 94           | 8836             | 87         |
| 69           | 4761             | 78         |

You'd like to use polynomial regression to predict a student's final exam score from their midterm exam score. Concretely, suppose you want to fit a model of the form hθ(x)=θ0+θ1x1+θ2x2, where x1 is the midterm score and x_2 is (midterm score)^2. Further, you plan to use both feature scaling (dividing by the "max-min", or range, of a feature) and mean normalization.

What is the normalized feature x(4)2? (Hint: midterm = 69, final = 78 is training example 4.) Please round off your answer to two decimal places and enter in the text box below.

Python Code:
```
import numpy as np
x_2 = np.array([7921,5184,8836,4761])
x_2_avg = np.mean(x_2)
x_2_range = np.max(x_2) - np.min(x_2)
x_2_normalized = (x_2 - x_2_avg)/ x_2_range
print(round(x_2_normalized[3],2))
```
### Answer
* -0.47

---

## Question 2
You run gradient descent for 15 iterations

with α=0.3 and compute J(θ) after each iteration. You find that the value of J(θ) increases over time. Based on this, which of the following conclusions seems most plausible?
### Answer
* Rather than use the current value of α, it'd be more promising to try a smaller value of α (say α=0.1).

---

## Question 3
Suppose you have m=14 training examples with n=3 features (excluding the additional all-ones feature for the intercept term, which you should add). The normal equation is θ=(XTX)−1XTy. For the given values of m and n, what are the dimensions of θ, X, and y in this equation?
### Answer
* X is 14×4, y is 14×1, θ is 4×1

---

## Question 4
Suppose you have a dataset with m=50 examples and n=15 features for each example. You want to use multivariate linear regression to fit the parameters θ to our data. Should you prefer gradient descent or the normal equation?
### Answer
* The normal equation, since it provides an efficient way to directly find the solution.

---

## Question 5
Which of the following are reasons for using feature scaling?
### Answer
* It speeds up gradient descent by making it require fewer iterations to get to a good solution.

---

## Question 6
You run gradient descent for 15 iterations with α=0.3 and compute J(θ) after each iteration. You find that the value of J(θ) decreases quickly then levels off. Based on this, which of the following conclusions seems most plausible?
### Answer
α=0.3 is an effective choice of learning rate.

---

## Question 7
Suppose you have m=28 training examples with n=4 features (excluding the additional all-ones feature for the intercept term, which you should add). The normal equation is θ=(XTX)−1XTy. For the given values of m and n, what are the dimensions of θ, X, and y in this equation?
### Answer
X is 28×5, y is 28×1, θ is 5×1

---

## Question 8
Suppose m=4 students have taken some class, and the class had a midterm exam and a final exam. You have collected a dataset of their scores on the two exams, which is as follows:
| midterm exam | (midterm exam)^2 | final exam |
|--------------|------------------|------------|
| 89           | 7921             | 96         |
| 72           | 5184             | 74         |
| 94           | 8836             | 87         |
| 69           | 4761             | 78         |
You'd like to use polynomial regression to predict a student's final exam score from their midterm exam score. Concretely, suppose you want to fit a model of the form hθ(x)=θ0+θ1x1+θ2x2, where x1 is the midterm score and x2 is (midterm score)2. Further, you plan to use both feature scaling (dividing by the "max-min", or range, of a feature) and mean normalization.

What is the normalized feature x(2)2? (Hint: midterm = 72, final = 74 is training example 2.) Please round off your answer to two decimal places and enter in the text box below.

Python Code:
```
import numpy as np
x_2 = np.array([7921,5184,8836,4761])
x_2_avg = np.mean(x_2)
x_2_range = np.max(x_2) - np.min(x_2)
x_2_normalized = (x_2 - x_2_avg)/ x_2_range
print(round(x_2_normalized[1],2))
```
### Answer
* -0.37

---

## Question 9
You run gradient descent for 15 iterations with α=0.3 and compute J(θ) after each iteration. You find that the value of J(θ) decreases slowly and is still decreasing after 15 iterations. Based on this, which of the following conclusions seems most plausible?
### Answer
* Rather than use the current value of α, it'd be more promising to try a larger value of α (say α=1.0).

---

## Question 10
Suppose you have a dataset with m=50 examples and n=200000 features for each example. You want to use multivariate linear regression to fit the parameters θ to our data. Should you prefer gradient descent or the normal equation?
### Answer
* Gradient descent, since (XTX)−1 will be very slow to compute in the normal equation.
