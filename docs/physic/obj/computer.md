# Computer (object)
The `computer` *object* (also shortened syntax of `pc`) is a derived `sobot`, representing is a multi-purpose desktop microcomputer whose size, capabilities, and price make it feasible for individual use.

```mermaid
    flowchart LR
    thingy((thingy)) --> robot([robot])
    robot --> sobot(sobot)
    sobot --> computer{{computer}}
```
<div style="text-align: right"><sub>Computer Hierarchy</sub></div>

<a name="declaration"></a>
## Declaration
The default declaration of the `computer` *object* is to at least provide a *moniker*. The shortened syntax of `pc` can be used freely and interchangeably. There are no *types* of the `computer` *object*. The `computer` object can also be declared by casting `sobot`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_computer(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_pc(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_sobot({computer},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_sobot({pc},`*`moniker`*`);`

<a name="referencing"></a>
## Referencing
To reference `computer`, use, either the `with` verb or the shortened syntax using brackets (`()`).  The type is implied from the declaration, or can be cast when referenced.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_computer(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_pc(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`computer_moniker`*`);`

## Posits

| `posit` | description | API |
| --- | --- | ---- |
| <a name="_opsys"></a> `_opsys()`<br>`_opsys(`*`op_sys`*`)` | Provide / declares the operating system(s) of the computer. | [opsys](../prop/opsys.md#computer) |
| <a name=""></a> `_()`<br>`_(`*` `*`)` | Provide / declare the . | [](../prop/.md#computer) |
| <a name=""></a> `_()`<br>`_(`*` `*`)` | Provide / declare the . | [](../prop/.md#computer) |
| <a name=""></a> `_()`<br>`_(`*` `*`)` | Provide / declare the . | [](../prop/.md#computer) |