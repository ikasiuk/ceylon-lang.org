---
layout: reference
title: `-` (difference) operator
tab: documentation
unique_id: docspage
author: Tom Bentley
milestone: Milestone 1
---

# #{page.title}

The left-associative, binary `-` operator is used to take the *difference* of 
two operands.

## Usage 

    Natural one = 3 - 2;

## Description

### Definition

The `-` operator is defined as 

    lhs.castTo<N>().minus(rhs.castTo<N>());

See the [language specification](#{site.urls.spec}#arithmetic) for more details.

### Polymorphism

The `-` operator is [polymorphic](/documentation/reference/operator/operator-polymorphism). 
The meaning of `-` depends on the 
[`Numeric`](#{site.urls.apidoc}/ceylon/language/interface_Numeric.html) and
[`Castable`](#{site.urls.apidoc}/ceylon/language/interface_Castable.html) interfaces.

### Meaning of *difference* for built-in types

For the built-in numeric types ([`Natural`](#{site.urls.apidoc}/ceylon/language/class_Natural.html), 
[`Integer`](#{site.urls.apidoc}/ceylon/language/class_Integer.html),
[`Float`](#{site.urls.apidoc}/ceylon/language/class_Float.html),
[`Whole`](#{site.urls.apidoc}/ceylon/language/class_Whole.html) and
[`Decimal`](#{site.urls.apidoc}/ceylon/language/class_Decimal.html) 
`-` performs normal mathematical subtraction, subject to the limitations
of the relevant type.

### Widening

Widening will be implemented in <!-- m2 -->

The types of the operands need not match because of the calls to `castTo<N>()` 
in the definition of the operator. In other words assuming it's possible to 
widen one of the `lhs` or `rhs` so that it's the same type as the other then 
such a widening will automatically be performed. It is a compile time error if 
such a widening is not possible.

## See also

* API documentation for [`Numeric`](#{site.urls.apidoc}/ceylon/language/interface_Numeric.html)
* API documentation for [`Castable`](#{site.urls.apidoc}/ceylon/language/interface_Castable.html)
* [difference in the language specification](#{site.urls.spec}#arithmetic)
* [operator precedence](#{site.urls.spec}#operatorprecedence) in the 
  language specification
* [Operator polymorphism](/documentation/tour/language-module/#operator_polymorphism) 
  and 
  [Numeric operator semantics](/documentation/tour/language-module/#numeric_operator_semantics) 
  in the Tour of Ceylon
* [~ (complement in)](../complement-in) the set-wise minus operator

