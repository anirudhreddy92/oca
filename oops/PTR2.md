###### #1
>+ The abstract keyword can be applied to a class or a non-static method.
>+ An abstract class may have methods or fields declared static. However, the abstract
keyword cannot be applied to fields or static methods.
>+ An abstract class can extend another abstract class or can implement an interface.
>+ An abstract class can be derived from a concrete class! Although the language allows
it, it is not a good idea to do so.
>+ An abstract class need not declare an abstract method, which means it is not
necessary for an abstract class to have any methods declared as abstract. However, if
a class has an abstract method, it should be declared as an abstract class.
>+ A subclass of an abstract class needs to provide implementation of all the abstract
methods; otherwise you need to declare that subclass as an abstract class.
###### #2
>+ The final modifier can be applied to a class, method, or variable. All methods of a
final class are implicitly final (hence non-overridable).
>+ A final variable can be assigned only once. If a variable declaration defines a
variable as final but did not initialize it, then it is referred to as blank final. You need
to initialize a blank final in all the constructors you have defined in the class or in an
initialization block.
>+ The keyword final can be applied to
###### #3
>+ The accessibility (public, protected, etc.) of the static nested class is defined by
the outer class.
>+ The name of the static nested class is expressed with
OuterClassName.NestedClassName syntax.
>+ When you define an inner nested class (or interface) inside an interface, the nested
class is declared implicitly public and static. This point is easy to remember: any
field in an interface is implicitly declared public and static, and static nested
classes have this same behavior.
>+ Static nested classes can be declared abstract or final.
>+ Static nested classes can extend another class or they can be used as base classes.
>+ Static nested classes can have static members. (As you’ll see shortly, this statement
does not apply to other kinds of nested classes.)
>+ Static nested classes can access the members of the outer class (only static members,
obviously).
>+ The outer class can also access the members (even private members) of the nested
class through an object of a nested class. If you don’t declare an instance of the
nested class, the outer class cannot access nested class elements directly.
###### #4
>+ The accessibility (public, protected, etc.) of the inner class is defined by the
outer class.
>+ Just like top-level classes, an inner class can extend a class or can implement
interfaces. Similarly, other classes can extend an inner class, and other classes or
interfaces can extend or implement an inner interface.
>+ An inner class can be declared final or abstract.
>+ Inner classes can have inner classes, but you’ll have a hard time reading or
understanding such complex nesting of classes. (Meaning: Avoid them!)
###### #5
>+ You can create a non-static local class inside a body of code. Interfaces cannot have
local classes, and you cannot create local interfaces.
>+ Local classes are accessible only from the body of the code in which the class is
defined. The local classes are completely inaccessible outside the body of the code in
which the class is defined.
>+ You can extend a class or implement interfaces while defining a local class.
>+ A local class can access all the variables available in the body of the code in which it
is defined. Variables accessed by local inner classes are considered effectively final.
###### #6
>+ Anonymous classes are defined in the new expression itself.
>+ You cannot explicitly extend a class or explicitly implement interfaces when defining
an anonymous class.
###### #7
>+ Enums are implicitly declared public, static, and final, which means you cannot
extend them.
>+ When you define an enumeration, it implicitly inherits from java.lang.Enum.
Internally, enumerations are converted to classes. Further, enumeration constants
are instances of the enumeration class for which the constant is declared as a
member.
>+ You can apply the valueOf() and name() methods to the enum element to return the
name of the enum element.
>+ If you declare an enum within a class, then it is by default static.
>+ You cannot use the new operator on enum data types, even inside the enum class.
>+ You can compare two enumerations for equality using == operator.
>+ If enumeration constants are from two different enumerations, the equals() method
does not return true.
>+ When an enumeration constant’s toString() method is invoked, it prints the name
of the enumeration constant.
>+ The static values() method in the Enum class returns an array of the enumeration
constants when called on an enumeration type.
>+ Enumeration constants cannot be cloned. An attempt to do so will result in a
CloneNotSupportedException.
###### #8
>+ An interface cannot be instantiated. A reference to an interface can refer to an object
of any of its derived types implementing it.
>+ An interface can extend another interface. Use the extends (and not the implements)
keyword for extending another interface.
>+ Interfaces cannot contain instance variables. If you declare a data member in an
interface, it should be initialized, and all such data members are implicitly treated as
“public static final” members.
>+ An interface can have three kinds of methods: abstract methods, default methods,
and static methods.
>+ An interface can be declared with empty body (i.e., an interface without any
members). For example, java.util defines the interface EventListener
without a body.
>+ An interface can be declared within another interface or class; such interfaces are
known as nested interfaces.
>+ Unlike top-level interfaces that can have only public or default access, a nested
interface can be declared public, protected, or private.
>+ If you are implementing an interface in an abstract class, the abstract class does not
need to define the method. But, ultimately a concrete class has to define the abstract
method declared in the interface.
>+ You can use the @Override annotation for a method to indicate that it is overriding a
method from its base type(s).
###### #9
>+ You cannot declare members as protected or private. Only public access is
allowed for members of an interface. Since all methods are public by default, you can
omit the public keyword.
>+ All methods declared in an interface (i.e., without a method body) are implicitly
considered to be abstract. If you want, you can explicitly use the abstract qualifier
for the method.
>+ Default methods must have a method body. Default methods must be qualified
using the default keyword. The classes implementing the interface inherit the
default method definitions and they can be overridden.
>+ A default method can be overridden in a derived class as an abstract method; for
such overriding, the @Override annotation can also be used.
>+ You cannot qualify default methods as synchronized or final.
>+ Static methods must have a method body and they are qualified using the static
keyword.
>+ You cannot provide abstract keyword for static methods: Remember that you
cannot override static methods in derived classes, so it’s conceptually not possible to
leave static methods abstract by not providing a method body.
>+ You cannot use default keyword for static methods because all default methods are
instance methods.
###### #10
>+ Annotate functional interfaces with @FunctionalInterface. Without that, if the
functional interface is improper (e.g., it has two abstract methods), the compiler will
not issue any errors.
>+ You can use the @FunctionalInterface annotation only for interfaces and not for
classes, enums, and so on.
>+ A derived interface can be a functional interface if it has only one abstract method or
inherits only one abstract method.
>+ For a functional interface, declaring methods from Object class in an interface does
not count as an abstract method.
###### #11
>+ Lambda expressions can occur only in the contexts where assignment, function calls,
or casts can occur.
>+ A lambda function is treated as a nested block. Hence, just like a nested block, we
cannot declare a variable with the same name as a local variable in the enclosing
block.
>+ Lambda functions must return values from all the branches—otherwise it will result
in a compiler error.
>+ When argument types are declared, the lambda is known as “explicitly typed”; if they
are inferred, it is “implicitly typed.”
>+ What happens if a lambda expression throws an exception? If it is a checked
exception, then the method in the functional interface should declare that;
otherwise it will result in a compiler error.
