---
layout: api-command
language: JavaScript
permalink: api/javascript/bitwise-not/
command: bitNot
io:
    -   - number
        - number
related_commands:
    bitwise-or: bitwise-or/
    bitwise-and: bitwise-and/
    bitwise-xor: bitwise-xor/
    bitwise-sal: bitwise-sal/
    bitwise-sar: bitwise-sar/
---

# Command syntax #

{% apibody %}
value.bitNot() &rarr; value
{% endapibody %}

# Description #

Bitwise NOT (~) the bits of a number together, returning the one's complement of that number.

The `bitNot` command can be called in either prefix or infix form; both forms are equivalent.

__Example:__ 55 ~ 5 = -56

```js
> r.expr(55).bitNot().run(conn, callback)
// result passed to callback
11 0111
-------
00 1000
IE. -56
```

__Example:__ Infix form

```js
> r.bitNot(55).run(conn, callback);
// result passed to callback
11 0111
-------
00 1000
IE. -56
```
