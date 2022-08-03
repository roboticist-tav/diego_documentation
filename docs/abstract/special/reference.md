# Reference (special)
Referencing *objects* in ***Diego*** 


```diego
add_int(integerA)_v(0);

// with reference
with_int(integerA)_inc(1);
// 1

// is identical to...
// with reference with whitespace
with_int(integerA)
    _inc(1)
;
// 2

// () shorthand reference
(integerA)_inc(1);
// 3

// () sub reference (this), implied and named
(integerA)
    ()_inc(1);
    ()_calc(++1);
    (integerA)_calc(--1);
;
// 4 -> 5 -> 4

// [] variable reference (this in expressions) implied
(integerA)_calc([]++);
// 5

// [] variable reference (this in expressions) named
(integerA)_calc([integerA]++);
// 6
```


