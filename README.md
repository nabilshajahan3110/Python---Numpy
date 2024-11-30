
# ASSIGNMENT 7 - NUMPY
Python exercise covering Numpy &amp; Pandas basics


import numpy as np

# Exercise 1: (Score : 1)
# Create a numpy array containing the numbers from 1 to 10, and then reshape it to a 2x5 matrix.

a1 = np.arange (1,11).reshape(2,5)
print(a1)
print(a1.shape)
print(a1.ndim)

![np1](https://github.com/user-attachments/assets/af254315-f201-44b9-83bd-71f4a1f9953a)


# Exercise 2: (Score : 1)
# Create a numpy array containing the numbers from 1 to 20, and then extract the elements between the 5th and 15th index.

a2 = np.arange (1,21)
print(a2)
print(a2[5:15])

![np2](https://github.com/user-attachments/assets/32224198-09b4-4776-b818-27ec5aa1b0fd)


# Exercise 3: (Score : 2)
# Create a Pandas series with the following data: {'apples': 3, 'bananas': 2, 'oranges': 1}. 
# Then, add a new item to the series with the key 'pears' and the value 4.

import pandas as pd
fruit = pd.Series ({'apples': 3, 'bananas': 2, 'oranges': 1})
print(fruit)
fruit["pears"] = 4
print(fruit)

![np3](https://github.com/user-attachments/assets/792a3ddb-5c19-4ac1-afd6-daeb4850e4ab)


# Exercise 4: (Score : 2)
# Create a dataframe with the following columns: name, age, and gender. The dataframe should have 10 rows of data.

df = pd.DataFrame({
    'name': ['Alice', 'Bob', 'Charlie', 'David', 'Eve', 
             'Frank', 'Grace', 'Hannah', 'Ian', 'Jane'],
    'age': [25, 30, 22, 35, 28, 40, 33, 27, 29, 31],
    'gender': ['Female', 'Male', 'Male', 'Male', 'Female', 
               'Male', 'Female', 'Female', 'Male', 'Female']
})
df

![np4](https://github.com/user-attachments/assets/3e7c821e-9b60-4247-83b7-9a766a631943)


# Exercise 5: (Score : 1)
# Add a new column to the data frame created in question 1, called occupation. 
# The values for this column should be Programmer, Manager, and Analyst, corresponding to the rows in the dataframe.

df['occupation'] = ['Programmer', 'Manager', 'Analyst', 'Manager', 'Programmer', 'Analyst', 'Manager', 'Analyst', 'Programmer', 'Analyst']
df

![np5](https://github.com/user-attachments/assets/76c81128-a882-4985-8f91-aff30b3b9686)


# Exercise 6: (Score : 1)
# Select the rows of the dataframe where the age is greater than or equal to 30.

age_condition = df[df['age'] >= 30]
print(age_condition)

![np6](https://github.com/user-attachments/assets/047a79b7-328c-4718-b16f-fe6920416fe4)


# Exercise 7: (Score : 2)
# Convert this dataframe to a csv file and read that csv file, finally display the contents.

df.to_csv('Employee.csv', index = False)
print("df saved as 'Employee.csv'.")
df_csv_read = pd.read_csv('Employee.csv')
print(df_csv_read)


![nplast](https://github.com/user-attachments/assets/8db1b3b7-2272-45aa-8084-30fbd35ead6c)















