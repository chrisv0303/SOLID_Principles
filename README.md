## SOLID Software Design Principles Notes

- SOLID principles are the foundation on which we can build clean, maintainable architectures and helps us to keep technical debt under control. There are benefits of writing SOLID code which they are:
	- Easy to understand and reason about
	- Changes are faster and have a minimal risk level
	- Highly maintainable over long periods of time
	- Cost effective

- The five SOLID principles of object-oriented design:
	- S - Single Responsibility Principle (SRP): every function, class or module should have one and only one reason to change where it establishes responsibilities to change. Examples of these responsibilities of change include:
		- Business Logic
		- User Interface
		- Persistence
		- Logging
		- Orchestration
		- Users
	- As a software developer, it is best to always identify the reasons to change that your components have and reduce them to a single one. We use SRP for a number of reasons:
		- It makes code easier to understand, fix, and maintain
		- Classes are less coupled and more resilient to change
		- More testable design
	- The symptoms of not using SRP are:
		- Code is more dificult to read and reason about
		- Decreased quality due to testing difficulty
		- Side effects
		- High coupling (most dangerous) - the level of interdependency between various software components that have many reasons to change that exposes you to the internal implementation of a particular class.

	- O - Open Closed Principle (OCP): Classes, functions, and modules should be closed for modification, but open for extension. When closed for modification, each new feature should not modify existing source code. At the same time, a component is open for extension if it allows us to make it behave in new ways by creating or writing new code. We should apply the OCP for these reasons:
		- New features can be added easily and with minimal cost
		- Minimizes the risk of regression bugs
		- Enforces decoupling by isolating changes in specific components, works along the SRP
	- Some strategies to apply the OCP is:
		- Start small - make changes inline where bug fixes can be implemented this way
		- More changes - consider using Inheritance
		- Many changes/dynamic decision - consider using interfaces and design patterns

	- L - Liskov Substitution Principle (LSP): Any object of a type must be substitutable by objects of a derived typed without altering the correctness of that program. It is all about relationships between types. In LSP, it is best to ask ourselves if a particular type is substitutable by another type instead of using a 'is-a' relationship. Incorrect relationships between types cause unexpected bugs or side effects. To refactor the code to LSP, there are two possibilities:
		- Eliminate incorrect relations between objects
		- Use "Tell, don't ask!" principle to eliminate type checking and casting.

	- I - Interface Segregation Principle (ISP): Clients should not be forced to depend on methods that they do not use. Normally, large interfaces would have to be split into more focused interfaces so that clients that use them will not be forced to depend on things that they do not need. The ISP can reinforce other principles with:
		- Liskov Substitution Principle - by keeping interfaces small, the classes that implement them have a higher chance to fully substitute the interface.
		- Single Responsibility Principle - classes that implement small interfaces are more focused and tend to have a single purpose.
	- The benefits of applying the ISP are:
		- Lean interfaces minimize dependencies on unused members and reduce code coupling
		- Code becomes more cohesive and focused
		- It reinforces the use of the SRP and LSP
	- Refactoring code that depends on large interfaces:
		- If owning your code - breaking interfaces is easy and safe due to the possibility to implement as many interfaces as we want
		- If working with external legacy code - you can't control the interfaces in the external code

	- D - Dependency Inversion Principle (DIP): High level modules should not depend on low level modules; both should depend on abstractions. Abstractions on the other hand, should not depend on details where details should depend upon abstraction. High level modules are modules written to solve real problems and use cases. They are more abstract and map to the business domain and tells us what the software should do instead of telling us how it should do. Low level modules contain implementation details that are required to execute the business policies. They are considered the "plumbing" or "internals" of an application and tells us how the software should do various tasks. Dependency injection is very used in conjunction with the dependency inversion principle however, they are not the same thing. Dependency injection is a technique that allows the creation of dependent objects outside of a class and provides those objects to a class. Inversion of control can help us create large systems by taking away the responsibility of creating objects. Inversion of control is a design principle in which the control of object creation, configuration, and lifecycle is passed to a container or framework. There are many IoC container benefits:
		- makes it easy to switch between different implementations at runtime
		- increases program modularity
		- manages the lifecycle of objects and their configuration
