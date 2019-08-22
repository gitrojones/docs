---
layout: api-command
language: JavaScript
permalink: api/javascript/bitwise-or/
command: bitOr
io:
    -   - number
        - number
related_commands:
    bitwise-and: bitwise-and/
    bitwise-xor: bitwise-xor/
    bitwise-not: bitwise-not/
    bitwise-sal: bitwise-sal/
    bitwise-sar: bitwise-sar/
---

# Command syntax #

{% apibody %}
value.bitOr(value[, value, ...]) &rarr; value
{% endapibody %}

# Description #

Bitwise OR (|) the bits of two or more numbers together, returning the binary result as a number.

The `bitOr` command can be called in either prefix or infix form; both forms are equivalent.

__Example:__ 55 | 5 = 55

```js
> r.expr(55).bitOr(5).run(conn, callback)
// result passed to callback
110111
000101
------
110111
IE. 55
```

__Example:__ Use [args](/api/javascript/args) with `bitOr` to bitwise-or multiple values.

```js
> vals = [55, 5, 15, 11];
> r.bitOr(r.args(vals)).run(conn, callback);
// result passed to callback
110111
000101
001111
001011
------
111111
IE. 63
```
