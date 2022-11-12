# Calculation (expression)
The `calc` *expressive object* provides a numeric output using a variety of numeric related expressions.

<a name="declare"></a>
## Declaration
Although the most common use of the `calc` *expressive object* is via a posit, it can be declared using the `add_` verb (or shortened `+_`). Since the `calc` *object* is expressive the expression brackets (`⟦⟧`) or double square brackets (`[[]]`) can be used directly, i.e. in place of the brackets (`()`). Multiple `calc`s are declared using a coma-separated list of *`moniker`* s.  If a moniker is used with an expression, the expression must be enclosed in expression brackets (`⟦⟧`) or double square brackets (`[[]]`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_calc(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_calc(`*`moniker1`*`,`*`moniker2`*`,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_calc⟦`*`expression`*`⟧;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_calc(⟦`*`expression1`*`⟧,⟦`*`expression2`*`⟧,⟦`*`…`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_calc(`*`moniker`*`,⟦`*`expression`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_calc(`*`moniker1`*`,⟦`*`expression1`*`⟧,`*`moniker2`*`,⟦`*`expression2`*`⟧,`*`moniker…`*`,⟦`*`expression…`*`⟧);`

The common declaration of the `calc` object is via posit syntax.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_calc(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_calc(`*`moniker1`*`,`*`moniker2`*`,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_calc⟦`*`expression`*`⟧;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_calc(⟦`*`expression1`*`⟧,⟦`*`expression2`*`⟧,⟦`*`…`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_calc(`*`moniker`*`,⟦`*`expression`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_calc(`*`moniker1`*`,⟦`*`expression1`*`⟧,`*`moniker2`*`,⟦`*`expression2`*`⟧,`*`moniker…`*`,⟦`*`expression…`*`⟧);`

<a name="reference"></a>
## Referencing
Referencing a `calc` *object* is achieved with the `with` verb (or shortened `>_`), or the shortened `(`*`calculation_moniker`*`)` syntax. For inside *expressions* use square brackets (`[]`) as in `[`*`stacle_moniker`*`]`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_calc(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_calc(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`calculation_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `⟦`*`…`*`[`*`calculation_moniker`*`]`*`…`*`⟧`

<a name="assign"></a>
## Assignment
Only other expressions can be assigned to the `calc` *object*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_calc(⟦`*`moniker`*`⟧,`*`expression`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(⟦`*`calculation_moniker`*`⟧,`*`expression`*`);`
_format
_unit()

<a name="type"></a>
## Typing

<a name="cast"></a>
## Casting

<a name="posit"></a>
# Posits

<a name="operate"></a>
# Operators

<a name="arithmetic"><a>
## Arithmetic Operators

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_calc⟦`*`…`*`+`*`…`*`⟧;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_calc⟦`*`…`*`-`*`…`*`⟧;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_calc⟦`*`…`*`*`*`…`*`⟧;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_calc⟦`*`…`*`×`*`…`*`⟧;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_calc⟦`*`…`*`/`*`…`*`⟧;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_calc⟦`*`…`*`÷`*`…`*`⟧;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_calc⟦`*`…`*`%`*`…`*`⟧;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_calc⟦`*`…`*`𝐦`*`…`*`⟧;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_calc⟦`*`…`*`𝐦(`*`sub_expression`*`)`*`…`*`⟧;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `_calc⟦`*`…`*`𝐦𝐨𝐝(`*`sub_expression`*`)`*`…`*`⟧;`