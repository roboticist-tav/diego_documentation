# Flag (object)
The `flag` *enumerator object* contains a multi-selectable list of static immutable bitwise enumerators with a *key* (positive signed integer of power of two ($2^n$)) and an *enumerator value* (an explicit string). There are no *types* of `flag`s.

<a name="declare"></a>
## Declaration
Flag enumerators can be declared using the `add_` verb (or shortened `+_`), with or without explicit values. The key and value datatypes are set at `⟪{2ⁿ}⟫` for keys, and `⟦{str}⟧` for values. Multiple `flag`s cannot be declared in a single declaration.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_flag(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_flag(`*`moniker`*`);`<br>

<a name="declare_assign"></a>
## Declaration & Assignment
For quick assignment at declaration, the key values can be omitted, and they will be dynaically created.  Otherwise, provide the key-value pairs using angled brackets for keys (`⟪⟫`), and expression brackets (`⟦⟧`) for values. Two patterns can be applied: key-value pairs; or, key-value groups. The key must follow the power of two ($2^n$), starting from one (`1`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_flag(`*`moniker`*`,⟦`*`value`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_flag(`*`moniker`*`,⟦`*`value1`*`,`*`value2`*`,`*`value...`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_flag(`*`moniker`*`,⟪1⟫,⟦`*`value`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_flag(`*`moniker`*`,⟪1,2,4`*`...`*`⟫,⟦`*`value1`*`,`*`value2`*`,`*`value...`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `+_flag(`*`moniker`*`,⟪1⟫,⟦`*`value1`*`⟧,⟪2⟫,⟦`*`value2`*`⟧,⟪4⟫,⟦`*`value`*`⟧,`*`...`*`);`

<a name="assign"></a>
## Assignment
Assignment after declaration is achieved using the `with_` verb (or shortened `>_`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_flag(`*`moniker`*`,⟦`*`value`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_flag(`*`moniker`*`,⟦`*`value1`*`,`*`value2`*`,`*`value...`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_flag(`*`moniker`*`,⟪1⟫,⟦`*`value`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_flag(`*`moniker`*`,⟪1,2,4`*`...`*`⟫,⟦`*`value1`*`,`*`value2`*`,`*`value...`*`⟧);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_flag(`*`moniker`*`,⟪1⟫,⟦`*`value1`*`⟧,⟪2⟫,⟦`*`value2`*`⟧,⟪4⟫,⟦`*`value`*`⟧,`*`...`*`);`

<a name="cast"></a>
## Casting
The `flag` *object* can be safely cast to a `enum` object. Casting from an `enum` object to `flag` object, will re-index the keys, if the key from the `enum` do not follow power of 2 datatype (`⟪{2ⁿ}⟫`).

<a name="property"></a>
## Properting
There are key-value associated posit properties of the `flag` *object*.

<a name="posit"></a>
## Posits

| `posit` | description | API |
| --- | --- | --- |
| <a name="keys"></a> `_keys` | Provides an array of keys, in input order. | [keys](../prop/keys.md) |

<a name="example"></a>
## Example

```diego
add_flag(ape,⟦gorilla,chimpanzee,orangutan⟧);
log_console()_(ape);
// ⟪1⟫,⟦gorilla⟧,⟪2⟫,⟦chimpanzee⟧,⟪4⟫,⟦orangutan⟧
```
<!-- http://net-informations.com/faq/netfaq/flags.htm -->