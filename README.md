# GitHub math bugs

Math on GitHub is buggy. (See
[my](https://nschloe.github.io/2022/05/20/math-on-github.html)
[blog](https://nschloe.github.io/2022/06/27/math-on-github-follow-up.html)
posts about it.)

To keep track of what's working and what isn't, I've created this repo with
some MWEs. If you have any more examples, let me know or PR!

### Dollar-math with spaces

- https://github.com/community/community/discussions/30747

This is the example from [GitHub's announcement blog
post](https://github.blog/2022-05-19-math-support-in-markdown/).

```markdown
When $a \ne 0$, there are two solutions to $(ax^2 + bx + c = 0)$ and they are
$$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $$
```

> When $a \ne 0$, there are two solutions to $(ax^2 + bx + c = 0)$ and they are
> $$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $$

### Backslashes in `$`-math

- https://github.com/community/community/discussions/16993
- https://github.com/community/community/discussions/17143
- https://github.com/community/community/discussions/31812

```markdown
$\{a\,b\}$
```

> $\{a\,b\}$

### Math vs. HTML mix-up

- https://github.com/community/community/discussions/17022

```markdown
$a <b > c$

$[a+b](c+d)$
```

> $a <b > c$
>
> <!--Terminate the (false) bold tag-->
> </b>
>
> $[a+b](c+d)$

### Sum/product signs in inline mode or fractions

- https://github.com/community/community/discussions/17051
- https://github.com/community/community/discussions/39432

````markdown
$f(x) = \sum_{i=0}^{n} \prod_{j=0}^{n} a_{i,j}$

```math
\frac{\sum_{i=1}^n a_i \prod_{i=1}^n b_i}{2}
```
````

> $f(x) = \sum_{i=0}^{n} \prod_{j=0}^{n} a_{i,j}$
>
> ```math
> \frac{\sum_{i=1}^n a_i \prod_{i=1}^n b_i}{2}
> ```

### Spacing around dollar sign in math mode

- https://github.com/community/community/discussions/17116

```markdown
$x = \$$
```

> $x = \$$

### Math in italic text

- https://github.com/community/community/discussions/17264

```markdown
_Equation $\Omega(69)$ in italic text_
```

> _Equation $\Omega(69)$ in italic text_

### Inline math and display math in same list item doesn't render

- https://github.com/community/community/discussions/17325
- https://github.com/community/community/discussions/18817
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

> - $a$
>
>   ```math
>   a
>   ```
>
> - ```math
>   b
>   ```

### Inline math can't be surrounded by brackets, quotation marks etc.

- https://github.com/community/community/discussions/28115
- https://github.com/community/community/discussions/30157

```markdown
$\pi$, "$\pi$", ($\pi$)
```

> $\pi$, "$\pi$", ($\pi$)

### Oversized sqrt symbol around fractions

- https://github.com/community/community/discussions/39251

````markdown
```math
\sqrt{\frac{1}{2}}
```
````

> ```math
> \sqrt{\frac{1}{2}}
> ```

### Dollar in `\text`

- https://github.com/community/community/discussions/39655

````markdown
```math
a
```

- ```math
  \text{$b$}
  ```
````

> ```math
> a
> ```
>
> - ```math
>   \text{$b$}
>   ```

### Issues with underscores

- https://github.com/community/community/discussions/36915
- https://github.com/community/community/discussions/41087

```markdown
${a}_b c_{d}$
```

> ${a}_b c_{d}$

### 50 or more colors in a block

- https://github.com/orgs/community/discussions/45276

````markdown
```math
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
```
````

> ```math
> 10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
> 10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
> 10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
> 10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
> 10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
```
