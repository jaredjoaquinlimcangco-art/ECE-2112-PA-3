# ECE-2112-PA-3
######  
Limcangco, Jared Joaquin M. || 2ECE-B

This repository contains everything included within our third programming assignment for our ECE2112 (Advanced Computer Programming and Algorithms) course. Below, there are three given problems related to Module 3, Pandas, where everything is going to be discussed. Let us get started.

#### 
####   
####   

First, `import pandas as pd` was added at the start in order to use pandas' functions throughout the whole process.

Additionally, `'cars = pd.read_csv ('cars.csv')` was put afterwards in order to read the cars.csv file so it can be stored as a DataFrame.

### Problem A: Positional and Label-Based Slicing
After loading cars, complete the following operations. 

a. Display the shape and complete list of column names of cars. 

b. Using positional slicing, create cars 6 to 10 containing rows 6 through 10 of the dataset, where the first data row is row 1. 

c. From cars 6 to 10, display only the columns Model, mpg, cyl, hp, and gear, in that order. 

Requirement: The row selection in part (b) must use iloc; the column selection in part (c) must use column labels.

#### The Process:
For solving this problem, the following functions were used,

A - a:
- `print ('Shape of Cars:', cars.shape)` = Displays number rows and columns.
- `print ('Column names:', cars.columns.tolist())` = Displays list of column names.

A - b:
- `cars_6_to_10 = cars.iloc [5:10]` = Selects rows 6 to 10.

A - c:
- `cars_6_to_10 = cars_6_to_10 [['Model', 'mpg', 'cyl', 'hp', 'gear']] ` = Selects the labeled columns.

These functions were used individually for each part to fulfill the following operations for a, b, and c. Below is the compilation of the functions.
```python
print ('Shape of Cars:', cars.shape)
print ('Column names:', cars.columns.tolist())

cars_6_to_10 = cars.iloc [5:10]
cars_6_to_10

cars_6_to_10 = cars_6_to_10 [['Model', 'mpg', 'cyl', 'hp', 'gear']]
cars_6_to_10
```

### Problem B: Model Lookup
Use Boolean indexing on the Model column to answer both requests.

a. Display the complete row for Toyota Corolla.

b. For Pontiac Firebird, display only Model, mpg, hp, and wt.

Store the two results in toyota and pontiac, respectively. Do not use a hard-coded row number to locate either model.

#### The Process:

For solving this problem, the following functions were used,

B - a:
- `toyota_c = cars[cars['Model'] == 'Toyota Corolla']` = Finds the Toyota Corolla model and displays its complete row.

B - b:
- `pontiac_f = cars[cars['Model'] == 'Pontiac Firebird'] [['Model', 'mpg', 'hp', 'wt']]` = Finds the Pontiac Firebird model and selects its labeled columns.

These functions were used individually for each part to fulfill the following operations for both a and b. Below is the compilation of the functions.
```python
toyota_c = cars[cars['Model'] == 'Toyota Corolla']
toyota_c

pontiac_f = cars[cars['Model'] == 'Pontiac Firebird'] [['Model', 'mpg', 'hp', 'wt']]
pontiac_f
```

### Problem C: Multi-Model Subsetting
Create a DataFrame named selected cars containing only the records for three models: Datsun 710, Lotus Europa, and Ferrari Dino.

For these records, retain only Model, mpg, cyl, hp, and gear. Select the rows by their model values rather than by row numbers. 

Display selected cars and its shape.

Required check: The final DataFrame must contain exactly three rows and five columns.

#### The Process:

For solving this problem, the following functions were used,
- `carselected = cars.loc[(cars['Model'] == 'Datsun 710') |  
                         (cars['Model'] == 'Lotus Europa') |
                         (cars['Model'] == 'Ferrari Dino'),
                         ['Model', 'mpg', 'cyl', 'hp', 'gear']]`

  = Finds the models for Datsun 710, Lotus Europa, and Ferrari Dino before selecting their labeled columns.
  
- `print ('Shape of Selected Cars:', carselected.shape)`

  = Displays the size of rows and columns.

These functions were successfully used to make a DataFrame for the three cars, which included their models and other components, before finally being displayed of the size of their DataFrame.
```python
carselected = cars.loc[(cars['Model'] == 'Datsun 710') |         
                         (cars['Model'] == 'Lotus Europa') |
                         (cars['Model'] == 'Ferrari Dino'),
                         ['Model', 'mpg', 'cyl', 'hp', 'gear']]
carselected

print ('Shape of Selected Cars:', carselected.shape)
```

### Thank you for reading this repository.
