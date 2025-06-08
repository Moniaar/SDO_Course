# Stanford Data Ocean (SDO) Course Notes

Welcome to my curated notes from the **Stanford Data Ocean Scholarship** course! This README organizes key concepts and tips learned throughout the program, with a focus on Python programming essentials.

> **Tip**: In Jupyter Notebook, press `H` in an empty cell to view a list of commands and shortcuts! 🚀

## 📝 General Notes: Python Essentials

### Key Concepts
1. **Floor Division (`//`)**: Returns only the integer part of a division (e.g., `7 // 2 = 3`).
2. **Division Always Returns a Float**: Even if the result is a whole number (e.g., `4 / 2 = 2.0`).
3. **Mixing Integers and Floats**: Operations between an integer and a float always yield a float.
4. **String Quotes**: Use double quotes (`"`) if a string contains an apostrophe (e.g., `"It's sunny"`).
5. **Variable Tracking**: Python updates variable values dynamically after reassignment.
6. **Case Sensitivity**: Python is case-sensitive (e.g., `Variable` ≠ `variable`).
7. **Multiple Variable Assignment (Unpacking)**: Assign multiple variables in one line (e.g., `x, y = 1, 2`), provided the number of values matches the variables.
8. **Constants**: Use uppercase names for constants (e.g., `MAX_SIZE = 100`).
9. **Type Casting**: Convert values to integers using `int()` (e.g., `int("5") = 5`).
10. **String Comparison**: Useful for tasks like password verification (e.g., `input_text == saved_password`).
11. **Nested Lists**: Lists can contain other lists (e.g., `[[1, 2], [3, 4]]`).
12. **Negative Indexing**: Use `-1` to access the last item in a list (e.g., `my_list[-1]`).
13. **Adding Elements**: Append items to a list using `.append()` (e.g., `my_list.append(5)`).
14. **Removing Elements**: Delete items using `del` with the index (e.g., `del my_list[0]`).
15. **Slicing**: Excludes the end index (e.g., `my_list[1:3]` includes indices 1 and 2).
16. **Range Exclusion**: The `range()` function excludes the end value (e.g., `range(1, 5)` generates `1, 2, 3, 4`).
17. **Flexible Range**: `range()` generates numbers that can be used outside a `for` loop or converted to a list (e.g., `list(range(3)) = [0, 1, 2]`).
18. A list comprehension is a list that is created based upon an existing list. You loop through the existing list and, optionally, perform some operation on each successive value before adding that value to the new list
19. To create a list of items that cannot be changed. you cab use Tuples to do just that. Python refers to values that cannot be changed as immutable. A tuple is identical to a list except it is immutable. A tuple is a simple data structure but can be very useful when you want to store a set of values that should not be changed.
20. Tuples are technically defined by the presence of a comma; the parentheses make them look neater and more readable. If you want to define a tuple with one element, you need to include a trailing comma: single_element_tuple = (8,). Without the trailing comma, it would just be an integer, not a tuple.
21. When the variable inside len() is a string, len() returns the number of characters in the string.
22. You can use any object that you can create in Python as a value in a dictionary. To get the value associated with a key, give the name of the dictionary and then place the key inside a set of square brackets (as we did when accessing the data within lists). Python returns the value associated with that key.
23. To use the key to access the associated value:
    ```
    for key in person:
        print(person[key])
    ```
    Or you can add the values() method to the dictionary for loop so that it just provides its values
24. Sets in python are unordered thats why you can't access it using indexing, every element has to be unique and it also returns the value in alphabetical order. You will more commonly use the set() function to convert a series of elements (like a list) to a set.


## 📝 General Notes: R Essentials
### Key Concpets
1. 3 %% 2 is named a Modulus/Remainder not a single %
2. Commenting style, characters, variable naming, Comparison Operators rules are same as python
3. You can concatenate (or combine) character types by using the paste() function: ``` paste("Here we go", "again!") ```
4. ``` print("Let's print some R!", quote = FALSE) ``` Setting the quote parameter to FALSE removes the quotes from the output.
5. ```
   # Using the noquote() function prevents quotes from being output.
   noquote("Let's print some R!") 
    ```
6. Assignment, in R, generally uses the leftward assignment operator (i.e., <- ). The equals operator (i.e., = ) can be used in some circumstances but not all. The <- operator can be used anywhere for assignment.
```
# Assigning a value to a variable:
           introduction <- "R here!"
            print(introduction)
```
7. The following shortcuts will insert the leftward assignment operator (<-):

Win: alt + -

Mac: option + -

8. ### Formatted printing

The **cat()** function can be used to concatenate and format character output.
```
# Format output (spaces are automatically added between items)

men <- 32
women <- 27

# Assigning the sum of the variables men and women to the variable num_participants.
num_participants <- men+women


# Concatenating the variable num_participants with two character strings and returning the output.
cat("There are", num_participants, "individuals currently participating in the study.")
```
9. T and F are reserved for TRUE and False respectively, and Any non-zero value is considered TRUE!.

### Data structures:
1. Vectors: The fundamental data structure in R is the vector. A vector is a one-dimensional sequence of data elements, of the same type, stored in a sequence. The elements are most commonly of type character, logical, integer or numeric.
2. Unlike most programming languages the index positions of a vector in R begin counting from 1.
3. You can get slices or subsets of a vector by placing the index position of items between square brackets
4. A negative value means to exclude the index position
5. Lists: can be created using the list() function where you can create different types of elements inside it.
6. Data Frames: Data frames are the most common way of storing and analyzing data in R. The columns (which are vectors) can be of different types, but they must be the same length.

### Importing data in R:
1. Comma separated values which is known as (csv) is a common way that data can be formatted. To import a csv file, read.csv() is used. The name of the file is passed in and the dataset will be imported as a data frame: ``` df <- read.csv("data/heart_disease.csv") ```.
2. head: The head() function displays the first six rows (by default), whereas The tail() function displays the last six rows (by default).
3. Another way that we can import data is by using read.table(). This reads a file in table format and creates a data frame from it. We can set its sep parameter to indicate how the data is separated (e.g., sep="," for comma separated values). Setting the header parameter to TRUE indicates that the first row contains the names of the columns: ``` df_table <- read.table("data/heart_disease.csv", sep=",", header=TRUE, ) ```
### Conditions in R: the format is as follows:
```
if (<condition>) {
  <block of code>
}
```
1. Basically it's like C in this formatting look at an example:
``` x <- 12
3. if(x > 0) {
  print("x is a positive number")
}
```
2. For multiple conditions we use if- else if:
```
if (<condition>) {
    <block of code>
} else if (<condition>) {
    <block of code>
}
```
- For an if-else if statement, only one of the conditions will be able to return TRUE (if any). The first condition to return TRUE will have its code block run and then the if statement will be exited. Therefore, it's important to consider the order in which you place your if statements. If no condition returns TRUE, no code will be executed.
3. If we want to guarantee that some action is taken regardless of the result of each condition, we use if else.
4. Same for loop foramtting as C.
  - function seq_along() which returns the index of each item in the vector.
### Functions in R:
Below shows the simplest structure of a function in R. You begin by using function() to indicate to R that you are defining a function. The function declaration will always be followed by parentheses within which you will provide any information the function needs to perform its job. Following the function() declaration is the function definition (the code to be executed to perform the desired task) contained within curly braces. The defined function should then be assigned to an appropriate function name. We use the keyword function to declare it. Here is an example:
```

``` R
name_of_function <- function() {
  <block of code to be executed>
}
```
And more clear one :
```
greeting <- function(){
  print("Hello!")
}
```
- Keep in Mind that just like any other programming language: No code is run when a function is defined. An instance of a function is created but no code is executed until the function is called.
1. Return in R: The standard return rule in R is that a function will return the last value that it computed. However, if we would like to be explicit about what is outputted, or end the execution, we can use return().
2. we can assign a function to each element of our vector using the sapply() method, we first pass a vector into sapply(). We then indicate the function that we would like to apply to each element within the passed-in vector by assigning the function to the FUN parameter. In this case, the square_num function was passed in so sapply returns the square of each number from the passed-in vector. FUN is a crucial component that defines the operation to be applied to each element of the input, aka specifies the function to be applied to each element of the input vector or list.
3. For asserting a method into a matrix we use apply() function: ``` apply(mat, MARGIN=2, FUN=mean) ```.
   Since a matrix is two dimensional, there's an additional required parameter called MARGIN which indicates whether you would like for the function to be applied over the rows (indicated by a 1) or over the columns (indicated by a 2). we first pass a matrix (mat) into apply(). We then indicate that we would like a function to be applied to the columns of the passed-in matrix by assigning 2 to the MARGIN parameter (2 indicates columns). Finally, we indicate the function that we would like to apply to each column of the passed-in matrix by assigning the function to the FUN parameter. In this case, the mean function was passed in so apply returns the mean of each column of the passed-in matrix.
4. Tip: To learn more about a function or an object, you can place a question mark ("?") before the object or use the help() function. Running the cell will display a description and details about the object along with exmples of how it's used: ``` ?sapply() ``` or ``` help(read.table) ```

## 📝 General Notes: Pandas Essentials
### Key Concpets
Pandas provides data structures and intuitive capabilities for performing fast and easy data cleaning, preparation, manipulation, aggregation, and sophisticated analysis.
1. Why do most programmers import pandas as pd? Traditionally, "pd" is used as the alias for pandas. Therefore, whenever you see pd. in the code, it's referring to the use of pandas and its capabilities.
2. Series: A Series is a one-dimensional object containing a sequence of values, very similar to a column of data in an Excel spreadsheet. The Series data structure has an associated index which can be either numbers, or strings (ie. named labels): ``` series_obj = pd.Series([10,20,30,40,50]) ``` The index of the Series object is displayed on the left, the values are displayed on the right and the data type is displayed beneath.
   - Notes: "dtype: int64" means data is stored as integers. Data type (dtype) represents how a value is stored in memory and, for numbers, it indicates how precisely it can be represented in memory.
   - Math can’t be applied to the string “10” so perhaps it would need to be converted to an integer (int64) data type in order to get descriptive statistics of the column (e.g., mean, standard deviation) or to perform machine learning.

Wearable data is somewhat unique and can be represented as any of the data types depending upon the values being collected. For example, the date of collection would be represented as type date64 in Pandas. The delta or difference between two time points would be stored as type timedelta. Moreover, wearable data is typically time series data that is stored as float64.
4. The values, in a Series object, can be accessed by placing the associated index position within square brackets. It is similar to how we access values from within a Python List.
```
series_obj = pd.Series([10,20,30,40,50])
series_obj[0]
```
5. Labling the data: A label can be used to identify each data point (row) by providing a list of the desired labels to the index property of the Series object.
```
series_obj = pd.Series([10,20,30,40,50], index = ["CA", "FL", "NY", "PA", "TX"])
```
6. When the values in a Series object have labels, you can use the labels to select values: ``` series_obj["CA"] ```. If you're requesting more than one label (index), they must be placed within a list:

``` series_obj[["CA", "NY", "TX"]] ```
### Element-wise operations
An operation can be applied to each element in a Series object. Element-wise operations are convenient as we don't need to use a for loop to apply the operation. Pandas will apply the operation to each element in the Series for us.
8. An operation can be applied to each element in a Series object. Element-wise operations are convenient as we don't need to use a for loop to apply the operation. Pandas will apply the operation to each element in the Series for us: ``` series_obj >20 ```
### DataFrames:
The DataFrame is another data structure in pandas. A DataFrame is a two-dimensional array of values. Much like an Excel spreadsheet, it is a rectangular table of columns and rows with both a row index and a column index. It can, somewhat, be thought of as a collection of Series objects, each of which can have a different data type (e.g., strings, numbers).
Typically, pandas will import data (e.g., from a csv file) as a DataFrame. However, a DataFrame may be constructed, for example, by using a dictionary (key/value pairs) with the key being the column name and the value being a list of row values.
```
# Creating a sample DataFrame using a dictionary of lists of values.

data = {"Name": ["Tim Miller", "Ann Carter", "Ellen Lee", "Sam Carr", "Al Ball", "Carl Zee", "Sara Martin"], 
        "Gender": ["Male", "Female", "Female", "Male", "Male", "Male", "Female"],
        "Age": [32, 44, 21, 19, 45, 27, 39]}
df = pd.DataFrame(data)
df
```
We can use the head function to preview only the first 5 rows: ``` df.head() ``` or tail() method to preview last 5 ones.
9. You can retrieve a column from a DataFrame by using the column's name between square brackets. (A Series object is returned.): ``` df['Name'] ``` You can also use dot notation to retrieve a column (Series) from a DataFrame, but only if the column name is a valid Python variable name (e.g., no spaces): ``` df.Name ```

<div class="alert alert-block alert-info">
<b>Tip:</b> When using dot notation (attribute notation), following the dot, you can use the tab key to complete the column name (or any other attribute). For example, using the above DataFrame, try typing just 'df.N'. Then use the tab key, and Jupyter will complete the rest, or present any other options that begin with 'df.N'. This is known as tab completion and is provided as a convenience by Jupyter.
</div>

### Dropping Rows and coloumns:
Here is how to make a dataFrame:
```
data = {"Name": ["Tim Miller", "Ann Carter", "Ellen Lee", "Sam Carr", "Al Ball", "Carl Zee", "Sara Martin"], 
        "Gender": ["Male", "Female", "Female", "Male", "Male", "Male", "Female"],
        "Age": [32, 44, 21, 19, 45, 27, 39]}
```
1. You can use the drop() method on the DataFrame to drop entries. Adding the desired axis will determine whether rows or columns will be dropped. There are two axes in pandas:
- Axis 0 indicates that you intend to drop a row.
- Axis 1 indicates that you intend to drop a column.
2. Row with index 6 will be dropped: ``` df.drop(6, axis = 0) ```
3. Printing the same dataframe again will return the same old one not the new one you used the drop method with as drop() returns a copy of the DataFrame so that the original DataFrame (df) remains unmodified.
4. Axis = 0 indicates that you intend for rows to be dropped. In the example above, you are indicating that you would like for the row at index position 6 to be dropped. Using axis = 1 would indicate that you intend for columns to be dropped. For example, you could type `df.drop("Age", axis = 1). This would indicate that you intend to drop the column 'Age'. Using any other value other than 0 or 1 for axis will return an error. Alternatively, you could use 'df.drop(index = 6)' to drop the row at index position 6. And you could use 'df.drop(columns = "Age")' to drop the column 'Age'. You can omit the axis thingy too and it will work without specifying it just put the value for the row or coloumn place: ``` df.drop(columns = "Age") ``` and you can do this too: ``` df = df.drop(index = [3, 6]) ``` 😃 or put the coloumns names inside the []!.
5. If you would like for the changes to be reflected in the original DataFrame (df), then you can set the original DataFrame (df) equivalent to the returned copy following the drop, as demonstrated below:
```
df = df.drop(6, axis = 0)

df
```
6. If you prefer to just have the DataFrame modify itself in place rather than return a copy of itself, then you can set the drop method's "inplace" parameter to True, as shown below: ``` df.drop(6, axis=0, inplace=True) ```
7. Note: Be careful when making changes "inplace". Inplace changes modify the original data and the only way to get it back is by reimporting it. Alternatively, by working with a copy, you can easily return to the original DataFrame when circumstances require it without needing to reimport data.
### Using loc() and iloc():
#### loc():
1. Using loc (short for location) allows you to select a subset of the rows and columns using the label/name of the row/column. If the rows were not given labels (named), then their index position is their label. Within the square brackets, the selection preceding the (optional) comma refers to the rows you would like selected. Following the (optional) comma is the selection referring to the desired columns. The selection is inclusive of the end position.
Selecting the rows 0 through (and including) 5, and the column "b":
```
data.loc[:5, "b"]
```
2. The comma is optional. No comma assumes all columns will be returned ```data.loc[:5] ``` If no comma follows the row selection then all columns are returned.
3. Selecting the rows 6 through to the end of the DataFrame, and the columns "a" through "e" (inclusive): ```data.loc[6:, 'a':'e'] ```
4. *Selecting all of the rows of the DataFrame, and the columns "c", "f" and "i" (in that order)*: ``` data.loc[:, ['c', 'f', 'i']]     # not consecutive ``` When selecting by label, the end point (stopping position) is included, for both rows and columns.
#### iloc():
1. Using iloc allows you to select a subset of the rows and columns using their index position. Thus, only integers can be used. Within the square brackets, the selection preceding the (optional) comma refers to the rows you would like selected. Following the (optional) comma is the selection referring to the desired columns. The selections will **_not_** include the end position.
2. *Selecting the rows from the beginning of the DataFrame (the first row) through to index position 5 (but not including index position 5). Then, selecting the columns located at index positions 2 through 5 (but not including index 5)*: ``` data.iloc[:5, 2:5] ```
3. Selecting rows at index 5, 0 and 3 (in that order). Then selecting columns located at index 9, 5 and 0 (in that order): ``` data.iloc[[5, 0, 3], [9, 5, 0]] ```
4. Select the rows where column "j" is greater than 50 (indicated by everything before the comma). Then, just select column "j" (indicated by what follows the comma). Now, set those values equal to 100:
```
data.loc[data["j"] > 50, 'j'] = 100

data
```
5. Select the rows with index positions 5 through 8, but not including 8 (indicated by everything before the comma). Then, just select the column at index position 0, the first column (indicated by what follows the comma). Now, set those values equal to -100:
```
data.iloc[5:8, 0] = -100
data
```
### How to import data from pandas:
- Here is how to import data into pandas:
```
df = pd.read_csv("data/heart_disease.csv")
```
- you can use the method sample to the DataFrame's sample() method returns a random sampling of rows from the dataset. The number passed to the method determines the number of rows returned: ``` df.sample(10) ```
## Descriptive and summary statistics
1. The describe() method displays the descriptive statistics about a DataFrame including the mean, median, min, max and quartile values for each numerical column: ``` df.describe() ```
2. You can also call individual methods on a column (Series object) to get a particular descriptive value for that column: ``` df["age"].min() ``` aka ``` df["chol"].mean() ```
3. To view a summary of non-numerical (categorical) columns, you should set the "include" parameter of the describe method equal to "object". In pandas, categorical variables are of type "object": ``` df.describe(include="object") ``` The summary will include the top occurring category for each column along with its frequency, or: ``` df["sex"].describe() ```
4. The info() method displays information about a DataFrame including column data type (dtype) and non-null values: ``` df.info() ``` Using the info() method can be a valuable way to determine if there are any missing values in our dataset. Above, note that info() indicates that the dataset has "303 entries". Also, note that it indicates that each column has "303 non-null" values. A "null" value indicates a missing value, so the above suggests that there are no missing values in the dataset. Further, info() helpfully provides information about the datatype (Dtype) of each column
5. How to display the unique values: ``` df["target"].unique() ```
6. A Series object (single column) can be passed into Python's built-in set() function to see the column's unique values: ``` set(df["target"]) ``` However, The unique() method tends to be faster. Python's set() function can be a little slower primarily because it sorts the returned values, which can be helpful in locating a specific category when there are a lot of distinct values within a given column.
7. The DataFrame's corr() method will display the pairwise correlations among the DataFrame's columns: ``` df.corr(numeric_only=True) ``` or select specfic columns ``` df[["age", "max_hr"]].corr() ``` It's important to be able to interpret correlation coefficients:
- Perfect: If the value is near ± 1, then as one variable increases, the other variable tends to also increase (if positive) or decrease (if negative).
- High: If the value lies between ± 0.50 and ± 1, then it is said to be a strong correlation.
- Moderate: If the value lies between ± 0.30 and ± 0.49, then it is said to be a moderate correlation.
- Low: When the value lies between ± .29 and 0, then it is said to be a small correlation.
- No correlation: When the value is zero there is no correlation between the variables.
8. We often need to convert categorical variable names into numbers for data analysis and machine learning, so being able to determine the number of unique values within a column can be helpful. For example, knowing that there are only two categories within a column, as shown above, we would know that we could perhaps convert 'Yes' to 1 and 'No' to 0, when numbers are required. If we hadn't determined the unique values with the column, perhaps we could have missed that there was a 'Maybe' option that also needed to be converted.
9. Identifying correlations among the columns (independent variables) in a dataset can be very important. This is known as _collinearity_ and can be detrimental to training a machine learning model.
10. Sorting dataframes: The DataFrame's sort_values() method takes a "by" parameter to indicate which column the DataFrame should be sorted by: ``` df.sort_values(by="age").head() ``` but By default, sort_values() will sort the values from smallest to largest. But remember that pandas don't modify the data unless you put the copied version into another dataFrame name variable, so to save your modification you do this: ``` df = df.sort_values(by="age") ``` or use inplace like I said above.
11. To sort the values from largest to smallest, you can set the "ascending" parameter of the sort_values() method to False: ``` df.sort_values(by="age", ascending=False).head() ```
### nlargest() & nsmallest:

### Data_Transformation
1. How to rename a column? You need to name your columns something meaningfull for you to be able to read and modify clearly. The DataFrame's rename() method uses a column parameter. Set the column parameter equal to a dictionary representing the present column name paired with the name that you would like the column renamed to:
```
df = df.rename(columns={"target":"heart_disease"})
df.head()
```
2. Transform categorical variables to numbers:
   - Most machine learning algorithms require numbers, so it can be imperative to convert all categorical variables to numerical representations.The DataFrame's map() method takes a dictionary of pairs representing the present value paired with the desired transformed value:
     ```
     df["sex"] = df["sex"].map({"Male":0, "Female":1})
     df.head()
     ```
   - Remember, a copy is returned so we set the existing column equal to the transformed values.
   - It is extremely useful to confirm a column's unique values prior to tranformation. It can clarify spelling and whether uppercase or lowercase was used. And, importantly, it can expose hidden spaces preceding or following a value.
  
### Data Analysis
1. Conditional selection: ``` df["sex"]==1 ``` Conditional (boolean) selection is a question and always returns either True or False. This result can be placed within the square brackets of a DataFrame, using .loc, and only the rows that were True will be returned.
   - Here is more example: Select the rows where the column "sex" is equivalent to 1 ("Female"). Then display just the column "age": ``` df.loc[df["sex"]==1, "age"] ```
3. The count() method displays the number of rows that are included in a selection, here is an example of how it works: Get the rows where the column chest_pain is equivalent to 3. Return only the column "sex", and display the number of rows returned:
```
# Use count() to get the number of rows (returned) in a selection.

df.loc[df["chest_pain"]== 3, "sex"].count()
```
4. The value_counts() method displays the itemized counts of each category within a column. In other words, it breaks the column down into its individual categories then sums by category. For example, if the column "sex" contained the values [M, F, F, M, F, M, F, F], value_counts() would return that there are 5 of the category F and 3 of the category M. Here is an example of how it works: Get the rows where the column chest_pain is equivalent to 3. Return only the column "sex", and itemize the number of rows returned by gender:
```
df.loc[df["chest_pain"]== 3, "sex"].value_counts()
```
5. Multiple conditions: Using .loc, you can set multiple conditions for a query. The ampersand (&) means "and" and the pipe symbol (|) means "or".
   - Get the rows where the column "sex" is equivalent to 1 ("Female") AND where the column "max_hr" is greater than the average "max_hr". Return only the column "sex", and display the number of rows returned:
     ```
     mean_max_heart_rate = df["max_hr"].mean()

     df.loc[(df["sex"]== 1) & (df["max_hr"] > mean_max_heart_rate), "sex"].count()
     ```
   - Get the rows where the column "chest_pain" is equivalent to 0 OR the column "age" is greater than 60; AND, from among those rows, get the rows where the column "sex" is equivalent to 0 ("Male"). Return only the column "heart disease", and display the itemized count of how many did and did not have heart disease:
     ```
     df.loc[((df["chest_pain"] == 0) | (df["age"] > 60)) &
     (df["sex"] == 0), "heart_disease"].value_counts()
     ```
   - Because of precedence and the order of operations, it's important to place parentheses around each condition to clarify the desired order of operations.

## 📝 General Notes: Introduction to Statistics
1. An effective way to understand a data distribution is to describe the center of the data--it's central tendency. The mean, median and mode are the fundamental ways to do this and are the most basic descriptive statistics functions.
### The mean
- you can calculate it either by summing up the values and dividing by their number, or my using the mean() method.
```
dataset["numbers"].sum()
len(dataset["numbers"])
dataset["numbers"].sum()/len(dataset)

or this:
dataset["numbers"].mean()
```
### The median
- If we have a dataset of 10 numbers, and our values are ordered (as the values in our dataset are), the median is the middle-most value if there are an odd number of values. If there are an even number of values, then we average the two center-most values. In our dataset, we have an even number of values so we will average the two center values ( 4 and 5) to attain a median value of 4.5. This value is slightly different from our mean value, but is another way to describe the center of our data.
- The median is useful in that, unlike the mean, it is fairly unaffected by outliers. Now we can use the median() method:
```
dataset["numbers"].median()
```
### The mode
- The mode is the most frequently occurring value or set of values. If any values are tied in terms of their frequency, then those values will be reported as modes together, and the dataset is said to be bimodal or multimodal. It's most useful when your data is repetitive and you want to identify which values occur most frequently. For our dataset, the most frequently occuring value is 5. It can be used to describe the central tendency of a dataset.
```
dataset["numbers"].mode()[0]
```

![image](https://github.com/user-attachments/assets/638d2af2-e17d-4d7d-b292-0c4b58c72a89)

- However, if there are extreme outliers (a value that is much higher or lower than the rest of the values), they will cause the mean to shift significantly in the direction of the outliers, whereas the median is fairly unaffected.
- The NightSignal Algorithm uses wearable data to detect pre-symptomatic and asymptomatic COVID-19 infections. The NightSignal Algorithm module on the Research page provides an example of the use of central tendency. It calculates the average resting heart rate (RHR) overnight each day for each individual, and then uses the median value as the healthy baseline. The median often gives a better sense of what a “typical” value is, which helps provide an intuition about the dataset.

### Standard_Deviation
An important characteristic of datasets is how much variability exists among individual samples. Without a measure of variability, you can’t effectively compare two datasets. For example, if one dataset consists of the values [99, 100, 101], and another dataset consists of the values [0, 100, 200], they both have the same mean and median values of 100, yet they have very different amounts of variability. There is a large amount of variability in the second dataset compared to the first. The variability is often a defining characteristic of a dataset. The standard deviation is perhaps the most informative and certainly the most widely used measure of a dataset's variability. Let's look at how it's calculated.
Let's use the ten values below to calculate the standard deviation of a dataset. We are interested in the average difference between each value in the distribution and the mean of the distribution. We first need to calculate the mean, as shown below:

![image](https://github.com/user-attachments/assets/7c88400e-d827-4e28-945d-46a94b9e97e3)

Next, the **average difference (or deviation)** is calculated by taking each individual value and subtracting the mean from that value. Once we calculate a deviation score for each individual value in the distribution, we can then sum the deviation scores and divide by n to get the average, which would be the standard deviation. However, there's one problem. Half of the deviation scores fall below the mean, and half fall above the mean. This means that when we sum these deviation scores together, we will get zero, as shown below. And zero divided by any number will be zero. Therefore, we need to do something to work around this issue.
We can make each deviation score positive by squaring it. Hence, for each value in the distribution, we subtract the mean of the distribution and then square the deviation. We then add up all of these squared deviations, giving us the <mark>**sum of the squared deviations**</mark>.
- In the image above, notice that the original column is named "Feature". In bioinformatics, what some may call a column, field, or independent variable is called a "feature". A feature is the generic name for any column within a dataset. It will be helpful to get used to the terminology commonly used in data science and bioinformatics.
We next divide by n (the number of samples in the distribution) minus one to get the average of the squared deviations. This is known as the variance.
Because we previously needed to square each deviation score to avoid getting a sum of zero, we now need to reverse that process. This is accomplished by taking the square root of the variance, and the result gets our values back into their original terms. The <mark>**square root of the variance**</mark> is known as the <mark>**standard deviation**</mark>. It is a measure of, on average, how much individual samples within a data set vary from the middle. You can use this method to display it: ``` dataset["numbers"].std() ```

![image](https://github.com/user-attachments/assets/49d7e84d-d6ce-4ac3-b4d3-e9b56c227578)

The standard deviation is extremely useful in helping us to understand our data. It effectively enables us to compare different data points within our dataset to each other. And it's especially effective in allowing us to compare values between different datasets.

The formula for the **`standard deviation`** of a dataset is:  


$$\Large\sqrt[]{\frac {\Sigma (x_{i}-\bar{x})^{2}}{n-1} }$$

_Let's walk through the above formula and summarize what we've discussed: The numerator is simply the sum of the squared distance that each value is from the mean. We then divide that sum by n-1 (we'll assume that the data is a sample from larger a population) to get the average squared distance or deviation from the mean. Finally, because we squared the deviations from the mean, we'll now take the square root of the calculated quantity to undo the squaring and put everything back into the original terms._
- The mean is interpreted as the expected value, and the standard deviation can be interpreted as the expected range of values around the mean.

### Normalization
<mark>**Normalization**</mark>, in the **_general sense_**, refers to scaling our numeric columns to bring them into the **same terms** so that they fall within a smaller and standard range of values, making it easier to compare them. This is useful because data variables are typically measured in varied units with varied magnitudes. For example, a patient's age is measured in terms of years while heart rate is measured in terms of beats per minute. These variables are measured in completely different terms which makes it difficult to make a comparison as to which may be better or worse than the other.
However, normalization, in the **_specific sense_**, refers to scaling variables so that their values fall strictly between 0 and 1, making it easier to compare them. This is also known as min-max scaling.
Normalization scales down the data values to between 0 and 1: $$\large\ normalization = \frac{X-X_{min}}{X_{max}-X_{min}}$$
Given any dataset you would do the following:
1. Identify the minimum and maximum values
2. Subtract both values, This becomes the denominator for our scaling.
3. Then apply the role above to any sample X.
Here is how to do it in code:
```
import pandas as pd
df = pd.read_csv("data/data_normalization/heart-disease.csv", usecols=[0,4,5])
df.head()
df.min()
df.max()
(df - df.min())/(df.max() - df.min())
```
It should now be clear why normalizing values is useful. It's an effective way of comparing values that are measured in different units and it scales values down into a standard range.
Another scaling technique that is used to transform variables so that they are in similar terms is called standardization. This technique scales values so that they are in terms of how far they are from their respective means (in terms of standard deviations). Rather than falling between 0 and 1 as normalization does, standardized values are scaled to fall typically between -3 and 3 (see Z-score).

## 📝 General Notes: Introduction to Data Visualization
### Heatmaps
A heatmap is a graphical representation of data where values are expressed as colors. It is an effective visual summary of information and enables a large volume of data to be communicated efficiently.
- If you want to view a matrix of the pair-wise correlations between the variables in the dataset:
  use the following: ``` df.corr(numeric_only=True) ```
  Here is how to render a heatmap in a family of blue colors. Note that the darker the blue, the higher the correlation between a given variable pair. The lighter the blue, the weaker the correlation between variable pairs.
  ```
  sns.heatmap(df.corr(numeric_only=True), cmap="Blues", annot=True);
  ```
### Heatmaps in medicine
A heatmap is a common method of visualizing gene expression changes from among hundreds to thousands of genes from different treatment conditions. The heatmap may also be combined with clustering methods which group genes and/or samples together based on the similarity of their gene expression pattern. This can be useful for identifying genes that are commonly regulated, or biological signatures associated with a particular condition (e.g a disease or an environmental condition).
- A heatmap is a common method of visualizing gene expression changes from among hundreds to thousands of genes from different treatment conditions. The heatmap may also be combined with clustering methods which group genes and/or samples together based on the similarity of their gene expression pattern. This can be useful for identifying genes that are commonly regulated, or biological signatures associated with a particular condition (e.g a disease or an environmental condition).
- Genes are represented in rows of the matrix and chips/samples in the columns. A colored matrix display represents the matrix of values as a grid; the number of rows is equal to the number of genes being analyzed, and the number of columns is equal to the number of chips/samples. The boxes of the grid are colored according to the numerical value in the corresponding matrix cell (the gene expression values).
- You will be able to pick genes based on their expression levels under different conditions. Some may not change but those that do change are of the greatest interest. These indicate gene expression associated with a particular condition. Heatmaps also help one to identify significant groupings among the genes through associations.
- Heatmaps are used to show relationships between two variables, one plotted on each axis. By observing how cell colors change across each axis, you can observe if there are any patterns in value for one or both variables. In heatmaps, the data is displayed in a grid where each row represents a gene and each column represents a sample. The color and intensity of the boxes are used to represent changes (not absolute values) of gene expression.
```
import pandas as pd
from bioinfokit import analys, visuz


df = pd.read_csv("data/data_heatmap/gene_expression.csv")
# set gene names as index
df = df.set_index(df.columns[0])
df.head()
visuz.gene_exp.hmap(df=df, rowclus=False, colclus=False, cmap='RdYlGn', tickfont=(6, 4), show=True)
```

### Volcano plot
A volcano plot is a 2-dimensional scatter plot that has the shape of a volcano. It makes it easy to visualize the expression of thousands of genes obtained from -omics research (e.g., transcriptomics, genomics, proteomics, etc.) and to identify genes with significant changes. It is used to plot the log fold change in the observation between two conditions (e.g., the gene expression between comparison and control conditions) on the x-axis. On the y-axis is the corresponding p-value for each observation, representing the statistical significance of the change (if any) between the different conditions. A volcano plot can visualize a lot of complex information in one plot. The wider the dispersion of data points in the volcano plot the greater the significance in gene expression changes between two conditions.
#### How can we read this plot though?
To be clear, the x-axis of a Volcano plot represents the amount of change following a condition or experiment. The zero (0) point on the x-axis represents no change. For every point increment to the right of 0, the amount of the change doubles. For example, 1 on the x-axis represents an increase of twice the original (control) value, 2 on the x-axis represents an increase of 4 times the original value, and 3 on the x-axis represents an increase of 8 times the original value. Every point below 0 is interpreted similarly except that it represents a decrease in the original (control) value.
The y-axis of a Volcano plot represents the significance of the change on the x-axis in p-values (probability values). The zero (0) point on the y-axis represents a p-value of 1.0. For every point increase on the y-axis, the decimal point of the p-value moves one place to the left. For example, 2 on the y-axis is equivalent to a p-value of .01, which can be interpreted as there's appoxiamtely a 1% chance that you could get the value that you observed, assuming that there is no difference between the control and experimental conditions. In other words, it suggests that the observation appears to be significant. (A 3 on the y-axis would represent a p-value of .001, a 4 would represent a p-value of .0001, etc.)
The volcano plot enables the ability to quickly see the effect (if any) of an experiment (e.g., change in protein expression) between two conditions in terms of both an increase and decrease of the observed value along with the statistical significance of any observed change.
#### Example:
```
import pandas as pd
from bioinfokit import analys, visuz

df = pd.read_csv("data/data_volcano_plot/volcano_data.csv")

df.head()
visuz.GeneExpression.volcano(df=df, lfc="log2FC", pv="p-value", show=True, plotlegend=True,
                                    sign_line=True, color=("#EC004F", "grey", "black"))
```
- The gray points indicate non-significant points. The red points indicate significant up-regulated genes and the black points indicate significant down-regulated genes.

![image](https://github.com/user-attachments/assets/d3cbffff-e213-4772-87cc-36aa380261ba)

#### Another example
The sample plot below is displayed with a log2-fold threshold of -1 and a p-value threshold of < 0.05 for significantly down-regulted genes. And a log2-fold threshold of 2 and a p-value threshold of < 0.01 for significantly up-regulted genes. The light gray points indicate non-significant points. The pink points indicate significant down-regulated genes (i.e., log2-fold < -1 and p-value < 0.05) and the cardinal points indicate significant up-regulated genes (log2-fold > 2 and p-value < 0.01).
```
visuz.GeneExpression.volcano(df=df, lfc='log2FC', pv='p-value', lfc_thr=(2, 1), pv_thr=(0.01, 0.05),
    color=("#A31746", "lightgrey", "#FF9595"), show=True, plotlegend=True, legendpos='upper right',
    sign_line=True, legendanchor=(1.46,1))
```
#### Customized plot
```
visuz.GeneExpression.volcano(df=df, lfc='log2FC', pv='p-value', lfc_thr=(2, 1), pv_thr=(0.01, 0.05),
    color=("#A31746", "lightgrey", "#FF9595"), show=True, plotlegend=True, legendpos='upper right',
    sign_line=True, legendanchor=(1.46,1), genenames=("LOC_Os09g01000.1", "LOC_Os01g50030.1", "LOC_Os06g40940.3", "LOC_Os03g03720.1"),
    gstyle=2, geneid="GeneNames")
```
#### Added gene names
```
visuz.GeneExpression.volcano(df=df, lfc='log2FC', pv='p-value', lfc_thr=(2, 1), pv_thr=(0.01, 0.05),
    color=("#A31746", "lightgrey", "#FF9595"), show=True, plotlegend=True, legendpos='upper right',
    sign_line=True, legendanchor=(1.46,1),
    genenames=({"LOC_Os09g01000.1":"EP", "LOC_Os01g50030.1":"CPuORF25", "LOC_Os06g40940.3":"GDH", "LOC_Os03g03720.1":"G3PD"}),
    gstyle=2, geneid="GeneNames")
```
## 📝 General Notes: Introduction to Cloud Computing
![image](https://github.com/user-attachments/assets/cd9dc254-a96d-4167-95c8-1dab64218047)

# 📖 Statistics 2 Notes
### Principal component analysis involves 5 steps:
- Standardize the range of values for each variable
- Compute the covariance matrix to identify correlations among the variables
- Compute the eigenvectors and eigenvalues of the covariance matrix to identify the principal components
- Decide how many principal components to keep
- Reorient the data along the principal components' axes

---

## 📚 How to Use These Notes
- **Browse** for quick reference during coding.
- **Practice** the examples in a Python environment like Jupyter Notebook.
- **Expand** on these concepts by exploring Python's official documentation or additional resources.

