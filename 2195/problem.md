## Description

<div><p>The Alice's computer is broken, so she can't play her favorite card game now. To help Alice, Bob wants to answer $n$ her questions. </p><p>Initially, Bob holds one card with number $0$ in the left hand and one in the right hand. In the $i$-th question, Alice asks Bob to replace a card in the left or right hand with a card with number $k_i$ (Bob chooses which of two cards he changes, Bob must replace exactly one card).</p><p>After this action, Alice wants the numbers on the left and right cards to belong to given segments (segments for left and right cards can be different). Formally, let the number on the left card be $x$, and on the right card be $y$. Then after the $i$-th swap the following conditions must be satisfied: $a_{l, i} \le x \le b_{l, i}$, and $a_{r, i} \le y \le b_{r,i}$.</p><p>Please determine if Bob can answer all requests. If it is possible, find a way to do it.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($2 \le n \le 100\,000$, $2 \le m \le 10^9$)&nbsp;— the number of questions and the maximum possible value on the card.</p><p>Then $n$ queries are described. Every description contains 3 lines.</p><p>The first line of the description of the $i$-th query contains a single integer $k_i$ ($0 \le k_i \le m$)&nbsp;— the number on a new card.</p><p>The second line of the description of the $i$-th query contains two integers $a_{l, i}$ and $b_{l, i}$ ($0 \le a_{l, i} \le b_{l, i} \le m$)&nbsp;— the minimum and maximum values of the card at the left hand after the replacement.</p><p>The third line of the description of the $i$-th query contains two integers $a_{r, i}$ and $b_{r,i}$ ($0 \le a_{r, i} \le b_{r,i} \le m$)&nbsp;— the minimum and maximum values of the card at the right hand after the replacement.</p></div><div class="output-specification"><p>At the first line, print "<span class="tex-font-style-tt">Yes</span>", if Bob can answer all queries, and "<span class="tex-font-style-tt">No</span>" otherwise.</p><p>If Bob can answer all $n$ queries, then at the second line print $n$ numbers: a way to satisfy all requirements. If in $i$-th query Bob needs to replace the card in the left hand, print $0$, otherwise print $1$. If there are multiple answers, print any.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($2 \le n \le 100\,000$, $2 \le m \le 10^9$)&nbsp;— the number of questions and the maximum possible value on the card.</p><p>Then $n$ queries are described. Every description contains 3 lines.</p><p>The first line of the description of the $i$-th query contains a single integer $k_i$ ($0 \le k_i \le m$)&nbsp;— the number on a new card.</p><p>The second line of the description of the $i$-th query contains two integers $a_{l, i}$ and $b_{l, i}$ ($0 \le a_{l, i} \le b_{l, i} \le m$)&nbsp;— the minimum and maximum values of the card at the left hand after the replacement.</p><p>The third line of the description of the $i$-th query contains two integers $a_{r, i}$ and $b_{r,i}$ ($0 \le a_{r, i} \le b_{r,i} \le m$)&nbsp;— the minimum and maximum values of the card at the right hand after the replacement.</p>

## Output

<p>At the first line, print "<span class="tex-font-style-tt">Yes</span>", if Bob can answer all queries, and "<span class="tex-font-style-tt">No</span>" otherwise.</p><p>If Bob can answer all $n$ queries, then at the second line print $n$ numbers: a way to satisfy all requirements. If in $i$-th query Bob needs to replace the card in the left hand, print $0$, otherwise print $1$. If there are multiple answers, print any.</p>





```input1
2 10
3
0 3
0 2
2
0 4
0 2
```




```input2
2 10
3
0 3
0 2
2
3 4
0 1
```




```input3
5 10
3
0 3
0 3
7
4 7
1 3
2
2 3
3 7
8
1 8
1 8
6
1 6
7 10
```




```output1
Yes
0 1
```




```output2
No
```




```output3
Yes
1 0 0 1 0
```


