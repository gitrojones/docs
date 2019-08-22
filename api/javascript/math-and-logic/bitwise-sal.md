---
layout: api-command
language: JavaScript
permalink: api/javascript/bitwise-sal/
command: bitSal
io:
    -   - number
        - number
related_commands:
    bitwise-or: bitwise-or/
    bitwise-and: bitwise-and/
    bitwise-xor: bitwise-xor/
    bitwise-not: bitwise-not/
    bitwise-sar: bitwise-sar/
---

# Command syntax #

{% apibody %}
value.bitSal(number) &rarr; value
{% endapibody %}

# Description #

Bitwise Shift Left (<<) the bits of one number with another, returning the shifted result of those numbers.

The `bitSal` command can be called in either prefix or infix form; both forms are equivalent.

__Example:__ 55 << 5 = 1760

```js
> r.expr(55).bitSal(5).run(conn, callback)
// result passed to callback
110111 << 5 -> 11011100000
IE. 1760
```

__Example:__ Infix form

```js
> r.bitSal(55, 5).run(conn, callback);
// result passed to callback
110111 << 5 -> 11011100000
IE. 1760
```
