## Description

<div><p>Imagine that you have a twin brother or sister. Having another person that looks exactly like you seems very unusual. It's hard to say if having something of an alter ego is good or bad. And if you do have a twin, then you very well know what it's like.</p><p>Now let's imagine a typical morning in your family. You haven't woken up yet, and Mom is already going to work. She has been so hasty that she has nearly forgotten to leave the two of her darling children some money to buy lunches in the school cafeteria. She fished in the purse and found some number of coins, or to be exact, <span class="tex-span"><i>n</i></span> coins of arbitrary values <span class="tex-span"><i>a</i><sub class="lower-index">1</sub>, <i>a</i><sub class="lower-index">2</sub>, ..., <i>a</i><sub class="lower-index"><i>n</i></sub></span>. But as Mom was running out of time, she didn't split the coins for you two. So she scribbled a note asking you to split the money equally.</p><p>As you woke up, you found Mom's coins and read her note. "But why split the money equally?" — you thought. After all, your twin is sleeping and he won't know anything. So you decided to act like that: pick for yourself some subset of coins so that the sum of values of your coins is <span class="tex-font-style-bf">strictly larger</span> than the sum of values of the remaining coins that your twin will have. However, you correctly thought that if you take too many coins, the twin will suspect the deception. So, you've decided to stick to the following strategy to avoid suspicions: you take the <span class="tex-font-style-bf">minimum number of coins</span>, whose sum of values is strictly more than the sum of values of the remaining coins. On this basis, determine what <span class="tex-font-style-bf">minimum</span> number of coins you need to take to divide them in the described manner.</p></div><div class="input-specification"><p>The first line contains integer <span class="tex-span"><i>n</i></span> (<span class="tex-span">1 ≤ <i>n</i> ≤ 100</span>) — the number of coins. The second line contains a sequence of <span class="tex-span"><i>n</i></span> integers <span class="tex-span"><i>a</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>a</i><sub class="lower-index">2</sub></span>, ..., <span class="tex-span"><i>a</i><sub class="lower-index"><i>n</i></sub></span> (<span class="tex-span">1 ≤ <i>a</i><sub class="lower-index"><i>i</i></sub> ≤ 100</span>) — the coins' values. All numbers are separated with spaces.</p></div><div class="output-specification"><p>In the single line print the single number — the minimum needed number of coins.</p></div>

## Input

<p>The first line contains integer <span class="tex-span"><i>n</i></span> (<span class="tex-span">1 ≤ <i>n</i> ≤ 100</span>) — the number of coins. The second line contains a sequence of <span class="tex-span"><i>n</i></span> integers <span class="tex-span"><i>a</i><sub class="lower-index">1</sub></span>, <span class="tex-span"><i>a</i><sub class="lower-index">2</sub></span>, ..., <span class="tex-span"><i>a</i><sub class="lower-index"><i>n</i></sub></span> (<span class="tex-span">1 ≤ <i>a</i><sub class="lower-index"><i>i</i></sub> ≤ 100</span>) — the coins' values. All numbers are separated with spaces.</p>

## Output

<p>In the single line print the single number — the minimum needed number of coins.</p>





```input1
2
3 3

```




```input2
3
2 1 2

```




```output1
2

```




```output2
2

```



## Note

<p>In the first sample you will have to take <span class="tex-span">2</span> coins (you and your twin have sums equal to <span class="tex-span">6, 0</span> correspondingly). If you take <span class="tex-span">1</span> coin, you get sums <span class="tex-span">3, 3</span>. If you take <span class="tex-span">0</span> coins, you get sums <span class="tex-span">0, 6</span>. Those variants do not satisfy you as your sum should be strictly more that your twins' sum.</p><p>In the second sample one coin isn't enough for us, too. You can pick coins with values <span class="tex-span">1, 2</span> or <span class="tex-span">2, 2</span>. In any case, the minimum number of coins equals <span class="tex-span">2</span>. </p>
