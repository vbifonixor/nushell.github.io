---
title: is-not-empty
categories: |
  filters
version: 0.91.0
filters: |
  Check for non-empty values.
usage: |
  Check for non-empty values.
feature: default
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for filters

<div class='command-title'>{{ $frontmatter.filters }}</div>

## Signature

```> is-not-empty {flags} ...rest```

## Parameters

 -  `...rest`: The names of the columns to check emptiness.


## Input/output types:

| input | output |
| ----- | ------ |
| any   | bool   |

## Examples

Check if a string is empty
```nu
> '' | is-not-empty
false
```

Check if a list is empty
```nu
> [] | is-not-empty
false
```

Check if more than one column are empty
```nu
> [[meal size]; [arepa small] [taco '']] | is-not-empty meal size
true
```