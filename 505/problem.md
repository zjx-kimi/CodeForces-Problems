## Description

<div><p><span class="tex-font-style-bf">This is the simple version of the problem. The only difference between the simple and hard versions is that in this version $u = 1$.</span></p><p>As is known, Omsk is the capital of Berland. Like any capital, Omsk has a well-developed metro system. The Omsk metro consists of a certain number of stations connected by tunnels, and between any two stations there is exactly one path that passes through each of the tunnels no more than once. In other words, the metro is a tree.</p><p>To develop the metro and attract residents, the following system is used in Omsk. Each station has its own weight $x \in \{-1, 1\}$. If the station has a weight of $-1$, then when the station is visited by an Omsk resident, a fee of $1$ burle is charged. If the weight of the station is $1$, then the Omsk resident is rewarded with $1$ burle.</p><p>Omsk Metro currently has only one station with number $1$ and weight $x = 1$. Every day, one of the following events occurs:</p><ul> <li> <span class="tex-font-style-it">A new station with weight $x$ is added to the station with number $v_i$, and it is assigned a number that is one greater than the number of existing stations.</span> </li><li> <span class="tex-font-style-it">Alex, who lives in Omsk, wonders: is there a subsegment$\dagger$ (possibly empty) of the path between vertices $u$ and $v$ such that, by traveling along it, exactly $k$ burles can be earned (if $k &lt; 0$, this means that $k$ burles will have to be spent on travel). In other words, Alex is interested in whether there is such a subsegment of the path that the sum of the weights of the vertices in it is equal to $k$. Note that the subsegment can be empty, and then the sum is equal to $0$.</span> </li></ul><p>You are a friend of Alex, so your task is to answer Alex's questions.</p><p>$\dagger$Subsegment&nbsp;— continuous sequence of elements.</p></div><div class="input-specification"><p>The first line contains a single number $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains the number $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of events.</p><p>Then there are $n$ lines describing the events. In the $i$-th line, one of the following options is possible:</p><ul> <li> First comes the symbol "+" (without quotes), then two numbers $v_i$ and $x_i$ ($x_i \in \{-1, 1\}$, it is also guaranteed that the vertex with number $v_i$ exists). In this case, a new station with weight $x_i$ is added to the station with number $v_i$. </li><li> First comes the symbol "?" (without quotes), and then three numbers $u_i$, $v_i$, and $k_i$ ($-n \le k_i \le n$). It is guaranteed that the vertices with numbers $u_i$ and $v_i$ exist. In this case, it is necessary to determine whether there is a subsegment (possibly empty) of the path between stations $u_i$ and $v_i$ with a sum of weights exactly equal to $k_i$. <span class="tex-font-style-bf">In this version of the task, it is guaranteed that $u_i = 1$.</span> </li></ul><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each of Alex's questions, output <span class="tex-font-style-tt">"Yes"</span> (without quotes) if the subsegment described in the condition exists, otherwise output <span class="tex-font-style-tt">"No"</span> (without quotes).</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line contains a single number $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains the number $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of events.</p><p>Then there are $n$ lines describing the events. In the $i$-th line, one of the following options is possible:</p><ul> <li> First comes the symbol "+" (without quotes), then two numbers $v_i$ and $x_i$ ($x_i \in \{-1, 1\}$, it is also guaranteed that the vertex with number $v_i$ exists). In this case, a new station with weight $x_i$ is added to the station with number $v_i$. </li><li> First comes the symbol "?" (without quotes), and then three numbers $u_i$, $v_i$, and $k_i$ ($-n \le k_i \le n$). It is guaranteed that the vertices with numbers $u_i$ and $v_i$ exist. In this case, it is necessary to determine whether there is a subsegment (possibly empty) of the path between stations $u_i$ and $v_i$ with a sum of weights exactly equal to $k_i$. <span class="tex-font-style-bf">In this version of the task, it is guaranteed that $u_i = 1$.</span> </li></ul><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each of Alex's questions, output <span class="tex-font-style-tt">"Yes"</span> (without quotes) if the subsegment described in the condition exists, otherwise output <span class="tex-font-style-tt">"No"</span> (without quotes).</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,3,4,5,6,7,8,9,10
1
8
+ 1 -1
? 1 1 2
? 1 2 1
+ 1 1
? 1 3 -1
? 1 1 1
? 1 3 2
? 1 1 0
```




```input2|2,3,4,5,6,7,8,9,10,11,12
1
10
+ 1 -1
+ 1 -1
+ 3 1
+ 3 -1
+ 3 1
? 1 6 -1
? 1 6 2
? 1 2 0
? 1 5 -2
? 1 4 3
```




```output1
NO
YES
NO
YES
YES
YES
```




```output2
YES
NO
YES
YES
NO
```



## Note

<p>Explanation of the first sample.</p><p>The answer to the second question is <span class="tex-font-style-tt">"Yes"</span>, because there is a path $1$.</p><p>In the fourth question, we can choose the $1$ path again.</p><p>In the fifth query, the answer is <span class="tex-font-style-tt">"Yes"</span>, since there is a path $1-3$.</p><p>In the sixth query, we can choose an empty path because the sum of the weights on it is $0$.</p><p>It is not difficult to show that there are no paths satisfying the first and third queries.</p>
