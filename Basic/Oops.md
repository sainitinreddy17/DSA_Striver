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

★ Inheritance is a core concept of Object-Oriented Programming (OOP) that allows a class to inherit properties and behaviors (fields and methods) from another class. It helps in reusing existing code and creating a hierarchical relationship between classes.

## Key Points:

★ Parent (Superclass) and Child (Subclass): In inheritance, the class that is inherited from is called the parent class (or superclass), and the class that inherits is called the child class (or subclass).

★ Reuse of Code: The child class automatically gets the properties and methods of the parent class, so there is no need to rewrite the same code.

★ Extending Functionality: The child class can add new features or override existing ones to modify the behavior inherited from the parent class.

```Java
// Base class
    class Vehicle {
        private String VehicleNumber;
        
        public Vehicle(String VehicleNumber) {
            this.VehicleNumber = VehicleNumber;
        }
        
        public void honk() {
            System.out.println("Honk !!!!!!!!!!!");
        }
        
        public void printVehicleNumber() {
            System.out.println(VehicleNumber);
        }
    }
    
    // Derived class
    class Car extends Vehicle{
        public Car(String CarNumber) {
            super(CarNumber);
        }
    }
    
    // Derived class
    class Bus extends Vehicle{
        public Bus(String BusNumber) {
            super(BusNumber);
        }
    }
    
    class Main {
        public static void main(String[] args) {
            Car car = new Car("AB12CD2345");
            car.printVehicleNumber();
            car.honk();
            
            Bus bus = new Bus("XY23MN5678");
            bus.printVehicleNumber();
            bus.honk();
        }
    }
```

In this example, the Derived Classes(Car and Bus) inherit the methods(honk() and printVehicleNumber()) from the Base Class(Vehicle). Note that the Derived Classes can have their own additional methods and variables different from the Base class.

---

# Polymorphism:

Polymorphism is a concept in Object-Oriented Programming (OOP) that allows objects to be treated as instances of their parent class or interface, while having the ability to take on different forms or behaviors. It enables the same method to perform different actions depending on the object calling it.

## Key Points :

★ Two Types of Polymorphism :

- Compile-time Polymorphism (Method Overloading): The ability to have multiple methods in the same class with the same name but different parameters.

- Runtime Polymorphism (Method Overriding): The ability of a subclass to provide a specific implementation of a method that is already defined in its parent class.

Method Overloading: Multiple methods can have the same name but different parameter lists (number or type of parameters).

Method Overriding: A method in the child class can have the same name and parameters as in the parent class, but the child class provides its own implementation.

```Java
// Base class
class Vehicle {
    private String VehicleNumber;
    
    public Vehicle(String VehicleNumber) {
        this.VehicleNumber = VehicleNumber;
    }
    
    public void honk() {
        System.out.println("Honk !!!!!!!!!!!");
    }
    
    public void printVehicleNumber() {
        System.out.println(VehicleNumber);
    }
}

// Derived class
class Car extends Vehicle{
    public Car(String CarNumber) {
        super(CarNumber);
    }
    
    @Override
    public void honk() {
        System.out.println("Car Honk !!!!!!!");
    }
}

// Derived class
class Bus extends Vehicle{
    public Bus(String BusNumber) {
        super(BusNumber);
    }
}

class Main {
    public static void main(String[] args) {
        Car car = new Car("AB12CD2345");
        car.printVehicleNumber();
        car.honk();
        
        Bus bus = new Bus("XY23MN5678");
        bus.printVehicleNumber();
        bus.honk();
    }
}
```

The above code provides an example of Method Overriding where the honk() method of the Vehicle(Base class) is overridden in the Car (Derived Class).

---

# Abstraction

Abstraction is a core concept of Object-Oriented Programming (OOP) in Java that focuses on hiding complex implementation details and exposing only the essential features of an object or method. It helps simplify programming by only showing what is necessary and keeping internal workings hidden.

## Key Points :

- Hides Complexity: Abstraction allows a user to interact with an object or method without needing to understand the underlying details of how it works.

- Simplifies Interaction: Only the important aspects are exposed, making it easier to use the object or method.

## Example : 

A real-world example of abstraction is a car. A driver only interacts with the steering wheel and pedals without knowing how the engine works internally.

In Java, the abstraction can be achieved in two ways:

- Abstract Classes
- Interfaces

# 1. Abstract Class :

An abstract class is a class that cannot be instantiated directly. It can have both abstract methods (methods without a body) and regular methods (methods with a body). Abstract methods are intended to be implemented by subclasses, ensuring that each subclass provides its own specific implementation of the method.

## Key points about Abstract Class : 

- Cannot be Instantiated: An abstract class cannot be used to create objects directly. It must be inherited by a subclass, and only the subclass can be instantiated.

- Abstract Methods: These are methods without implementation in the abstract class, and the subclasses are required to provide their own implementations.

- Can Have Regular Methods: Along with abstract methods, an abstract class can also have fully defined methods.

```Java
abstract class Animal {
    // Abstract method (no implementation)
    abstract void sound();

    // Regular method
    void sleep() {
        System.out.println("This animal sleeps.");
    }
}

// Subclass providing implementation for abstract method
class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks.");
    }
}
```

In this example, Animal is an abstract class with an abstract method sound(). The subclass Dog must provide its own implementation for sound(), while it can also inherit and use the regular method sleep().

# 2. Interfaces : 

In Java, abstraction can also be achieved using interfaces. An interface is a completely abstract type that defines a contract for classes to implement. It contains only abstract methods (prior to Java 8), which must be implemented by any class that "implements" the interface. From Java 8 onwards, interfaces can also contain default and static methods with implementation.

## Key points about interfaces :

- Pure Abstraction: An interface only defines what methods should be present; the actual implementation is provided by the classes that implement the interface.

- No Instantiation: Like abstract classes, interfaces cannot be instantiated. They only serve as a blueprint.

- Multiple Implementation: A class can implement multiple interfaces, allowing for more flexibility compared to single inheritance in classes.

```Java
interface Animal {
    void sound(); // Abstract method (no body)
}

// Class implementing the interface
class Dog implements Animal {
    public void sound() {
        System.out.println("Dog barks.");
    }
}
```

In this example, Animal is an interface, and the Dog class implements the sound() method. Any class that implements Animal must provide its own implementation of the sound() method.

## Advantages of Abstraction with Interfaces :

- Multiple Inheritance: A class can implement multiple interfaces, unlike classes that can only extend one class.

- Loose Coupling: Interfaces help to reduce the dependencies between different parts of the code, making the system more modular and easier to maintain.

