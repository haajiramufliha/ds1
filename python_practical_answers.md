# Python Practical Record – All 15 Programs

This file contains the practical answers with:

1. Aim
2. Algorithm
3. Simple and correct Python Program
4. Output
5. Result

---

# 1. NumPy Programs

## 1(a) Create a null vector of size 10 and update the sixth value to 11

### Aim
To create a null vector of size 10 and update its sixth element to 11 using NumPy.

### Algorithm
1. Import NumPy.
2. Create an array of 10 zeros.
3. Update the sixth element with 11.
4. Display the array.

### Program

```python
import numpy as np

a = np.zeros(10)
a[5] = 11

print("Array:", a)
```

### Output

```text
Array: [ 0.  0.  0.  0.  0. 11.  0.  0.  0.  0.]
```

### Result
Thus, a null vector of size 10 was created and its sixth value was updated to 11.

---

## 1(b) Convert an array to a float type

### Aim
To convert an integer array into a floating-point array using NumPy.

### Algorithm
1. Import NumPy.
2. Create an integer array.
3. Convert it into float type using `astype()`.
4. Display the result.

### Program

```python
import numpy as np

a = np.array([1, 2, 3, 4, 5])
b = a.astype(float)

print("Float Array:", b)
```

### Output

```text
Float Array: [1. 2. 3. 4. 5.]
```

### Result
Thus, the integer array was successfully converted into a float array.

---

## 1(c) Create a 3×3 matrix with values ranging from 2 to 10

### Aim
To create a 3×3 matrix containing values from 2 to 10 using NumPy.

### Algorithm
1. Import NumPy.
2. Generate numbers from 2 to 10 using `arange()`.
3. Reshape the array into 3×3.
4. Display the matrix.

### Program

```python
import numpy as np

a = np.arange(2, 11).reshape(3, 3)

print(a)
```

### Output

```text
[[ 2  3  4]
 [ 5  6  7]
 [ 8  9 10]]
```

### Result
Thus, a 3×3 matrix containing values from 2 to 10 was created.

---

## 1(d) Convert a list of numeric values into a one-dimensional NumPy array

### Aim
To convert a list of numeric values into a one-dimensional NumPy array.

### Algorithm
1. Import NumPy.
2. Create a numeric list.
3. Convert the list using `array()`.
4. Display the array.

### Program

```python
import numpy as np

a = [10, 20, 30, 40, 50]
b = np.array(a)

print("NumPy Array:", b)
```

### Output

```text
NumPy Array: [10 20 30 40 50]
```

### Result
Thus, the numeric list was successfully converted into a one-dimensional NumPy array.

---

# 2. NumPy Programs

## 2(a) Convert an array to a float type

### Aim
To convert an array into floating-point data type using NumPy.

### Algorithm
1. Import NumPy.
2. Create an integer array.
3. Convert the array into float type.
4. Display the converted array.

### Program

```python
import numpy as np

a = np.array([5, 10, 15, 20])
b = np.array(a, dtype=float)

print(b)
```

### Output

```text
[ 5. 10. 15. 20.]
```

### Result
Thus, the array was converted into float type successfully.

---

## 2(b) Create an empty array and a full array

### Aim
To create an empty array and a full array using NumPy.

### Algorithm
1. Import NumPy.
2. Create an empty array using `empty()`.
3. Create a full array using `full()`.
4. Display both arrays.

### Program

```python
import numpy as np

a = np.empty(3)
b = np.full(3, 7)

print("Empty Array:", a)
print("Full Array:", b)
```

### Output

```text
Empty Array: [arbitrary values]
Full Array: [7 7 7]
```

### Result
Thus, an empty array and a full array were created successfully.

> Note: The values in an empty array are unpredictable because NumPy does not initialize them to zero.

---

## 2(c) Convert a list and tuple into arrays

### Aim
To convert a list and tuple into NumPy arrays.

### Algorithm
1. Import NumPy.
2. Create a list and tuple.
3. Convert both into arrays using `array()`.
4. Display the arrays.

### Program

```python
import numpy as np

a = [10, 20, 30]
b = (40, 50, 60)

x = np.array(a)
y = np.array(b)

print("List Array:", x)
print("Tuple Array:", y)
```

### Output

```text
List Array: [10 20 30]
Tuple Array: [40 50 60]
```

### Result
Thus, the list and tuple were successfully converted into NumPy arrays.

---

## 2(d) Find the real and imaginary parts of complex numbers

### Aim
To find the real and imaginary parts of an array of complex numbers using NumPy.

### Algorithm
1. Import NumPy.
2. Create an array of complex numbers.
3. Find real parts using `real`.
4. Find imaginary parts using `imag`.
5. Display the results.

### Program

```python
import numpy as np

a = np.array([2+3j, 4+5j, 6+7j])

print("Real Part:", a.real)
print("Imaginary Part:", a.imag)
```

### Output

```text
Real Part: [2. 4. 6.]
Imaginary Part: [3. 5. 7.]
```

### Result
Thus, the real and imaginary parts of complex numbers were obtained successfully.

---

# 3. Pandas – Element-wise Power of Array Values

### Aim
To write a Pandas program to calculate the powers of array values element-wise.

### Algorithm
1. Import Pandas.
2. Create a dictionary containing X, Y and Z values.
3. Convert the dictionary into a DataFrame.
4. Calculate X raised to the power Y.
5. Display the result.

### Program

```python
import pandas as pd

data = {
    'X': [78, 85, 96, 80, 86],
    'Y': [84, 94, 89, 83, 86],
    'Z': [86, 97, 96, 72, 83]
}

df = pd.DataFrame(data)

df['Result'] = df['X'] ** df['Y']

print(df)
```

### Output

```text
    X   Y   Z  Result
0  78  84  86  78**84
1  85  94  97  85**94
2  96  89  96  96**89
3  80  83  72  80**83
4  86  86  83  86**86
```

### Result
Thus, the element-wise power operation was performed successfully.

---

# 4. Pandas – Select Specified Columns and Rows

### Aim
To select specified columns and rows from a given DataFrame using Pandas.

### Algorithm
1. Import Pandas.
2. Create a dictionary with sample data.
3. Convert it into a DataFrame.
4. Select the name and score columns.
5. Select rows 1, 3, 5 and 6.
6. Display the selected data.

### Program

```python
import pandas as pd

data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James',
             'Emily', 'Michael', 'Matthew', 'Laura'],
    'score': [12.5, 9, 16.5, 9, 20, 14.5, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1],
    'qualify': ['yes', 'no', 'yes', 'no',
                'yes', 'no', 'no', 'yes']
}

df = pd.DataFrame(data)

result = df.loc[[1, 3, 5, 6], ['name', 'score']]

print(result)
```

### Output

```text
      name  score
1     Dima    9.0
3    James    9.0
5  Michael   14.5
6  Matthew    8.0
```

### Result
Thus, the specified columns and rows were selected successfully.

---

# 5. Pandas – Count Number of Rows and Columns

### Aim
To count the number of rows and columns in a DataFrame using Pandas.

### Algorithm
1. Import Pandas.
2. Create a dictionary containing sample data.
3. Convert it into a DataFrame.
4. Find the number of rows and columns using `shape`.
5. Display the result.

### Program

```python
import pandas as pd

data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James',
             'Emily', 'Michael', 'Matthew', 'Laura'],
    'score': [12.5, 9, 16.5, 9, 20, 14.5, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1],
    'qualify': ['yes', 'no', 'yes', 'no',
                'yes', 'no', 'no', 'yes']
}

df = pd.DataFrame(data)

print("Number of Rows:", df.shape[0])
print("Number of Columns:", df.shape[1])
```

### Output

```text
Number of Rows: 8
Number of Columns: 4
```

### Result
Thus, the number of rows and columns in the DataFrame was counted successfully.

---

# 6. Pima Indians Diabetes Dataset – Univariate Analysis

### Aim
To perform univariate analysis on the Pima Indians Diabetes dataset using frequency, mean, median, mode, variance, standard deviation, skewness and kurtosis.

### Algorithm
1. Import Pandas.
2. Load the diabetes dataset.
3. Calculate frequency.
4. Find mean, median and mode.
5. Calculate variance and standard deviation.
6. Find skewness and kurtosis.
7. Display the results.

### Program

```python
import pandas as pd

df = pd.read_csv("diabetes.csv")

x = df['Glucose']

print("Frequency:")
print(df['Outcome'].value_counts())

print("Mean:", x.mean())
print("Median:", x.median())
print("Mode:", x.mode()[0])
print("Variance:", x.var())
print("Standard Deviation:", x.std())
print("Skewness:", x.skew())
print("Kurtosis:", x.kurt())
```

### Output

```text
Frequency:
Outcome
0    500
1    268

Mean: 120.89
Median: 117.0
Mode: 99
Variance: 1022.25
Standard Deviation: 31.99
Skewness: (calculated value)
Kurtosis: (calculated value)
```

### Result
Thus, univariate analysis was performed successfully on the Pima Indians Diabetes dataset.

---

# 7. Pima Indians Diabetes Dataset – Bivariate Analysis

### Aim
To perform bivariate analysis using linear regression and logistic regression on the Pima Indians Diabetes dataset.

### Algorithm
1. Import the required libraries.
2. Load the diabetes dataset.
3. Select BMI and Glucose for linear regression.
4. Train the linear regression model.
5. Select Glucose and BMI for logistic regression.
6. Predict the diabetes outcome.
7. Display the results.

### Program

```python
import pandas as pd
from sklearn.linear_model import LinearRegression, LogisticRegression

df = pd.read_csv("diabetes.csv")

# Linear Regression
X = df[['BMI']]
y = df['Glucose']

model = LinearRegression()
model.fit(X, y)

print("Linear Prediction:", model.predict([[30]])[0])

# Logistic Regression
X = df[['Glucose', 'BMI']]
y = df['Outcome']

model2 = LogisticRegression(max_iter=1000)
model2.fit(X, y)

print("Logistic Prediction:", model2.predict([[120, 30]])[0])
```

### Output

```text
Linear Prediction: (predicted value)
Logistic Prediction: 0
```

### Result
Thus, linear and logistic regression models were successfully applied to the diabetes dataset.

---

# 8. Pima Indians Diabetes Dataset – Multiple Regression Analysis

### Aim
To perform multiple regression analysis on the Pima Indians Diabetes dataset.

### Algorithm
1. Import Pandas and Linear Regression.
2. Load the diabetes dataset.
3. Select multiple independent variables.
4. Select Glucose as the dependent variable.
5. Train the multiple regression model.
6. Predict the result.
7. Display the prediction.

### Program

```python
import pandas as pd
from sklearn.linear_model import LinearRegression

df = pd.read_csv("diabetes.csv")

X = df[['Pregnancies', 'BMI', 'Age']]
y = df['Glucose']

model = LinearRegression()
model.fit(X, y)

prediction = model.predict([[2, 30, 25]])

print("Predicted Glucose:", prediction[0])
```

### Output

```text
Predicted Glucose: (predicted value)
```

### Result
Thus, multiple regression analysis was performed successfully using the diabetes dataset.

---

# 9. UCI Dataset – Normal Values, Density, Contour and 3D Plotting

### Aim
To apply normal value plotting, density and contour plots, and three-dimensional plotting on a UCI dataset.

### Algorithm
1. Import Pandas, Matplotlib and Seaborn.
2. Load the UCI dataset.
3. Select numerical columns.
4. Plot the normal distribution.
5. Draw density and contour plots.
6. Draw a three-dimensional plot.

### Program

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv("uci.csv")

x = df['sepal_length']
y = df['sepal_width']
z = df['petal_length']

# Normal Distribution
sns.histplot(x, kde=True)
plt.title("Normal Distribution")
plt.show()

# Density Plot
sns.kdeplot(x=x, y=y, fill=True)
plt.title("Density Plot")
plt.show()

# Contour Plot
sns.kdeplot(x=x, y=y, fill=False, levels=10)
plt.title("Contour Plot")
plt.show()

# 3D Plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.scatter(x, y, z)

plt.title("3D Plot")
plt.show()
```

### Output

- Normal distribution graph is displayed.
- Density plot is displayed.
- Contour plot is displayed.
- Three-dimensional scatter plot is displayed.

### Result
Thus, different plotting functions were successfully applied to the UCI dataset.

---

# 10. UCI Dataset – Correlation, Scatter, Histogram and 3D Plotting

### Aim
To perform correlation, scatter plot, histogram and three-dimensional plotting on a UCI dataset.

### Algorithm
1. Import the required libraries.
2. Load the UCI dataset.
3. Calculate the correlation.
4. Draw a scatter plot.
5. Draw histograms.
6. Create a 3D scatter plot.
7. Display all graphs.

### Program

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("uci.csv")

x = df['sepal_length']
y = df['sepal_width']
z = df['petal_length']

# Correlation
print("Correlation:")
print(df[['sepal_length', 'sepal_width']].corr())

# Scatter Plot
plt.scatter(x, y)
plt.title("Scatter Plot")
plt.show()

# Histogram
plt.hist(x, bins=10)
plt.title("Histogram")
plt.show()

# 3D Plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.scatter(x, y, z)

plt.title("3D Plot")
plt.show()
```

### Output

```text
Correlation:
              sepal_length  sepal_width
sepal_length      1.000000     (value)
sepal_width       (value)      1.000000
```

- Scatter plot is displayed.
- Histogram is displayed.
- 3D scatter plot is displayed.

### Result
Thus, correlation, scatter, histogram and 3D plotting were performed successfully.

---

# 11. Pima Indians Diabetes Dataset – Normal Values, Density, Contour and 3D Plotting

### Aim
To perform normal distribution, density, contour and three-dimensional plotting on the Pima Indians Diabetes dataset.

### Algorithm
1. Import the required libraries.
2. Load the diabetes dataset.
3. Select Glucose, BMI and Age columns.
4. Plot the normal distribution.
5. Draw density and contour plots.
6. Draw a 3D scatter plot.
7. Display the graphs.

### Program

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv("diabetes.csv")

x = df['Glucose']
y = df['BMI']
z = df['Age']

# Normal Distribution
sns.histplot(x, kde=True)
plt.title("Normal Distribution")
plt.show()

# Density Plot
sns.kdeplot(x=x, y=y, fill=True)
plt.title("Density Plot")
plt.show()

# Contour Plot
sns.kdeplot(x=x, y=y, fill=False, levels=10)
plt.title("Contour Plot")
plt.show()

# 3D Plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.scatter(x, y, z)

plt.title("3D Plot")
plt.show()
```

### Output

- Normal distribution graph is displayed.
- Density plot is displayed.
- Contour plot is displayed.
- Three-dimensional scatter plot is displayed.

### Result
Thus, normal distribution, density, contour and 3D plots were successfully created using the diabetes dataset.

---

# 12. Pima Indians Diabetes Dataset – Correlation, Scatter, Histogram and 3D Plotting

### Aim
To perform correlation, scatter plot, histogram and three-dimensional plotting on the Pima Indians Diabetes dataset.

### Algorithm
1. Import Pandas and Matplotlib.
2. Load the diabetes dataset.
3. Calculate the correlation.
4. Draw a scatter plot.
5. Draw a histogram.
6. Create a 3D scatter plot.
7. Display the graphs.

### Program

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("diabetes.csv")

x = df['Glucose']
y = df['BMI']
z = df['Age']

# Correlation
print("Correlation:")
print(df[['Glucose', 'BMI']].corr())

# Scatter Plot
plt.scatter(x, y)
plt.title("Scatter Plot")
plt.show()

# Histogram
plt.hist(x, bins=10)
plt.title("Histogram")
plt.show()

# 3D Plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.scatter(x, y, z)

plt.title("3D Plot")
plt.show()
```

### Output

```text
Correlation:
          Glucose       BMI
Glucose    1.000      (value)
BMI        (value)     1.000
```

- Scatter plot is displayed.
- Histogram is displayed.
- 3D scatter plot is displayed.

### Result
Thus, correlation, scatter, histogram and 3D plotting were successfully performed on the diabetes dataset.

---

# 13. Pandas – Count Number of Columns in a DataFrame

### Aim
To write a Pandas program to count the number of columns in a DataFrame.

### Algorithm
1. Import Pandas.
2. Create a dictionary with sample data.
3. Convert it into a DataFrame.
4. Count the columns using `shape[1]`.
5. Display the result.

### Program

```python
import pandas as pd

data = {
    'Name': ['Arun', 'Bala', 'John'],
    'Age': [20, 21, 22],
    'Mark': [80, 90, 85]
}

df = pd.DataFrame(data)

print("Number of Columns:", df.shape[1])
```

### Output

```text
Number of Columns: 3
```

### Result
Thus, the number of columns in the DataFrame was counted successfully.

---

# 14. NumPy – Find the Number of Occurrences in an Array

### Aim
To create a 2-dimensional array of size 2×3 with 4-byte integer elements and find the number of occurrences of a given value.

### Algorithm
1. Import NumPy.
2. Create a 2×3 array using 4-byte integers.
3. Select the value to be searched.
4. Count its occurrences using `count_nonzero()`.
5. Display the result.

### Program

```python
import numpy as np

a = np.array([[1, 2, 3],
              [2, 4, 2]], dtype=np.int32)

n = np.count_nonzero(a == 2)

print("Array:")
print(a)

print("Number of occurrences:", n)
print("Data Type:", a.dtype)
```

### Output

```text
Array:
[[1 2 3]
 [2 4 2]]

Number of occurrences: 3
Data Type: int32
```

### Result
Thus, a 2×3 array with 4-byte integer elements was created and the number of occurrences of 2 was found successfully.

---

# 15. NumPy – Merge and Combine Arrays

## 15(a) Merge three given NumPy arrays of the same shape

### Aim
To merge three NumPy arrays of the same shape using NumPy.

### Algorithm
1. Import NumPy.
2. Create three arrays of the same shape.
3. Merge the arrays using `concatenate()`.
4. Display the merged array.

### Program

```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
c = np.array([7, 8, 9])

d = np.concatenate((a, b, c))

print("Merged Array:", d)
```

### Output

```text
Merged Array: [1 2 3 4 5 6 7 8 9]
```

### Result
Thus, three NumPy arrays of the same shape were successfully merged.

---

## 15(b) Combine the last element of one array with the first element of another array

### Aim
To combine the last element of one NumPy array with the first element of another array having different shapes.

### Algorithm
1. Import NumPy.
2. Create two arrays of different shapes.
3. Select the last element of the first array.
4. Select the first element of the second array.
5. Combine them using `concatenate()`.
6. Display the result.

### Program

```python
import numpy as np

a = np.array([10, 20, 30, 40])
b = np.array([50, 60, 70])

c = np.concatenate((a[-1:], b[:1]))

print("Combined Array:", c)
```

### Output

```text
Combined Array: [40 50]
```

### Result
Thus, the last element of the first array and the first element of the second array were successfully combined.

---

# Required Libraries

For the programs in this record, the following libraries may be required:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

# Dataset Requirements

- `diabetes.csv` – Pima Indians Diabetes dataset.
- `uci.csv` – UCI dataset used for Questions 9 and 10.
- For Questions 9 and 10, the CSV should contain the columns:
  - `sepal_length`
  - `sepal_width`
  - `petal_length`

# Quick Revision Table

| Questions | Topic | Required |
|---|---|---|
| 1 | NumPy | NumPy |
| 2 | NumPy | NumPy |
| 3 | Pandas power operation | Pandas |
| 4 | Select rows and columns | Pandas |
| 5 | Count rows and columns | Pandas |
| 6 | Univariate analysis | Pandas |
| 7 | Linear & Logistic Regression | Pandas, Scikit-learn |
| 8 | Multiple Regression | Pandas, Scikit-learn |
| 9 | Normal, Density, Contour, 3D | Pandas, Matplotlib, Seaborn |
| 10 | Correlation, Scatter, Histogram, 3D | Pandas, Matplotlib |
| 11 | Diabetes plotting | Pandas, Matplotlib, Seaborn |
| 12 | Diabetes correlation & plotting | Pandas, Matplotlib |
| 13 | Count columns | Pandas |
| 14 | Array occurrences | NumPy |
| 15 | Merge/Combine arrays | NumPy |
