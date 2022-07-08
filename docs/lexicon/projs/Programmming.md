Programmming

### case

```Diego

case_Robot(alif)_metric(airtemp) ?????;
    ? when


```

# Variables

https://rosettacode.org/wiki/Variables






Scope

For globally-scoped variable (known as cloud scope)

add_var(_variablename_)_toglobal();    // variant datatype
add_var(_variablename_)_datatype(_datatype_)_toglobal();
add_var({_datatype_}, _variablename_)_toglobal();

// mist-scoped variable
    // variant datatype
add_var(_variablename_)_datatype(_datatype_);
add_var({_datatype_}, _variablename_);

// local-scoped variable (known as thingy scope)
add_var(_variablename_)_me();    // variant datatype
add_var(_variablename_)_datatype(_datatype_)_me();
add_var({_datatype_}, _variablename_)_me();

// Note variable names can be reused, the thingy will have to workout from context which variablename to use, or ask for clarification


// Initialisation

add_var(_variablename_)_value(_value_)

add_var(a)_value(0)_datatype(_datatype_);

// local-scoped variable
add_var(b)_values(0)_me();

// global scope
with_var(a, b, c);

// declare
add_var(a, b, c)_dtype(int);
add_int(a, b, c);



add_var(a, b, c)_dtype(int, string);


begin_instruct(A + B);
    ask_me()_prompt(enter A number)_var(a)_restrictrange(-1000, 1000);
    ask_me()_prompt(enter B number)_var(b)_restrictrange(-1000, 1000);
    print_me()_valof(a)_msg( )_valof(b);
    print_me()_calcof(a+b);
end_instruct(A + B);

exec_instruct(A + B)_me();

# Formatted Numeric Output

https://rosettacode.org/wiki/Formatted_numeric_output

```Diego
print_me()_valof(7.125)_format(%09.3f)_n();
print_me()_valof(7.125)_format(%09.3f)_notat(west)_n();
print_me()_valof(7.125)_format(%09.3f)_notat(euro)_n();
```
Output
00007.125
00007.125
00007,125



| Test | Example |
|---|---|
| show version | `print_version()_me();` |
| implicit prologue | _none_ |
| hello world | `print_me()_msg(Hello World!);` |
| file suffixes | .dgo |
| statement separator | `;` |
| block delimiters | `begin_`<br>...<br>`end_` |
| end-of-line comment | 










