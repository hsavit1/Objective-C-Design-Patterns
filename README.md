## Design patterns will be based off of my own knowledge, ___Cocoa Design Patterns___ by Eric Buck, and ___PRO Objective-C Design Patterns___

##Object Creation

_you should use these patterns to create objects_

* **Prototype**: The Protoype design pattern is handy in the following use cases
	* We need to create objects that should be independent of what they are and how they are created
	* Classes to be instantiated are determined at runtime
	* We don't want to have a hierarchy of factories for a corresponding hierarchy of problems
    * The differences between instances of different classes are just a few combinations of state. Then it's more conveinent to clone a corresponding number of prototypes rather than instatiating them manually
    * Classes are not easy to create, such as compositie objects in which each component can have other components as children. I'd be easier to clone _existing_ compositie objects and modify the copies
    * **bottom line** is to make a _true copy_ of an object so that we can use it as a basis (prototype) for something else related in the same context
    
* **Factory Method**
* **Abstract Factory**
* **Builder**
* **Singleton**

####Interface Adaptation
- **Adapter**
- **Bridge**
- **Façade**

####Decoupling of Objects
- **Mediator**
- **Observer**

####Abstract Collection
- **Composite**
- **Iterator**

####Behavioral Extension
- **Visitor**
- **Decorator**
- **Chain of Responsibility**

####Algorithm Encapsulation
- **Template Method**
- **Strategy**
- **Command**

####Performance and Object Access
- **Flyweight**
- **Proxy**

####State of the Object
- **Memento**
