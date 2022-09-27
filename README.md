# Introduction-to-Data-Science-with-Python
This article guides you through the fundamentals of data science

**Audience:** This article is intended for those who are familiar with the fundamentals of Python.

We live in an information-rich world. Because of the strong desire to exploit data, data science positions are always in demand making employment opportunities in the field quite accessible. In this article, I'll walk you through the fundamentals of data science.

## What exactly is data science?

![463627_1_En_BookFrontmatter_Fig1_HTML-removebg-preview](https://user-images.githubusercontent.com/87413874/192567113-2375b876-52e7-40cd-b1bc-5e0ce96db642.png)

Data science is a *field of study that includes modern tools and methods for extracting, processing, and analyzing data*. These tools may only be provided by libraries used in programming languages such as **Python**, **JavaScript**, and **R programming**. However, Python will be the focus of this article.

## What is a module?
A module is a library that groups together similar tools. Numpy, Pandas, Matplotlib, Seaborn, and other modules fall into this category. Learn more about modules [here](https://www.programiz.com/python-programming/modules#:~:text=What%20are%20modules%20in%20Python,small%20manageable%20and%20organized%20files.).

## What is pandas?
The Pandas module allows you to work with tabular data. Data in a tabular format is divided into rows and columns. Pandas is a popular library because it performs a wide range of data science functions. Learn how to set up Pandas [here](https://www.pythoncentral.io/how-to-install-pandas-in-python/#:~:text=Enter%20the%20command%20%E2%80%9Cpip%20install,Pandas%20in%20your%20Python%20programs.).

### Uses of pandas
Pandas engage in the following activities:
- Load tabular data from different sources.
- Look for a particular column or row.
- Compute total statistics.
- Combines data from various sources

## DataFrames
### Definition:
A dataframe is a variable that has tabular data. A dataframe can be filled with data by using comma-separated values (csv) file.

### How to load a csv file into a dataframe
1. Import pandas
```
import pandas as pd
```
2. Read and save the file into a dataframe using the read_csv() function as shown below.
```
name_of_dataframe = pd.read_csv("name.csv")
```
Where name refers to any name given to the csv file.

### Inspecting a dataframe
A dataframe can be examined in a number of ways.

**- Using the head method.head()** 
returns the first few rows of the dataframe.   
```
Syntax: name_of_dataframe.head( )
```
look at the dataframe below, for employee_info.

![Screenshot (25)](https://user-images.githubusercontent.com/87413874/192569598-43c33f8f-8de0-4106-9b3e-dc09b2d946c8.png)

Printing the dataframe's head results in 

![Screenshot (27)](https://user-images.githubusercontent.com/87413874/192571260-6f5ee89f-06d9-43bd-ba3e-024257505b86.png)


**- Using the info method .info()**
```
syntax: name_of_dataframe.info()
```
It returns information about the dataframe, including the number of rows and columns, and the data type of each value.

**- Using the describe method.describe()**
```
syntax: name_of_dataframe.describe()
```
It shows the description of a dataframe.

**- Using the shape attribute .shape**

```
syntax: name_of_dataframe.shape
```
Parentheses are not used because, shape is an attribute. It returns the total number of columns and rows in a dataframe.

For example, the employee_info dataframe has 9 rows and 4 columns.

### Selecting columns in a dataframe
**Why do we select columns?**
- In order to compute
- For data visualization

There are several ways to select columns in a dataframe, but we'll look at two for now

**- Using square brackets([ ])**

we select a column as follows
```
name_of_dataframe[‘name of column’]
```
for example employee_info['names'] 

![image](https://user-images.githubusercontent.com/87413874/192572874-14aff834-e310-4461-9dcf-13e95aa41cb2.png)

This method is used when the column name contains letters or special characters such as -,? etc.

**- Selecting with a dot (.)**

 We use this technique when the column name contains only letters, strings, or underscores. It can be used in the following ways.
```
syntax: name_of_dataframe. column name
```

**- Selecting multiple columns**
```
Syntax: name_of_dataframe[[‘name of column1’ , ’ name of column2’]]
```
**Example:** 
Employee_info[ [‘names’,’ city ’] ]

![image](https://user-images.githubusercontent.com/87413874/192573484-f53a20eb-aa5e-46c5-9740-97d7f007b01c.png)

**- Selecting rows in a dataframe**
To select rows from a dataframe, logic statements such as **==,>**, and so on are used.
```
Syntax: name_of_dataframe[name_of_dataframe[‘column name’] logical statement value]
```
Consider the employee information dataframe from earlier. Let's select the rows from the employee_info table where the age is 20. 

employee info [employee info['age']==20]

**Output**

![image](https://user-images.githubusercontent.com/87413874/192573941-5b119936-9dca-46bc-b57f-1dc30ee9e1d2.png)

## Creating plots
### - Creating line plots

![image](https://user-images.githubusercontent.com/87413874/192574172-dcc858e0-6dc2-4460-8229-d3f0b2072333.png)

To create a line plot, we must do the following.
1. From matplotlib import pyplot
```
import matplotlib.pyplot as plt
```
2. Use the plot() function to plot x and y values on your graph

```
plt.plot (x-values, y-values)

Where x-values and y-values are the column names containing the values.
```
3. Use the show() function to see how the plot looks.

```
plt.show()
```



### - Creating scatter plots

![image](https://user-images.githubusercontent.com/87413874/192574442-60ac25db-c7db-4f1d-8a48-8ce377895608.png)

A scatter plot illustrates how each data point appears on a graph.
A scattered plot is an excellent way to view unordered plots.

Creating a scattered plot is like creating a line plot. The only difference is that we use the scatter() function instead of the plot() function, as shown below.

```
plt.scatter (x-values, y-values)
```

## Adding texts to plots

### Adding x -axis label

To add an x-axis label, we use the.xlabel() method.

```
plt.xlabel("x label name")
```

### Adding y-axis labels

We use the.ylabel() method for this.

```
plt.ylabel("y label name")
```

### Adding titles

We use the.title() method to add titles.

```
plt.title("plot title name")
```



## Conclusion
 Part two of this article will be posted in a few days. I hope this article has been useful in launching your data science career. Please react, comment, and follow for more information. Corrections are always welcome.
