# GitHub math bugs

#### Two brackets

```markdown
$[a+b](c+d)$
```

$[a+b](c+d)$

#### Backslashes in `$`-math

- https://github.com/community/community/discussions/16993
- https://github.com/community/community/discussions/31812

```markdown
$\{a\}$
```

$\{a\}$

#### Inline math and display math in same list item doesn't render 

- https://github.com/community/community/discussions/17325
- https://github.com/community/community/discussions/39545
- https://github.com/community/community/discussions/40775

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


#### Inline math can't be surrounded by brackets, quotation marks etc. https://github.com/community/community/discussions/30157

```markdown
$\pi$, "$\pi$", ($\pi$)
```

$\pi$, "$\pi$", ($\pi$)

#### Dollar-math with spaces https://github.com/community/community/discussions/30747

```markdown
A
$$ x = 1 $$
```

A
$$ x = 1 $$

#### Oversized sqrt symbol around fractions https://github.com/community/community/discussions/39251

```math
\sqrt{\frac{1}{2}}
```

#### Sum in fraction https://github.com/community/community/discussions/39432

```math
\frac{\sum_{i=1}^n}{2}
```

##### Dollar in `\text` https://github.com/community/community/discussions/39655

```math
a
```

- ```math
  \text{$b$}
  ```

#### Issues with underscores

- https://github.com/community/community/discussions/36915
- https://github.com/community/community/discussions/41087

  ```markdown
  ${a}_b c_{d}$
  ```

  ${a}_b c_{d}$
