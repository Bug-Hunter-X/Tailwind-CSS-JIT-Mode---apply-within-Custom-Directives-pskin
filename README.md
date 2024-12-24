# Tailwind CSS JIT Mode: @apply within Custom Directives

This repository demonstrates a bug in Tailwind CSS's JIT mode where `@apply` directives within custom directives may not be correctly processed. This can lead to styles not being applied or unexpected behavior.

## Bug Description

When using `@apply` inside a custom directive defined within a `@layer`, the JIT mode of Tailwind CSS may fail to apply the utility classes correctly.  This is because JIT processes custom directives differently from regular classes.

## Steps to Reproduce

1. Create a Tailwind CSS project.
2. Define a custom directive with `@apply` as shown in the `bug.css` file.
3. Use the custom directive in your HTML.
4. Observe the unexpected styling or missing styles.

## Solution

The solution provided in `bugSolution.css` demonstrates a work-around to mitigate this issue by directly applying the utility classes, avoiding the use of `@apply` within the custom directive.