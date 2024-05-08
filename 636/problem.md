## Description

<div><p>You have long dreamed of working in a large IT company and finally got a job there. You have studied all existing modern technologies for a long time and are ready to apply all your knowledge in practice. But then you sit down at your desk and see a sheet of paper with the company's motto printed in large letters: <span class="tex-font-style-tt">abcdabcdabcdabcd...</span>.</p><p>The company's motto contains four main principles— <span class="tex-font-style-tt">a</span> (Willi), <span class="tex-font-style-tt">b</span> (Nilli), <span class="tex-font-style-tt">c</span> (Crack), <span class="tex-font-style-tt">d</span> (Release). Therefore, you consider strings of length $n$ consisting of these four Latin letters. <span class="tex-font-style-bf">Unordered</span> pairs of letters "<span class="tex-font-style-tt">ab</span>", "<span class="tex-font-style-tt">bc</span>", "<span class="tex-font-style-tt">cd</span>", and "<span class="tex-font-style-tt">da</span>" in this motto are adjacent, so we will call such pairs of symbols <span class="tex-font-style-it">good</span>. So, if you are given a string $s$ of length $n$, and it is known that the unordered pair of symbols $\{ x, y \}$ is good, then you can perform one of the following operations on the string:</p><ul> <li> if $s_n = x$, then you are allowed to replace this symbol with $y$, </li><li> if there exists $1 \le i &lt; n$ such that $s_i = x$ and $s_{i+1} = \ldots = s_n = y$, then you are allowed to replace the $i$-th symbol of the string with $y$, and all subsequent symbols with $x$. </li></ul><p>For example, the string <span class="tex-font-style-tt">bacdd</span> can be replaced with one of the strings <span class="tex-font-style-tt">bacda</span>, <span class="tex-font-style-tt">bacdc</span>, or <span class="tex-font-style-tt">badcc</span>, and the string <span class="tex-font-style-tt">aac</span> can be replaced with <span class="tex-font-style-tt">aab</span> or <span class="tex-font-style-tt">aad</span>.</p><p>A non-empty sequence of operations for the string $s$ will be called <span class="tex-font-style-it">correct</span> if the following two conditions are met:</p><ol> <li> after performing all operations, the string becomes $s$ again, </li><li> no string, except for $s$, will occur more than once during the operations. At the same time, the string $s$ can occur exactly twice - before the start of the operations and after performing all operations. </li></ol><p>Now we are ready to move on to the problem statement! You have a set of strings that is initially empty. Then, each of $q$ queries adds another string $t_i$ to the set, or removes the string $t_i$ from the set. After each query, you need to output the minimum and maximum size of a correct sequence of operations in which each word occurs at least once. The choice of the initial string $s$ is up to you.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $q$ ($1 \le n \le 20$, $1 \le q \le 100\,000$)&nbsp;— the length of the strings under consideration and the number of queries to modify the set of strings.</p><p>Each of the next $q$ lines contains a string $t_i$ ($\lvert t_i \rvert = n$). All strings consist of characters "<span class="tex-font-style-tt">a</span>", "<span class="tex-font-style-tt">b</span>", "<span class="tex-font-style-tt">c</span>" and "<span class="tex-font-style-tt">d</span>". If the string $t_i$ was not in the set before the query, it is added to the set, otherwise it is removed from the set.</p></div><div class="output-specification"><p>For each of the $q$ queries, output two integers: the minimum and maximum size of a correct sequence of operations in which each word from the set appears at least once.</p><p>If there is no sequence of operations that satisfies the condition of the problem, output a single number $-1$.</p></div>

## Input

<p>The first line contains two integers $n$ and $q$ ($1 \le n \le 20$, $1 \le q \le 100\,000$)&nbsp;— the length of the strings under consideration and the number of queries to modify the set of strings.</p><p>Each of the next $q$ lines contains a string $t_i$ ($\lvert t_i \rvert = n$). All strings consist of characters "<span class="tex-font-style-tt">a</span>", "<span class="tex-font-style-tt">b</span>", "<span class="tex-font-style-tt">c</span>" and "<span class="tex-font-style-tt">d</span>". If the string $t_i$ was not in the set before the query, it is added to the set, otherwise it is removed from the set.</p>

## Output

<p>For each of the $q$ queries, output two integers: the minimum and maximum size of a correct sequence of operations in which each word from the set appears at least once.</p><p>If there is no sequence of operations that satisfies the condition of the problem, output a single number $-1$.</p>





```input1
2 4
aa
ac
dd
ac
```




```input2
3 2
acc
bdd
```




```output1
2 12
4 4
-1
12 12
```




```output2
2 44
28 44
```



## Note

<p>Let's consider the first test example.</p><ul> <li> After the first query, the set of important words is equal to $\{$<span class="tex-font-style-tt">aa</span>$\}$, the minimum sequence of actions has the following form: <span class="tex-font-style-tt">aa</span>, <span class="tex-font-style-tt">ab</span>, <span class="tex-font-style-tt">aa</span>. The maximum sequence of actions that fits is <span class="tex-font-style-tt">aa</span>, <span class="tex-font-style-tt">ab</span>, <span class="tex-font-style-tt">ba</span>, <span class="tex-font-style-tt">bb</span>, <span class="tex-font-style-tt">bc</span>, <span class="tex-font-style-tt">cb</span>, <span class="tex-font-style-tt">cc</span>, <span class="tex-font-style-tt">cd</span>, <span class="tex-font-style-tt">dc</span>, <span class="tex-font-style-tt">dd</span>, <span class="tex-font-style-tt">da</span>, <span class="tex-font-style-tt">ad</span>, <span class="tex-font-style-tt">aa</span>. </li><li> After the second query, the set of important words is equal to $\{$<span class="tex-font-style-tt">aa, ac</span>$\}$. The minimum and maximum sequences of actions are: <span class="tex-font-style-tt">aa</span>, <span class="tex-font-style-tt">ab</span>, <span class="tex-font-style-tt">ac</span>, <span class="tex-font-style-tt">ad</span>, <span class="tex-font-style-tt">aa</span>. </li><li> After the third query, the set of important words is equal to $\{$<span class="tex-font-style-tt">aa, ac, dd</span>$\}$. There is no sequence of actions that fits the condition, so $-1$ should be outputted. </li><li> After the fourth query, the set of important words is equal to $\{$<span class="tex-font-style-tt">aa, dd</span>$\}$. The minimum and maximum sequences of actions are as follows: <span class="tex-font-style-tt">aa</span>, <span class="tex-font-style-tt">ab</span>, <span class="tex-font-style-tt">ba</span>, <span class="tex-font-style-tt">bb</span>, <span class="tex-font-style-tt">bc</span>, <span class="tex-font-style-tt">cb</span>, <span class="tex-font-style-tt">cc</span>, <span class="tex-font-style-tt">cd</span>, <span class="tex-font-style-tt">dc</span>, <span class="tex-font-style-tt">dd</span>, <span class="tex-font-style-tt">da</span>, <span class="tex-font-style-tt">ad</span>, <span class="tex-font-style-tt">aa</span>. </li></ul>
