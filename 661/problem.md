## Description

<div><p>Suppose you have $n$ boxes. The $i$-th box contains infinitely many balls of color $i$. Sometimes you need to get a ball with some specific color; but you're too lazy to do it yourself.</p><p>You have bought two robots to retrieve the balls for you. Now you have to program them. In order to program the robots, you have to construct two lists $[a_1, a_2, \dots, a_k]$ and $[b_1, b_2, \dots, b_{n-k}]$, where the list $a$ represents the boxes assigned to the first robot, and the list $b$ represents the boxes assigned to the second robot. <span class="tex-font-style-bf">Every integer from $1$ to $n$ must be present in exactly one of these lists</span>.</p><p>When you request a ball with color $x$, the robots work as follows. Each robot looks through the boxes that were assigned to that robot, in the order they appear in the list. The first robot spends $s_1$ seconds analyzing the contents of a box; the second robot spends $s_2$. As soon as one of the robots finds the box with balls of color $x$ (and analyzes its contents), the search ends. The search time is the number of seconds from the beginning of the search until one of the robots finishes analyzing the contents of the $x$-th box. If a robot analyzes the contents of all boxes assigned to it, it stops searching.</p><p>For example, suppose $s_1 = 2$, $s_2 = 3$, $a = [4, 1, 5, 3, 7]$, $b = [2, 6]$. If you request a ball with color $3$, the following happens:</p><ul> <li> initially, the first robot starts analyzing the box $4$, and the second robot starts analyzing the box $2$; </li><li> at the end of the $2$-nd second, the first robot finishes analyzing the box $4$. It is not the box you need, so the robot continues with the box $1$; </li><li> at the end of the $3$-rd second, the second robot finishes analyzing the box $2$. It is not the box you need, so the robot continues with the box $6$; </li><li> at the end of the $4$-th second, the first robot finishes analyzing the box $1$. It is not the box you need, so the robot continues with the box $5$; </li><li> at the end of the $6$-th second, the first robot finishes analyzing the box $5$. It is not the box you need, so the robot continues with the box $3$. At the same time, the second robot finishes analyzing the box $6$. It is not the box you need, and the second robot has analyzed all the boxes in its list, so that robot stops searching; </li><li> at the end of the $8$-th second, the first robot finishes analyzing the box $3$. It is the box you need, so the search ends; </li><li> so, the search time is $8$ seconds. </li></ul><p>You know that you are going to request a ball of color $1$ $r_1$ times, a ball of color $2$ $r_2$ times, and so on. You want to construct the lists $a$ and $b$ for the robots in such a way that the total search time over all requests is the minimum possible.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of two lines: </p><ul> <li> the first line contains three integers $n$, $s_1$, $s_2$ ($2 \le n \le 2 \cdot 10^5$; $1 \le s_1, s_2 \le 10$); </li><li> the second line contains $n$ integers $r_1, r_2, \dots, r_n$ ($1 \le r_i \le 10^6$). </li></ul><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print two lines. The first line should contain the list $a$, the second line — the list $b$. Each list has to be printed as follows: first, print the number of elements in it, and then the elements themselves.</p><p>If there are multiple answers, you may print any of them.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of two lines: </p><ul> <li> the first line contains three integers $n$, $s_1$, $s_2$ ($2 \le n \le 2 \cdot 10^5$; $1 \le s_1, s_2 \le 10$); </li><li> the second line contains $n$ integers $r_1, r_2, \dots, r_n$ ($1 \le r_i \le 10^6$). </li></ul><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print two lines. The first line should contain the list $a$, the second line — the list $b$. Each list has to be printed as follows: first, print the number of elements in it, and then the elements themselves.</p><p>If there are multiple answers, you may print any of them.</p>





```input1|2,3,6,7
3
7 3 1
8 6 4 4 4 1 7
5 1 10
1 1 1 1 1
8 1 1
4 5 6 8 1 7 3 2
```




```output1
2 5 6
5 1 7 2 4 3
5 4 3 5 2 1
0
4 4 2 7 5
4 6 3 1 8
```


