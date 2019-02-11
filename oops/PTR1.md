###### #1
>+ Overload resolution takes place entirely at compile time (not at runtime).
>+ You cannot overload methods with the methods differing in return types alone.
>+ You cannot overload methods with the methods differing in exception specifications
alone
>+ For overload resolution to succeed, you need to define methods such that the
compiler finds one exact match. If the compiler finds no matches for your call or
if the matching is ambiguous, the overload resolution fails and the compiler issues
an error.

###### #2
>+ The main() method, where the main execution of the program starts, is always
declared static. Why? If it were an instance method, it would be impossible to invoke
it. You’d have to start the program to be able to create an instance and then call the
method, right?
>+ You cannot override a static method provided in a base class. Why? Based on the
instance type, the method call is resolved with runtime polymorphism. Since static
methods are associated with a class (and not with an instance), you cannot override
static methods, and runtime polymorphism is not possible with static methods.
>+ A static method cannot use the this keyword in its body. Why? Remember that static
methods are associated with a class and not an instance. Only instance methods
have an implicit reference associated with them; hence class methods do not have a
this reference associated with them.
>+ A static method cannot use the super keyword in its body. Why? You use the super
keyword for invoking the base class method from the overriding method in the
derived class. Since you cannot override static methods, you cannot use the super
keyword in its body.
>+ Since static methods cannot access instance variables (nonstatic variables), they are
most suited for utility functions. That’s why there are many utility methods in Java.
For example, all methods in the java.lang.Math library are static.
>+ Calling a static method is considered to be slightly more efficient compared to calling
an instance method. This is because the complier need not pass the implicit t
