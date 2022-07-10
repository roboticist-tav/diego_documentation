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
