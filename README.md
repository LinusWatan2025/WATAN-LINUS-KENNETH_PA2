## OVERVIEW

This repository contains the solutions for **PA2 of the Advanced Computer Programming and Algorithms (ECE2112)** course. The project introduces fundamental Python concepts such as **Numpy operations, normalization, matrix manipulation, and logical indexing**. Each problem strengthens understanding of data preprocessing and array-based problem solving, which are essential for engineering and data science applications.

---

## PROBLEM 1: Normalization

**What it is:**

A program that generates a random 5×5 ndarray, normalizes it using mean and standard deviation, and saves the result in a file named **`x_normalized.npy`**.

**Why it's useful:**

Normalization is a key preprocessing step in data analytics and machine learning. It ensures that features are on the same scale, improving the stability and accuracy of models.

**How to get started:**

First, import Numpy and create a random 5×5 ndarray. Using `np.random.rand()` is a quick way to generate numbers between 0 and 1, which simulates raw data.

```python
import numpy as np

#create a random 5x5 ndarray
x = np.random.rand(5, 5)
```

Next, calculate the **mean** and **standard deviation**. These are used to center the data (subtracting the mean) and scale it (dividing by the standard deviation).

```python
#compute for mean and standard deviation
m = x.mean()
s = x.std()
```

Normalize the array using the formula ( Z = \frac{x - m}{s} ). This ensures all values are expressed in terms of how far they are from the mean in standard deviation units.

```python
#normalize x
Z = (x - m) / s
```

Finally, save the normalized array to a `.npy` file for later use and print both arrays for comparison. The `.npy` format is efficient for storing and reloading Numpy arrays.

```python
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

This problem shows how to apply **mathematical operations and boolean indexing** in Numpy. Filtering based on divisibility is a common technique for data selection and preprocessing.

**How to get started:**

First, generate an array of integers from 1 to 100 using `np.arange()`. Then square them to simulate a transformed dataset. Reshape the results into a 10×10 matrix for easier visualization.

```python
#create an array with the first 100 positive integers
n = np.arange(1, 101)

#square the elements
s = n ** 2

#reshape into a 10x10 ndarray
a = s.reshape(10, 10)
```

Next, apply **boolean indexing** to extract elements divisible by 3. The condition `a % 3 == 0` checks each element and returns only those satisfying the rule.

```python
#select elements divisible by 3
d = a[a % 3 == 0]
```

Finally, save the filtered array into a `.npy` file and print both the full matrix and the divisible-by-3 elements. This step demonstrates how to preserve processed data for reuse.

```python
#save the result
np.save("div_by_3.npy", d)

print("Array with squares of the first 100 positive integers:\n", a)
print("\nDivisible by 3:\n", d)
```

**Output:**

<img width="656" height="347" alt="image" src="https://github.com/user-attachments/assets/5980f75c-2aaf-48a9-9dc8-6e570cc4483f" />  

