# Specificity

## Order of precedence
1. !important
1. id
1. class
1. tag selection

## Rules
1. A higher number of selectors in one level implies a higher level of specificity for that level. In the following example, the second set of styles wins out because it has two class specifiers.

    ```css
    .btn {
      ...styles
    }

    .btn.btn-default {
      ...styles
    }
    ```

1. A higher score in a higher level of precedence automatically overrides any lower-level scores. In the following example, the first wins out because it has a class specifier, whereas the second has only two tag-level specifiers.

    ```css
    p.test {
      ...styles
    }

    div p {
      ...styles
    }
    ```

1. If two sets of styles have the same specificity, the one that occurs last wins. In the following example, the second set of styles would win

    ```css
    p.testclass {
      ...styles
    }

    div .testclass {
      ...styles
    }
    ```
