# Brackets

| Brackets | description |
| --- | --- |
| `()` | **Moniker Brackets**<br>Moniker allocation or groupings of statements or reference of moniker. |
| `[]` | **Square Brackets**<br>Value reference of variable. |
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

In the first statement, `add_var({dbl},myDouble,⟦21.34⟧);` the brackets (`()`) enclose all the comma-separated,declarations of the new variable called `myDouble`. This is an abstract statement. The curly brackets in `{dbl}` provide the datatype of the variable `myDouble`. The next curly brackets (`{0.2}`)declare the precision or format of `myDouble`, as zero-leading for values less than one (1) and rounded to two (2) decimal places. The `myDouble` is the moniker of the new variable. The value initial assignment of 21.34 is enclosed inside double square brackets (`⟦21.34⟧`).

After this declaration the `myDouble` variable can be called using the `with_dbl` (or `width_double`) verb-object statement.

In, `add_distan(❬m❭,myDistance,[myDouble]);` we are declaring a metaphysical distance object (`distan`) called `myDistance`.
