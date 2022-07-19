# Computer (object)
The `computer` *object* is a derived `sobot`, representing is a multi-purpose desktop microcomputer whose size, capabilities, and price make it feasible for individual use.

```mermaid
    flowchart LR
    thingy((thingy)) --> robot([robot])
    robot --> sobot(sobot)
    sobot --> computer{{computer}}
```
<div style="text-align: right"><sub>Computer Hierarchy</sub></div>

<a name="declaration"></a>
## Declaration
The default declaration of the `computer` *object* is to at least provide a *moniker*. A type can be provided at declaration using curly brackets (`{}`). The derived *objects* can be declared by name. The `computer` object can also be declared by casting `sobot`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_computer(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_computer({`*`type`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_sobot({computer},`*`moniker`*`);`

<a name="referencing"></a>
## Referencing
To reference `computer`, use, either the `with` verb or the shortened syntax using brackets (`()`).  The type is implied from the declaration, or can be cast when referenced.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_computer(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_computer({`*`type`*`,`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`computer_moniker`*`);`

<a name="types"></a>
## Types
The [*types*](../../metaphysic/prop/type.md#computer) of `computer` are realised through the operating system the computer runs on. There are only four defined `computer` *types*.

| `{type}` | description | API |
| --- | --- | --- |
| <a name="win"></a>  `{win}` | Microsoft&reg; Windows&#8482;. | [win](#type) |
| <a name="android"></a> `{osx}` &nbsp; `{os_x}` | Apple&reg; OS X&#8482;. | [osx](#type) |
| <a name="linux"></a> `{linux}` | Linux.  | [linux](#type) |
| <a name=""></a> `{chrome}` &nbsp; `{chrome}` &nbsp; `{chrome_os}` | Google&reg; Chrome OS&#8482;. | [chrome](#type) |


## Posits

| `posit` | description | API |
| --- | --- | ---- |
| <a name="_opsys"></a> `_opsys()`<br>`_opsys(`*`op_sys`*`)` | Provide / declare the operating system of the computer. | [opsys](../prop/opsys.md#computer) |
| <a name=""></a> `_()`<br>`_(`*` `*`)` | Provide / declare the . | [](../prop/.md#computer) |
| <a name=""></a> `_()`<br>`_(`*` `*`)` | Provide / declare the . | [](../prop/.md#computer) |
| <a name=""></a> `_()`<br>`_(`*` `*`)` | Provide / declare the . | [](../prop/.md#computer) |