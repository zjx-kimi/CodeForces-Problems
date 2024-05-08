## Description

<div><p><span class="tex-font-style-it">This is an interactive problem.</span></p><p>As is well known, the city "E" has never had its roads repaired in its a thousand and a half years old history. And only recently the city administration repaired some of them.</p><p>It is known that in total in the city "E" there are $n$ intersections and $m$ roads, which can be used in both directions, numbered with integers from $1$ to $m$. The $i$-th road connects intersections with numbers $a_i$ and $b_i$.</p><p>Among all $m$ roads, some subset of the roads has been repaired, but you do not know which one. The only information you could get from the city's road services is that you can get from any intersection to any other intersection by driving only on the roads that have been repaired.</p><p>You are a young entrepreneur, and decided to organize a delivery service of fresh raw meat in the city "E" (in this city such meat is called "steaks", it is very popular among the locals). You have already recruited a staff of couriers, but the couriers are willing to travel only on repaired roads. Now you have to find out which roads have already been repaired.</p><p>The city administration has given you the city for a period of time, so you can make different queries of one of three types:</p><ol> <li> Block the road with the number $x$. In this case, movement on the road for couriers will be forbidden. <span class="tex-font-style-bf">Initially all roads are unblocked</span>.</li><li> Unblock the road with the number $x$. In this case, couriers will be able to move on the road $x$ if it is repaired.</li><li> Try to deliver the order to the intersection with the number $y$. In this case, one of your couriers will start moving from intersection with number $s$ you don't know and deliver the order to intersection with number $y$ if there is a path on unblocked repaired roads from intersection $s$ to intersection $y$. It is guaranteed that intersection $s$ <span class="tex-font-style-bf">will be chosen beforehand</span>. </li></ol><p>Unfortunately, the city is placed at your complete disposal for a short period of time, so you can make no more than $100 \cdot m$ requests.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 1\,000$) — the number of test cases. The description of test cases follows.</p><p>The first line contains two integers $n$ and $m$ ($2 \le n \le 2\,000$, $n - 1 \le m \le 2\,000$)&nbsp;—the number of intersections and roads in the city "E".</p><p>Each of the following $m$ lines describes one road. The $i$-th of these lines contains two integers $a_i$ and $b_i$ ($1 \le a_i, b_i \le n$)&nbsp;— the ends of the $i$-th road. It is guaranteed that no road connects the city to itself, while it is possible that there are several roads between a pair of different intersections.</p><p>It is guaranteed that the sum of $n$ and the sum of $m$ over all test cases does not exceed $2\,000$.</p></div><div><h2>Interaction</h2><p>Once you have read the description of the test case, you can make queries. Queries can be of three types:</p><ol> <li> "<span class="tex-font-style-tt">-</span> $x$" ($1 \le x \le m$). In this case the road with the number $x$ is blocked if it has not already been blocked.</li><li> "<span class="tex-font-style-tt">+</span> $x$" ($1 \le x \le m$). In this case the road with the number $x$ is unblocked. Note that road $x$ must be blocked beforehand. <span class="tex-font-style-bf">All roads are initially unblocked</span>.</li><li> "<span class="tex-font-style-tt">?</span> $y$" ($1 \le y \le n$). In this case the jury program chooses some city $s$. If you can get from town $s$ to town $y$ by unblocked repaired roads, the jury program will output $1$, otherwise the jury program will output $0$. Note that city $s$ <span class="tex-font-style-bf">will be selected before getting information about city $y$</span>, but your previous requests may be taken into account when selecting city $s$. </li></ol><p>In total, you can make no more than $100 \cdot m$ queries for each set of input data.</p><p>After you have found all repaired roads, output "<span class="tex-font-style-tt">!</span> $c_1,\ c_2,\ c_3,\ \ldots,\ c_m$", where $c_i$ is $1$ if road $i$ is repaired, and $0$ if road is not repaired. This output <span class="tex-font-style-bf">will not count</span> in the total number of queries. The jury program will output $1$ if your answer is correct, and $0$ if the answer is not correct. If you received $0$, your program must terminate immediately to receive a <span class="tex-font-style-tt">Wrong Answer</span> verdict. Otherwise you can get any verdict, because the program will continue reading from the closed stream. If you read $1$, move on to the next test case, or terminate the program if there is none.</p><p>Note that you do not have to unblock all roads before outputting the answer. It is guaranteed that all repaired roads are fixed initially and will not be changed by the jury program depending on queries.</p><p>After outputting a query or the answer do not forget to output the end of line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use:</p><ul><li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++;</li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java;</li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal;</li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python;</li><li> see the documentation for other languages.</li></ul> <span class="tex-font-style-bf">Hacks</span><p>You can't do hacks on this problem.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 1\,000$) — the number of test cases. The description of test cases follows.</p><p>The first line contains two integers $n$ and $m$ ($2 \le n \le 2\,000$, $n - 1 \le m \le 2\,000$)&nbsp;—the number of intersections and roads in the city "E".</p><p>Each of the following $m$ lines describes one road. The $i$-th of these lines contains two integers $a_i$ and $b_i$ ($1 \le a_i, b_i \le n$)&nbsp;— the ends of the $i$-th road. It is guaranteed that no road connects the city to itself, while it is possible that there are several roads between a pair of different intersections.</p><p>It is guaranteed that the sum of $n$ and the sum of $m$ over all test cases does not exceed $2\,000$.</p>





```input1
2
2 2
1 2
2 1


1

0



1

1
3 3
1 2
2 3
3 1


1

1


1

0


1

1

1

1
```




```output1
- 1
? 1

? 2

- 2
+ 1
? 1

! 1 0





- 1
? 2

? 1

- 2
? 3

? 3

+ 1
? 3

? 2

? 1

! 1 1 1
```



## Note

<p>In the first test case, road $1$ was repaired, while road $2$ was not. For the first delivery request, intersection $1$ was selected as $s$, and the path from intersection $1$ to $1$ exists. For the second delivery request, intersection $1$ was selected as $s$. Since the only repaired road was blocked, there was no path between intersections $1$ and $2$. For the third delivery request, intersection $2$ was selected as $s$, the path between intersections $2$ and $1$ exists along road $1$, which is repaired and unblocked.</p><p>In the second test case, intersections $1$, $3$, $1$, $2$, $2$, $3$, $1$ were selected as starting intersections for delivery requests.</p>
