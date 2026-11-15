# **Tutorial 6: *Java Methods***
# 24226197 Liang Wen Je

### ✦Question 1  
Write statements for each of the following

#### a. Define a static method that returns the maximum number from 3 integer parameters.
```java
public static int getMax(int a, int b, int c) {
    int max = a;
    if (b > max) max = b;
    if (c > max) max = c;
    return max;
}
```

#### b. Define a static method that determine whether the given integer is a square number.
```java
public static boolean isSquare(int num) {
    if (num < 0) return false;
    int root = (int) Math.sqrt(num);
    return root * root == num;
}
```

#### c. Define a static method that use to compute combination function $C(n,k)$. $C(n,k)=n!/(k!(n-k)!)$
```java
public static long combination(int n, int k) {
    if (k < 0 || k > n) return 0;
    return factorial(n) / (factorial(k) * factorial(n - k));
}

public static long factorial(int num) {
    long fact = 1;
    for (int i = 2; i <= num; i++) {
        fact *= i;
    }
    return fact;
}
```

#### d. Define a static method that used to determine whether the parameter is a pentagonal number. $P_n=\frac{1}{2}n(3n-1)$
```java
public static boolean isPentagonal(int num) {
    if (num <= 0) return false;
    int n = 1;
    int p = 0;
    while (p < num) {
        p = n * (3 * n - 1) / 2;
        if (p == num) return true;
        n++;
    }
    return false;
}
```

#### e. Define a static method that displays the number of letters and the number of digits of a String parameter.
```java
public static void countLettersAndDigits(String str) {
    int letters = 0, digits = 0;
    for (int i = 0; i < str.length(); i++) {
        char ch = str.charAt(i);
        if (Character.isLetter(ch)) {
            letters++;
        } else if (Character.isDigit(ch)) {
            digits++;
        }
    }
    System.out.println("Number of letters: " + letters);
    System.out.println("Number of digits: " + digits);
}
```

#### f. Define a static void method that generates 10 random numbers within 0 to 100 to the method's parameter. The random numbers can be accessed by the main method.
```java
public static void generateRandomNumbers(int[] numbers) {
    for (int i = 0; i < 10 && i < numbers.length; i++) {
        numbers[i] = (int) (Math.random() * 101);
    }
}
```

#### g. Define a static void method that returns the area and the circumference of a circle given the argument is radius. $Area=\pi r^{2}$ and $Circumference=2\pi r$.
```java
public static void calculateCircle(double radius, double[] results) {
    results[0] = Math.PI * radius * radius; // Area
    results[1] = 2 * Math.PI * radius;      // Circumference
}
```

#### h. Define a static method that generate random number within $0-10$. The method will return the first random number that generate twice.
```java
public static int firstDuplicateRandom() {
    boolean[] seen = new boolean[11];
    while (true) {
        int rand = (int) (Math.random() * 11);
        if (seen[rand]) {
            return rand;
        }
        seen[rand] = true;
    }
}
```

### ✦Question 2  
Write a program that consists of a method that can display three numbers in decreasing order.

```java
import java.util.Scanner;

public class DecreasingOrder {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter three numbers: ");
        double n1 = scanner.nextDouble();
        double n2 = scanner.nextDouble();
        double n3 = scanner.nextDouble();
        
        displayDecreasingOrder(n1, n2, n3);
    }

    public static void displayDecreasingOrder(double a, double b, double c) {
        double temp;
        if (a < b) { temp = a; a = b; b = temp; }
        if (a < c) { temp = a; a = c; c = temp; }
        if (b < c) { temp = b; b = c; c = temp; }
        
        System.out.println("Numbers in decreasing order: " + a + ", " + b + ", " + c);
    }
}
```
