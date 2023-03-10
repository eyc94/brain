# :heavy_check_mark: Structured Programming

![Image of structured programming](../images/programming-paradigms/structured-programming.png)

## :round_pushpin: Introduction
`Structured Programming` is a programming paradigm aimed at improving the clarity, quality, and development time of a computer program by making extensive use of the structured control flow constructs of selection (`if/then/else`) and repetition (`while` and `for`), block structures, and subroutines.

This is the first paradigm to be adopted but not to be invented. This was discovered by `Edsger Wybe Dijkstra` in 1968. He showed that the use of unrestrained jumps (`goto` statments) is harmful to program structure.

He replaced those jumps with `if/then/else` and `do/while/until` constructs.

> Structured programming imposes discipline on direct transfer of control.

It emphasizes the use of structured control flow constructs to improve the clarity, quality, and maintainability of computer programs.

It was created in response to shortcomings in earlier programming approaches that were based on unstructured, ad hoc techniques.

The main idea is to break down a program into small, well-defined, and modularized pieces, called functions or procedures, that can be easily understood and tested. It advocates the use of control structures such as conditionals (`if/else` statements), loops (`for`, `do-while` statements), and subroutines to create clear and predictable program logic.

Emphasizes the use of top-down design, which involves breaking down a complex problem into smaller sub-problems, and solving each sub-problem in turn.

## :round_pushpin: Example
Here is an example in Java:
```java
import java.util.Scanner;

public class EvenOdd {
  public static void main(String[] args) {
    // Get input from user.
    Scanner scanner = new Scanner(System.in);
    System.out.print("Enter a number: ");
    int number = scanner.nextInt();

    // Check if the number is even or odd.
    if (number % 2 == 0) {
      System.out.println(number + " is even");
    } else {
      System.out.println(number + " is odd");
    }
  }
}
```

We defined a main method that prompts the user to enter a number, check if the number is even or odd using conditionals, and then prints the result.

## :round_pushpin: Structured vs Modular Programming
Some people refer to structured programming as modular programming.

However, `Modular Programming` refers to the practice of breaking a program down into smaller, more manageable modules or components. Each module is responsible for a task and can be developed and tested separately. The goal of modular programming is to make the code more modular, reusable, and maintainable.

While structured programming and modular programming have some similarities, they are not interchangeable terms.

`Structured Programming` is a way of organizing control flow in a program, while `Modular Programming` is a way of organizing the structure of the program itself. However, the two concepts are often used together to create well-structured and modularized programs.

## :round_pushpin: Benefits and Downsides
There are many **benefits**:
- Clarity.
- Maintainability.
- Modularity.
- Reliability.
- Efficiency.

There are also **downsides**:
- Overhead.
- Limited expressiveness.
- Difficulty with certain problems.
- Steep learning curve.
- Limited creativity.

## :round_pushpin: Supplemental Sources
1. [Wikipedia](https://en.wikipedia.org/wiki/Structured_programming#:~:text=Structured%20programming%20is%20a%20programming,%2C%20block%20structures%2C%20and%20subroutines.)
