# PA2 - Numerical Python
###### This repository contains Python scripts that address programming problems titled 'Normalization' and 'Divisible by 3.' 

###### A preview of the code is provided below, and a Jupyter notebook is also available in the files section.

## 1. Normalization Problem
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

## 2. Divisible by 3 Problem 
``` python
import numpy as np

# Create an array with the first 100 positive integers and square each element to create 10x10 array
integers = np.arange(1,101)**2

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




