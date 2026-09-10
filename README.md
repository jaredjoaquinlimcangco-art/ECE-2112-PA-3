# ECE-2112-PA-3
######  
Limcangco, Jared Joaquin M. || 2ECE-B

This repository contains everything included within our third programming assignment for our ECE2112 (Advanced Computer Programming and Algorithms) course. Below, there are three given problems related to Module 3, NumPy, where everything is going to be discussed. Let us get started.

#### 
####   
####   

First, `import pandas as npy` was added at the start in order to use its functions throughout the whole process.

### Problem A: Reproducible Normalization Problem

#### The Process:
For solving this problem, the following functions were used,
- `np.random.seed(2112)` = Sets random seed to 2112 for random values each time.
- `X = np.random.randint(10, 101, size=(5, 5)) ` = Creates a 5x5 array that generates random values from 10 - 100.
- `X_mean = X.mean()` = Calculates mean of all values in X.
- `X_std = X.std()` = Calculates population standard deviation of all values in X.
- `X_normalized = (X - X_mean) / X_std` = Normalizes each value using mean and std.

Using these functions, they were put together to form a program that normalizes any array with any given values.
```python
np.random.seed(2112)                          
X = np.random.randint(10, 101, size=(5, 5))         
X
X_mean = X.mean()                        
X_std = X.std()                    
X_normalized = (X - X_mean) / X_std         
X_normalized
print('X:')                                         
print(X)
print('X_normalized:')                              
print(X_normalized)
print('Mean of X_normalized:')                  
print(X_normalized.mean())
print('Standard deviation of X_normalized:')       
print(X_normalized.std())
np.save('X_normalized.npy', X_normalized)
```
(X_normalized.npy can be viewed through the repository home page.)

### Problem B: Cubes Divisible By 4 Problem

#### The Process:
For solving this problem, the following functions were used,
- `C = np.arange(1, 101) ** 3` = Creates first 100 values and cubes.
- `C = C.reshape(10, 10)` = Reshapes cubed values into 10x10 array.
- `div_by_4 = C[C % 4 == 0]` = Selects values divisible by 4.

These functions were then used to create a program that examines given values from an array and identifies which of them are divisible by 4.
```python
C = np.arange(1, 101) ** 3
C = C.reshape(10, 10) 
C
div_by_4 = C[C % 4 == 0]         
div_by_4
print('Shape of C:')                    
print(C.shape)
print('div_by_4:')
print(div_by_4)
print('Number of selected elements:')    
print(div_by_4.size)
np.save('div_by_4.npy', div_by_4)
```
(div_by_4.npy can be viewed through the repository home page.)

### Problem C: Above-Mean Squares Problem

#### The Process:
For solving this problem, the following functions were used,
- `S = np.arange(1, 37)**2` = Creates first 36 values and squares.
- `S = S.reshape(6, 6)` = Reshapes squared values into 6x6 array.
- `S_mean = S.mean()` = Calculates mean of all values.
- `above_mean = S[S > S_mean]` = Selects values that are greater than the mean.

With the use of these functions, a program was created for the sole purpose of choosing values that are greater than the mean in an array.
```python
S = np.arange(1, 37)**2  
S = S.reshape(6, 6)      
S
S_mean = S.mean()       
S_mean
above_mean = S[S > S_mean]    
above_mean
print('S:')                                     
print(S)
print('S_mean:')                              
print(S_mean)
print('above_mean:')                          
print(above_mean)
print('Number of selected elements:')         
print(above_mean.size)
np.save('above_mean.npy', above_mean)
```
(above_mean.npy can be viewed through the repository home page.)

### Thank you for reading this repository.
