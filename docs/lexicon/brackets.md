# Brackets

| Brackets | description |
| --- | --- |
| `()` | **Moniker Brackets**<br>Monikers, groups of statements, references to objects. |
| `[]` | **Square Brackets**<br>Values of variables, references to values. |
| `{}` | **Curly Brackets**<br>Types and datatypes. |
| `❬❭` | **Angle Brackets**<br>Units and formats. |
| `⟪⟫` | **Double Angle Brackets**<br>Keys and indexes. |
| `⟦⟧` | **Double Square Brackets**<br>Expressions, values and conditions. |

```diego

add_var({dbl},{0.2},myDouble,⟦21.34⟧);
add_dbl(myOtherDistance);
with_dbl(myOtherDistance)_v⟦22.877⟧;
add_distan(❬m❭,myDistance,[myDouble]);
(myDistance)_calc(myCalc,⟦[myInt]+4⟧);
()_calc⟦[]]-0.12⟧;
add_dict(myDistances,⟪{int}⟫,⟦{dbl⟧)
    ()_dict(⟪0⟫,⟦myDistance⟧);
    ()_dict(⟪0⟫,⟦21.09⟧);
    ()_dict(⟪0⟫,[myOtherDistance]);
;
```

In the first statement, `add_var({dbl},{0.2},myDouble,⟦21.34⟧);` the brackets (`()`) enclose all the comma-separated,declarations of the new variable called `myDouble`. This is an abstract statement. The curly brackets in `{dbl}` provide the datatype of the variable `myDouble`. The next curly brackets (`{0.2}`)declare the precision or format of `myDouble`, as zero-leading for values less than one (1) and rounded to two (2) decimal places. The `myDouble` is the moniker of the new variable. The value initial assignment of 21.34 is enclosed inside double square brackets (`⟦21.34⟧`) as an expression. 

After this declaration the `myDouble` variable can be called using the `with_dbl` (or `width_double`) verb-object statement.

In, `add_distan(❬m❭,myDistance,[myDouble]);` we are declaring a metaphysical distance object (`distan`) called `myDistance`.

They all keep history

var*iable* - mutable  - returns only last one
val*uable* - immutable - return first one
array      - mutable - no history returns remaining
arran      - immutable (sort of) - return history and remaining - no changes, no re-indexing (only pip and pop) 
tup*le*    - mutable - returns history and remaining - all changes accepted.


`ca6c0845b685d0a3357fb4d37ad6723d9bc6609f|1,2,3,4,5,6`   - initialisation

`27444ec1dc916e6e436d45cae0541f65fbfa9ea4,ca6c0845b685d0a3357fb4d37ad6723d9bc6609f|1,3,3,4,5,6`    - 2 -> 3

`2744,ca6c|1,3,3,4,5,6`    - 2 -> 3

1,2,7,8|3,3,3,4,5,6    - 1 -> 3
3,1,2,7,8|3,3,1,4,5,6    - 3 -> 1


arity()_picto()

arity()_pitco({full})
arity(⟪h:ca6c0845b685d0a3357fb4d37ad6723d9bc6609f⟫)_who()
arity(⟪h:ca6c⟫)_who()
arity(⟪0⟫)_who()


|1,2,3,4,5,6,7,8

4(5)⟦6⟧|1,2,3,4,6,6,7,8


tup*le* - keeps history as array

```
add_var(var1);
add_val(val1);
add_tup(van1);

>_(var1,⟦1⟧);
>_(val1,⟦1⟧);
>_(van1,⟦1⟧);

log_console()_text("var1: "&[var1]&", val1: "&val1]&", van1: "&[van1]);
// var1: 1, val1: 1, van1: 1

>_(var1,⟦2⟧);
>_(val1,⟦2⟧); // with_val(val1)_err(a243,`val1` has already been initialised)
>_(van1,⟦2⟧);

log_console()_text⟦"var1: "&[var1]&", val1: "&[val1]&", van1: "&[van1]⟧;
// var1: 2, val1: 1, van1: 1,2

log_console()_text⟦"var1: " & arity([var1]) & ", val1: " & arity(val1) & ", van1: " & arity(van1)⟧;
// var1: 1|2, val1: 2|1, van1: |1,2


add_int(int1,{var},⟦1,2,3,4⟧); // value = 4; arity = 1,2,3|4
add_int(int1,{val},⟦1,2,3,4⟧); // value = 1; arity = 4,3,2|1
add_int(int1,{tup},⟦1,2,3,4⟧); // value = 1,2,3,4; arity = |1,2,3,4


```



