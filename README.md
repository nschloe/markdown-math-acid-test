# GitHub math bugs

Math on GitHub is buggy. (See my blog posts
[https://nschloe.github.io/2022/05/20/math-on-github.html,
https://nschloe.github.io/2022/06/27/math-on-github-follow-up.html] posts about
it.)

To keep track of what's working and what isn't, I've created this repo with
some MWEs. If you have any more examples, let me know or PR!

### Inline and display math in same list item doesn't render

- https://github.com/orgs/community/discussions/17325
- https://github.com/orgs/community/discussions/18817
- https://github.com/orgs/community/discussions/39545
- https://github.com/orgs/community/discussions/40775

````markdown
- $`a`$

  ```math
  a
  ```

- ```math
  b
  ```
````

> - $`a`$
>
>   ```math
>   a
>   ```
>
> - ```math
>   b
>   ```

### Images and math in the same list breaks images

```markdown
- ![node logo](https://nodejs.org/static/images/logo.svg)
- $`x`$
```

> - ![node logo](https://nodejs.org/static/images/logo.svg)
> - $`x`$

### Inline and display math in `<details>`

- https://github.com/orgs/community/discussions/57950

````markdown
<details>

$`A = 5`$

```math
A = 5
```

</details>
````

> <details>
>
> $`A = 5`$
>
> ```math
> A = 5
> ```
>
> </details>

### `<` without surrounding whitespace

- https://github.com/orgs/community/discussions/55225

````markdown
$`a<b`$

```math
a<b
```
````

> $`a<b`$
>
> ```math
> a<b
> ```

### Math doesn't render in footnotes

- https://github.com/orgs/community/discussions/55227

```markdown
[^a]

[^a]: Lorem $`a`$
```

> [^a]
>
> [^a]: Lorem $`a`$

### Math doesn't render in links

- https://github.com/orgs/community/discussions/55232

```markdown
[$`a`$](x)
```

> [$`a`$](x)

### Math doesn't render if preceeded by an alphabetic character

- https://github.com/orgs/community/discussions/55343

```markdown
a$`x`$

-$`x`$

1$`x`$
```

> a$`x`$
>
> -$`x`$
>
> 1$`x`$

### Inline math with `%\n`

- https://github.com/orgs/community/discussions/55237

```markdown
$`a+%
b`$
```

> $`a+%
> b`$

### Comments before bracket delimiters

- https://github.com/orgs/community/discussions/55228

````markdown
```math
\left%
(a+b\right)
```
````

> ```math
> \left%
> (a+b\right)
> ```

### Sum/product signs in inline mode or fractions

- https://github.com/orgs/community/discussions/17051
- https://github.com/orgs/community/discussions/39432

````markdown
$`f(x) = \sum_{i=0}^{n} \prod_{j=0}^{n} a_{i,j}`$

```math
\frac{\sum_{i=1}^n a_i \prod_{i=1}^n b_i}{2}
```
````

> $`f(x) = \sum_{i=0}^{n} \prod_{j=0}^{n} a_{i,j}`$
>
> ```math
> \frac{\sum_{i=1}^n a_i \prod_{i=1}^n b_i}{2}
> ```

### `\operatorname` not working

- https://github.com/orgs/community/discussions/55368

````markdown
```math
\operatorname*{Min}_{x}
```
````

> ```math
> \operatorname*{Min}_{x}
> ```

### Inline math at the end of italic text

- https://github.com/orgs/community/discussions/55033

```markdown
_$`a`$ equals $`b`$_

_$`a`$ equals $`b`$_

**$`a`$ equals $`b`$**
```

> _$`a`$ equals $`b`$_
>
> _$`a`$ equals $`b`$_
>
> **$`a`$ equals $`b`$**

### Dollar in `\text`

- https://github.com/orgs/community/discussions/39655

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

### 50 or more colors in a block

- https://github.com/orgs/community/discussions/45276

49 `color`s:

```math
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
10:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
9:  {\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}{\color{red}a}
```

50 `color`s:

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
> ```

### 100 or more bracketed exponents or subscripts

- https://github.com/orgs/community/discussions/59960

````markdown
```math
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
```
````

> ```math
> a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
> a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
> a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
> a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
> a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
> a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
> a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
> a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
> a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
> a^{1} a^{2} a^{3} a^{4} a^{5} a^{6} a^{7} a^{8} a^{9} a^{10}
> ```

### Backslashes in `$`-math

- ~~https://github.com/orgs/community/discussions/16993~~
- ~~https://github.com/orgs/community/discussions/17143~~
- ~~https://github.com/orgs/community/discussions/31812~~
- ~~https://github.com/orgs/community/discussions/46788~~
- ~~https://github.com/orgs/community/discussions/47295~~

```markdown
$\{a\,b\}$
```

> $\{a\,b\}$

Fixed by using backtick delimiters:

> $`\{a\,b\}`$

### Math vs. HTML mix-up

- ~~https://github.com/orgs/community/discussions/17022~~
- ~~https://github.com/orgs/community/discussions/36915~~
- ~~https://github.com/orgs/community/discussions/41087~~
- https://github.com/orgs/community/discussions/54934

```markdown
$a <b > c$

$[(a+b)c](d+e)$

${a}_b c_{d}$
```

> $a <b > c$
>
> <!--Terminate the (false) bold tag-->
> </b>
>
> $[(a+b)c](d+e)$
>
> ${a}_b c_{d}$

Some fixed by using backtick delimiters:

> $`a <b > c`$
>
> $`[(a+b)c](d+e)`$
>
> $`{a}_b c_{d}`$

### Dollar-math with spaces

- https://github.com/orgs/community/discussions/30747

This is the example from [GitHub's announcement blog
post](https://github.blog/2022-05-19-math-support-in-markdown/).

```markdown
When $a \ne 0$, there are two solutions to $(ax^2 + bx + c = 0)$ and they are
$$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $$
```

> When $a \ne 0$, there are two solutions to $(ax^2 + bx + c = 0)$ and they are
> $$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $$

Fixed by using backtick delimiters:

> When $`a \ne 0`$, there are two solutions to $`(ax^2 + bx + c = 0)`$ and they are
>
> ```math
> x = {-b \pm \sqrt{b^2-4ac} \over 2a}
> ```

### Spacing around dollar sign in math mode

- ~~https://github.com/orgs/community/discussions/17116~~

```markdown
$x = \$$
```

> $x = \$$

Fixed by using backtick delimiters:

> $`x = \$`$

### Math in italic text

- ~~https://github.com/orgs/community/discussions/17264~~

```markdown
_Equation $\Omega(69)$ in italic text_
```

> _Equation $\Omega(69)$ in italic text_

Fixed by using backtick delimiters:

> _Equation $`\Omega(69)`$ in italic text_

### Inline math can't be preceded by brackets, quotation marks etc.

- ~~https://github.com/orgs/community/discussions/28115~~
- ~~https://github.com/orgs/community/discussions/30157~~

```markdown
$\pi$
'$\pi$
"$\pi$
($\pi$
[$\pi$
{$\pi$
/$\pi$
```

> $\pi$
> '$\pi$
> "$\pi$
> ($\pi$
> [$\pi$
> {$\pi$
> /$\pi$

Fixed by using backtick delimiters:

> $`\pi`$
> '$`\pi`$
> "$`\pi`$
> ($`\pi`$
> [$`\pi`$
> {$`\pi`$
> /$`\pi`$

### Oversized sqrt symbol around fractions

- https://github.com/orgs/community/discussions/39251

````markdown
```math
\sqrt{\frac{1}{2}}
```
````

> ```math
> \sqrt{\frac{1}{2}}
> ```

### Matrices without line breaks in $$-math

- https://github.com/orgs/community/discussions/52991

```markdown
$$
\begin{pmatrix}a & b\\ c & d\end{pmatrix}
$$
```

> $$
> \begin{pmatrix}a & b\\ c & d\end{pmatrix}
> $$

What works: Using triple-backtick delimiters, or inserting a linebreak after the `\\`.

> ```math
> \begin{pmatrix}a & b\\ c & d\end{pmatrix}
> ```
