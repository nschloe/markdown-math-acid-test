# Markdown math test page

This is a test page for Markdown math with delimiters
``$`...`$`` and

````
```math
...
```
````

This template and links to more test pages can be found at
https://github.com/nschloe/markdown-math-tester.

### Basic example

````markdown
When $`a \ne 0`$, there are two solutions to
$`(ax^2 + bx + c = 0)`$ and they are
```math
x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}
```
````

---

When $`a \ne 0`$, there are two solutions to
$`(ax^2 + bx + c = 0)`$ and they are
```math
x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}
```

---
Relevant issues:

- https://github.com/orgs/community/discussions/30747

### Subsequent math

````markdown
$`\alpha`$$`\beta`$

```math
\gamma
```
```math
\delta
```
````

---

$`\alpha`$$`\beta`$

```math
\gamma
```
```math
\delta
```

---
Relevant issues:

- https://github.com/github/markup/issues/1741
- https://gitlab.com/gitlab-org/gitlab/-/issues/431890

### Indented math

````markdown
$`\alpha`$

```math
\alpha
```

 $`\alpha`$

 ```math
 \alpha
 ```

  $`\alpha`$

  ```math
  \alpha
  ```

   $`\alpha`$

   ```math
   \alpha
   ```
````

---

$`\alpha`$

```math
\alpha
```

 $`\alpha`$

 ```math
 \alpha
 ```

  $`\alpha`$

  ```math
  \alpha
  ```

   $`\alpha`$

   ```math
   \alpha
   ```

---
Relevant issues:

- https://github.com/go-gitea/gitea/issues/27834
- https://gitlab.com/gitlab-org/gitlab/-/issues/431893

### Math in quote blocks

````markdown
> $`\alpha`$
>
> ```math
> \beta
> ```
> ```math
> \gamma
> ```
````

---

> $`\alpha`$
>
> ```math
> \beta
> ```
> ```math
> \gamma
> ```

---
Relevant issues:

- https://github.com/github/markup/issues/1732
- https://github.com/go-gitea/gitea/issues/27777
- https://gitlab.com/gitlab-org/gitlab/-/issues/431889

### Escaped dollar sign

````markdown
$`\sqrt{\$4}`$, $`x = \$`$

```math
\sqrt{\$4},\\
x = \$.
```
````

---

$`\sqrt{\$4}`$, $`x = \$`$

```math
\sqrt{\$4},\\
x = \$.
```

---
Relevant issues:

- https://github.com/orgs/community/discussions/17116
- https://github.com/go-gitea/gitea/issues/27618

### Inline and display math in same list

````markdown
- $`a`$

  ```math
  a
  ```

- ```math
  b
  ```
````

---

- $`a`$

  ```math
  a
  ```

- ```math
  b
  ```

---
Relevant issues:

- https://github.com/orgs/community/discussions/17325
- https://github.com/orgs/community/discussions/18817
- https://github.com/orgs/community/discussions/39545
- https://github.com/orgs/community/discussions/40775
- https://gitlab.com/gitlab-org/gitlab/-/issues/431895

### Math in footnotes

```markdown
[^a]

[^a]: Lorem $`a`$
```

---

[^a]

[^a]: Lorem $`a`$

---
Relevant issues:

- https://github.com/orgs/community/discussions/55227

### Math in links

```markdown
[$`a`$](x)
```

---

[$`a`$](x)

---
Relevant issues:

- https://github.com/orgs/community/discussions/55232

### Escaped symbols in math

```markdown
$`\{a\,b\}`$
```

---

$`\{a\,b\}`$

---
Relevant issues:

- https://github.com/orgs/community/discussions/16993
- https://github.com/orgs/community/discussions/17143
- https://github.com/orgs/community/discussions/31812
- https://github.com/orgs/community/discussions/46788
- https://github.com/orgs/community/discussions/47295
- https://gitlab.com/gitlab-org/gitlab/-/issues/431896

### Images and math in the same list

```markdown
- ![node logo](https://nodejs.org/static/images/logo.svg)
- $`x`$
```

---

- ![node logo](https://nodejs.org/static/images/logo.svg)
- $`x`$

---
Relevant issues:

- https://github.com/github/markup/issues/1743

### Math in `<details>`

````markdown
<details>

$`A = 5`$

```math
A = 5
```

</details>
````

---

<details>

$`A = 5`$

```math
A = 5
```

</details>

---
Relevant issues:

- https://github.com/orgs/community/discussions/57950

### `<` without surrounding whitespace

````markdown
$`a<b`$

```math
a<b
```
````

---

$`a<b`$

```math
a<b
```

---
Relevant issues:

- https://github.com/orgs/community/discussions/55225
- https://gitlab.com/gitlab-org/gitlab/-/issues/431897

### Inline math preceeded by non-whitespace

```markdown
$`x`$ a$`x`$ 1$`x`$ -$`x`$ '$`x`$ "$`x`$ ($`x`$ [$`x`$ {$`x`$ /$`x`$
```

---

$`x`$ a$`x`$ 1$`x`$ -$`x`$ '$`x`$ "$`x`$ ($`x`$ [$`x`$ {$`x`$ /$`x`$

---
Relevant issues:

- https://github.com/orgs/community/discussions/28115
- https://github.com/orgs/community/discussions/30157
- https://github.com/orgs/community/discussions/55343
- https://github.com/github/markup/issues/1742
- https://github.com/go-gitea/gitea/issues/27605

### Inline math succeeded by non-whitespace

```markdown
$`x`$ $`x`$a $`x`$1 $`x`$- $`x`$' $`x`$" $`x`$) $`x`$] $`x`$} $`x`$/
```

---

$`x`$ $`x`$a $`x`$1 $`x`$- $`x`$' $`x`$" $`x`$) $`x`$] $`x`$} $`x`$/

---
Relevant issues:

- https://github.com/github/markup/issues/1742
- https://gitlab.com/gitlab-org/gitlab/-/issues/431869
- https://github.com/go-gitea/gitea/issues/27605
- https://github.com/jgm/pandoc/issues/9192

### Inline math with `%\n`

```markdown
$`a+%
b`$
```

---

$`a+%
b`$

---
Relevant issues:

- https://github.com/orgs/community/discussions/55237
- https://github.com/go-gitea/gitea/issues/27617
- https://github.com/jgm/pandoc/issues/9193

### Comments before bracket delimiters

````markdown
```math
\left%
(a+b\right)
```
````

---

```math
\left%
(a+b\right)
```

---
Relevant issues:

- https://github.com/orgs/community/discussions/55228

### Sum/product signs in inline mode or fractions

````markdown
$`f(x) = \sum_{i=0}^{n} \prod_{j=0}^{n} a_{i,j}`$

```math
\frac{\sum_{i=1}^n a_i \prod_{i=1}^n b_i}{2}
```
````

---

$`f(x) = \sum_{i=0}^{n} \prod_{j=0}^{n} a_{i,j}`$

```math
\frac{\sum_{i=1}^n a_i \prod_{i=1}^n b_i}{2}
```

---
Relevant issues:

- https://github.com/orgs/community/discussions/17051
- https://github.com/orgs/community/discussions/39432

### `\operatorname`

````markdown
```math
\operatorname*{Min}_{x}
```
````

---

```math
\operatorname*{Min}_{x}
```

---
Relevant issues:

- https://github.com/orgs/community/discussions/55368

### Math in stylized text

```markdown
_Equation $`\Omega(69)`$ in italic text_

*Equation $`\Omega(69)`$ in italic text*

**Equation $`\Omega(69)`$ in bold text**

***Equation $`\Omega(69)`$ in bold italic text***
```

---

_Equation $`\Omega(69)`$ in italic text_

*Equation $`\Omega(69)`$ in italic text*

**Equation $`\Omega(69)`$ in bold text**

***Equation $`\Omega(69)`$ in bold italic text***

---
Relevant issues:

- https://github.com/orgs/community/discussions/17264

### Inline math at the end of stylized text

```markdown
_$`a`$ equals $`b`$_

*$`a`$ equals $`b`$*

**$`a`$ equals $`b`$**

***$`a`$ equals $`b`$***
```

---

_$`a`$ equals $`b`$_

*$`a`$ equals $`b`$*

**$`a`$ equals $`b`$**

***$`a`$ equals $`b`$***

---
Relevant issues:

- https://github.com/orgs/community/discussions/55033

### Dollar in `\text`

```markdown
$`a`$

- $`\text{$b$}`$
```

---

$`a`$

- $`\text{$b$}`$

---
Relevant issues:

- https://github.com/orgs/community/discussions/39655
- https://github.com/go-gitea/gitea/issues/28070

### Math vs. HTML mix-ups

```markdown
$`a <b > c`$

<!--Terminate the (false) bold tag-->
</b>

$`[(a+b)c](d+e)`$

$`{a}_b c_{d}`$
```

---

$`a <b > c`$

<!--Terminate the (false) bold tag-->
</b>

$`[(a+b)c](d+e)`$

$`{a}_b c_{d}`$

---
Relevant issues:

- https://github.com/orgs/community/discussions/17022
- https://github.com/orgs/community/discussions/36915
- https://github.com/orgs/community/discussions/41087
- https://github.com/orgs/community/discussions/54934

### sqrt symbol around fractions

````markdown
```math
\sqrt{\frac{1}{2}}
```
````

---

```math
\sqrt{\frac{1}{2}}
```

---
Relevant issues:

- https://github.com/orgs/community/discussions/39251

### Matrix without line breaks

````markdown
$`\begin{pmatrix}a & b\\ c & d\end{pmatrix}`$

```math
\begin{pmatrix}a & b\\ c & d\end{pmatrix}
```
````

---

$`\begin{pmatrix}a & b\\ c & d\end{pmatrix}`$

```math
\begin{pmatrix}a & b\\ c & d\end{pmatrix}
```

---
Relevant issues:

- https://github.com/orgs/community/discussions/52991

### 50 or more colors in a block

````markdown
```math
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}\\
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}\\
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}\\
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}\\
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
```
````

---

```math
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}\\
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}\\
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}\\
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}\\
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
```

---
Relevant issues:

- https://github.com/orgs/community/discussions/45276

### 100 or more bracketed exponents or subscripts

````markdown
```math
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
```
````

---

```math
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}\\
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
```

---
Relevant issues:

- https://github.com/orgs/community/discussions/59960