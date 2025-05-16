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

## 📚 How to Use These Notes
- **Browse** for quick reference during coding.
- **Practice** the examples in a Python environment like Jupyter Notebook.
- **Expand** on these concepts by exploring Python's official documentation or additional resources.
