# Variable (object) / Variant (object)
The `var` object is the primitive one-dimensional storage *object*, also known as just the 'variable' or the 'variant' (after the default implied datatype).

<a name="declare"></a>
## Declaration
The default declaration of the `var` (or lengthened `variable`) *object* is to use the `add_` verb (or shortened `+_`) and provide a *datatype* (optional) and a *moniker*. Multiple `var`s are declared using a coma-separated list of *`moniker`* s. If not datatype is provided the variable is classed as a `variant` and will be dynamically typed.  All expressions must be enclosed in expression brackets (`⟦⟧`) or double square brackets (`[[]]`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_variable({`*`datatype`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_var({`*`datatype`*`},`*`moniker1`*`,`*`moniker2`*`,`*`...`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_var(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_var(`*`moniker1`*`,`*`moniker2`*`,`*`...`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_var(`*`moniker`*`,[[`*`expression`*`]]);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_var(`*`moniker1`*`,⟦`*`expression1`*`⟧,`*`moniker2`*`,⟦`*`expression2`*`⟧,`*`moniker...`*`,⟦`*`expression...`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_var({`*`datatype`*`},`*`moniker`*`,⟦`*`expression`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_var({`*`datatype`*`},`*`moniker1`*`,⟦`*`expression1`*`⟧,`*`moniker2`*`,⟦`*`expression2`*`⟧,`*`moniker...`*`,⟦`*`expression...`*`⟧);`

