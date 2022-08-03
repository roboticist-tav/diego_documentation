# Room (object)
The 'room' *object* is a representation of a physical enclosed space.

<a name="declaration"></a>
## Declaration
The default declaration of the `room` *object* is to at least provide a *moniker*. There are no *types* of the `room` *object*.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_room(`*`moniker`*`);`

<a name="referencing"></a>
## Referencing
To reference `room`, use, either the `with` verb or the shortened syntax using brackets (`()`).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_room(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`room_moniker`*`);`

<a name="verbs"></a>
## Verbs

| `verb_` | Description | API |
| --- | --- | --- |
| <a name="enter"></a> `enter_` | The proceeding *room* has the adjacent *object* entering (or will enter) into the proceeding *room* | [enter](../verb/enter.md#room) |
| <a name="exit"></a> `exit_` | The proceeding *room* has the adjacent *object* exiting (or will exit) out of the proceeding *room* | [exit](../verb/exit.md#room) |


<a name="properties"></a>
## Properties

| `property` | Description | API |
| --- | --- | --- |
| <a name="shape"></a> `shape` | Shape of the room | [shape](../../metaphysic/funct/shape.md#room) |
| <a name="width"></a> `width` | Width (length on x-plane) of the room | [width](../../metaphysic/prop/width.md#room) |
| <a name="length"></a> `length` | Length (length on y-plane) of the room | [length](../../metaphysic/propr/length.md#room) |
| <a name="height"></a> `height` | Height (length on z-plane) of the room | [height](../../metaphysic/prop/height.md#room) |