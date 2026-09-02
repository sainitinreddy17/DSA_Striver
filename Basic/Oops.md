# Object Oriented Programming

## Introduction :

Object-oriented programming is a programming paradigm ased on the concept of classes and objects, which can contain data and cde to manipulative that data.

★ Understanding OOP is vital as it allows for more organized, modular, and re-usable code, which is particularly important when dealing with complex problems in DS & Algo.

## Classes and Objects :

★ Class : In Java, a class serves as a blue print (or) a template for creating objects. A class encapsulates data for the object and methods to manipulate that data.

Code in java is typically defined within a class, which means that almost everything revolves around the concept of Objects and classes.

★ Object : An object is an instance of a class. When a class is defined, no memory is alocated (or) action performed util an object is created from that class.

## Access Specifiers :

Access Specifiers in java determine the visibility and accessibility of classes, methods amd variables. The most common access specifiers are :

★ Public : When a class (or) method is declared as public, it is accessible from anywhere in the program.

★ Private : Declaring something as a private restricts it's access to within the class it is declared in.

★ Protected : A protected entity is accessible within it's own package and by sub-classes.

- If no access specifier is used, java assigns a default access level, known as package-priavte, meaning the class (or) method is accessible within its own package.

## Static Methods :

A Staticmethod belongs to the class rather than any instance of the class. This allows for calling a static method directly using the class name without the need to create an object.

`className.methodName();`

## Creating and using Objects :

In Java, objects are instances (Copies of classes). To access non static methods, an object of he class must be created using the `new` keyword, followed by the class constructor.

` Ex : className objName = new className();`

★ Now, the objects are instance of class. It holds actual data in the form of attributesand can perform actions using the methods defined in the class.

```Java
class Test{
    int age;
    public void assignAge(int num){
        age = num;
    }
}

class Basics{
    public static void main(String[] args){
        Test test1 = new Test();
        test1.assignAge(10);
        Test test2 = new Test();
        test2.assignAge(19);
        System.out.println(test1.age);
        System.out.println(test2.age);
    }
}
```

## Arguments in Methods

Arguments are the values (or) variables passed to a function (or) method when it is called. These arguments provide the neccessary inputs that the function uses to perform it's operations.

```Java
class Test{
    public int sum(int num1, nt num2){
        return num1+num2;
    }
}

class Basics{
    public static void main(String[] args){
        // creating an object of class test
        Test test = new Test();
        int sum = test.sum(10, 15);
        System.out.println(sum);
    }
}
```

---

# Constructors :

★ In Object-Orieneted programming in java, a constructor is a special type of method used to initialize objects. It is called automatically when an object of a class is created.

★ Constructor's main role is to set initial values for the object's attributes and perform any neccessary tasks.

- Same Name as Class : A Constructor has the same Nameas the class it belongs to.
- No Return Type : Constructors do not have a return type, not even void.
- Called automatically : When an object is created using the new keyword, the constructor is called automatically.

## Types of Constructors :

★ Default Constructor : A default constructor is a constructor that has no `parameters`. if no constructor is defined in a class, Java automatically provides a default constructor that initializes object fields to their default values.

★ Parameterized Constructor : It allows passing arguments to the constructor, so that specifi values can be assigned to object attributes at the time of creation.

## NOTE : 

★ In java, a class can have multiple constructors, a concept known as constructor overloading.

★ This allows the class to have different constructorswith varying parameters.

★ Each constructor can perform, different initializations based on the number of type of arguments passed during object creation.

---

# Encapsulation :

It is one of the core concepts of object oriented programming. it refers to the practice of bundling data (variables) and methods (functions) that operate on the data into a single unit, known as class, and restricting direct access to the data from outside the class.

## Key points :

★ Data Hiding : It hides the internal details of how an object works. The object's data is kept private and can only be accessed (or) modified through methods (`Getters & Setters`).

★ Controlled Access : Through Encapsulation, only specificmethods are provided to access (or) modify the data, ensuring more controlled and secure interactions with the object's data.

```Java
class BankAccount {
    private int balance;
    public int getBalance(){
        return balance;
    }
    public void setName(int newBalance){
        balance = newBalance;
    }
}
```

# NOTE 

★ Here, the `balance` variable is private, so it can't be accessed directly from outside the `BankAcount` class. it can only be accessed (or) modified using the `getBalanec()` and `setName()`methods, which provide controlled access to the data.

---

# Inheritance

★ It is a core concept of OOPS that allows a class to in-herit properties and behaviours (fields and methods) from another class.

★ It helps in  