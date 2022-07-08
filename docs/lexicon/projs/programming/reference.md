# Referencing

## Referencing Functions

```diego
// traditional anonymous function
add_funct()_arg(a)
    with_funct(a)_ret([a]+100);
;

// one line anonymous function
add_funct()_arg(a)_ret([a]+100);

// Arrow function breakdown

// [1] Remove the word verb-object `add_funct`
()(a)_ret([a]+100);

// [2] Remove the brackets and the posit `_ret` is implied
()(a)[a]+100;



````

```diego
add_funct(x)
    ()_arg(a,b);
    ()_ret([a]+[b]);
;

add_var(result)_funct(x)_arg(1,2);      // result = 3 variant

with_funct()_ret({int);
with_var(result)_funct(x)_arg(1,2);
// result = 3 integer
// a = 1
// b = 2

add_funct(c)_arg(d)_ret([d]*2);
with_var(result)_funct(x)_arg()_funct(c)_arg(3)_v(2);
// result = 8 integer
// a = c = 6
// b = 2
// c = d = 6
// d = 6

with_var(result)_funct(x)_arg()_function(c)_arg()_var(e)_v(3)_v(2);
// result = 8 integer
// a = c = 6
// b = 2
// c = 6
// d = e = 3
// e = 3

with_var(e)_push(1);    
// using `push` converts integer to integer stack (or queue, or array)

with_var(result)_funct(x)_arg()_function(c)_arg()_stack(e)_v(2);
// result = 8,4 integer stack
// a = c = 6,2
// b = 2
// c = 6,2
// d = e = 3,1
// e = 3,1


```
<!-- (result)_(x)_(c)_(3)_(2);-->

## Referencing Variables
Referencing variables is achieved using the verb-object `with_var`, or implied `with_var` with the use of `()` and `[]` brackets, and combinations of.

When referencing variables the use of `()` brackets refers to the name of the variable.  Using the `[]` brackets refers to value of the variable to be the variable name.  Using the square brackets nested inside brackets, `([])`, refers the to variable name which can be manipulated.  Use of `[[]]` refers to the value to the variable name to the value of the variable to be the name of the variable.

For example:

```diego
add_var(a);                     // a = undefined variant
add_var({int}b);                // b = undefined integer 

with_var(a)_value(0);           // a = 0 variant
with_var({int}a)_v(1);          // a = 1 integer
with_var([a])_v(2);             // a = 2 integer

with_var[a]_v(3);               
// same as `with_var(3)_v(3);`
// callee will ask `with_var(3)_askdec();`

(a)_v(3);                       // a = 3 integer    // same as `add_var(a)_v(3);`
([a])_v(4);                     // a = 4 integer    // same as `add_var([a])_v(4);`

[a]_v(5);
// same as `with_var(3)_v(5);`
// callee will ask `with_var(3)_askdec();`

(a)_calc([a]+1);                // a = 5

add_var({str}varname)_v(a);
with_var[varname]_v(6);         // a = 6 integer
[varname]_inc();                // a = 7 integer    // same as `with_var(a)_inc();`

with_var([a]+1);                // a = 6 integer
with_var([a]+1)_v(7);           // a = 8 integer

with_var([[varname]]+1);        // a = 9 integer
with_var[[varname]]_inc();      // a = 10 integer
with_var([varname]+1);          // varname = "a1"

with_var({double},a)_v(11);     // a = 11.0 double

(varname)_v(a)_inc(2);          // varname = "c"    // same as `with_var(a)_v(a)_inc(2);`
with_var(varname)_v(b);         // varname = "b"
with_var[varname]_v(0);         // b = 0
([varname])_v(1);               // b = 1            // same as `with_var(b)_v(1);`
```