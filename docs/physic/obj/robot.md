# Robot (object)
The `robot` *object* is a derived [`thingy`](./thingy.md), representing a self-propelled thingy in the physical 'real' world.

```mermaid
    flowchart LR
    thingy((thingy)) --> robot([robot])
```
<div style="text-align: right"><sub>Robot Hierarchy</sub></div>

<a name="declaration"></a>
## Declaration
The default declaration of the `robot` *object* is to at least provide a *moniker*. There are no *types* of the `robot` *object*. The `robot` object can also be declared by casting `thingy`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_robot(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_thingy({robot},`*`moniker`*`);`

<a name="referencing"></a>
## Referencing
To reference `robot`, use, either the `with` verb or the shortened syntax using brackets (`()`).  The type is implied from the declaration, or can be cast when referenced.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_robot(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`robot_moniker`*`);`

## Posits

| `posit` | description | API |
| --- | --- | ---- |
| <a name="_opsys"></a> `_opsys()`<br>`_opsys(`*`operating_system`*`)` | Provide / declares the operating system(s) of the robot. | [opsys](../../metaphysic/prop/opsys.md#robot) |
| <a name="opframe"></a> `_opframe()`<br>`_opframe(`*`operating_framework`*`)` | Provide / declare the operating framework of the robot. | [opframe](../../metaphysic/prop/opframe.md#robot) |
| <a name=""></a> `_()`<br>`_(`*` `*`)` | Provide / declare the . | []() |
| <a name=""></a> `_()`<br>`_(`*` `*`)` | Provide / declare the . | []() |