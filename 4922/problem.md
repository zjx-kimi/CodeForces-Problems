## Description

<div><p>Monocarp is playing yet another computer game. And yet again, his character is killing some monsters. There are $n$ monsters, numbered from $1$ to $n$, and the $i$-th of them has $a_i$ health points initially.</p><p>Monocarp's character has an ability that deals $k$ damage to the monster with the <span class="tex-font-style-bf">highest current health</span>. If there are several of them, <span class="tex-font-style-bf">the one with the smaller index is chosen</span>. If a monster's health becomes less than or equal to $0$ after Monocarp uses his ability, then it dies.</p><p>Monocarp uses his ability until all monsters die. Your task is to determine the order in which monsters will die.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n \le 3 \cdot 10^5$; $1 \le k \le 10^9$)&nbsp;— the number of monsters and the damage which Monocarp's ability deals.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the initial health points of monsters.</p><p>The sum of $n$ over all test cases doesn't exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print $n$ integers&nbsp;— the indices of monsters in the order they die. </p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n \le 3 \cdot 10^5$; $1 \le k \le 10^9$)&nbsp;— the number of monsters and the damage which Monocarp's ability deals.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the initial health points of monsters.</p><p>The sum of $n$ over all test cases doesn't exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print $n$ integers&nbsp;— the indices of monsters in the order they die. </p>





```input1|2,3,6,7
3
3 2
1 2 3
2 3
1 1
4 3
2 8 3 5
```




```output1
2 1 3 
1 2 
3 1 2 4
```



## Note

<p>In the first example, the health points change as follows: $[1, 2, \underline{3}] \rightarrow [1, \underline{2}, 1] \rightarrow [\underline{1}, 0, 1] \rightarrow [-1, 0, \underline{1}] \rightarrow [-1, 0, -1]$. The monster that is going to take damage the next time Monocarp uses his ability is underlined.</p><p>In the second example, the health points change as follows: $[\underline{1}, 1] \rightarrow [-2, \underline{1}] \rightarrow [-2, -2]$.</p><p>In the third example, the health points change as follows: $[2, \underline{8}, 3, 5] \rightarrow [2, \underline{5}, 3, 5] \rightarrow [2, 2, 3, \underline{5}] \rightarrow [2, 2, \underline{3}, 2] \rightarrow [\underline{2}, 2, 0, 2] \rightarrow [-1, \underline{2}, 0, 2] \rightarrow [-1, -1, 0, \underline{2}] \rightarrow [-1, -1, 0, -1]$. </p>
