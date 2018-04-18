**Polymorphism & Composition Homework – Quiz****Polymorphism**1 - What does the word 'polymorphism' mean?Poly = many, morph = forms. Something that can have many forms. 2 - What does it mean when we apply polymorphism to OO design? Give a simple Java example.When a class can be itself, but also another object. For example, a broomstick, when linked via an interface, can also be a flying object (such as an IFlyable). In other words, a broomstick can take many forms.3 - What can we use to implement polymorphism in Java?Interfaces:  the class that a developer wants to be in many forms much access an interface, the methods of which can be shared with other related classes. All of these classes can then be called together in a ‘runner’ class and the shared method called on the interface class.4 - How many 'forms' can an object take when using polymorphism?It could take many forms, depending on the project for which the code is being written. 5 - Give an example of when you could use polymorphism.
 In the example of a themepark, attractions (e.g. rollercoaster, dodgems, tea cups) could have an entertainment rating and a restriction method: rather than calling these methods on all three individual attractions, and have 6 extra lines of code, combine them into two interfaces, and run them in two lines through the themepark runner file. **Composition**6 - What do we mean by 'composition' in reference to object-oriented programming?Objects that have other objects in them. Classes that contain instances of other classes, rather than from inheriting from a parent class. 7 - When would you use composition? Provide a simple example in Java.If you wanted to model a Wizard,  and add a dragon to their constructor, you would create a Wizard and a Dragon class, then give the Wizard class an ArrayList of Dragons, which would require the structure you had provided in the dragon class. This is composition: no inheritance or polymorphism needs to be involved. It simply means that the Wizard HAS A dragon.

~~~java
public class Wizard{
private String name:
private Dragon dragons:

public Wizard(String name, Dragon dragons){
this.name = name;
this.dragons = dragons;

}
~~~

8 - What is/are the advantage(s) of using composition?

Composition allows the use of strategy patterns: where a single runner class can access multiple related classes via interfaces. This keeps the code DRY.
More flexible than inheritance and keeps the code simple, without an unnecessarily complicated code architecture.9 - What happens to the behaviours when the object composed of them is destroyed?

Assuming behaviours are interfaces (e.g. IFlyable) and that the object composed of them (i.e. the runner, such as wizard) is Wizard then...the behaviours will remain and could be used again in another object. 