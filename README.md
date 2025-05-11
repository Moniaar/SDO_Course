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

---

## 📚 How to Use These Notes
- **Browse** for quick reference during coding.
- **Practice** the examples in a Python environment like Jupyter Notebook.
- **Expand** on these concepts by exploring Python's official documentation or additional resources.
