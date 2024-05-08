## Description

<div><p>Sasha decided to give his girlfriend the best handbag, but unfortunately for Sasha, it is very expensive. Therefore, Sasha wants to earn it. After looking at earning tips on the internet, he decided to go to the casino.</p><p>Sasha knows that the casino operates under the following rules. If Sasha places a bet of $y$ coins (where $y$ is a positive integer), then in case of winning, he will receive $y \cdot k$ coins (i.e., his number of coins will increase by $y \cdot (k - 1)$). And in case of losing, he will lose the entire bet amount (i.e., his number of coins will decrease by $y$).</p><p>Note that the bet amount must always be a positive ($&gt; 0$) integer and cannot exceed Sasha's current number of coins.</p><p>Sasha also knows that there is a promotion at the casino: he cannot lose more than $x$ times in a row.</p><p>Initially, Sasha has $a$ coins. He wonders whether he can place bets such that he is guaranteed to win any number of coins. In other words, is it true that for any integer $n$, Sasha can make bets so that for any outcome that does not contradict the rules described above, at some moment of time he will have at least $n$ coins.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$) — the number of test cases. The description of the test cases follows.</p><p>The single line of each test case contains three integers $k, x$ and $a$ ($2 \leq k \leq 30$, $1 \leq x \leq 100$, $1 \leq a \leq 10^9$) — the number of times the bet is increased in case of a win, the maximum number of consecutive losses, and the initial number of coins Sasha has.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes) if Sasha can achieve it and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>" and "<span class="tex-font-style-tt">Yes</span>" will be recognized as a positive answer).</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$) — the number of test cases. The description of the test cases follows.</p><p>The single line of each test case contains three integers $k, x$ and $a$ ($2 \leq k \leq 30$, $1 \leq x \leq 100$, $1 \leq a \leq 10^9$) — the number of times the bet is increased in case of a win, the maximum number of consecutive losses, and the initial number of coins Sasha has.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes) if Sasha can achieve it and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>" and "<span class="tex-font-style-tt">Yes</span>" will be recognized as a positive answer).</p>





```input1|2,4,6,8,10
9
2 1 7
2 1 1
2 3 15
3 3 6
4 4 5
5 4 7
4 88 1000000000
25 69 231
13 97 18806
```




```output1
YES
NO
YES
NO
NO
YES
NO
NO
NO
```



## Note

<p>In the first test case, Sasha can proceed as follows:</p><ul><li> If Sasha places a bet for the first time or if he won the previous bet, then he places $1$ coin.</li><li> If Sasha lost the previous bet, then he places $2$ coins.</li></ul><p>Note that Sasha cannot lose more than once in a row.</p><p>It can be proven that with this strategy, Sasha can obtain as many coins as he wants.</p><p>In the second test case, Sasha can only place $1$ coin for the first time. But in case of a loss, he will not be able to place any more bets, so he will not be able to guarantee having as many coins as he wants.</p>
