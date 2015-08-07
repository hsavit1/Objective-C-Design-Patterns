#### Design patterns will be based off of my own knowledge, ___Cocoa Design Patterns___ by Eric Buck, and ___PRO Objective-C Design Patterns___

#### Index:
- [Object Creation](#Object Creation)
- [Interface Adaptation][]
- [Decoupling of Objects][]
- [Abstract Collection][]
- [Behavioral Extension][]
- [Algorithm Encapsulation][]
- [Performance and Object Access][]
- [State of the Object][]

##Object Creation

1. **Prototype**: The Protoype design pattern is one of the easiest design patterns to implement. A client knows an abstract Prototype Class. At runtime any object that is a subclass of the abstract prototype can be cloned at the client's will. So the client can make multiple instances of the same type without creating them manually. It's handy in the following use cases:
	* We need to create objects that should be independent of what they are and how they are created
	* Classes to be instantiated are determined at runtime
	* We don't want to have a hierarchy of factories for a corresponding hierarchy of problems
    * The differences between instances of different classes are just a few combinations of state. Then it's more conveinent to clone a corresponding number of prototypes rather than instatiating them manually
    * Classes are not easy to create, such as compositie objects in which each component can have other components as children. I'd be easier to clone _existing_ compositie objects and modify the copies
    * **bottom line** is to make a _true copy_ of an object so that we can use it as a basis (prototype) for something else related in the same context
    
    ###### Using the Prototype Pattern
    To use the Prototype pattern, try implementing the `<NSCopying>` protocol, which requires using the `- (id)copyWithZone:(NSZone *)zone` method. Remember that the NSObject protocol doesn't have a copy method declared, but NSObject does Here's an example
    ``` 
    -(id)copyWithZone:(NSZone *)zone{
    		Stroke *strokeCopy = [[[self class] allocWithZone:zone] init];
            [strokeCopy setSize:size_];
    		return strokeCopy;
        }
    ```
    ###### Summary
    The prototype pattern is one of the simplest and easiest patterns for object creation. This pattern is good for understanding the differences between shallow and deep copying
    
2. **Factory Method**
3. **Abstract Factory**
4. **Builder**
5. **Singleton**

##Interface Adaptation
- **Adapter**
- **Bridge**
- **Façade**

##Decoupling of Objects
- **Mediator**
- **Observer**

##Abstract Collection
- **Composite**
- **Iterator**

##Behavioral Extension
- **Visitor**
- **Decorator**
- **Chain of Responsibility**

##Algorithm Encapsulation
- **Template Method**
- **Strategy**
- **Command**

##Performance and Object Access
- **Flyweight**
- **Proxy**

##State of the Object
- **Memento**
