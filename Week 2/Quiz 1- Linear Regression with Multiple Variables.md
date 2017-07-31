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

import numpy as np

x_2 = np.array([7921,5184,8836,4761])

x_2_avg = np.mean(x_2)

x_2_range = np.max(x_2) - np.min(x_2)

x_2_normalized = (x_2 - x_2_avg)/ x_2_range

print(round(x_2_normalized[3],2))

### Answer
* -0.47

---

