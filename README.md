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
---

## 📚 How to Use These Notes
- **Browse** for quick reference during coding.
- **Practice** the examples in a Python environment like Jupyter Notebook.
- **Expand** on these concepts by exploring Python's official documentation or additional resources.
