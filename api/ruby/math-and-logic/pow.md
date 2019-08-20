---
layout: api-command
language: Ruby
permalink: api/ruby/pow/
command: pow
io:
    -   - number
        - number
related_commands:
    '*': mul/
    '/': div/
---
# Command syntax #

{% apibody %}
number ** number &rarr; number
{% endapibody %}

# Description #

Returns the calling number raised to the given value.

__Example:__ Return 10 raised to the power of 2.

```rb
> (r.expr(10) ** 2).run(conn)
// Result passed to callback
100
```
