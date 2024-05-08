## Description

<div><p>There are $n$ cities and $n-1$ two-way roads in Treeland. Each road connects a pair of different cities. From any city you can drive to any other, moving only along the roads. Cities are numbered from $1$ to $n$. Yes, of course, you recognized an undirected tree in this description.</p><p>The government plans to repair all the roads. Each road will be repaired by some private company. In total, the country has $10^6$ private companies that are numbered from $1$ to $10^6$. It is possible that some companies will not repair roads at all, and some will repair many roads.</p><p>To simplify the control over the work of private companies, the following restriction was introduced: for each city, we calculate the number of different companies that repair roads that have this city at one end. This number for each city should not exceed $2$. In other words, for each city, there should be no more than two different companies that repair roads related to this city.</p><p>The National Anti-Corruption Committee of Treeland raises concerns that all (or almost all) of the work will go to one private company. For this reason, the committee requires that roads be distributed among companies in such a way as to minimize the value of $r$. For each company, we calculate the number of roads assigned to it, the maximum among all companies is called the number $r$.</p><p>Help the government find such a way to distribute all roads among companies in the required way.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 1000$) — the number of input cases in the input. Next, the input cases themselves are given. The first line of each test case set contains an integer $n$ ($2 \le n \le 3000$) — the number of cities in Treeland. Next, in the $n-1$ lines the roads are written: a line contains two integers $x_i$, $y_i$ ($1 \le x_i, y_i \le n$), indicating that the $i$-th road connects the cities $x_i$ and $y_i$.</p><p>It is guaranteed that the sum of all values $n$ ​​for all test cases in the input does not exceed $3000$.</p></div><div class="output-specification"><p>Print the answers for all $t$ test cases in the input. Each test case must begin with a line that contains $r$ — the minimum possible number of roads assigned to the most used company. Next, in the next line print $n-1$ the number $c_1, c_2, \dots, c_{n-1}$ ($1 \le c_i \le 10^6$), where $c_i$ indicates the company to repair the $i$-th road. If there are several optimal assignments, print any of them.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 1000$) — the number of input cases in the input. Next, the input cases themselves are given. The first line of each test case set contains an integer $n$ ($2 \le n \le 3000$) — the number of cities in Treeland. Next, in the $n-1$ lines the roads are written: a line contains two integers $x_i$, $y_i$ ($1 \le x_i, y_i \le n$), indicating that the $i$-th road connects the cities $x_i$ and $y_i$.</p><p>It is guaranteed that the sum of all values $n$ ​​for all test cases in the input does not exceed $3000$.</p>

## Output

<p>Print the answers for all $t$ test cases in the input. Each test case must begin with a line that contains $r$ — the minimum possible number of roads assigned to the most used company. Next, in the next line print $n-1$ the number $c_1, c_2, \dots, c_{n-1}$ ($1 \le c_i \le 10^6$), where $c_i$ indicates the company to repair the $i$-th road. If there are several optimal assignments, print any of them.</p>





```input1
3
3
1 2
2 3
6
1 2
1 3
1 4
1 5
1 6
7
3 1
1 4
4 6
5 1
2 4
1 7
```




```output1
1
10 20
3
1 1 1 2 2 
2
11 11 12 13 12 13
```


