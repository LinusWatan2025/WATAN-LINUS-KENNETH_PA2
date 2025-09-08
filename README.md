## OVERVIEW

This repository contains the solutions for **PA1 of the Advanced Computer Programming and Algorithms (ECE2112)** course. The project introduces fundamental Python concepts such as **Numpy operations, normalization, matrix manipulation, and logical indexing**. Each problem strengthens understanding of data preprocessing and array-based problem solving, which are essential for engineering and data science applications.

---

## PROBLEM 1: Normalization

**What it is:**

A program that generates a random 5×5 ndarray, normalizes it using mean and standard deviation, and saves the result in a file named **`X_normalized.npy`**.

**Why it's useful:**

Normalization is a key preprocessing step in data analytics and machine learning. It ensures that features are on the same scale, improving the stability and accuracy of models. This exercise demonstrates how to center data and scale it efficiently using NumPy functions.

**How to get started:**

```python
import numpy as np

#create a random 5x5 ndarray
x = np.random.rand(5, 5)

#using syntaxex to compute for mean and standard deviation
m = x.mean()
s = x.std()

#normalize x
Z = (x - m) / s

#save the normalized array
np.save("x_normalized.npy", Z)

print("Original Array (x):\n", x)
print("\nNormalized Array (Z):\n", Z)
```

**Output:**

<img width="575" height="284" alt="image" src="https://github.com/user-attachments/assets/b480cb36-3467-4528-bf1f-9f36923ec880" />


---

## PROBLEM 2: Divisible by 3

**What it is:**

A program that creates a 10×10 ndarray containing the squares of the first 100 positive integers, then extracts all elements divisible by 3 and saves them in a file named **`div_by_3.npy`**.

**Why it's useful:**

This problem demonstrates the use of array creation, mathematical transformations, and boolean indexing in NumPy. Identifying elements based on divisibility helps build intuition for filtering data, a common task in analytics and algorithm design.

**How to get started:**

```python
import numpy as np

#create an array with the first 100 positive integers
n = np.arange(1, 101)

#squaring the elements
s = n ** 2

#reshape into a 10x10 ndarray 
a = s.reshape(10, 10)

#selecting elements divisible by 3. using modulo operator, we check if each element leaves remainder 0 when divided by 3.
d = a[a % 3 == 0]

#save the result
np.save("div_by_3.npy", d)

print("Array with squares of the first 100 positive integers:\n", a)
print("\nDivisible by 3:\n", d)
```

**Output:**

<img width="656" height="347" alt="image" src="https://github.com/user-attachments/assets/5980f75c-2aaf-48a9-9dc8-6e570cc4483f" />

