###### Implement encapsulation
>+	 Encapsulation: Combining data and the functions operating on it as a single unit.
>+	 You cannot access the private methods of the base class in the derived class.
>+	 You can access the protected method either from a class in the same package (just
like package private or default) as well as from a derived class.
>+	 You can also access a method with a default access modifier if it is in the same
package.
>+	 You can access public methods of a class from any other class.
###### Implement inheritance including visibility modifiers and composition
>+	 Inheritance: Creating hierarchical relationships between related classes. Inheritance
is also called an "IS-A" relationship.
>+	 You use the super keyword to call base class methods.
>+	 Inheritance implies IS-A and composition implies HAS-A relationship.
>+	 Favor composition over inheritance.
###### Implement polymorphism
>+	 Polymorphism: Interpreting the same message (i.e., method call) with different
meanings depending on the context.
>+	 Resolving a method call based on the dynamic type of the object is referred to as
runtime polymorphism.
>+	 Overloading is an example of static polymorphism (early binding) while overriding is
an example of dynamic polymorphism (late binding).
>+	 Method overloading: Creating methods with same name but different types and/or
numbers of parameters.
>+	 You can have overloaded constructors. You can call a constructor of the same class in
another constructor using the this keyword.
>+	 Overload resolution is the process by which the compiler looks to resolve a call when
overloaded definitions of a method are available.
>+	 In overriding, the name of the method, number of arguments, types of arguments,
and return type should match exactly.
>+	 In covariant return types, you can provide the derived class of the return type in the
overriding method.
###### Override hashCode, equals, and toString methods from Object class
>+	 You can override clone(), equals(), hashCode(), toString() and finalize()
methods in your classes. Since getClass(), notify(), notifyAll(), and the
overloaded versions of wait() method are declared final, you cannot override these
methods.
>+	 If you’re using an object in containers like HashSet or HashMap, make sure you
override the hashCode() and equals() methods correctly. For instance, ensure that
the hashCode() method returns the same hash value for two objects if the equals()
method returns true for them.
###### Create and use singleton classes and immutable classes
>+	 A singleton ensures that only one object of its class is created.
>+	 Making sure that an intended singleton implementation is indeed singleton is a
nontrivial task, especially in a multi-threaded environment.
>+	 Once an immutable object is created and initialized, it cannot be modified.
>+	 Immutable objects are safer to use than mutable objects; further, immutable objects
are thread safe; further, immutable objects that have same state can save space by
sharing the state internally.
>+	 To define an immutable class, make it final. Make all its fields private and final.
Provide only accessor methods (i.e., getter methods) but don’t provide mutator
methods. For fields that are mutable reference types, or methods that need to mutate
the state, create a deep copy of the object if needed.
###### Develop code that uses static keyword on initialize blocks, variables, methods, and classes
>+	 There are two types of member variables: class variables and instance variables.
All variables that require an instance (object) of the class to access them are
known as instance variables. All variables that are shared among all instances and
are associated with a class rather than an object are referred to as class variables
(declared using the static keyword).
>+	 All static members do not require an instance to call/access them. You can directly
call/access them using the class name.
>+	 A static member can call/access only a static member of the same class.
