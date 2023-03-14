# :heavy_check_mark: Screaming Architecture

## :round_pushpin: Introduction
When you look at blueprints for homes, you general *know* exactly what it is by looking at it. It should "scream" what that blueprint represents.

What does your architecture of your app scream when you see the top-level directory?

## :round_pushpin: The Theme of an Architecture
The architecture of an application should scream about the use cases of the app.

Architectures are not (or should not be) about frameworks. They are tools.

## :round_pushpin: The Purpose of an Architecture
Good architectures are centered around use cases. We should be able to describe what something does by looking at them.

We need to allow for decisions to be left open and put off for the future.

## :round_pushpin: But What About The Web?
The web is *not* an architecture. It is a delivery mechanism (IO device). Delivering over the web is a detail and should not dominate your system structure.

## :round_pushpin: Frameworks Are Tools, Not Ways Of Life
Makers of frameworks are true believers of what they create. They tell you how to use their framework and whatnot. They tell you to "let the framework do everything".

This is not the right approach. Question every framework and view it skeptically. Do not let frameworks take over your architecture.

## :round_pushpin: Testable Architectures
You should not need the server running to run tests. You should not need the database connected to run tests. Everything from entities should work together without complications from frameworks.
