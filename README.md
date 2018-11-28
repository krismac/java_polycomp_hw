# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?

    The term polymorphism comes from two Greek words: 'poly' meaning 'many' and "morph" meaning 'change'. When we talk of something being 'polymorphic' we mean that it can have 'many forms'.


2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.

  We can treat an instance of a class as if it is also another class/type at the same time.
   
        public interface Wildlife{}
        public class Animal{}
        public class Rhino extends Animal implements Wildlife{}
  
The Rhino class is considered to be polymorphic since this has multiple inheritance. Following are true for the above   examples
 
   - A Rhino IS - A Animal
   - A Rhino IS - Wildlife
   - A Rhino IS - A Rhino
   - A Rhino IS - A Object

3. What can we use to implement polymorphism in Java?

      Polymorphism can be implemented using both abstract classes and interfaces. Remember that all classes which inherit from a class can take the type of the superclass. To use an abstract class we create a superclass which all the classes we want to treat as being the same can inherit from. But, inheritance is fraught with problems and we can quickly get into a mess. We can also just have one superclass.

      Interfaces also allow us to treat a class as being of another type. When a class implements an interface it gains the type of the interface without having the difficulty of an inheritance chain. We can have as many interfaces rather than just one inherited super class.

4. How many 'forms' can an object take when using polymorphism?

      Many forms

5. Give an example of when you could use polymorphism.

      A class Animal with Cat as a subclass of Animal. So, any cat IS animal. 
      Cat satisfies the IS-A relationship for its own type as well as its super class Animal.

# Composition

6. What do we mean by 'composition' in reference to object-oriented programming?

      Composition is about ownership. When we assign an object to be part of the composition of another object.

7. When would you use composition? Provide a simple example in Java.

      The main reason to use composition is that it allows you to reuse code. A person is not an job; it has one.
      
            public class Job {
                private String role;
                private long salary;
                private int id;

                public String getRole() {
                    return role;
                }

this can be given a relationship to person

            public class Person {

                private Job job;

                public Person(){
                    this.job=new Job();
                    job.setSalary(1000L);
                }
    
8. What is/are the advantage(s) of using composition?
   - Java doesn't support multiple inheritance.
   - Composition offers better test-ability of a class than Inheritance. If one class is composed of another class, you can easily create Mock Object representing composed class for sake of testing. Inheritance doesn't provide this. 
    - Many object oriented design patterns favors Composition over Inheritance e.g. to change Context’s behavior, without touching context code. 
    - Though both Composition and Inheritance allows you to reuse code, one of the disadvantage of Inheritance is that it breaks encapsulation. If sub class is depending on super class behavior for its operation, it suddenly becomes fragile. 
    - Another reason of favoring Composition over inheritance is flexibility. If you use Composition you are flexible enough to replace implementation of Composed class with better and improved version. 

9. What happens to the behaviours when the object composed of them is destroyed?
          In composition, the object composed of other behaviours owns those behaviours. This means that when the object is destroyed all of its behaviours are also destroyed.
