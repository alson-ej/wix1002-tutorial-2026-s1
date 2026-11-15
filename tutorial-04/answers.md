# **Tutorial 4: *Flow of Control (Repetition)***
# 24226197 Liang Wen Je

### ✦Question 1  
Write statements for each of the following

#### a. Find the largest integer n so that $n^{3}$ is less than 2000.
```java
int n = 1;
while (Math.pow(n, 3) < 2000) {
    n++;
}
n--;
System.out.println("The largest integer n is: " + n);
```

#### b. Display the square number of the first twelve integers starting from 1.
```java
for (int i = 1; i <= 12; i++) {
    System.out.println(i * i);
}
```

#### c. Display a 4-by-5 matrix using random number within 0 to 100.
```java
for (int i = 0; i < 4; i++) {
    for (int j = 0; j < 5; j++) {
        System.out.print((int)(Math.random() * 101) + " ");
    }
    System.out.println();
}
```

#### d. Compute the sum of numbers from 1 to a given number.
```java
int sum = 0;
int givenNumber = 50; 
for (int i = 1; i <= givenNumber; i++) {
    sum += i;
}
System.out.println("Sum: " + sum);
```

#### e. Compute the sum of the series: 1/25+2/24+3/23 ... +25/1 in two decimal places.
```java
double sum = 0;
for (int i = 1, j = 25; i <= 25; i++, j--) {
    sum += (double) i / j;
}
System.out.printf("Sum: %.2f\n", sum);
```

### ✦Question 2  
Correct the error for the following statements.

#### a.  
```text
Question
    for (x=10;x>0;x++)
    sum +=X;
```
```java
Answer
    for (int x = 10; x > 0; x--)
        sum += x;
```

#### b.  
```text
Question
    do
    x+=2
    y+=x;
    System.out.println(x + " and " + y);
    while (x<100)
```
```java
Answer
    do {
        x += 2;
        y += x;
        System.out.println(x + " and " + y);
    } while (x < 100);
```

#### c.  
```text
Question
    for ( x==1, y==20; x < y, x++, y-=2);
    System.out.println(x & " " & y);
```
```java
Answer
    for (int x = 1, y = 20; x < y; x++, y -= 2) {
        System.out.println(x + " " + y);
    }
```

#### d.  
```text
Question
    i=1
    while(i<10) {
    if (i=-10)
    System.out.println("Program End");
    }
```
```java
Answer
    int i = 1;
    while (i < 10) {
        if (i == 10)
            System.out.println("Program End");
        i++;
    }
```

### ✦Question 3  
Write the statements that display the first ten values of the Fibonacci sequence. Given the formula $f_{1}=1$, $f_{2}=1$, $f_{n}=f_{n-1}+f_{n-2}$

```java
int f1 = 1, f2 = 1;
System.out.print(f1 + ", " + f2);
for (int i = 3; i <= 10; i++) {
    int fn = f1 + f2;
    System.out.print(", " + fn);
    f1 = f2;
    f2 = fn;
}
System.out.println();
```

### ✦Question 4  
Write the statements that display the string in reverse order. (use String.length() to get the length of the string)

```java
String str = "Universiti Malaya";
for (int i = str.length() - 1; i >= 0; i--) {
    System.out.print(str.charAt(i));
}
System.out.println();
```