---
layout: api-command
language: JavaScript
permalink: api/javascript/pow/
command: pow
io:
    -   - number
        - number
related_commands:
    mul: mul/
    div: div/
---
# Command syntax #

{% apibody %}
number.pow() &rarr; number
{% endapibody %}

# Description #

Returns the calling number raised to the given value.

__Example:__ Return 10 raised to the power of 2.

```js
r.expr(10).pow(2).run(conn, callback);
// Result passed to callback
100
```
