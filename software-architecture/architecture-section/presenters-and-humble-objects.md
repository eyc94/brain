# :heavy_check_mark: Presenters and Humble Objects

## :round_pushpin: Introduction
We have seen presenters. Presenters are a form of the `Humble Object` pattern. This helps us identify and protect architectural boundaries.

The `Clean Architecture` section [here](clean-architecture.md) is full of `Humble Ojbect` implementations.

## :round_pushpin: The Humble Object Pattern
The `Humble Object` pattern is a design pattern made to help unit testers separate behaviors that are easy to test and hard to test.

We split the behaviors into two modules or classes. One of those modules is humble. It contains all the hard-to-test behaviors stripped down to their barest essence.

The other contains all testable behaviors stripped out of the humble object.

GUIs are hard to unit test because it is hard to write tests that can see the screen and check the elements are displayed. However, most behaviors of GUIs are easy to test. Using `Humble Object` pattern, separate two kinds of behaviors into two different classes called the Presenter and the View.

## :round_pushpin: Presenters and Views
The `View` is the humble object that is hard to test. The code here is kept as simple as possible. It moves data into the GUI but does not process the data.

The `Presenter` is the testable object. Its job is to get data from app and format it for the `View`, so it can move it to the screen. If the app wants a date in a field, it hands the `Presenter` a `Date` object. The `Presenter` formats it into an appropriate string and place it in a data structure called the `View Model`, where the `View` can find it.

Everything is loaded in the `View Model` by the `Presenter`. The `View` only loads what is in the `View Model` to the screen. Nothing else. The `View` is humble.

## :round_pushpin: Testing and Architecture
Testability is an attribute of good architecture. The `Humble Object` pattern is a good example because of the separation of testable and non-testable parts.

## :round_pushpin: Database Gateways
Between the use case interactors and the database are *database gateways*. These are polymorphic interfaces that contain methods for the database CRUD operations. If an app needs to know the last names of all users who logged in yesterday, then `UserGateway` interface will have a method named `getLastNamesOfUsersWhoLoggedInAfter` that takes a `Date` as its argument and returns a list of last names.

We do not allow SQL in the use cases layer. We use gateway interfaces that have the methods we need. Those gateways are implemented by classes in the database layer. That implementation is the humble object. It uses SQL, or whatever query language, to get what we need.

The interactors are not humble because they encapsulate app-specific business rules. They are not humble, but those interactors are testable. Gateways can be replaced with appropriate stubs and test-doubles.

## :round_pushpin: Data Mappers
Which layer do you think ORMs like Hibernate will belong?

Let's get something straight. There is no such thing as an Object Relational Mapper (ORM). Why? Objects are not data structures. They are not data structures from the user's point of view.

Users of an object cannot see the data because they are all private. Those users only see public methods. So from the user's point of view, an object is just a set of operations.

A data structure is a set of public data variables with no implied behavior. ORMs would be better named "data mappers". They load data into data structures from relational database tables.

So, where should ORMs reside? In the database layer of course. ORMs form another kind of *Humble Object* boundary between gateway interfaces and database.

## :round_pushpin: Service Listeners
If your app needs to communicate with other services, or if your app provides a set of services, will we find the *Humble Object* pattern?

Yes. The app loads data into simple data structures and then pass those data structures across the boundary to modules that properly format the data and send it to external services.

On input, the service listeners will receive data from the service interface and format it into a simple data structure that can be used by the app.

That data structure is then passed across the service boundary.
