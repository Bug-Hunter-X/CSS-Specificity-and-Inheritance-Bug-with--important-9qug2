# CSS Specificity and Inheritance Bug

This repository demonstrates a subtle bug related to CSS specificity and inheritance when using the `!important` declaration. The `!important` declaration only applies directly to the element it's used on, but inheritance can still occur from ancestors if not carefully managed.  The solution shows how to correct the behavior to ensure consistent styling across all elements.

## Bug Description:

The core problem lies in the interaction between the `!important` flag and CSS inheritance.  When a more specific rule sets a style with `!important`, it overrides less-specific rules for that element. However, descendants may still inherit styles from ancestors, leading to unexpected behavior.

## Solution:

The solution involves re-evaluating the CSS rules to explicitly apply styles to the specific elements we want to modify, resolving the inheritance conflict.