---
layout: api-command
language: JavaScript
permalink: api/javascript/bitwise-xor/
command: bitXor
io:
    -   - number
        - number
related_commands:
    bitwise-or: bitwise-or/
    bitwise-and: bitwise-and/
    bitwise-not: bitwise-not/
    bitwise-sal: bitwise-sal/
    bitwise-sar: bitwise-sar/
---

# Command syntax #

{% apibody %}
value.bitXor(value[, value, ...]) &rarr; value
{% endapibody %}

# Description #

Bitwise XOR (⊕) the bits of two or more numbers together, returning the binary result as a number.

The `bitXor` command can be called in either prefix or infix form; both forms are equivalent.

__Example:__ 55 ⊕ 5 = 50

```js
> r.expr(55).bitXor(5).run(conn, callback)
// result passed to callback
110111
000101
------
110010
IE. 50
```

__Example:__ Use [args](/api/javascript/args) with `bitXor` to bitwise-xor multiple values.

```js
> vals = [55, 5, 15, 11];
> r.bitXor(r.args(vals)).run(conn, callback);
// result passed to callback
110111
000101
001111
001011
------
110110
IE. 54
```
