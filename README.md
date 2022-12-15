# GitHub math bugs

##### Two brackets

```markdown
$[a+b](c+d)$
```

$[a+b](c+d)$

##### Backslashes in `$`-math https://github.com/community/community/discussions/16993

```markdown
$\{a\}$
```

$\{a\}$

##### Dollar-math with spaces https://github.com/community/community/discussions/30747

```markdown
A
$$ x = 1 $$
```

A
$$ x = 1 $$

##### Oversized sqrt symbol around fractions https://github.com/community/community/discussions/39251

```math
\sqrt{\frac{1}{2}}
```

##### Sum in fraction https://github.com/community/community/discussions/39432

```math
\frac{\sum_{i=1}^n}{2}
```

##### Inline math and display math in same list item doesn't render https://github.com/community/community/discussions/39545 https://github.com/community/community/discussions/40775

````markdown
- $a$

  ```math
  a
  ```

- ```math
  b
  ```
````

- $a$

  ```math
  a
  ```

- ```math
  b
  ```

##### Dollar in `\text` https://github.com/community/community/discussions/39655

```math
a
```

- ```math
  \text{$b$}
  ```

##### Issues with underscores

- https://github.com/community/community/discussions/30747

  ```markdown
  ${a}_b c_{d}$
  ```

  ${a}_b c_{d}$

- https://github.com/community/community/discussions/41087

  ```markdown
  $[x]_y a_{b}$
  ```

  $[x]_y a_{b}$
