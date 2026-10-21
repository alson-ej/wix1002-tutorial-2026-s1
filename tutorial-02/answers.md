# **Tutorial 2: *Java Fundamental***
# 24226197 Liang Wen Je
## Java Coding  
### ✦Question 1  
Display the sentence Faculty of Computer Science and Information Technology.  
#### a. In one line using multiple Java statements
```java
    System.out.print("Faculty of Computer Science ");
    System.out.println("and Information Technology");
```
#### b. In multiple lines using one Java statement
```java
    System.out.println("Faculty of\nComputer Science\nand Information Technology");
```

### ✦Question 2  
Write a Java statement that print "SDN" - Software-defined networking.
```java
    System.out.println("\"SDN\" - Software-defined networking");
```

### ✦Question 3  
Correct the error for the following statements.

#### a. System.Println("Java Programming");  
    System.out.println("Java Programming");  
#### b. System.in.println("Introduction to Java!")  
    System.out.println("Introduction to Java!");  
#### c. System.out.println("\t is the horizontal tab character");  
    System.out.println("\\t is the horizontal tab character");  
#### d. system.out.println("Java is case sensitive!" );  
    System.out.println("Java is case sensitive!");  

### ✦Question 4  
Write statements for each of the following  
#### a. Declare a variable that used to store the value of a matric number.
```java
String matricNumber;
```
#### b. Declare a variable that used to store the value of π.
```java
double pi;
```
#### c. Initialize a variable named M with the value set to false.
```java
boolean M = false;
```
#### d. Initialize a variable named P with the value set to 8800000000.
```java
long P = 8800000000L;
```
#### e. Initialize a variable named letter with the value set to U.
```java 
char letter = 'U';
```
#### f. Declare a constant variable named PRO. The value of the constant variable is Java. 
```java
final String PRO = "Java";
```

### ✦Question 5
Correct the error for the following statements.  
#### a.  
```text
Question
    final double AMOUNT = "32.5";  
    AMOUNT += 10;  
    System.out.println("The amount is " + AMOUNT);  
```
```java
Answer
    double amount = 32.5;
    amount += 10;
    System.out.println("The amount is " + amount);
```
#### b.
```text 
Question
    string chapter = 'Summary';
    System.out.println(chapter);
```
```java
Answer
    String chapter = "Summary";
    System.out.println(chapter);
```
#### c.
```text
Question
    int num;
    ++num++;
    num1 = num;
```
```java
Answer
    int num = 0, num1;
    num++;
    num1 = num;
```

```
d.
```text
Question
    int num = 3000;
    System.out.printf("%4.2f\n", num);
```
```java
Answer
    int num = 3000;
    System.out.printf("%d\n", num);
```
e.
```text
Question
    String contact;
    Scanner keyboard = new Scanner(System.out);
    contact = keyboard.nextLine();
```
```java
Answer
import java.util.Scanner;
    String contact;
    Scanner keyboard = new Scanner(System.in);
    contact = keyboard.nextLine();
```

### ✦Question 6
Write a java program that print the circumference of a circle. The input of the program is diameter. Display the result in three decimal places. (Note pi = Math.PI)

```java
import java.util.Scanner;

public class Question6 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter diameter: ");
        double diameter = scanner.nextDouble();

        double circumference = Math.PI * diameter;

        System.out.printf("The circumference of the circle is : %.3f\n", circumference);

        scanner.close();
    }

}
```

### ✦Question 7
Write a java program that converts inches to meters. (Given 1 inch equals to 2.54 centimeters). Print the output in two decimal places.

```java 
import java.util.Scanner;

public class Question7 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter value in inch: ");
        double inches = scanner.nextDouble();
        
        double meters = inches * 2.54 / 100;

        System.out.printf("%.2f inches = %.2f meters", inches, meters);

        scanner.close();
    }
}
```