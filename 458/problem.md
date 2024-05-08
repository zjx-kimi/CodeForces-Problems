## Description

<div><p>Alchemist Nastya loves mixing potions. There are a total of $n$ types of potions, and one potion of type $i$ can be bought for $c_i$ coins.</p><p>Any kind of potions can be obtained in no more than one way, by mixing from several others. The potions used in the mixing process will be <span class="tex-font-style-bf">consumed</span>. Moreover, no potion can be obtained from itself through one or more mixing processes.</p><p>As an experienced alchemist, Nastya has an <span class="tex-font-style-bf">unlimited</span> supply of $k$ types of potions $p_1, p_2, \dots, p_k$, but she doesn't know which one she wants to obtain next. To decide, she asks you to find, for each $1 \le i \le n$, the minimum number of coins she needs to spend to obtain a potion of type $i$ next.</p></div><div class="input-specification"><p>The first line of each test contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Each test case is described as follows:</p><p>The first line contains two integers $n$ and $k$ ($1 \le k &lt; n \le 2 \cdot 10^5$)&nbsp;— the total number of potion types and the number of potion types Nastya already has.</p><p>The second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($1 \le c_i \le 10^9$)&nbsp;— the costs of buying the potions.</p><p>The third line contains $k$ distinct integers $p_1, p_2, \dots, p_k$ ($1 \le p_i \le n$)&nbsp;— the indices of potions Nastya already has an <span class="tex-font-style-bf">unlimited</span> supply of.</p><p>This is followed by $n$ lines describing ways to obtain potions by mixing.</p><p>Each line starts with the integer $m_i$ ($0 \le m_i &lt; n$)&nbsp;— the number of potions required to mix a potion of the type $i$ ($1 \le i \le n$).</p><p>Then line contains $m_i$ distinct integers $e_1, e_2, \dots, e_{m_i}$ ($1 \le e_j \le n$, $e_j \ne i$)&nbsp;— the indices of potions needed to mix a potion of the type $i$. If this list is empty, then a potion of the type $i$ can only be bought.</p><p>It is guaranteed that no potion can be obtained from itself through one or more mixing processes.</p><p>It is guaranteed that the sum of all $n$ values across all test cases does not exceed $2 \cdot 10^5$. Similarly, it is guaranteed that the sum of all $m_i$ values across all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output $n$ integers&nbsp;— the minimum number of coins Nastya needs to spend to obtain a potion of each type.</p></div>

## Input

<p>The first line of each test contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Each test case is described as follows:</p><p>The first line contains two integers $n$ and $k$ ($1 \le k &lt; n \le 2 \cdot 10^5$)&nbsp;— the total number of potion types and the number of potion types Nastya already has.</p><p>The second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($1 \le c_i \le 10^9$)&nbsp;— the costs of buying the potions.</p><p>The third line contains $k$ distinct integers $p_1, p_2, \dots, p_k$ ($1 \le p_i \le n$)&nbsp;— the indices of potions Nastya already has an <span class="tex-font-style-bf">unlimited</span> supply of.</p><p>This is followed by $n$ lines describing ways to obtain potions by mixing.</p><p>Each line starts with the integer $m_i$ ($0 \le m_i &lt; n$)&nbsp;— the number of potions required to mix a potion of the type $i$ ($1 \le i \le n$).</p><p>Then line contains $m_i$ distinct integers $e_1, e_2, \dots, e_{m_i}$ ($1 \le e_j \le n$, $e_j \ne i$)&nbsp;— the indices of potions needed to mix a potion of the type $i$. If this list is empty, then a potion of the type $i$ can only be bought.</p><p>It is guaranteed that no potion can be obtained from itself through one or more mixing processes.</p><p>It is guaranteed that the sum of all $n$ values across all test cases does not exceed $2 \cdot 10^5$. Similarly, it is guaranteed that the sum of all $m_i$ values across all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output $n$ integers&nbsp;— the minimum number of coins Nastya needs to spend to obtain a potion of each type.</p>





```input1|2,3,4,5,6,7,8,9,16,17,18,19,20,21,22,23
4
5 1
30 8 3 5 10
3
3 2 4 5
0 
0 
2 3 5
0 
3 2
5 143 3
1 3
1 2
0 
2 1 2
5 1
5 4 1 3 4
2
2 4 5
3 3 5 4
2 1 4
1 5
0 
4 2
1 1 5 4
2 4
3 2 4 3
0 
2 2 4
1 2
```




```input2|2,3,4,5,6,7,8,9,10,20,21,22,23,24
3
6 3
5 5 4 5 2 2
3 4 5
2 2 5
1 5
3 4 1 6
4 2 6 1 5
0 
0 
6 2
1 4 4 1 5 2
3 6
4 6 3 4 5
4 6 5 3 4
0 
1 5
1 6
0 
2 1
4 3
1
0 
1 1
```




```output1
23 8 0 5 10 
0 143 0 
5 0 1 3 4 
0 0 0 0
```




```output2
0 0 0 0 0 2 
0 0 0 0 0 0 
0 0
```



## Note

<p>In the first test case of the first sample, it is optimal:</p><ul> <li> Get a potion of the first type by buying and mixing $2$, $4$ and $5$; </li><li> a potion of the second type can only be obtained by purchasing it; </li><li> Nastya already has an unlimited number of potions of the third type; </li><li> a potion of the fourth type is more profitable to buy than to buy and mix other potions; </li><li> a potion of the fifth type can only be obtained by purchasing it. </li></ul>
