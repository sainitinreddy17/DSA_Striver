# Java Basics

★ ☆
☆ Java is a high-level, class-bawsed, object-oriented programming language that is designed to have as few implementation dependencies as possible.

☆ It is a general purpose programming language intended to let application developers <mark> Write Once - Run Anywhere (WORA) </mark> meaning that compiled java code can run on all platforms that support java without the need of re-compilation.

## Sample Code

```Java
public class main{
    public static void main(String[] args){
        System.out.println("Hello, World!");
    }
}
```

## Understanding the parts : 

★ Class Main : Everything in java happens inside a class. we define a class named `Main` ideally, the file name should also be `Main.java`.

★ public static void main(String[] args) : This is entry point

★ public : Access modifier, means it can be accessed from anywhere.

★ static : it can be run without creating an object of the class.

★ void : it doesnot return any value.

★ main : The name of the method.

★ (String[] args) : command line arguments, we can pass inputs to the program when running it from the command line.

★ System.out.println() : The command to print output to the screen. `println` means `print line`, so it moves to a new line after printing.

---

# 2. Comments in java

★ Single Line : // Comment here
★ Multi line : /* Comment here */

---

# 3. Data Types in Java

Java has 8 primitive data types to store different values.

1. `byte :` 1 byte, small integers ( -128 to 128 )

2. `short :` 2 bytes, integers

3. `int :` 4 bytes, integers (most common)

4. `long :` 8 bytes, large integers

5. `float :` 4 bytes, decimals (needs `f` suffix, e.g: `3.14f`)

6. `double :` 8 bytes, decimals (most common for fractions)

7. `char :` 2 bytes, single character (`e.g: 'A'`)

8. `boolean :` 1 bit (true (or) false)

---

# 4. operators

## Arithemetic : 

1. Addition (+) : Adds two values
2. Subtraction (-) : Subtracts right operand from the left
3. Multiplication (*) : Multiplies two values
4. Division (/) : Divides the left operand by the right
5. Modulo (%) : Returns remainder of a division operation

## Unary Operators : 

★ Operators that require only one operand

1. Increment (++) : increases a value by 1.
2. Decrement (--) : Decreases a value by 1.
3. Logical Not (!) : Inverts the boolean value.

## Relational Operators : 

★ Used to compare two values. They return a boolean result (T/F)

1. Equal to (==) : checks if two values are equal.
2. Not Equal to (!=) : checks if two values are not equal.
3. Greater than (>) : Checks if the left value is greater than right.
4. Lesser than (<) : Checks if the left value is less than the right.
5. (>=) : checks if left value is greater (or) equal to right.
6. (<=) : checks if left value is lesser (or) equal to right.

## Logical Operators :

★ Used to determine the logic b/w variables (or) values.

1. Logical AND (&&) : returns true if both statements are true.
2. Logical OR (||) : returns true, if atleast one statement is true.

## Assignment Operators :

★ Used to assign values to variables

1. (=) : Assigns value on the right to the variable on the left.
2. (+=) : Adds a value to the variable and assigns the result.
3. (-=) : subtracts a value from the variable and assigns the result.
4. (*=) : Multiplies the variable by a value and assigns the result.
5. (/=) : Divides the variable by a value and assigns the result.
6. (%=) : Assigns the remainder of the division to variable.

---

# 5. Strings 

★ Strings are objects in java, not primitives. They store text.

☆ Immutable : Once created, a String object cannot be changed. Modifying it creates a new object.

```Java
String s1 = "Hello";

char[] arr = {'w', 'o', 'r', 'l', 'd'};

String s2 = new String(arr); // Char array to string

System.out.println(s1 + " " + s2); // concatenate : Hello World
System.out.println(s1.CharAt(1)); // char at index 1 : `e`
System.out.println(s1.length()); // length : 5
System.out.println(s1.substring(0,2)); // substring : He
System.out.println(s1.equals("Hello")); /* checks content equality : true*/
```
---

# 6. input/Output

★ For Input we use the scanner class.

```Java
import java.util.Scanner;
public class InputExample {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int age = sc.nextInt();
        String name = sc.next();
        System.out.println(name + " is " + age);
        sc.close();
    }
}
```
---

