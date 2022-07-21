---
title: Implementation
nav_order: 2
---

{% include abbreviations.md %}

# {{ page.title }}
{:.no_toc}

<details markdown="block">
  <summary>Page contents</summary>
* TOC
{:toc}
</details>

## Declaration

In the `com.tlglearning.Square` class, the `isPerfectSquare` method is declared with the following signature, return type, and modifiers:
 
```java
public static boolean isPerfectSquare(long input) throws IllegalArgumentException
```

The implementation **must not** change the modifiers, return type, method name, parameter types/number/order, or possible exceptions shown above.

## Specifications

The implementation **must** provide this functionality:

1. If `input` is negative, `isPerfectSquare(input)` **must** throw `java.lang.IllegalArgumentException`;

2. Otherwise, if `input` is a perfect square, `isPerfectSquare(input)` **must** return `true`; 

3. Otherwise, `isPerfectSquare(input)` **must** return `false`.

## Tips

1. For computing square roots, `Math.sqrt` is preferred over `Math.pow`. In particular, the former provides a stronger accuracy guarantee when the argument is in fact a perfect square.

2. Whenever practical, perform calculations in the integer domain. For example, if `a` and `b` are both `long`, the `boolean` expression `a == b * b` will evaluate correctly in all cases, while `Math.sqrt(a) == b` can give a misleading result for some large `a` and `b` values. (Try this with the values `9_223_372_030_926_249_000L` for `a` and `3_037_000_499L` for `b`.) Note that this doesn't mean you shouldn't use the `Math.sqrt` method in your implementation, but only that you shouldn't rely on it exclusively.

3. There are multiple ways to round a floating-point value to an integer, including these:

    * The `Math.round` method rounds a `double` or `float` to the nearest integer, returning the value as a `long` or `int`, respectively.

    * Casting with `(long)` or `(int)` (for example) truncates the fractional portion of a `double` or `float`, effectively rounding toward zero (0), and instructs the compiler to treat the result as a `long` or `int`, respectively.

    * The `Math.floor` method rounds down (toward $-\infty$), returning the value as a `double` (not a `long` or `int`) without a fractional part.

    * The `Math.ceil` method rounds up (toward $\infty$), returning the value as a `double` (not a `long` or `int`) without a fractional part.

4. You may find it useful to create one or more additional `static` methods as "helpers"; the problem can be solved without doing so, however.

5. Do not hesitate to declare any `static` fields (especially `static final` constants) that you feel might simplify or clarify your code.

6. The method to be completed includes a `TODO` comment to that effect.
