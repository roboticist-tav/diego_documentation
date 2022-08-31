ject(ob)
ject(sub)

# Signs

Signs are using in traffic object recognition.

## Instincts

Current instincts availble for sign are in `apt_instinct(sign);`

```diego
\*
** Instincts for `sign`
** {"version":"1.0"}
** 
*/

// All `sign`s are obs
with_ject(ob)_toobject(sign);

// Provide best-matching class if non-existant
with_sign()_posit(class)_exists(false)?;
? with_sign()_class(other);

// Provide locale
with_sign()_locale()_me();


```
V4UMW+AV
idontcare1234567@

| object | notes |
| --- | --- |
| `vision`, `fov` | field of view, a 3d spacial zone where pose from camera position and angle range should trigger a find, fix, finish procedure. |


with_vision()_current()?:

use the vectors of the current vision to determine which signs to find, fix and finish.

fov - field of view also: vision
vision -




`vector(`*`x`*`, `*`y`*`, `*`z`*`, `*`magnitude-value`*`)_magnitude(`*`scalar`*`)_unit(`*`unit`*`)`

`vector(23.42335, -28.44076, 0.20290, 64.3)_magnitude(cadence)_unit(rpm)`





PIOSEE

PIOSEE - Acronym for decision making.

P - Problem identify

I - Information anailable

O - Options

S - Select option

E - Execute option

E - Evaluate


begin_poisee()_prob()_info()_opt()_select()_exec()_eval();



end_poisee();



