# Stacle (object)
The primitive *object* representing a stationary object ([obstacle](./obstacle.md)) or a moving object ([substacle](./substacle.md)) that blocks a route/path/way of a thingy.  The converse of a [ject](./ject.md).

```mermaid
    flowchart LR
    ob(ob) <--> stacle([stacle])
    sub(sub) <--> stacle
    stacle --> obstacle(obstacle)
    stacle --> substacle(substacle)
    ob <--> ject(ject)
    sub <--> ject
    ject --> object(object)
    ject --> subject(subject)
```
<div style="text-align: right"><sub>Stacle & Ject Hierarchy</sub></div>

<a name="declaration"></a>
## Declaration
The default declaration of the `stacle` *object* is to at least provide a *moniker*. A type (`{ob}` or `{sub}`) can be provided at declaration using curly brackets (`{}`). The derived *objects* can be declared by name. The `cellphone` object can also be declared by casting `mobot`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_stacle(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_stacle({`*`ob`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_stacle({`*`sub`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_ob({stacle},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_sub({stacle},`*`moniker`*`);`

<a name="declare_assign"></a>
## Declaration & Assignment

<a name="reference"></a>
## Referencing
Referencing a `stacle` *object* is achieved with the `with` verb (or shortened `>_`), or the shortened `(`*`stacle_moniker`*`)` syntax using brackets (`()`). For inside *expressions* use square brackets (`[]`) as in `[`*`stacle_moniker`*`]`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_stacle(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_stacle(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`stacle_moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `⟦`*`…`*`[`*`stacle_moniker`*`]`*`…`*`⟧`

<a name="type"></a>
## Typing
There are only two types of stacles: `{ob}` representing obstacles, stationary objects that block a thingy's path; and, `{sub}` representing substacles, moving objects that black a thingy's path.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_stacle({`*`ob`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_stacle({`*`ob`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_stacle(`*`moniker`*`)_type(`*`ob`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_stacle({`*`sub`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_stacle({`*`sub`*`},`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_stacle(`*`moniker`*`)_type(`*`sub`*`);`

<a name="cast"></a>
## Casting

<a name="posit"></a>
# Posits

<a name="operate"></a>
# Operators