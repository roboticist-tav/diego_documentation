# Mobot (object)
A `mobot` is a conveyed `thing`, that is not self-propelled, but interacts physically in the physical world, such as a [cell phone](./cellphone.md).

The `mobot` is derived from a `thing`, and a `thing` is derived from `thingy`. This is depicted in the 'Mobot Hierarchy'.
```mermaid
    flowchart LR
    thingy([thingy]) --> thing([thing])
    thing --> mobot
    mobot --> cellphone{{cellphone}}
    mobot --> watch{{smartwatch}}
    mobot --> laptop{{laptop}}
```
<div style="text-align: right"><sub>Mobot Hierarchy</sub></div>

## Declaration
The default declaration of the `mobot` *object* is to at least provide a *moniker*. A type can be provided at declaration using curly brackets (`{}`). The derived *objects* can be declared by name.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_mobot(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_mobot({`*`type`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_cellphone(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_watch(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_laptop(`*`moniker`*`);`

## Referencing
To reference the `mobot`, use, either the `with` verb or the shortened syntax using brackets (`()`).  The type is implied from the declaration, or can be cast when referenced.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_mobot(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_mobot({`*`type`*`,`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_cellphone(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_watch(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_laptop(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`sobot_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`cellphone_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`watch_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`laptop_moniker`*`);`

## Posits

| method | description | API |
| --- | -------- | --- |
| <a name="_ident"></a> `_ident()` | Provides or sets identity information. | [ident](#ident) |

### Ident