---
layout: api-command
language: JavaScript
permalink: api/javascript/bitwise-sar/
command: bitSar
io:
    -   - number
        - number
related_commands:
    bitwise-or: bitwise-or/
    bitwise-and: bitwise-and/
    bitwise-xor: bitwise-xor/
    bitwise-not: bitwise-not/
    bitwise-sal: bitwise-sal/
---

# Command syntax #

{% apibody %}
value.bitSar(number) &rarr; value
{% endapibody %}

# Description #

Bitwise Shift Right (>>) the bits of one number with another, returning the shifted result of those numbers.

The `bitSar` command can be called in either prefix or infix form; both forms are equivalent.

__Example:__ 55 >> 5 = 1

```js
> r.expr(55).bitSar(5).run(conn, callback)
// result passed to callback
110111 >> 5 -> 000001
IE. 1
```

__Example:__ Infix form

```js
> r.bitSar(55, 5).run(conn, callback);
// result passed to callback
110111 >> 5 -> 000001
IE. 1
```
