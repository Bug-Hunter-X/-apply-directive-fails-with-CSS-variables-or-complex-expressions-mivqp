# Tailwind CSS @apply Directive Issue with CSS Variables

This repository demonstrates a bug encountered when using Tailwind CSS's `@apply` directive with CSS variables or complex expressions.  The problem arises from the interplay between the CSS preprocessor's variable handling and the way `@apply` injects classes. 

## Problem Description

The `@apply` directive, while powerful, doesn't directly support dynamic evaluation of variables or expressions. When attempting to use CSS variables (or custom functions) within an `@apply` rule, the expected class might not be applied. This results in unexpected styling, often resulting in no styling at all.  See `bug.css` for an example.

## Solution

A workaround is to avoid using variables or complex expressions directly within the `@apply` directive. Instead, apply classes directly with the resolved CSS variable, see `bugSolution.css`.  Alternatively, use a utility-first approach where possible to avoid this scenario entirely.