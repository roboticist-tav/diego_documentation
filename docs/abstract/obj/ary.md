# Array (object)
The `array` object, as with arrays in other programming languages, enables storing a collection of multiple items under a single variable name, and has members for performing common array operations.

## Sytnax
The default declaration of the `arrat` object is to at least provide a *moniker*. With no datatype provided, the `{variant}` datatype is implied. The shortened form `ary` can be used.  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_ary(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_array(`*`moniker`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_ary({`*`datatype`*`},`*`moniker`*`)`

All arrays are dynamic and mutable, they can be declared with a fixed length but this is not enforced. Any value given with no value will return as `undefined` when referenced.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_ary(`*`moniker`*`)_len(`*`length`*`)`

Arrays tend to be based from zero, however, this all depends upon the thingy's upbringing, set with `set_numbase(`*`numbase`*`)`. The caller can declare the number base.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_ary(`*`moniker`*`)_base(`*`numbase`*`);`

Assignment of array is allowed at declaration, initialisation, and post-declaration. The `_value`, and, `_set` posits are used for assignment, their equivalent syntax, `_values`, `_v` are identical and can be used freely and interchangeably. The `set_` verb can also be used to the same effect as the `_set` posit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_ary(`*`moniker`*`)_value(`*`val`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_array(`*`moniker`*`)_values(`*`val1`*`,`*`val2`*`,`*`…`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`arraymoniker`*`)_set(`*`val1`*`,`*`val2`*`,`*`…`*`)`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `set_ary(`*`moniker`*`,`*`val1`*`,`*`val2`*`,`*`…`*`)`

Values can be assigned at different indexes using the `_at` posit.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_ary(`*`moniker`*`)_at(`*`index`*`)_v(`*`val`*`)`

Arrays have various properties and methods…

## Posits

| method | description |
| --- | -------- |
| <a name="arity"></a> `_arity()` | Provides the number of elements in the array |
| <a name="at"></a> `_at(`*`index`*`)`<br>`_at()` | Provides the element at index *index* |
| <a name="concat_a"></a> `_concat()`<br>`_concatenate()` | Merges proceeding *objects* (*arrays*) with proceeding *objects* (*arrays*) |
| <a name="concat_b"></a> `_concat(`*`arymoniker`*`)`<br>`_concatenate(`*`arymoniker`*`)` | Merges array *arymoniker* with preceeding *objects* (*arrays*) |
| <a name="concat_c"></a> `_concat(`*`arymoniker1`*`,`*`arymoniker1`*`,`*`…`*`)`<br>`_concatenate(`*`arymoniker1`*`,`*`arymoniker1`*`,`*`…`*`)` | Merges arrays *arymonikers* with preceeding *objects* (*arrays*) |
| <a name="copyin_a"></a> `_copyin(`*`targetindex`*`)` |  Shallow copies all elements of the preceeding array into the same array from index without modifying its length  |
| <a name="copyin_b"></a> `_copyin(`*`targetindex`*`,`*`startindex`*`)` |  Shallow copies part of the preceeding array to another location in the same array without modifying its length  |
| <a name="copyin_c"></a> `_copyin(`*`targetindex`*`)`<br>`_copyin(`*`targetindex`*`,`*`startindex`*`)`<br>`_copyin(`*`targetindex`*`,`*`startindex`*`,`*`endindex`*`)` |  Shallow copies part of the preceeding array to another location in the same array without modifying its length  |
| <a name="dt"></a> `_dt({`*`datatype`*`)` | Cast / convert proceeding *objects* (*arrays*)  |
| <a name="len_a"></a> `add`*`<…>`*`_len(`*`length`*`)`<br>`add`*`<…>`*`_length(`*`length`*`)` | Sets the number of elements in the array at declaration |
| <a name="len_b"></a> `_len(`*`length`*`)`<br>`_length(`*`length`*`)` | Destructively resizes the array |
| <a name="lens"></a> `_lens(`*`arymoniker`*`)` | Declares a sub-view block of array called *moniker* |
| <a name="oflens_a"></a> `_oflens(`*`length`*`)` | Sets a specifc sub-view block of the array to *length*  |
| <a name="oflens_b"></a> `_oflens(`*`startindex`*`,`*`endindex`*`)` | Sets a specific sub-view block of the array from *startindex* to *endindex*  |
| <a name="todict"></a> `_todict()`<br>`_todict(`*`moniker`*`)` | Provides a new `dict` object from preceeding *array* uses a numeric iterator |
| <a name>



add_check(isBelowThreshold)_param()_test([]<30);
add_check(Are)
add_ary(array1)_v(1, 30, 39, 29, 10, 13);

log_console()_ary(array1)_every(isBelowThreshold);


// Create a new dynamic array with length zero, variant and/or mixed datatypes
add_array(myEmptyArray);

// Create a new dynamic array with length zero, of integers with no mixed datatypes
add_array({int},myIntegerArray);
 
// Create a new fixed-length array with length 5
add_array(myFiveArray)_len(5)_base(0);   // The value base '_base(0)' is usually defaulted to zero, depends upon thing. 

// Create an array with 2 members (length is 2) 
add_ary(myStringArray)_value(Item1,Item2);   // '_array' can be shortened to '_ary'
 
// Assign a value to member [2]
with_ary(myChangeArray)_at(2)_v(5);    // '_value' can be shortened to '_v'
 
// Add a member to an array with the push function (defaulted at end), length increased by one
[myExpandedArray]_push()_v(9);    // 'with_ary(…)' can be shortened to '[…]'
[myExpandedArray]_append()_v(9);

// Add a member to an array with the push function (at a location), length increased by one
[myExpandedArray]_pushat(3)_v(8);
 
// Remove a member to an array with the pop function (defaulted at end), length reduced by one
[myExpandedArray]_pop();

// Remove a member to an array with the pop function (at a location), length reduced by one
[myExpandedArray]_popat(3);

// Swap a member to an array with the swap function
[myExpandedArray]_swapfrom(2)_swapto(6);
[myExpandedArray]_swap(2, 6);






// Rectiline a member in an array
[MyCaterpillarArray]_rectilat(4)_rectilup(2);
[MyCaterpillarArray]_rectilup(4, 2);
[MyCaterpillarArray]_rectilat(5)_rectildown(3);
[MyCaterpillarArray]_rectildown(5, 3);

// Null a member to an array with the pluck function (defaulted at end)
[myExpandedArray]_pluck();

// Null a member to an array with the pluck function (at a location)
[myExpandedArray]_pluckat(3);

// Get size of array
[mySizableArray]_size();    // '_len()' can also be used
[myMultidimensialArray]_size()

// Retrieve an element of an array
[myArray]_at(3);
[myArray]_first();    // Retrieve first element in an array
[myArray]_last();     // Retrieve last element in an array

// More transformations of arrays (like append, union, intersection) are available

// For multi-dimensional array use the 'matrix' object

set_matrixorder(row-major);    // set major order as row- or column-major order depends on the thing
set_handrule(right);           // set hand-rule, most things will use right hand-rule

// Create a new dynamic two-dimensional array with length zero, variant and/or mixed datatypes
add_matrix(myMatrix)_dim(2);

// Create a new dynamic three-dimensional array with length zero, of integers with no mixed datatypes
add_matrix({int}my3DEmptyMatrix)_dim(3);
 
// Convert an array to a matrix by adding a new dimension with length zero, variant and/or mixed datatypes
with_array(MyConvertedArray)_dim();    // Should now use '_matrix' object rather than '_array'
with_array(MyConvertedArray)_dim(3);   // Add three dimensions to array, should now use '_matrix' object rather than '_array'

// Create a new fixed-length traditional (2D) matrix with 5 rows and 4 columns
add_matrix(myMatrix)_rows(5)_columns(4);
add_matirx(myMatrix)_subs(5, 4);  // check or set major order first

// Create a new fixed-length mutil-dimensional matrix with 5 rows, 4 columns, 6 subscripts, and 8 subscripts 
add_matrix(myMatrix)_rows(5)_columns(4)_subs(6)_subs(8);
add_mat(myMatrix)_subs(5, 4, 6, 8);  // check or set major order first, '_matrix' can be shortened to 'mat'

// Create a 4 x 4 identiy matrix:
add_mat(myIdentityMatrix)_subs(4, 4)_identity();    // …or…

add_mat(myMorphedMatrix)_subs(4, 4)
with_mat(myMorphedMatrix)_trans(morph)_identity();   // More transformations available
 
// Assign a value to member [2,4]
with_mat(myMatrix)_row(2)_col(4)_value(5);    // …or…
with_mat(myMatrix)_at(2, 4)_v(5);    // check or set major order first
 
// Add a member(s) to a matrix using push functions is available
// Remove a member(s) from a matrix with the pop functions is available
// Swap a member(s) in a matrix with the swap functions is available

// Rectiline a single member in a three-dimensional matrix
[MyWobbleMatrix]_rectilat()_row(3)_col(3)_sub(3)_rectilto()_row(-1)_col(1)_sub(0);    // …or…
[MyWobbleMatrix]_rectilat(3, 3, 3)_rectilto(-1, 1, 0);    // check or set major order first, …or…
[MyWobbleMatrix]_rectilat(3, 3, 3)_rectilleft(1)_rectilup(1);    / check or set hand-rule, …or…

// Also 'crab', 'elevate', 'slide' and 'pump' movements are available
// Also 'row', 'pitch', and 'yaw' movements are available
// Also, quaternions calculations are available
// Null a member in a matrix using pluck functions is available

// Get size of a matrix
mat(mySizableMatrix)_size();    // will return an array of the size()
[myMultidimensialArray]_len();  // '_len()' can also be used

// Retrieve an element of a matrix
[myMatrix]_at(3, 2);
[myArray]_first()_atsub(2);    // Retrieve first element of a row/column/subscript of a matrix
[myArray]_last()_atsub(2);     // Retrieve last element of a row/column/subscript of a matrix
[myArray]_origin();    // Retrieve first element in a matrix
[myArray]_end();       // Retrieve last element in a matrix

reset_ns[];</lang>
