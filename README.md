# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?

    The term polymorphism comes from two Greek words: 'poly' meaning 'many' and "morph" meaning 'change'. When we talk of something being 'polymorphic' we mean that it can have 'many forms'.


2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.

    We can treat an instance of a class as if it is also another class/type at the same time.

3. What can we use to implement polymorphism in Java?

      Polymorphism can be implemented using both abstract classes and interfaces. Remember that all classes which inherit from a class can take the type of the superclass. To use an abstract class we create a superclass which all the classes we want to treat as being the same can inherit from. But, inheritance is fraught with problems and we can quickly get into a mess. We can also just have one superclass.

      Interfaces also allow us to treat a class as being of another type. When a class implements an interface it gains the type of the interface without having a horrible inheritance chain. We can have as many interfaces as we like, too. Rather than just one super class.

4. How many 'forms' can an object take when using polymorphism?

      Many forms

5. Give an example of when you could use polymorphism.

      A class Animal - Cat be a subclass of Animal. So, any cat IS animal. Here, Cat satisfies the IS-A relationship for its own type as well as its super class Animal.

# Composition

6. What do we mean by 'composition' in reference to object-oriented programming?

      Composition is about ownership. When we assign an object to be part of the composition of another object.

7. When would you use composition? Provide a simple example in Java.

           
      The main reason to use composition is that it allows you to reuse code. A car is not an engine; it has one.

8. What is/are the advantage(s) of using composition?
          1) Java doesn't support multiple inheritance.
          2) Composition offers better test-ability of a class than Inheritance. If one class is composed of another class, you can easily create Mock Object representing composed class for sake of testing. Inheritance doesn't provide this. 
          3) Many object oriented design patterns favors Composition over Inheritance e.g. to change Context’s behavior, without touching context code. 
          4) Though both Composition and Inheritance allows you to reuse code, one of the disadvantage of Inheritance is that it breaks encapsulation. If sub class is depending on super class behavior for its operation, it suddenly becomes fragile. 
          5) Another reason of favoring Composition over inheritance is flexibility. If you use Composition you are flexible enough to replace implementation of Composed class with better and improved version. 

9. What happens to the behaviours when the object composed of them is destroyed?
          In composition, the object composed of other behaviours owns those behaviours. This means that when the object is destroyed all of its behaviours are also destroyed.
