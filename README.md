# PA2 - Numerical Python
###### This repository contains Python scripts that address programming problems titled 'Normalization' and 'Divisible by 3.' 

###### A preview of the code is provided below, and a Jupyter notebook is also available in the files section.

## 1. Normalization Problem

## Introduction
##### Greetings! This code is about creating a random 5x5 array using NumPy, normalizing it, and saving the results. 

## Overview 
##### This project normalizes a randomly generated 5x5 array by centering the data (subtracting the mean) and scaling it (dividing by the standard deviation). The resulting normalized array is then saved as `X_normalized.npy`.

``` python
import numpy as np

# Create a randon 5x5 nd array
X = np.random.rand(5,5)

# Calculate the mean & standard deviation of the array
mean_X = X.mean()
std_X = X.std()

# Normalize the array using the formula: Z = (X - mean) / standard deviation 
X_normalized = (X - mean_X) / std_X

# Save the normalized array to a file
np.save('X_normalized.npy', X_normalized)

# Print the original and normalized arrays 
print("Original array:\n", X)
print("\nNormalized array:\n", X_normalized)
```

## Possible Input / Output
_**Input:**_
The code does not take user input; instead, it generates a random 5x5 NumPy array with values between 0 and 1.

_**Output:**_
Two arrays are printed to the console: the original random array and its normalized version. The normalized array is also saved to a file named X_normalized.npy.

## This is the output I obtained:
<img width="510" alt="Screenshot 2024-09-06 at 9 56 12 PM" src="https://github.com/user-attachments/assets/2cf4c805-ac54-413c-b99c-3d995267b77b">



## 2. Divisible by 3 Problem 
## Introduction: 
##### Greetings! This script creates and processes a 10x10 array based on the first 100 positive integers.

## Overview: 
##### The script begins by squaring each of these integers and reshaping the resulting values into a 10x10 array. It then identifies and extracts the elements within this array that are divisible by 3, saving these elements to a file named div_by_3.npy. Both the full 10x10 array and the elements divisible by 3 are printed to the console.

``` python
import numpy as np

# Create an array with the first 100 positive integers and square each element to create 10x10 array
integers = np.arange(1,101)

# Square each element to create 10x10 array
A = integers**2

# Reshape to 10x10 ndarray
A = A.reshape(10,10)

# Determine the elements divisible by 3
divisible_by_3 = A[A % 3 == 0]

# Save the result to a file
np.save('div_by_3.npy', divisible_by_3)

# Print the array and the elements divisible by 3
print("10x10 Array A:\n", A)
print("\nElements divisible by 3:\n", divisible_by_3)
```
## Possible Inputs / Outputs:
**Inputs:**
No external input is required; the script uses predefined values.

**Outputs:**
A 10x10 array of squared integers.
A file named `div_by_3.npy` contains elements from the array that are divisible by 3.
Console output displays the 10x10 array and the divisible elements by 3.

## This is the output I obtained:
<img width="566" alt="Screenshot 2024-09-06 at 10 01 35 PM" src="https://github.com/user-attachments/assets/7f9ba3fc-b5c2-458a-9a33-77825f777a0d">







