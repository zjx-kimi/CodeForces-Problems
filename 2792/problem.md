## Description

<div><p>Sarah has always been a lover of nature, and a couple of years ago she saved up enough money to travel the world and explore all the things built by nature over its lifetime on earth. During this time she visited some truly special places which were left untouched for centuries, from watching icebergs in freezing weather to scuba-diving in oceans and admiring the sea life, residing unseen. These experiences were enhanced with breathtaking views built by mountains over time and left there for visitors to see for years on end. Over time, all these expeditions took a toll on Sarah and culminated in her decision to settle down in the suburbs and live a quiet life. </p><p>However, as Sarah's love for nature never faded, she started growing flowers in her garden in an attempt to stay connected with nature. At the beginning she planted only blue orchids, but over time she started using different flower types to add variety to her collection of flowers. This collection of flowers can be represented as an array of $N$ flowers and the $i$-th of them has a type associated with it, denoted as $A_i$. Each resident, passing by her collection and limited by the width of his view, can only see $K$ contiguous flowers at each moment in time. To see the whole collection, the resident will look at the first $K$ contiguous flowers $A_1, A_2, ..., A_K$, then shift his view by one flower and look at the next section of K contiguous flowers $A_2, A_3, ..., A_{K+1}$ and so on until they scan the whole collection, ending with section $A_{N-K+1}, ..., A_{N-1}, A_N$.</p><p>Each resident determines the beautiness of a section of $K$ flowers as the number of distinct flower types in that section. Furthermore, the <span class="tex-font-style-bf">beautiness</span> of the whole collection is calculated by summing the beautiness values of each contiguous section. Formally, beautiness $B_i$ of a section starting at the $i$-th position is calculated as $B_i = distinct(A_i, A_{i+1}, ..., A_{i+K-1})$, and <span class="tex-font-style-bf">beautiness</span> of the collection $B$ is calculated as $B=B_1 + B_2 + ... + B_{N-K+1}$.</p><p>In addition, as Sarah wants to keep her collection of flowers have a fresh feel, she can also pick two points $L$ and $R$, dispose flowers between those two points and plant new flowers, all of them being the same type.</p><p>You will be given $Q$ queries and each of those queries will be of the following two types: </p><ol> <li> You will be given three integers $L, R, X$ describing that Sarah has planted flowers of type $X$ between positions $L$ and $R$ inclusive. Formally collection is changed such that $A[i]=X$ for all $i$ in range $[L.. R]$. </li><li> You will be given integer $K$, width of the resident's view and you have to determine the beautiness value $B$ resident has associated with the collection </li></ol><p>For each query of second type print the result – beautiness $B$ of the collection.</p></div><div class="input-specification"><p>First line contains two integers $N$ and $Q \;(1 \leq N, Q \leq 10^5)\,$ — number of flowers and the number of queries, respectively.</p><p>The second line contains $N$ integers $A_1, A_2, ..., A_N\;(1 \leq A_i \leq 10^9)\,$ — where $A_i$ represents type of the $i$-th flower.</p><p>Each of the next $Q$ lines describe queries and start with integer $T\in\{1, 2\}$. </p><ul> <li> If $T = 1$, there will be three more integers in the line $L, R, X\;(1 \leq L, R \leq N;\; 1 \leq X \leq 10^9)\,$ — $L$ and $R$ describing boundaries and $X$ describing the flower type </li><li> If $T = 2$, there will be one more integer in the line $K\;(1 \leq K \leq N)\,$ — resident's width of view </li></ul></div><div class="output-specification"><p>For each query of the second type print the beautiness $B$ of the collection.</p></div>

## Input

<p>First line contains two integers $N$ and $Q \;(1 \leq N, Q \leq 10^5)\,$ — number of flowers and the number of queries, respectively.</p><p>The second line contains $N$ integers $A_1, A_2, ..., A_N\;(1 \leq A_i \leq 10^9)\,$ — where $A_i$ represents type of the $i$-th flower.</p><p>Each of the next $Q$ lines describe queries and start with integer $T\in\{1, 2\}$. </p><ul> <li> If $T = 1$, there will be three more integers in the line $L, R, X\;(1 \leq L, R \leq N;\; 1 \leq X \leq 10^9)\,$ — $L$ and $R$ describing boundaries and $X$ describing the flower type </li><li> If $T = 2$, there will be one more integer in the line $K\;(1 \leq K \leq N)\,$ — resident's width of view </li></ul>

## Output

<p>For each query of the second type print the beautiness $B$ of the collection.</p>





```input1
5 5
1 2 3 4 5
2 3
1 1 2 5
2 4
1 2 4 5
2 2
```




```output1
9
6
4
```



## Note

<p>Let's look at the example.</p><p>Initially the collection is $[1, 2, 3, 4, 5]$. In the first query $K = 3$, we consider sections of three flowers with the first being $[1, 2, 3]$. Since beautiness of the section is the number of distinct flower types in that section, $B_1 = 3$. Second section is $[2, 3, 4]$ and $B_2 = 3$. Third section is $[3, 4, 5]$ and $B_3 = 3$, since the flower types are all distinct. The beautiness value resident has associated with the collection is $B = B_1 + B_2 + B_3 = 3 + 3 + 3 = 9$.</p><p>After the second query, the collection becomes $[5, 5, 3, 4, 5]$. </p><p>For the third query $K = 4$, so we consider sections of four flowers with the first being $[5, 5, 3, 4]$. There are three distinct flower types $[5, 3, 4]$ in this section, so $B_1 = 3$. Second section $[5, 3, 4, 5]$ also has $3$ distinct flower types, so $B_2 = 3$. The beautiness value resident has associated with the collection is $B = B_1 + B_2 = 3 + 3 = 6$</p><p>After the fourth query, the collection becomes $[5, 5, 5, 5, 5]$.</p><p>For the fifth query $K = 2$ and in this case all the four sections are same with each of them being $[5, 5]$. Beautiness of $[5, 5]$ is $1$ since there is only one distinct element in this section $[5]$. Beautiness of the whole collection is $B = B_1 + B_2 + B_3 + B_4 = 1 + 1 + 1 + 1 = 4$</p>
