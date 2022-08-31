# List (object)
A database-assigned collection type call *moniker* assigned exclusively from database queries.





```diego

use_me();

add_list(accts)_sql(SELECT CreatedById, CreatedDate, LastModifiedById, 
                       LastModifiedDate, BillingCity 
                       FROM Account 
                       WHERE Name='Acme' OR Name='Salesforce');

add_ary({id},acctCreator)_list(accts)_ofsql([CreatedById]);

add_list(creators)_sql(SELECT FirstName, LastName
                        FROM User
                        WHERE Id IN:[acctCreator] );

log_console(List of account creators: [])_list(creators)_calc([FirstName]&' '&[LastName]);
// List of account creators: James Bond, Sherlock Holmes, Oliver Twist

reset_me();

```

<a name="declare"></a>
## Declaration

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_(`*`moniker`*`);`<br>

<a name="declare_assign"></a>
## Declaration & Assignment

<a name="initial"></a>
## Initialisation

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_(`*`moniker`*`);`<br>

<a name="assign"></a>
## Assignment

<a name="reference"></a>
## Referencing
Referencing a ` ` *object* is achieved with the `with` verb, or the shortened `(`*` `*`)` syntax. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_(`*`moniker1`*`,`*`moniker2`*`,`*`...`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`_moniker`*`);`

<a name="type"></a>
## Typing

<a name="get"></a>
## Getting

<a name="set"></a>
## Setting

<a name="cast"></a>
## Casting

<a name="properties"></a>
## Properties

<a name="example"></a>
## Examples
