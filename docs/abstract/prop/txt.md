# Text (expression)
The `txt` (or lengthened `text`) *expressive object* provides a _portion_ of written text.

<a name="declare"></a>
## Declaration
Although the most common use of the `txt` expression is via a posit, it can be declared using the `add_` verb (or shortened `+_`). Since the `txt` *object* is expressive the be expression brackets (`⟦⟧`) or double square brackets (`[[]]`) can be used directly, i.e. in place of the brackets (`()`). Multiple `txt`s are declared using a coma-separated list of *`moniker`* s.  If a moniker is used with an expression, the expression must be enclosed in expression brackets (`⟦⟧`) or double square brackets (`[[]]`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_text(`*`moniker`*`);`<br>
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

<a name="reference"></a>
## Referencing
Referencing a `txt` *object* is achieved with the `with` verb (or shortened `>_`), or the shortened `(`*`text_moniker`*`)` syntax. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_txt(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_txt(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`text_moniker`*`);`

<a name="assign"></a>
## Assignment
Only other expressions can be assigned to the `calc` *object*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_calc(⟦`*`moniker`*`⟧,`*`expression`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(⟦`*`calculation_moniker`*`⟧,`*`expression`*`);`
_format
_unit()

# Operators

| `operator` | description | API |
| --- | --- | --- |
| <a name="[]"></a> *`…`*`[`*`variable_moniker`*`]`*`…`* | Variable call. | [variable](../special/var.md) |
| <a name="{}"></a> *`…`*`{`*`object_moniker`*`}`*`…`* &nbsp; *`…`*`{`*`object_moniker`*`.`*`child_object_moniker`*`}`*`…`* &nbsp; *`…`*`{`*`object_moniker`*`.`*`child_object_moniker`*`.`*`property_moniker`*`}`*`…`*  | Object call. | [object](./obj/object.md) |
| <a name="_r"></a> *`…`*`\n`*`…`*  | New line. | [](/md) |
| <a name="_n"></a> *`…`*`\r`*`…`* | Carriage return. | [](/md) |
| <a name="emoji"></a> *`…`*`:`*`emoji_moniker`*`:`*`…`* | Emoji. | [emoji](../special/emoji.md) |
| <a name=""></a> *`…`*`$`*`math_sub-expression`*`$`*`…`* | Maths. | [math](../funct/math.md) |
| <a name=""></a> *`…`*` `*`…`* | . | [](/md) |
| <a name=""></a> *`…`*` `*`…`* | . | [](/md) |
| <a name=""></a> *`…`*` `*`…`* | . | [](/md) |



<a name="posit"></a>
# Posits

| posit | description | API |
| --- | -------- | --- |
| <a name="chapter"> `_chapter` | A key-value `dict` dipicting the main division dict, with number (`key`) and 


 a line of metrical writing

text([first_name] [last_name]\n[mailing_street]\n[city])
// John Zimmmermann
// 1 Home Street
// Home City



```diego

add_txt(The_Count_of_Monte_Cristo);

with_txt(The_Count_of_Monte_Cristo)
    add_txt({en},⟦When Dantès returned next morning to the chamber of his companion in captivity, he found Faria seated and looking composed. In the ray of light which entered by the narrow window of his cell, he held open in his left hand, of which alone, it will be recollected, he retained the use, a morsel of paper, which, from being constantly rolled into a small compass, had the form of a cylinder, and was not easily kept open. He did not speak, but showed the paper to Dantès.⟧)
        ()_vol(1)_chapter([18],The Treasure)_para(1);
    add_txt⟦Lorsque Dantès rentra le lendemain matin dans la chambre de son compagnon de captivité, il trouva Faria assis, le visage calme.
    Sous le rayon qui glissait à travers l’étroite fenêtre de sa cellule, il tenait ouvert dans sa main gauche, la seule, on se le rappelle, dont l’usage lui fût resté, un morceau de papier, auquel l’habitude d’être roulé en un mince volume avait imprimé la forme d’un cylindre rebelle à s’étendre.⟧
        ()_vol(1)_chapter([18],Le Trésor)_para(1,2)_lang(fr);
    ;
;

log_console()_(The_Count_of_Monte_Cristo)_i()_wordcount();  // 87,72
log_console()_(The_Count_of_Monte_Cristo)_i(0)_charcount(); // 468
log_console()_(The_Count_of_Monte_Cristo,[1])_paracount();   // 2
log_console()_chapter(The Treasure)_wordlenavg();  // 4.4
log_console()_chapter[18]_syllablecount();  // 120,115
```

<!-- https://wordcounter.net/ -->