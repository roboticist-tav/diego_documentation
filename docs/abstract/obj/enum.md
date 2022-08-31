# Enumeration (object) / Enumerator (object) / Enumerator (function)
The `enum` *object* contains a list of static immutable enumerators with a *key* (usually an integer) and an *enumerator value* (usually an explicit string).

<a name="declare"></a>
## Declaration
Enumerators can be declared using the `add_` verb (or shortened `+_`), with or without explicit values. When declared without explicit values the default datatypes of `⟪{int}⟫` for keys, and `⟦{str}⟧` for values are used, however, this syntax is  dynamically typed, so datatypes will change upon assignment. Key datatype declarations are enclosed in angled and curly brackets (`⟪{}⟫`), and value datatype declarations are enclosed in expression and curly brackets (`⟦{}⟧`). Multiple `enum`s cannot be declared in a single declaration.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_enum(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_enum(⟪{`*`key_datatype`*`}⟫,⟦{`*`value_datatype`*`}⟧,`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_enum(⟪{`*`key_datatype`*`}⟫,`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_enum(⟦{`*`value_datatype`*`}⟧,`*`moniker`*`);`<br>

<a name="declare_assign"></a>
## Declaration & Assignment




&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_calc(⟦`*`expression1`*`⟧,⟦`*`expression2`*`⟧,⟦`*`...`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_calc(`*`moniker`*`,⟦`*`expression`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_calc(`*`moniker1`*`,⟦`*`expression1`*`⟧,`*`moniker2`*`,⟦`*`expression2`*`⟧,`*`moniker...`*`,⟦`*`expression...`*`⟧);`

  If a moniker is used with an expression, the expression must be enclosed in expression brackets (`⟦⟧`) or double square brackets (`[[]]`).

```diego
add_enum(⟪{int}⟫,⟦{str}⟧,urgency)
    ()_enum(⟪4⟫,⟦emergent⟧)_static(URGENCY_EMERGENT)_colour(red)_color({hex},#ca0031)_desc(The most urgent (critical) state, severe risk.);
    ()_enum(⟪3⟫,⟦exigent⟧)_static(URGENT_EXIGENT)_colour(orange)_color({hex},#ff6400)_desc(The high urgent state, high risk.);
    ()_enum(⟪2⟫,⟦urgent⟧)_static(URGENT_URGENT)_colour(yellow)_color({hex},#fce001)_desc(The elevated urgent state, elevated risk.);
    ()_enum(⟪1⟫,⟦infergent⟧)_static(URGENT_INFERGENT)_colour(blue)_color({hex},#3566cd)_desc(The low urgent state, low / guarded risk.);
    ()_enum(⟪0⟫,⟦nonurgent⟧)_static(URGENT_NON)_colour(green)_color({hex},#009a66)_desc(The non-urgent state, negligible risk.);
;
Without explicit values (and dynamic typing):

add_enum(fruits,⟦apple,banana,cherry⟧);
```






---

<a name="seealso"></a>
## See Also

* Similar objects: [`flag`](./flag.md)
* Enumerations in Diego on [Rosetta Code](https://rosettacode.org/wiki/Enumerations#Diego)
