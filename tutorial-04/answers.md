# WIX1002 Tutorial 4
#### Name: Ainul Afiqah binti Shuhazmir
#### Matrics No.: 25000924


## Question 1 : Write statements for each of the following. 
#### (a) Find the largest integer n so that n³ is less than 2000.
``` java
    public static void main(String[] args) {
        int num = 0;
        while ((num + 1)*(num + 1)*(num + 1)< 2000){
            num++;
        }
        System.out.println("Largest integer n so that n³ is less than 2000 is " + num);
    }
```
#### (b) Display the square number of the first twelve integers starting from 1.
``` java
   public static void main(String[] args) {
        for (int i = 1 ; i <= 12; i++){
            System.out.println(i + " squared equals " + (i*i));
        }
    }
```
#### (c) Display a 4-by-5 matrix using random number within 0 to 100.
``` java
   public static void main(String[] args) {
        Random rand = new Random(); //import java.util.Random;
        for (int row = 1; row <= 4; row++){
            for (int col =1; col <= 5; col++){
                System.out.printf("%5d", rand.nextInt(101));
            } System.out.println("");
        }
    }
```
#### (d) Compute the sum of numbers from 1 to a given number. 
``` java
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in); //import java.util.Scanner;
        
        System.out.print("Enter an integer: ");
        int n = sc.nextInt();
        
        int sum = 0;
        
        for (int i = 1; i <= n; i++){
            sum += i;
        }
        
        System.out.println("Sum of numbers from 1 to " + n + " is " + sum);
    }
```
#### (e) Compute the sum of the series: 1/25+2/24+3/23 … + 25/1 in two decimal places.
``` java
    public static void main(String[] args) {
        double sum = 0;
        
        for (int i = 1; i <= 25; i++){
            sum += (double) i / (26-i);
        }
        
        System.out.printf("Sum = %.2f%n", sum);
    }
```

## Question 2 : Correct the error for the following statements.

#### (a)
##### Corrected code:
``` java
for (x = 10; x > 0; x--) // Placing x++ will make the loop go on forever.
sum += x;
```
#### (b)
##### Corrected code:
``` java
int x = 0, y = 0; //Initialize x and y values.
do{ // Put curly brackets to ensure all steps gets executed.
 x += 2;
 y += x;
 System.out.println(x + " and " + y);
}while (x < 100); //Need to put semicolon for do-while loop.
```
#### (c)
##### Corrected code: 
``` java
for (int x=1, y=20; x < y; x++, y-=2) //Declare x and y as integers. No semicolon after for loop.
 System.out.println(x + " " + y); //& is not string concatenation.
```
#### (d)
##### Corrected code:
``` java
int i = 1; //Declare datatype for variable i
while(i<10) {
 if (i==10)
   System.out.println("Program End");
 i++; // Put increment for i
}

```

## Question 3 : Write the statements that display the first ten values of the Fibonacci sequence. Given the formula f₁ = 1, f₂ =1, fₙ = fₙ₋₁ + fₙ₋₂.
``` java
public static void main(String[] args) {
      int prev = 1, cont = 1;
      
      System.out.print(prev + ", " + cont);
        
      for (int n = 3; n <= 10; n++){
          int next = prev + cont;
          System.out.print( ", " + next);
          prev = cont;
          cont = next;
      }
        System.out.println("");
    }
```

## Question 4 : Write the statements that display the string in reverse order. (use String.length() to get the length of the string)
``` java
public static void main(String[] args) {
      Scanner sc = new Scanner(System.in); //import java.util.Scanner;
      
      System.out.print("Enter a string: ");
      String str = sc.nextLine();
      
      String reversed = "";
      for (int i = str.length()-1; i >= 0; i--){
          reversed += str.charAt(i);
      }
        System.out.println("Reverse: " + reversed);
    }
```
