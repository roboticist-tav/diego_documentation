# String (object)
The `str` (or lengthened `string`) primitive *object* provides a sequence of characters, as a variable.

<a name="declare"></a>
## Declaration
Although the most common use of the `str` expression is via a posit, it can be declared using the `add_` verb (or shortened `+_`). Since the `str` *object* is expressive the be expression brackets (`⟦⟧`) or double square brackets (`[[]]`) can be used directly, i.e. in place of the brackets (`()`). Multiple `str`s are declared using a coma-separated list of *`moniker`* s.  If a moniker is used with an expression, the expression must be enclosed in expression brackets (`⟦⟧`) or double square brackets (`[[]]`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_str(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_txt(`*`moniker1`*`,`*`moniker2`*`,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_txt⟦`*`expression`*`⟧;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_txt(⟦`*`expression1`*`⟧,⟦`*`expression2`*`⟧,⟦`*`…`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_txt(`*`moniker`*`,⟦`*`expression`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_txt(`*`moniker1`*`,⟦`*`expression1`*`⟧,`*`moniker2`*`,⟦`*`expression2`*`⟧,`*`moniker…`*`,⟦`*`expression…`*`⟧);`

The common declaration of the `txt` object is via posit syntax.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_text(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_txt(`*`moniker1`*`,`*`moniker2`*`,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_txt⟦`*`expression`*`⟧;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_txt(⟦`*`expression1`*`⟧,⟦`*`expression2`*`⟧,⟦`*`…`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_txt(`*`moniker`*`,⟦`*`expression`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *`<object>`*`_txt(`*`moniker1`*`,⟦`*`expression1`*`⟧,`*`moniker2`*`,⟦`*`expression2`*`⟧,`*`moniker…`*`,⟦`*`expression…`*`⟧);`