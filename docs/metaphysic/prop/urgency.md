# Urgency (enumerator)
The `❬urgency❭` enumerator provides five levels of urgency for an action to take place to resolve the five levels of risk.

| `⟪key⟫` | `⟦enum⟧` | `[STATIC]` | `hex` &nbsp; `RGB` | description |
| --- | --- | --- | --- | --- |
| <a name="emergent"></a> `⟪4⟫` | `⟦emergent⟧` | `[URGENCY_EMERGENT]` | <span class="tl tl-sq tl-ca0031"></span> `#ca0031` &nbsp; `#ca0031ff` | The most urgent (critical) state, severe risk. |
| <a name="exigent"></a> `⟪3⟫` | `⟦exigent⟧` | `[URGENT_EXIGENT]` | <span class="tl tl-sq tl-ff6400"></span> `#ff6400` &nbsp; `#ff6400ff` | The high urgent state, high risk. |
| <a name="urgent"></a> `⟪2⟫` | `⟦urgent⟧` | `[URGENT_URGENT]` |<span class="tl tl-sq tl-fce001"></span> `#fce001` &nbsp; `#fce001ff` | The elevated urgent state, elevated risk. |
| <a name="infergent"></a> `⟪1⟫` | `⟦infergent⟧` | `[URGENT_INFERGENT]` | <span class="tl tl-sq tl-3566cd"></span> `#3566cd` &nbsp; `#3566cdff` | The low urgent state, low / guarded risk. |
| <a name="nonurgent"></a> `⟪0⟫` | `⟦nonurgent⟧` | `[URGENT_NON]` |  <span class="tl tl-sq tl-009a66"></span> `#009a66` &nbsp; `#009a66ff` | The non-urgent state, negligible risk. |


```diego
add_enum(⟪{int}⟫,⟦{str}⟧,urgency)
    ()_enum(⟪4⟫,⟦emergent⟧)_static(URGENCY_EMERGENT)_colour(red)_color({hex},#ca0031)_desc(The most urgent (critical) state, severe risk.);
    ()_enum(⟪3⟫,⟦exigent⟧)_static(URGENT_EXIGENT)_colour(orange)_color({hex},#ff6400)_desc(The high urgent state, high risk.);
    ()_enum(⟪2⟫,⟦urgent⟧)_static(URGENT_URGENT)_colour(yellow)_color({hex},#fce001)_desc(The elevated urgent state, elevated risk.);
    ()_enum(⟪1⟫,⟦infergent⟧)_static(URGENT_INFERGENT)_colour(blue)_color({hex},#3566cd)_desc(The low urgent state, low / guarded risk.);
    ()_enum(⟪0⟫,⟦nonurgent⟧)_static(URGENT_NON)_colour(green)_color({hex},#009a66)_desc(The non-urgent state, negligible risk.);
;

add_enum(fruits,⟦apple,banana,cherry⟧);

```