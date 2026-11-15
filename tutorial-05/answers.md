# **Tutorial 5: *Arrays***
# 24226197 Liang Wen Je

### ✦Question 1  
Write statements for each of the following

#### a. Declare an array that used to store 12 floating point numbers.
```java
double[] numbers = new double[12];
```

#### b. Initialize an array that used to store the value of A to E.
```java
char[] letters = {'A', 'B', 'C', 'D', 'E'};
```

#### c. Declare an array that used to store 100 students name.
```java
String[] studentNames = new String[100];
```

#### d. Declare an array for a table with 6 rows 2 columns that used to store integer value.
```java
int[][] table = new int[6][2];
```

#### e. Initialize an array with the following value: $\begin{pmatrix}6&9\\ 2&5\\ 4&6\end{pmatrix}$
```java
int[][] matrix = {
    {6, 9},
    {2, 5},
    {4, 6}
};
```

#### f. After initialize the array, modify the value of the above array to $\begin{pmatrix}6&9\\ 2&4\\ 3&7\end{pmatrix}$
```java
matrix[1][1] = 4;
matrix[2][0] = 3;
matrix[2][1] = 7;
```

#### g. Display all the values of an array name contact in separate lines.
```java
for (int i = 0; i < contact.length; i++) {
    System.out.println(contact[i]);
}
```

### ✦Question 2  
Correct the error for the following statements.

#### a.  
```text
Question
    String[] code = {'AAA', 'AAB', 'AAC', 'AAD'};
```
```java
Answer
    String[] code = {"AAA", "AAB", "AAC", "AAD"};
```

#### b.  
```text
Question
    int[]num=new num[10];
    for(int k=0; k <=num.length();k++)
    sum+=num;
```
```java
Answer
    int[] num = new int[10];
    for (int k = 0; k < num.length; k++)
        sum += num[k];
```

#### c.  
```text
Question
    int [][]t=new int[3][];
    t[1][2]=5;
```
```java
Answer
    int[][] t = new int[3][3];
    t[1][2] = 5;
```

#### d.  
```text
Question
    int i=4;
    int []score=new int[5];
    score [1]=78;
    score[++i]=100;
```
```java
Answer
    int i = 4;
    int[] score = new int[5];
    score[1] = 78;
    score[i] = 100;
```

### ✦Question 3  
Determine the values of each element of array `marks`. Assume the array was declared as:
```java
int[] marks = new int[5];
int i = 0, j = 1;
marks[i] = 12;
marks[j] = marks[i] + 19;
marks[j - 1] = marks[j] * marks[j];
marks[j * 3] = marks[i + 1];
marks[++j] = marks[i] % 5;
marks[2 * j] = marks[j - 1];
```

**Trace & Final Values:**
* `marks[0]` = **961** 
* `marks[1]` = **31** 
* `marks[2]` = **1** 
* `marks[3]` = **31** 
* `marks[4]` = **31** 

### ✦Question 4  
Write the statements that display the number of occurrence of the word "the" (case sensitive) in a string array name `sentence`.

```java
int count = 0;
for (String str : sentence) {
    String[] words = str.split(" ");
    for (String word : words) {
        if (word.equals("the")) {
            count++;
        }
    }
}
System.out.println("Number of occurrences of \"the\": " + count);