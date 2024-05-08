## Description

<div><p>Carol has a sequence $s$ of $n$ non-negative integers. She wants to play the "Guess Game" with Alice and Bob.</p><p>To play the game, Carol will <span class="tex-font-style-bf">randomly</span> select two integer indices $i_a$ and $i_b$ within the range $[1, n]$, and set $a=s_{i_a}$, $b=s_{i_b}$. Please note that $i_a$ and $i_b$ may coincide.</p><p>Carol will tell:</p><ul> <li> the value of $a$ to Alice; </li><li> the value of $b$ to Bob; </li><li> the value of $a \mid b$ to both Alice and Bob, where $|$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#OR">bitwise OR operation</a>. </li></ul><p>Please note that Carol will <span class="tex-font-style-bf">not</span> tell any information about $s$ to either Alice or Bob.</p><p>Then the guessing starts. The two players take turns making guesses, with Alice starting first. The goal of both players is to establish which of the following is true: $a &lt; b$, $a &gt; b$, or $a = b$.</p><p>In their turn, a player can do one of the following two things:</p><ul> <li> say "I don't know", and pass the turn to the other player; </li><li> say "I know", followed by the answer "$a&lt;b$", "$a&gt;b$", or "$a=b$"; then the game ends. </li></ul><p>Alice and Bob hear what each other says, and can use this information to deduce the answer. Both Alice and Bob are smart enough and only say "I know" when they are completely sure.</p><p>You need to calculate the expected value of the number of turns taken by players in the game. Output the answer modulo $998\,244\,353$.</p><p>Formally, let $M = 998\,244\,353$. It can be shown that the answer can be expressed as an irreducible fraction $\frac{p}{q}$, where $p$ and $q$ are integers and $q \not \equiv 0 \pmod{M}$. Output the integer equal to $p \cdot q^{-1} \bmod M$. In other words, output such an integer $x$ that $0 \le x &lt; M$ and $x \cdot q \equiv p \pmod{M}$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each testcase contains a single integer $n$ ($1 \le n \le 2\cdot 10^5$).</p><p>The second line of each testcase contains $n$ integers $s_1,s_2,\ldots, s_n$ ($0 \le s_i &lt; 2^{30}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. </p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the answer to the problem modulo $998\,244\,353$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each testcase contains a single integer $n$ ($1 \le n \le 2\cdot 10^5$).</p><p>The second line of each testcase contains $n$ integers $s_1,s_2,\ldots, s_n$ ($0 \le s_i &lt; 2^{30}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. </p>

## Output

<p>For each test case, print a single integer&nbsp;— the answer to the problem modulo $998\,244\,353$.</p>





```input1|2,3,6,7
4
2
2 3
3
0 0 0
3
9 9 6
8
34124838 0 113193378 8 321939321 113193378 9463828 99
```




```output1
499122179
1
332748120
77987843
```



## Note

<p>In the first test case, there are only $4$ possible situations:</p><ol> <li> $i_a=1$, $i_b=1$, $a=2$, $b=2$, the number of turns is $2$; </li><li> $i_a=1$, $i_b=2$, $a=2$, $b=3$, the number of turns is $3$; </li><li> $i_a=2$, $i_b=1$, $a=3$, $b=2$, the number of turns is $2$; </li><li> $i_a=2$, $i_b=2$, $a=3$, $b=3$, the number of turns is $3$. </li></ol><p>The expected number of turns is $\frac{2+3+2+3}{4}=\frac{5}{2}=499122179\pmod{998244353}$.</p><p>Consider the first case, when $a=2$, $b=2$. The guessing process is as follows.</p><p>In the first turn, Alice thinks, "I know that $a=2, a\mid b=2$. I can infer that $b=0$ or $b=2$, but I am not sure which one". Thus, she says, "I don't know".</p><p>In the second turn, Bob thinks, "I know that $b=2, a\mid b=2$. I can infer that $a=0$ or $a=2$. But if $a=0$, then Alice would have already said that $a&lt;b$ in the first turn, but she hasn't. So $a=2$". Thus, he says, "I know, $a=b$". The game ends. </p><p>In the second test case, for $a=0$, $b=0$, Alice knows that $a=b$ immediately. The expected number of turns equals $1$.</p>
