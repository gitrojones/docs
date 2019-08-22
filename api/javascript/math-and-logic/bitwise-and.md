---
layout: api-command
language: JavaScript
permalink: api/javascript/bitwise-and/
command: bitAnd
io:
    -   - number
        - number
related_commands:
    bitwise-or: bitwise-or/
    bitwise-xor: bitwise-xor/
    bitwise-not: bitwise-not/
    bitwise-sal: bitwise-sal/
    bitwise-sar: bitwise-sar/
---

# Command syntax #

{% apibody %}
value.bitAnd(value[, value, ...]) &rarr; value
{% endapibody %}

# Description #

Bitwise AND (&) the bits of two or more numbers together, returning the binary result as a number.

The `bitAnd` command can be called in either prefix or infix form; both forms are equivalent.

__Example:__ 55 & 5 = 5

```js
> r.expr(55).bitAnd(5).run(conn, callback)
// result passed to callback
110111
000101
------
000101
IE. 5
```

__Example:__ Use [args](/api/javascript/args) with `bitAnd` to bitwise-and multiple values.

```js
> vals = [55, 5, 15, 11];
> r.bitAnd(r.args(vals)).run(conn, callback);
// result passed to callback
110111
000101
001111
001011
------
000001
IE. 1
```
