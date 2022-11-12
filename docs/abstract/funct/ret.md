# Return (function)
The return function (`return`, or shortened as `ret`) returns the output of the proceeding *object* to the preceding *object*.

## Syntax
The `ret` function comes in two forms: an expression, returning the result of the expression (and any porceeding *object* output) and returning the result to the preceding *object*. The other form is as a gate passing the result of the proceeding *objects* to the preceding *objects*, with no interfering expression.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_ret(`*`expression`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_ret(`*`expression`*`)_`*`….`*`;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_ret()_`*`….`*`;`


# Example
The `ret` function is an expression function.  When left parameter-less the `ret` function will act as gate passing the result of the proceeding *objects* to the preceding *objects*.

```diego
add_funct({int},addplus)_param({int},a,b)_ret()_param(a)_plus(b);

add_funct({int},addcalc)_param({int},a,b)_ret()_calc([a]+[b]);

add_funct({int},addret)_param({int},a,b)_ret([a]+[b]);

add_funct({int},addvar)_param({int},a,b)
    add_var({int},return)_calc([a]+[b]);
    ()_ret([return]);
;
```







```cpp
int result = 0;              // Declare and initialize an integer.
double coefficient = 10.8;   // Declare and initialize a floating
                             // point value.
auto name = "Lady G.";       // Declare a variable and let compiler
                             // deduce the type.
auto address;                // error. Compiler cannot deduce a type
                             // without an intializing value.
age = 12;                    // error. Variable declaration must
                             // specify a type or use auto!
result = "Kenny G.";         // error. Can’t assign text to an int.
string result = "zero";      // error. Can’t redefine a variable with
                             // new type.
int maxValue;                // Not recommended! maxValue contains
                             // garbage bits until it is initialized.
```

```diego
{int}(result)_(0);           // Declare and initialize an integer.
{double}(coefficient)_(10.8);// Declare and initialize a floating
                             // point value.
{}(name)_(Lady G.);       // Declare a variable and let compiler
                             // deduce the type.
{}(address);                // error. Compiler cannot deduce a type
                             // without an intializing value.
{}(age)_(12);                    // error. Variable declaration must
                             // specify a type or use auto!
result = "Kenny G.";         // error. Can’t assign text to an int.
string result = "zero";      // error. Can’t redefine a variable with
                             // new type.
int maxValue;                // Not recommended! maxValue contains
                             // garbage bits until it is initialized.
```
