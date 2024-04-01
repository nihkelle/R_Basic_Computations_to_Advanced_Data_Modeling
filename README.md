# 🖥️ R | Basic Computations to Advanced Data Modeling | Comprehensive Data Analysis Techniques

## Description
- This project involves data manipulation and analysis tasks using R programming. It covers a range of topics including vector operations, categorical data handling, data frame manipulation, and matrix operations. These codes represent typical operations encountered in data analysis workflows, from basic vector operations to more advanced statistical computations and matrix manipulations. The project aims to improve proficiency in R programming for data analysis tasks, covering fundamental concepts and practical applications.

## 💻 Vector Operations and Summation

<b> Code Overview: </b>
- This code performs operations on two vectors (`v1` and `v2`), handles warnings, creates a new vector `v3`, calculates the sum of specific elements in v4, renames elements in `v5`, and computes the sum of `v5`.

```r
v1 <- 1:5
v2 <- c(2, 4, 6, 8)
# v1 + v2: Warning message that stated longer object length is not a multiple of shorter object length. 
v3 <- c(v2, 10)
v4 <- v1 + v3
print(v4)
v5 <- v4[-c(1, length(v4))]
print(v5)
names(v5) <- c("First:", "Second:", "Third:")
print(v5)
SumResults <- sum(v5)
print(SumResults)
```

<b> Skills Devloped - </b>

Vector Operations: 
- Demonstrates performing arithmetic operations on vectors, combining elements, and handling warnings arising from vector lengths.
  
Indexing and Slicing:
- Utilizes indexing and slicing operations to manipulate vectors and extract specific elements.
  
Data Summation: 
- Calculates the sum of elements in a vector, a fundamental operation in data analysis.

## 📊 Handling Categorical Data

<b> Code Overview: </b>
- This code deals with categorical data, creates a factor variable `RatingFactor` with specified levels, computes minimum and maximum values, converts factors to integers, and generates dummy variables.

```r
RatingLevels <- c("Poor", "Medium", "Great")
RatingData <- c("Great", "Great", "Medium", "Great", "Medium")
RatingFactor <- factor(RatingData, levels = RatingLevels, ordered = TRUE)
print("min(RatingFactor):")
print(min(RatingFactor))
print("max(RatingFactor):")
print(max(RatingFactor))
print("as.integer(RatingFactor):")
print(as.integer(RatingFactor))
DummyVariables <- model.matrix(~ RatingFactor - 1)
print("Dummy Variables:")
print(DummyVariables)
```

<b> Skills Devloped - </b>

Categorical Data Handling: 
- Demonstrates creating factors, specifying levels, and understanding ordered factors in R.
  
Statistical Analysis: 
- Calculates summary statistics like minimum, maximum, and converts factors to integers.
  
Model Matrix Generation: 
- Constructs dummy variables from categorical data, useful in statistical modeling.

## 🧮 Working with Data Frames

<b> Code Overview: </b>
- This code constructs a data frame `TemperatureDF` from vectors, assigns row names, calculates statistics (standard deviation and mean), corrects specific values, and extracts subsets of data.

```r
HighTemp <- c(75, 78, 72, 77, 80)
LowTemp <- c(63, 59, 60, 63, 65)
DayOfWeek <- c("Monday", "Tuesday", "Wednesday", "Thursday", "Friday")
TemperatureDF <- data.frame(High = HighTemp, Low = LowTemp)
rownames(TemperatureDF) <- DayOfWeek
print("TemperatureDF:")
print(TemperatureDF)
highSD <- sd(TemperatureDF$High)
print("Standard Deviation of High Temperature:")
print(highSD)
lowM <- mean(TemperatureDF$Low)
print("Average of Low Temperature:")
print(lowM)
TemperatureDF["Monday", "High"] <- 76
TemperatureDF["Friday", "Low"] <- 60
print("Corrected TemperatureDF:")
print(TemperatureDF)
print("Tuesday and Thursday Rows:")
print(TemperatureDF[c("Tuesday", "Thursday"), ])
```

<b> Skills Devloped - </b>

Data Frame Manipulation: 
- Creates and manipulates data frames, assigns row names, and accesses specific elements.
  
Statistical Analysis: 
- Computes basic statistics such as standard deviation and mean from data frames.
  
Data Correction and Subset Selection: 
- Demonstrates correcting data errors and extracting subsets of data based on specific criteria.

## 🕸️ Matrix Operations


<b> Code Overview: </b>
-  This code performs matrix operations, creating two matrices (`Mat1` and `Mat2`), multiplies them, and prints the result.

```r
MatrixData1 <- 6:1
MatrixData2 <- 1:9
Mat1 <- matrix(MatrixData1, nrow = 2, ncol = 3, byrow = TRUE)
Mat2 <- matrix(MatrixData2, nrow = 3, ncol = 3, byrow = FALSE)
MatMul <- Mat1 %*% Mat2
print("Matrix Multiplication Result (MatMul):")
print(MatMul)
```

<b> Skills Devloped - </b>

Matrix Operations: 
- Demonstrates matrix creation, multiplication, and handling in R, essential for numerical computations.
  
Linear Algebra: 
- Applies matrix multiplication, a fundamental operation in linear algebra, useful in various mathematical and statistical analyses.
