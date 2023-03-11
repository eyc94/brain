# :heavy_check_mark: Object-Oriented Programming

![Image of object-oriented programming](../images/programming-paradigms/object-oriented-programming.png)

## :round_pushpin: Introduction
Second paradigm to be adopted was the `Object-Oriented Programming (OOP)` paradigm. It was discovered by Ole Johan Dahl and Kristen Nygaard. They noticed that the function call stack frame in the `ALGOL` language could be moved to a heap, allowing local variables declared by a function to exist long after the function returned.

This function became a constructor for a class, the local variables became instance variables, and the nested functions became methods.

This led to the discovery of `polymorphism` through the use of function pointers.

> Object-oriented programming imposes discipline on indirect transfer of control.

## :round_pushpin: Background
There are *three* words that we can use to describe OO:
1. `Encapsulation`
2. `Inheritance`
3. `Polymorphism`

The idea is that OO is the mixture of these three things or that an OO language must support these three things.

OOP is based on the concept of `objects` which can contain data and code. The data is in the form of `fields` (attributes and properties), and the code is in the form of `procedures` (methods).

OOP emphasizes the use of objects and classes to structure code and data. OOP is a way of organizing code that allows for more efficient and modular programming, making it easier to maintain and reuse code.

Everything in OOP is labeled as an object, which is an instance of a class. A class is a blueprint that defines the characteristics and behaviors of an object. Objects have state (data) and behavior (methods) that can be accessed and manipulated through well-defined interfaces.

## :round_pushpin: Features
Key features:
- Encapsulation: The practice of bundling data and methods within a class and restricting access to them from outside the class.
- Inheritance: Allows one class to inherit properties and methods from another, reducing code duplication and making it easier to create new classes based on existing ones.
- Polymorphism: Allows different objects to be treated as if they were the same type, making it easier to write code that works with multiple types of objects.

### Encapsulation
`OO` languages provide each and effective encapsulation of data and function.

A line can be drawn around a cohesive set of data and functions. Outside of that line, the data is *hidden* and only some of the functions are known.

This concept is known as the *private data members* and the *public member functions* of a class.

This idea is *not* unique to `OO`. We had encapsulation in `C`.

The idea is that the users of a public member function will have no idea about *how* the function is implemented. They simply call the function and something happens.

`C` is *not* an `OO` language and performs encapsulation perfectly. The client will never know about the private member variables because the header files and implementation files are *separate*.

However, in `C++`, this is broken. Here, the header files required that the private member variables be declared in the header file. This allows the client to see the private variables.

The variables `private`, `public`, and `protected` were introduced to mitigate this. But this was more of a *hack*.

It is difficult to accept that `OO` depends on strong encapsulation. Many `OO` languages have little or no enforced encapsulation. So, it is up to the user to *enforce* the standards of encapsulation.

### Inheritance

### Polymorphism

## :round_pushpin: Example
```java
public class Car {
  private String make;
  private String model;
  private int year;

  public Car(String make, String model, int year) {
    this.make = make;
    this.model = model;
    this.year = year;
  }

  public String getMake() {
    return make;
  }

  public String getModel() {
    return model;
  }

  public int getYear() {
    return year;
  }

  public void start() {
    System.out.println("The " + make + " " + model + " is starting.");
  }

  public void stop() {
    System.out.println("The " + make + " " + model + " is stopping.");
  }
}
```

Here, we have a class called `Car`. It has three instance variables: `make`, `model`, and `year`. This class also has a constructor that takes these variables as parameters and sets them to the instance variables. There are also methods in this class as well.

We can make `Car` objects with this blueprint.

```java
Car myCar = new Car("Toyota", "Camry", 2018);
System.out.println(myCar.getMake()); // Output: Toyota
System.out.println(myCar.getModel()); // Output: Camry
System.out.println(myCar.getYear()); // Output: 2018
myCar.start(); // Output: The Toyota Camry is starting.
myCar.stop(); // Output: The Toyota Camry is stopping.
```

## :round_pushpin: Benefits and Downsides
There are many **benefits** to using OOP:
- Code reuse.
- Improved modularity.
- Easier maintenance.
- Encapsulation.
- Inheritance.
- Polymorphism.

There are also **downsides** to using OOP:
- Complexity.
- Performance.
- Over-engineering.
- Overuse.

## :round_pushpin: Applications
There are various applications of OOP:
- Desktop and mobile applications.
- Video games.
- Web applications.

## :round_pushpin: Supplemental Sources
1. [Wikipedia](https://en.wikipedia.org/wiki/Object-oriented_programming)
