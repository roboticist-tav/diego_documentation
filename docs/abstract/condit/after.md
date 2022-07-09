# After (condition)
A temporal condit used to determine if the preceeding *object* is _after_ the provided [date](/abstract/dt/date.md) \| [datetime](/abstract/dt/datetime.md) for proceeding *object* to do proceeding *action*. `after` functions as a boolean return switch, returning `true` if the condition is met.

When no matching datatype (`{date}`, `{datetime}`, or, `{time}`) of the preceeding *object* is provided the current datetime of the callee (`_now()`) is used in the condition expression.

## Syntax

`_after(`*`date`*`)`<br>
`_after(`*`datetime`*`)`<bR>
`_after(`*`time`*`)`