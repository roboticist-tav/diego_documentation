# Language Syntax

## Simple Command

Diego is a very structured instructional language and follows a strict syntax.  It is also executes commands synchronously by the terminator `;` keysymbol.  The common and most simplified command syntax is:
```Diego
{verb}_{object}({moniker|uuid});
```
The command will do `{verb}` to an `{object}` *type* identified as `{moniker|uuid}`.  The Diego engine will initiate this command and then move on to the next command immediately, it will not wait for the command to return success (`1` or `true`) or failure (`0` or `false`).  To catch a response to the command, wait for the command to finish the developer will need to use the *'elvish'* operator.

## The Elvish Operator

The elvish operator is a word pun on the [Elvis Operator](https://en.wikipedia.org/wiki/Elvis_operator) as it is similar *-ish* to the Elvis operator.  Here are some variations of syntax of a command using the elvish operator:

```Diego
{verb}_{object}({moniker|uuid}) ? ;
{verb}_{object}({moniker|uuid}) ? : ;
{verb}_{object}({moniker|uuid}) : ;
{verb}_{object}({moniker|uuid}) ? {verb}_{object}({moniker|uuid});
{verb}_{object}({moniker|uuid}) ? {verb}_{object}({moniker|uuid}) : ;
{verb}_{object}({moniker|uuid}) ? : {verb}_{object}({moniker|uuid}) ;
{verb}_{object}({moniker|uuid}) ? {verb}_{object}({moniker|uuid}) : {verb}_{object}({moniker|uuid});
{verb}_{object}({moniker|uuid}) : {verb}_{object}({moniker|uuid});
```

The first three command syntaxes are semantically the same, however, the second syntax (`{verb}_{object}({moniker|uuid}) ? : ;`) is preferred as it provides placeholders for future use.

The full asynchronous command syntax is as follows:

```Diego
{verb}_{object}({moniker|uuid}) ? {verb}_{object}({moniker|uuid}) : {verb}_{object}({moniker|uuid});

{go_diego command} ? {hey_diego command} : {oh_diego command};
```
When the elvish operator is used the Diego engine will initiate and wait for completion of the command (asynchronous).  Upon completion of the first command (known as the *'go_deigo command'*) any successful result(s) will be passed to the next command after the `?` operator, this command is known as the *'hey_diego command'*. Similarly any failures/failed results/errors will be passed to the *'oh_diego'* command, after the `:` operator.  Unless otherwise set, the default process of all commands that use the elvish operator (`?` and/or `:`) if one or more `valid` objects are provided for successes and one or more `err` object provided for failures/errors.

## Child Commands

The *go_diego*, *hey_diego*, and *oh_diego* commands can have objects children 

## Sibling Commands

The *hey_diego* and *oh_diego* commands can have siblings identified using the `|` operator.  Each sibling command is initiated synchronously unless an elvish operator is used. The *go_diego* command cannot have any siblings. For ease-of-reading whitespace can be used, for example:

```Diego
{go_diego command} ? {hey_diego command}
                   | {sibling hey_diego command} ? :
                   : {oh_diego command}
                   | {sibling oh_diego command};
```

## Nesting Commands

Commands can be nested to the *n*th level, however, for ease-of-reading it is recommended to encapsulate nested commands into `instruct`s.  Examples:

```Diego
{go_diego command} ? {hey_diego command}
                            ? {nested hey_diego-hey_diego command}
                            : {nested hey_diego-oh_diego command}
                   : {oh_diego command}
                            ? {nested oh_diego-hey_diego command}
                            : {nested oh_diego-oh_diego command};

{go_diego command} ? {hey_diego command}
                            ? {nested hey_diego-hey_diego command}
                                ? {nested hey_diego-hey_diego-hey_diego command}
                                : {nested hey_diego-hey_diego-oh_diego command}
                            : {nested hey_diego-oh_diego command}
                                ? {nested hey_diego-oh_diego-hey_diego command}
                                : {nested hey_diego-oh_diego-oh_diego command}
                   : {oh_diego command}
                            ? {nested oh_diego-hey_diego command}
                                ? {nested oh_diego-hey_diego-hey_diego command}
                                : {nested oh_diego-hey_diego-oh_diego command}
                            : {nested oh_diego-oh_diego command}
                                ? {nested oh_diego-oh_diego-hey_diego command}
                                : {nested oh_diego-oh_diego-oh_diego command};

{go_diego command} ? {hey_diego command}
                            ? {nested hey_diego-hey_diego command}
                            : {nested hey_diego-oh_diego command}
                   : {oh_diego command}
                            ? {nested oh_diego-hey_diego command}
                            : {nested oh_diego-oh_diego command}
                   | {sibling hey_diego command}
                            ? {nested sibling hey_diego-hey_diego command}
                            : {nested sibling hey_diego-oh_diego command}
                   : {sibling oh_diego command}
                            ? {nested sibling oh_diego-hey_diego command}
                            : {nested sibling oh_diego-oh_diego command};

{go_diego command} ? {instruct} : {instruct};
```

## Recursive Commands

```Diego
begin_funct(fact)_param(n,int);
    proviso(n)_equals(0) ? with_funct()_this()_return(1);
    add_calc(nwith_funct()_this()_return(1);
end_funct(fact);

```

