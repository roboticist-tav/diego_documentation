# Arrangement (object)
An associative data type, as an extension of an array with negative length acting as a *history* of plucked or popped elements.

## Sytnax
The default declaration of the `arran`gement object is to at least provide a *moniker*. With no datatype provided for values the `{variant}` datatype is implied. The datatype of the values can be declared at declaration. `arran` has are several shortened terms, `arn`, `arrangem`, `arrangement`, which can be used freely and interchangabily. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_arran(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_arn(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_arrangem(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_arrangement({`*`valdt`*`},`*`moniker`*`)`

## Posits

| posit | description |
| --- | -------- |
| <a name="arity"></a> `_arity()` | Provides the number of elements in full extend of the arran, both negative and positive |
| <a name="at"></a> `_at(`*`index`*`)`<br>`_at()` | Provides the element at index *index* |
| <a name="concat_a"></a> `_concat()`<br>`_concatenate()` | Concatenates proceeding *objects* with proceeding *objects* |
| <a name="concat_b"></a> `_concat(`*`arymoniker`*`)`<br>`_concatenate(`*`arymoniker`*`)` | Merges array *arymoniker* with preceeding *objects* (*arrays*) |
| <a name="concat_c"></a> `_concat(`*`arymoniker1`*`,`*`arymoniker1`*`,`*`...`*`)`<br>`_concatenate(`*`arymoniker1`*`,`*`arymoniker1`*`,`*`...`*`)` | Merges arrays *arymonikers* with preceeding *objects* (*arrays*) |
| <a name="copyin_a"></a> `_copyin(`*`targetindex`*`)` |  Shallow copies all elements of the preceeding array into the same array from index without modifying its length  |
| <a name="copyin_b"></a> `_copyin(`*`targetindex`*`,`*`startindex`*`)` |  Shallow copies part of the preceeding array to another location in the same array without modifying its length  |
| <a name="copyin_c"></a> `_copyin(`*`targetindex`*`)`<br>`_copyin(`*`targetindex`*`,`*`startindex`*`)`<br>`_copyin(`*`targetindex`*`,`*`startindex`*`,`*`endindex`*`)` |  Shallow copies part of the preceeding array to another location in the same array without modifying its length  |
| <a name="dt"></a> `_dt({`*`datatype`*`)` | Cast / convert proceeding *objects* (*arrays*)  |
| <a name="len_a"></a> `add`*`<...>`*`_len(`*`length`*`)`<br>`add`*`<...>`*`_length(`*`length`*`)` | Sets the number of elements in the array at declaration |
| <a name="len_b"></a> `_len(`*`length`*`)`<br>`_length(`*`length`*`)` | Destructively resizes the array |
| <a name="lens"></a> `_lens(`*`arymoniker`*`)` | Declares a sub-view block of array called *moniker* |
| <a name="oflens_a"></a> `_oflens(`*`length`*`)` | Sets a specifc sub-view block of the array to *length*  |
| <a name="oflens_b"></a> `_oflens(`*`startindex`*`,`*`endindex`*`)` | Sets a specific sub-view block of the array from *startindex* to *endindex*  |
| <a name="todict"></a> `_todict()`<br>`_todict(`*`moniker`*`)` | Provides a new `dict` object from preceeding *array* uses a numeric iterator |



```diego

add_arran({int},arran1)_v(1,2,3,4,5,6,7,8);

log_console()_(arran1);           // 1,2,3,4,5,6,7,8
log_console()_(arran1)_len();     // 8
(arran1)_pop();
log_console()_(arran1);           // 8|1,2,3,4,5,6,7
log_console()_(arran1)_len();     // 7
log_console()_(arran1)_arity();   // 8
(arran1)_pop()_pop()_pip();
log_console()_(arran1);           // 7,8|1,2,3,4,5,6
```


add_arrangem()
add