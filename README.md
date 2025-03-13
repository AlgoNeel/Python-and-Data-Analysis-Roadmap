# Python & Data Analysis Learning Roadmap

This roadmap is designed to guide you through mastering Python, data analysis, and key Python libraries used in data science. Follow the steps in sequence to build a solid foundation in Python and develop the skills necessary to analyze and visualize data.

---

## 🔹 **Learn Python & Data Analysis - Detailed Roadmap**

### 1. **Master Python Basics**

#### 1.1 **Variables & Data Types**
- **Understanding Variables**: How to assign values to variables.
- **Basic Data Types**:
  - **Strings**: `"hello"`, multi-line strings (`'''string'''`), string operations (`+`, `*`, `len()`, etc.)
  - **Integers**: Whole numbers (positive/negative).
  - **Floats**: Decimal numbers.
  - **Booleans**: `True` or `False`.
  - **Lists**: Ordered collection of items, can be of mixed data types (e.g., `my_list = [1, 2, 3, 'four']`).
  - **Tuples**: Immutable ordered collection (e.g., `my_tuple = (1, 2, 3)`).
  - **Dictionaries**: Key-value pairs (e.g., `my_dict = {'key1': 10, 'key2': 20}`).
  - **Sets**: Unordered collection of unique items (e.g., `my_set = {1, 2, 3}`).

#### 1.2 **Control Structures**
- **If-Else Statements**: Conditional logic for decision-making.
    ```python
    if x > 10:
        print("Greater than 10")
    else:
        print("Less than or equal to 10")
    ```
- **Loops**:
  - **For Loop**: Iterate over lists, ranges, or dictionaries.
    ```python
    for i in range(5):
        print(i)
    ```
  - **While Loop**: Repeats code while a condition is `True`.
    ```python
    while x < 10:
        x += 1
    ```
- **List Comprehensions**: Shorter syntax for loops.
    ```python
    squared = [x**2 for x in range(10)]
    ```

#### 1.3 **Functions**
- **Defining Functions**: Reusable blocks of code.
    ```python
    def greet(name):
        return f"Hello, {name}!"
    ```
- **Function Parameters**: Passing values to functions.
- **Return Values**: Returning output from functions.
- **Lambda Functions**: Anonymous functions (useful for short, throwaway functions).
    ```python
    add = lambda x, y: x + y
    ```

#### 1.4 **Object-Oriented Programming (OOP)**
- **Classes & Objects**: Defining a class and creating objects.
    ```python
    class Dog:
        def __init__(self, name, age):
            self.name = name
            self.age = age
        def speak(self):
            return f"{self.name} says Woof!"
    my_dog = Dog("Rex", 5)
    ```
- **Inheritance**: A class can inherit attributes and methods from another class.
    ```python
    class Puppy(Dog):
        def __init__(self, name, age, breed):
            super().__init__(name, age)
            self.breed = breed
    ```
- **Polymorphism & Encapsulation**: Understanding method overriding and hiding implementation details.

#### 1.5 **Error Handling**
- **Try-Except**: Handling exceptions in code.
    ```python
    try:
        result = 10 / 0
    except ZeroDivisionError:
        print("You can't divide by zero!")
    ```
- **Raising Exceptions**: Custom errors for specific cases.
    ```python
    raise ValueError("This is an error message!")
    ```

---

### 2. **Learn Data Analysis with Pandas, NumPy, and Matplotlib**

#### 2.1 **Pandas (Data Manipulation & Analysis Library)**
- **Series & DataFrame**: Pandas’ core data structures for handling data.
    ```python
    import pandas as pd
    data = {'Name': ['Alice', 'Bob'], 'Age': [24, 27]}
    df = pd.DataFrame(data)
    ```
- **DataFrame Operations**: Accessing, slicing, and filtering data.
    ```python
    df['Age']  # Accessing a column
    df.loc[0]  # Accessing a row
    df[df['Age'] > 25]  # Filtering rows
    ```
- **Data Cleaning**: Handling missing data (NaN), filling or dropping missing values.
    ```python
    df.isna()  # Check for NaN values
    df.fillna(0)  # Fill NaN with 0
    df.dropna()  # Drop rows with NaN values
    ```
- **Merging & Joining**: Combining multiple DataFrames.
    ```python
    pd.merge(df1, df2, on='column_name')
    ```
- **Grouping & Aggregating**: Grouping data based on categories and performing calculations.
    ```python
    df.groupby('column_name').mean()
    ```

#### 2.2 **NumPy (Numerical Computing Library)**
- **Arrays**: Efficient data structures for large data.
    ```python
    import numpy as np
    arr = np.array([1, 2, 3, 4, 5])
    ```
- **Array Operations**: Vectorized operations (no need for explicit loops).
    ```python
    arr + 5  # Add 5 to each element
    arr * 2  # Multiply each element by 2
    ```
- **Mathematical Functions**: NumPy provides functions for stats, random numbers, linear algebra, etc.
    ```python
    np.mean(arr)  # Mean
    np.median(arr)  # Median
    np.random.randn(3)  # Random numbers
    ```

#### 2.3 **Matplotlib (Plotting & Visualization Library)**
- **Basic Plotting**:
    ```python
    import matplotlib.pyplot as plt
    plt.plot([1, 2, 3, 4], [10, 20, 25, 30])  # Basic line plot
    plt.show()
    ```
- **Types of Plots**: Line plots, bar plots, histograms, scatter plots.
    ```python
    plt.bar([1, 2, 3], [3, 4, 5])  # Bar plot
    plt.scatter(x, y)  # Scatter plot
    ```
- **Customizing Plots**: Titles, labels, legends, colors, and gridlines.
    ```python
    plt.title('My Plot')
    plt.xlabel('X-axis')
    plt.ylabel('Y-axis')
    plt.legend(['Line'])
    ```

#### 2.4 **Advanced Data Visualization**
- **Seaborn**: High-level data visualization built on top of Matplotlib.
    ```python
    import seaborn as sns
    sns.lineplot(x='column_name', y='other_column', data=df)
    ```
- **Plotly**: Interactive visualizations for dashboards and reports.

---

### 3. **Use Jupyter Notebook for Coding**

#### 3.1 **Setting up Jupyter**
- Install Jupyter via `pip install notebook` or `conda install jupyter`.
- Open Jupyter using `jupyter notebook` in your terminal.

#### 3.2 **Writing Code in Cells**
- **Code Cells**: Write Python code in these cells and execute by pressing `Shift + Enter`.
- **Markdown Cells**: Use markdown for documentation and explanations.
    ```markdown
    # Heading
    Some explanation about the code.
    ```
- **Visualizing Data**: Plot charts directly in notebooks.
- **Interactive Widgets**: Use widgets for interactive plots and data manipulation.

#### 3.3 **Data Analysis Projects in Jupyter**
- Start with mini projects to practice the skills you've learned, such as:
  - **Exploratory Data Analysis (EDA)**: Analyze a dataset, plot distributions, and visualize relationships.
  - **Data Cleaning Projects**: Clean a messy dataset by removing duplicates, handling missing values, and transforming columns.

#### 3.4 **Saving and Exporting**
- **Saving Notebooks**: Save your work as `.ipynb` files.
- **Exporting to Other Formats**: Export to HTML, PDF, or Python scripts.
    ```python
    File -> Download as -> PDF
    ```

---

## 📚 **Key Learning Resources**

- **Books**: 
   - "Automate the Boring Stuff with Python" by Al Sweigart
   - "Python for Data Analysis" by Wes McKinney
   - "Python Crash Course" by Eric Matthes
- **Courses**:
   - [Coursera: Python for Everybody](https://www.coursera.org/specializations/python)
   - [Kaggle: Python Data Science Handbook](https://www.kaggle.com/learn/python)
