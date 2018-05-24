- POLYMORPHISM

1. What does the word 'polymorphism' mean?

If something is polymorphic it means it has many forms. A shape can be one of many things, for example a square, a triangle, a circle etc.

2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.

Applying polymorphism in OO design means we can have instances of classes that are also instances of other classes at the same time. In java this can be done through using parent/child(inheritance) class structures and by using interfaces.

  - Using inheritance

    - public abstract class Shape {
          private String colour;

          public Shape(String colour) {
              this. colour = colour;
          }
      }

    - public class Circle extends Shape {
          private int radius;

          public Circle(String colour, int radius) {
              super(colour)
              this.radius = radius;
          }
      }

3. What can we use to implement polymorphism in Java?

Interfaces and Inheritance(above)

  - Using an Interface

    - public interface IUseThumbs {

          public void grip() {}
      }
    - public class Human implements IUseThumbs {

          public String grip() {
              return "I can grip with my hands";
          }
      }
    - public class Chimp implements IUseThumbs {

          public String grip() {
              return "I can grip with my hands and feet";
          }
      }


4. How many 'forms' can an object take when using polymorphism?

Dynamic (runtime)
  - methods in subclasses get precedence over superclass methods

Static (compile-time)
  - more than one method can have the same name, but with different different arguments required. Depending on the objects number of arguments either method will take precedence.

5. Give an example of when you could use polymorphism.

You could use polymorphism in a OO project to model a classroom of people.

You could have a 'Teacher' and 'Student' class inheriting from a parent 'Person' class.

The 'Teacher' and 'Student' class will share the behaviours of the 'Person' class but may also have their own individual methods/variables (such as a 'Student' having a matriculation number).

Both 'Teacher' and 'Student' classes could implement an IAttendSchool interface.

The interface would give the shared behaviour 'travelToSchool()' to both subclasses of 'Person'(the 'Person' superclass would not implement such a behaviour).

 The 'Teacher' would implement the shared behaviour differently from the 'Student, such as 'driving' as apposed to 'getting the school bus'.

- COMPOSITION

6. What do we mean by 'composition' in reference to object-oriented programming?

Composition in OO means that one object can 'have' other objects. This allows an object to broken down into smaller composite parts.

7. When would you use composition? Provide a simple example in Java.

We would use composition to allow an object to use the behaviours of other types of objects without needed to inherit directly from them.

  - public class tableTennisGame() {
        private int numberOfServesPerPlayer;
        private ArrayList<IPerson>() players;
        private IPerson playerServing;
        private IPerson playerReceivingServe;
        private Ball ball;
    }

  - In above example the two players of the game rotate every set number of serves.

8. What is/are the advantage(s) of using composition?

Avoids the needs for complicated inheritance structures.
Provides ability to change behaviour of overall owner object by changing out one of the composite objects.

9. What happens to the behaviours when the object composed of them is destroyed?

The behaviours of composite objects can no longer be used when the owning object is destroyed as they too are destroyed.
