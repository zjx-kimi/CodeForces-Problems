## Description

<div><p>Aidan and Nadia are long-time friends with a shared passion for mathematics. Each of them has a favorite number: Aidan's favorite number is $p$, and Nadia's is $q$. </p><p>To commemorate their friendship, their friends want to make a present: a plaque with an arithmetic expression whose value is equal to their favorite numbers. At first glance, it sounds impossible, but the answer is simple: Aidan reads <span class="tex-font-style-it">left-to-right</span>, while Nadia reads <span class="tex-font-style-it">right-to-left</span>, so the same expression can have different values for them.</p><p>For example, if <span class="tex-font-style-tt">2023-12-13</span> is written on the plaque, then Aidan would calculate the result as $2023-12-13 = 1998$, and Nadia would calculate it as $31-21-3202=-3192$.</p><p>Find an arithmetic expression that, when read left-to-right, evaluates to $p$, and, when read right-to-left, evaluates to $q$. Its length must be at most $1000$ characters. It's guaranteed that such an expression exists for all valid inputs.</p></div><div class="input-specification"><p>The first line of the input contains two integers $p$ and $q$ ($-10^{18} \le p, q \le 10^{18}$).</p></div><div class="output-specification"><p>Print the expression without spaces or line breaks. It can only contain digits 0 through 9, '<span class="tex-font-style-tt">+</span>', '<span class="tex-font-style-tt">-</span>', and '<span class="tex-font-style-tt">*</span>' characters.</p><p>The expression must contain at most $1000$ characters. Leading zeros in numbers are not allowed (the only exception is the notation '<span class="tex-font-style-tt">0</span>' representing the number $0$) in both the expression and its reverse. Use of unary '<span class="tex-font-style-tt">+</span>' or '<span class="tex-font-style-tt">-</span>' is not allowed. The expression must be well-formed in both directions. The calculation uses the standard operator precedence. </p></div>

## Input

<p>The first line of the input contains two integers $p$ and $q$ ($-10^{18} \le p, q \le 10^{18}$).</p>

## Output

<p>Print the expression without spaces or line breaks. It can only contain digits 0 through 9, '<span class="tex-font-style-tt">+</span>', '<span class="tex-font-style-tt">-</span>', and '<span class="tex-font-style-tt">*</span>' characters.</p><p>The expression must contain at most $1000$ characters. Leading zeros in numbers are not allowed (the only exception is the notation '<span class="tex-font-style-tt">0</span>' representing the number $0$) in both the expression and its reverse. Use of unary '<span class="tex-font-style-tt">+</span>' or '<span class="tex-font-style-tt">-</span>' is not allowed. The expression must be well-formed in both directions. The calculation uses the standard operator precedence. </p>





```input1|
1998 -3192
```




```input2|
413 908
```




```output1
2023-12-13
```




```output2
12*34+5
```


