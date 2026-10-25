# WIX1002 Tutorial 3
#### Name: Ainul Afiqah binti Shuhazmir
#### Matrics No.: 25000924


## Question 1 
#### (a)
``` java
    public static void main(String[] args) {
        boolean isEqual = 3*8 == 27;
        System.out.println("3*8 == 27 is "+ isEqual);
    }
```
#### (b)
``` java
   public static void main(String[] args) {
        Scanner sc = new Scanner(System.in); // imported java.util.Scanner before using
        
        System.out.print("Enter an integer: ");
        int num = sc.nextInt();
        
        if (num%2 == 0){
            System.out.println(num + " is an even number.");
        } else {
            System.out.println(num + " is an odd number.");
        }
    }
```
#### (c)
``` java
   public static void main(String[] args) {
        Scanner sc = new Scanner(System.in); //imported java.util.Scanner before using
        
        System.out.print("Enter a letter: ");
        char letter = sc.next().charAt(0);
        
        if (letter >= 'A' && letter <= 'Z'){
            System.out.println(letter + " is a capital letter.");
        } else {
            System.out.println(letter + " is not a capital letter.");
        }
    }
```
#### (d)
``` java
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in); //imported java.util.Scanner before using
        
        System.out.print("Enter your first string: ");
        String s1 = sc.next();
        System.out.print("Enter your second string: ");
        String s2 = sc.next();
        
        if (s1.compareToIgnoreCase(s2) <= 0){
            System.out.println(s1 + " " + s2);
        } else {
            System.out.println(s2 + " " + s1);
        }

    }
```
#### (e)
``` java
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in); //imported java.util.Scanner before using
        
        System.out.print("Enter a number (0-6): ");
        int day = sc.nextInt();
        
        switch (day){
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
                System.out.println("Invalid number. Please try again.");
                break;
        }

    }
```

## Question 2

#### (a)
##### Incorrect code:
##### Corrected code:
``` java
if (num1 == num2) // Correction: Use "==" for comparison.
System.out.println("Number 1 is equal to number 2.");
```
#### (b)
##### Corrected code:
``` java
if (x > y && x > z) // Error: if statements cannot compare a boolean value (true/false) to a number.
 System.out.println("x is the largest number.");
```
#### (c)
##### Corrected code: 
``` java
String s1 = "Apple", s2 = "Android"; // Error: Strings are not initialized.
if (s1.equals(s2))  // Error: "==" are used to compare references. To compare between strings, .equals() is used instead.
 System.out.println("They are equal strings.");
else // Error: "else" does not need a condition statement.
 System.out.println("They are not equal strings.");
```
#### (d)
##### Corrected code:
``` java
if (x > 0 || y > 0) // Correction: Place the conditions in a bracket, and use "||" in place of "or". No need to put a semicolon after "if".
 System.out.println("Either x or y is positive");
```

## Question 3

#### (a) Output:
```
#####
$$$$$
```
#### (b) Output:
```
#####
$$$$$
```
#### (c) Output:
```
#####
```
#### (d) Output:
```
 
```

## Question 4
``` java
import java.util.Scanner;

public class LargestofThree {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.print("Enter the value of a: ");
        int a = sc.nextInt();
        System.out.print("Enter the value of b: ");
        int b = sc.nextInt();
        System.out.print("Enter the value of c: ");
        int c = sc.nextInt();
        
        int largest = a;
        
        if (b > largest)
            largest = b;
        if (c > largest)
            largest = c;
        
        System.out.println("The biggest number is " + largest);
    }
}
```

## Question 5
``` java
import java.util.Scanner;

public class LeapYearFinder {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.print("Enter a year: ");
        int year = sc.nextInt();
        
        boolean isLeapYear = year % 400 == 0 || (year % 4 == 0 && year % 100 != 0);
        
        if (isLeapYear)
            System.out.println(year + " is a leap year.");
        else
            System.out.println(year + " is not a leap year.");
        
    }
    
}
```
