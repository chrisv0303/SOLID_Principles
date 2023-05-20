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
	As a software developer, it is best to always identify the reasons to change that your components have and reduce them to a single one. We use SRP for a number of reasons:
		- It makes code easier to understand, fix, and maintain
		- Classes are less coupled and more resilient to change
		- More testable design
	The symptoms of not using SRP are:
		- Code is more dificult to read and reason about
		- Decreased quality due to testing difficulty
		- Side effects
		- High coupling (most dangerous) - the level of interdependency between various software components that have many reasons to change that exposes you to the internal implementation of a particular class.
	- O - Open Closed Principle (OCP): Classes, functions, and modules should be closed for modification, but open for extension. When closed for modification, each new feature should not modify existing source code. At the same time, a component is open for extension if it allows us to make it behave in new ways by creating or writing new code. We should apply the OCP for these reasons:
		- New features can be added easily and with minimal cost
		- Minimizes the risk of regression bugs
		- Enforces decoupling by isolating changes in specific components, works along the SRP
	Some strategies to apply the OCP is:
		- Start small - make changes inline where bug fixes can be implemented this way
		- More changes - consider using Inheritance
		- Many changes/dynamic decision - consider using interfaces and design patterns
	- L - Liskov Substitution Principle (LSP): Any object of a type must be substitutable by objects of a derived typed without altering the correctness of that program. It is all about relationships between types. In LSP, it is best to ask ourselves if a particular type is substitutable by another type instead of using a 'is-a' relationship. Incorrect relationships between types cause unexpected bugs or side effects. To refactor the code to LSP, there are two possibilities:
		- Eliminate incorrect relations between objects
		- Use "Tell, don't ask!" principle to eliminate type checking and casting.
	- I - Interface Segregation Principle
	- D - Dependency Inversion Principle
