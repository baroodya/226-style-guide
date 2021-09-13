Throwing exceptions is also likely a new topic for you in this course. 
Exceptions are very simple: they act as a way to let the use know what
went wrong in the running of the program so that the user can (hopefully)
remedy the problem. For this reason, it is of the utmost importance that
your exceptions are specific and accurate. 

Let's consider a basic division function for the sake of example: the function 
`div(double num, double denom)` takes two arguments and divides `num` by `denum`.
In this function, we would want to check that the arguments are appropriate for
the operation using `if...throw` statements:

```
public double div(double num, double denom) {
   if (denom == 0.0) throw IllegalArgumentExeption("Denominator cannot equal " + denom + ".");

   ...
}
```

This statement is **Good Style** because it specifically tells the user that the `denom` argument was the one that caused the Exception; it also lets the user know that `0.0` is an Illegal Argument, rather than alerting for some other error. Finally, the function only checks for `denom == 0.0`, because `num` can be `0.0` with no consequences. 

The following are examples of **Bad Style**:

```
public double div(double num, double denom) {
   if (denom == 0.0) throw BaseException();

   ...
}
```
This is bad style because the exception is generic. The user will have no idea as to why the code is failing to run properly.

```
public double div(double num, double denom) {
   if (denom == 0.0) throw Null­Pointer­Exception();

   ...
}
```
This is bad style because the exception is inaccurate. The user will search for a null pointer rather than an illegal argument and likely will not be able to solve the problem without contacting the developer.
