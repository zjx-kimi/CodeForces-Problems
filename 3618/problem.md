## Description

<div><p>The director of the famous dance show plans a tour. It is already decided that the tour will consist of up to $m$ concerts.</p><p>There are $n$ dancers in the troupe. Each dancer is characterized by her awkwardness: the awkwardness of the $i$-th dancer is equal to $a_i$.</p><p>The director likes diversity. For this reason, each concert will be performed by a different set of dancers. A dancer may perform in multiple concerts. For example, it is possible that a set of dancers performs in one concert and a subset of this set of dancers performs in another concert. The only constraint is that the same set of dancers cannot perform twice.</p><p>The director prefers the set with larger number of dancers over the set with smaller number of dancers. If two sets consist of the same number of dancers, then the director prefers the one which has smaller sum of awkwardness of dancers. If two sets of dancers are equal in size and total awkwardness, then the director does not have a preference which one is better.</p><p>A marketing study shows that viewers are not ready to come to a concert if the total awkwardness of all the dancers performing in the concert is greater than $k$.</p><p>The director wants to find the best plan for $m$ concerts. He thinks to write down all possible sets of dancers; then get rid of the sets with total awkwardness greater than $k$. The remaining sets of dancers will be sorted according to his preference. The most preferred set of dancers will give the first concert, the second preferred set — the second concert and so on until the $m$-th concert. If it turns out that the total number of valid sets is less than $m$, then the total number of concerts will be equal to the number of valid sets.</p><p>It turns out that the director delegated finding the plan to you! Please, notice that there might be several acceptable plans due to the fact that the director does not have a preference over sets of dancers with the same size and total awkwardness. In this case any of these plans is good enough. For each concert find the number of dancers and the total awkwardness of the set performing. Also, for the last concert find its set of dancers.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10^5$) — the number of test cases in the input. Then the test cases follow.</p><p>Each test case begins with a line containing three integers $n$, $k$ and $m$ ($1 \le n \le 10^6$, $1 \le k \le 10^{18}$, $1 \le m \le 10^6$) — the total number of dancers, the maximum acceptable awkwardness of a set of dancers and the maximum number of concerts, respectively.</p><p>The following line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^{12}$), where $a_i$ is the awkwardness of the $i$-th dancer.</p><p>The sum of the values of $n$ over all test cases in the input does not exceed $10^6$. Similarly, the sum of the values of $m$ over all test cases in the input does not exceed $10^6$.</p></div><div class="output-specification"><p>Print the answers to all test cases in the input.</p><p>If the troupe cannot give concerts at all, then simply print one line "<span class="tex-font-style-tt">0</span>". In this case, you should not print anything else.</p><p>If the troupe gives a positive number of concerts $r$ ($r$ is equal to the minimum of $m$ and the total number of valid sets), then first print the value of $r$, then $r$ lines: the $j$-th line should contain two integers $s_j$ and $t_j$ — the number of dancers in the $j$-th concert and the total awkwardness of the dancers performing in the $j$-th concert. Complete the output to a test case with a line that describes the last set: print exactly $s_r$ distinct integers from $1$ to $n$ — the numbers of the dancers who will perform at the $r$-th (last) concert, in any order. If there are several answers, print any of them.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10^5$) — the number of test cases in the input. Then the test cases follow.</p><p>Each test case begins with a line containing three integers $n$, $k$ and $m$ ($1 \le n \le 10^6$, $1 \le k \le 10^{18}$, $1 \le m \le 10^6$) — the total number of dancers, the maximum acceptable awkwardness of a set of dancers and the maximum number of concerts, respectively.</p><p>The following line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^{12}$), where $a_i$ is the awkwardness of the $i$-th dancer.</p><p>The sum of the values of $n$ over all test cases in the input does not exceed $10^6$. Similarly, the sum of the values of $m$ over all test cases in the input does not exceed $10^6$.</p>

## Output

<p>Print the answers to all test cases in the input.</p><p>If the troupe cannot give concerts at all, then simply print one line "<span class="tex-font-style-tt">0</span>". In this case, you should not print anything else.</p><p>If the troupe gives a positive number of concerts $r$ ($r$ is equal to the minimum of $m$ and the total number of valid sets), then first print the value of $r$, then $r$ lines: the $j$-th line should contain two integers $s_j$ and $t_j$ — the number of dancers in the $j$-th concert and the total awkwardness of the dancers performing in the $j$-th concert. Complete the output to a test case with a line that describes the last set: print exactly $s_r$ distinct integers from $1$ to $n$ — the numbers of the dancers who will perform at the $r$-th (last) concert, in any order. If there are several answers, print any of them.</p>





```input1
3
7 13 10
3 1 5 1 8 2 13
2 10 1
12 12
3 32 100000
2 1 5
```




```output1
10
5 12
4 7
4 9
4 10
4 11
4 11
4 12
4 13
3 4
3 5
2 4 1 
0
7
3 8
2 3
2 6
2 7
1 1
1 2
1 5
3
```


