###### Develop code that uses abstract classes and methods
>+ An abstraction specifying functionality supported without disclosing finer level
details.
>+ You cannot create instances of an abstract class.
>+ Abstract classes enable runtime polymorphism, and runtime polymorphism in turn
enables loose coupling.
###### Develop code that uses a final keyword
>+ A final class is a non-inheritable class (i.e., you cannot inherit from a final class).
>+ A final method is a non-overridable method (i.e., subclasses cannot override a final
method).
>+ All methods of a final class are implicitly final (i.e., non-overridable).
>+ A final variable can be assigned only once.
###### Create inner classes including static inner class, local class, nested class, and anonymous inner class
>+ Java supports four types of nested classes: static nested classes, inner classes, local
inner classes, and anonymous inner classes.
>+ Static nested classes may have static members, whereas the other flavors of nested
classes can’t.
	 Static nested classes and inner classes can access members of an outer class (even
private members). However, static nested classes can access only static members of
outer classes.
>+ Local classes (both local inner classes and anonymous inner classes) can access all
variables declared in the outer scope (whether a method, constructor, or a statement
block).
###### Use enumerated types including methods, and constructors in an enum type
>+ Enums are a typesafe way to achieve restricted input from users.
>+ You cannot use new with enums, even inside the enum definition.
>+ Enum classes are by default final classes.
>+ All enum classes are implicitly derived from java.lang.Enum.
###### Develop code that declares, implements, and/or extends interfaces and use the atOverride annotation
>+ An interface can have three kinds of methods: abstract methods, default methods,
and static methods.
>+ The “diamond problem” occurs when a derived type inherits two method definitions
in the base types that have the same signature.
>+ If two super interfaces have the same method name and one of them has a
definition, the compiler will issue an error; this conflict has to be resolved
manually.
>+ If a base class and a base interface define methods with the same signature, the
method definition in the class is used and the interface definition is ignored.
>+ A functional interface consists of exactly one abstract method but can contain any
number of default or static methods.
>+ A declaration of a functional interface results in a “functional interface type” that can
be used with lambda expressions.
>+ For a functional interface, declaring methods from Object class in an interface does
not count as an abstract method.
###### Create and use Lambda expressions
>+ In a lambda expression, the left side of the -> provides the parameters; the right
side, the body. The arrow operator (“->”) helps in concise expressions of lambda
functions.
>+ You can create a reference to a functional interface and assign a lambda expression
to it. If you invoke the abstract method from that interface, it will call the assigned
lambda expression.
>+ Compiler can perform type inferences of lambda parameters if omitted. When
declared, parameters can have modifiers such as final.
>+ Variables accessed by a lambda function are considered to be effectively final.
