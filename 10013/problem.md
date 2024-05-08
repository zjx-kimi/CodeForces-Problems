## Description

<div><p>You are playing a computer game. The current level of this game can be modeled as a straight line. Your character is in point $0$ of this line. There are $n$ monsters trying to kill your character; the $i$-th monster has health equal to $a_i$ and is initially in the point $x_i$.</p><p>Every second, the following happens:</p><ul> <li> first, you fire up to $k$ bullets at monsters. Each bullet targets exactly one monster and decreases its health by $1$. For each bullet, you choose its target arbitrary (for example, you can fire all bullets at one monster, fire all bullets at different monsters, or choose any other combination). Any monster can be targeted by a bullet, regardless of its position and any other factors; </li><li> then, all alive monsters with health $0$ or less die; </li><li> then, all alive monsters move $1$ point closer to you (monsters to the left of you increase their coordinates by $1$, monsters to the right of you decrease their coordinates by $1$). If any monster reaches your character (moves to the point $0$), you lose. </li></ul><p>Can you survive and kill all $n$ monsters without letting any of them reach your character?</p></div><div class="input-specification"><p>The first line of the input contains one integer $t$ ($1 \le t \le 3 \cdot 10^4$) — the number of test cases.</p><p>Each test case consists of three lines:</p><ul> <li> the first line contains two integers $n$ and $k$ ($1 \le n \le 3 \cdot 10^5$; $1 \le k \le 2 \cdot 10^9$); </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$); </li><li> the third line contains $n$ integers $x_1, x_2, \dots, x_n$ ($-n \le x_1 &lt; x_2 &lt; x_3 &lt; \dots &lt; x_n \le n$; $x_i \ne 0$). </li></ul><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">YES</span> if you can kill all $n$ monsters before they reach your character, or <span class="tex-font-style-tt">NO</span> otherwise.</p><p>You can output each letter of the answer in any case (upper or lower). For example, the strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span>, and <span class="tex-font-style-tt">YES</span> will all be recognized as positive responses.</p></div>

## Input

<p>The first line of the input contains one integer $t$ ($1 \le t \le 3 \cdot 10^4$) — the number of test cases.</p><p>Each test case consists of three lines:</p><ul> <li> the first line contains two integers $n$ and $k$ ($1 \le n \le 3 \cdot 10^5$; $1 \le k \le 2 \cdot 10^9$); </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$); </li><li> the third line contains $n$ integers $x_1, x_2, \dots, x_n$ ($-n \le x_1 &lt; x_2 &lt; x_3 &lt; \dots &lt; x_n \le n$; $x_i \ne 0$). </li></ul><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print <span class="tex-font-style-tt">YES</span> if you can kill all $n$ monsters before they reach your character, or <span class="tex-font-style-tt">NO</span> otherwise.</p><p>You can output each letter of the answer in any case (upper or lower). For example, the strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span>, and <span class="tex-font-style-tt">YES</span> will all be recognized as positive responses.</p>





```input1|2,3,4,8,9,10,14,15,16
5
3 2
1 2 3
-1 2 3
2 1
1 1
-1 1
4 10
3 4 2 5
-3 -2 1 3
5 3
2 1 3 2 5
-3 -2 3 4 5
2 1
1 2
1 2
```




```output1
YES
NO
YES
YES
NO
```



## Note

<p>In the first example, you can act as follows:</p><ul> <li> during the $1$-st second, fire $1$ bullet at the $1$-st monster and $1$ bullet at the $3$-rd monster. Then the $1$-st monster dies, the $2$-nd and the $3$-rd monster move closer; </li><li> during the $2$-nd second, fire $2$ bullets at the $2$-nd monster. Then the $2$-nd monster dies, the $3$-rd monster moves closer; </li><li> during the $3$-rd second, fire $2$ bullets at the $3$-rd monster. Then the $3$-rd monster dies. </li></ul><p>In the second example, you can fire only $1$ bullet, so you can kill only one of the two monsters during the $1$-st second. Then, the remaining monster moves closer and kills your character.</p>
