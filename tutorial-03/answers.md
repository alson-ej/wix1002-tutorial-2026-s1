# **Tutorial 3: *Flow of Control (Selection)***
# 24226197 Liang Wen Je

### ✦Question 1  
Write statements for each of the following

#### a. Determine whether $3\times8=27$
```java
if (3 * 8 == 27) {
    System.out.println("3 * 8 is equal to 27");
} else {
    System.out.println("3 * 8 is not equal to 27");
}
```

#### b. Determine whether an input integer is an odd number or even number.
```java
if (num % 2 == 0) {
    System.out.println("Even number");
} else {
    System.out.println("Odd number");
}
```

#### c. Determine whether a character is a capital letter.
```java
if (ch >= 'A' && ch <= 'Z') {
    System.out.println("Capital letter");
}
```

#### d. Display two strings in alphabetical order ignoring their case.
```java
if (s1.compareToIgnoreCase(s2) <= 0) {
    System.out.println(s1 + ", " + s2);
} else {
    System.out.println(s2 + ", " + s1);
}
```

#### e. A switch statement that display Sunday, Monday, .., Satudary if the input is 0, 1, ..., 6.
```java
switch (day) {
    case 0:
        System.out.println("Sunday");
        break;
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break;
    case 4:
        System.out.println("Thursday");
        break;
    case 5:
        System.out.println("Friday");
        break;
    case 6:
        System.out.println("Saturday");
        break;
    default:
        System.out.println("Invalid input");
        break;
}
```

### ✦Question 2  
Correct the error for the following statements.

#### a.  
```text
Question
    if (num1=num2)
    System.out.println("Number 1 is equal to number 2.");
```
```java
Answer
    if (num1 == num2)
        System.out.println("Number 1 is equal to number 2.");
```

#### b.  
```text
Question
    if (x>y>z)
    System.out.println("x is the largest number");
```
```java
Answer
    if (x > y && x > z)
        System.out.println("x is the largest number");
```

#### c.  
```text
Question
    String s1, s2;
    if (s1--s2)
    System.out.println("They are equal strings.");
    else (s1!=s2)
    System.out.println("They are not equal strings.");
```
```java
Answer
    String s1, s2;
    if (s1.equals(s2))
        System.out.println("They are equal strings.");
    else
        System.out.println("They are not equal strings.");
```

#### d.  
```text
Question
    if x>0 or y>0
    System.out.println("Either x or y is positive");
```
```java
Answer
    if (x > 0 || y > 0)
        System.out.println("Either x or y is positive");
```

### ✦Question 3  
Write the output for the following statements when $x=9$ and $y=10$

#### a.  
```text
Question
    if (x<10)
    if (y>10)
    System.out.println("*****");
    else
    System.out.println("#####");
    System.out.println("$$$$$");
```
```text
Output
#####
$$$$$
```

#### b.  
```text
Question
    if (x<10) {
    if (y<10)
    System.out.println("*****");
    else {
    System.out.println("#####");
    System.out.println("$$$$$");
    }}
```
```text
Output
#####
$$$$$
```

#### c.  
```text
Question
    if (x<10) {
    if (y<10)
    System.out.println("*****");
    System.out.println("#####");
    }
    else {
    System.out.println("$$$$$");
    }
```
```text
Output
#####
```

#### d.  
```text
Question
    if (x>10) {
    if (y>10) {
    System.out.println("*****");
    System.out.println("#####"); }
    else
    System.out.println("$$$$$");
    }
```
```text
Output
(No output)
```

### ✦Question 4  
Write the java statements that used the if statement to find the biggest number among three given integers.

```java
int a, b, c;
int max;

if (a >= b && a >= c) {
    max = a;
} else if (b >= a && b >= c) {
    max = b;
} else {
    max = c;
}

System.out.println("The biggest number is: " + max);
```

### ✦Question 5  
Write the java statements that determine whether the Leap year. A Leap year is divisible by 4 but not by 100. However, a Leap year is also divisible by 400.

```java
int year;
boolean isLeapYear;

if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
    isLeapYear = true;
} else {
    isLeapYear = false;
}

if (isLeapYear) {
    System.out.println(year + " is a leap year.");
} else {
    System.out.println(year + " is not a leap year.");
}
```