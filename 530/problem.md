## Description

<div><p>In a small town, there is a workshop specializing in woodwork. Since the town is small, only <span class="tex-font-style-bf">three</span> carvers work there.</p><p>Soon, a wooden toy festival is planned in the town. The workshop employees want to prepare for it.</p><p>They know that $n$ people will come to the workshop with a request to make a wooden toy. People are different and may want different toys. For simplicity, let's denote the pattern of the toy that the $i$-th person wants as $a_i$ ($1 \le a_i \le 10^9$).</p><p>Each of the carvers can choose an integer pattern $x$ ($1 \le x \le 10^9$) in advance, <span class="tex-font-style-bf">different carvers can choose different patterns</span>. $x$ is the integer. During the preparation for the festival, the carvers will perfectly work out the technique of making the toy of the chosen pattern, which will allow them to cut it out of wood instantly. To make a toy of pattern $y$ for a carver who has chosen pattern $x$, it will take $|x - y|$ time, because the more the toy resembles the one he can make instantly, the faster the carver will cope with the work.</p><p>On the day of the festival, when the next person comes to the workshop with a request to make a wooden toy, the carvers can choose who will take on the job. At the same time, the carvers are very skilled people and can work on orders for different people <span class="tex-font-style-bf">simultaneously</span>.</p><p>Since people don't like to wait, the carvers want to choose patterns for preparation in such a way that the <span class="tex-font-style-bf">maximum</span> waiting time over all people is as <span class="tex-font-style-bf">small</span> as possible.</p><p>Output the <span class="tex-font-style-it">best</span> maximum waiting time that the carvers can achieve.</p></div><div class="input-specification"><p>The first line of the input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of a test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of people who will come to the workshop.</p><p>The second line of a test case contains $n$ integers $a_1, a_2, a_3, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the patterns of toys.</p><p>The sum of all $n$ values over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>Output $t$ numbers, each of which is the answer to the corresponding test case&nbsp;— the <span class="tex-font-style-it">best</span> maximum waiting time that the carvers can achieve.</p></div>

## Input

<p>The first line of the input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Then follow the descriptions of the test cases.</p><p>The first line of a test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of people who will come to the workshop.</p><p>The second line of a test case contains $n$ integers $a_1, a_2, a_3, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the patterns of toys.</p><p>The sum of all $n$ values over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>Output $t$ numbers, each of which is the answer to the corresponding test case&nbsp;— the <span class="tex-font-style-it">best</span> maximum waiting time that the carvers can achieve.</p>





```input1|2,3,6,7,10,11
5
6
1 7 7 9 9 9
6
5 4 2 1 30 60
9
14 19 37 59 1 4 4 98 73
1
2
6
3 10 1 17 15 11
```




```output1
0
2
13
0
1
```



## Note

<p>In the first example, the carvers can choose patterns $1$, $7$, $9$ for preparation.</p><p>In the second example, the carvers can choose patterns $3$, $30$, $60$ for preparation.</p><p>In the third example, the carvers can choose patterns $14$, $50$, $85$ for preparation.</p>
