## Description

<div><p><a href="https://jojowiki.com/Dio_Brando">DIO</a> knows that the Stardust Crusaders have determined his location and will be coming to fight him. To foil their plans he decides to send out some <a href="https://jojo.fandom.com/wiki/Stand">Stand</a> users to fight them. Initially, he summoned $n$ Stand users with him, the $i$-th one having a strength of $a_i$. Using his vampiric powers, he can do the following as many times as he wishes:</p><ul> <li> Let the <span class="tex-font-style-bf">current</span> number of Stand users be $m$. </li><li> DIO chooses an index $i$ ($1 \le i \le m$). </li><li> Then he summons a new Stand user, with index $m+1$ and strength given by: $$a_{m+1} = a_i \oplus a_{i+1} \oplus \ldots \oplus a_m,$$<p>where the operator $\oplus$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR operation</a>. </p></li><li> Now, the number of Stand users becomes $m+1$. </li></ul><p>Unfortunately for DIO, by using Hermit Purple's divination powers, the Crusaders know that he is plotting this, and they also know the strengths of the original Stand users. Help the Crusaders find the maximum possible <span class="tex-font-style-it">strength</span> of a Stand user among all possible ways that DIO can summon.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10\,000$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$) &nbsp;– the number of Stand users initially summoned.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i &lt; 2^8$) &nbsp;– the strength of each Stand user.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer, maximum <span class="tex-font-style-it">strength</span> of a Stand user among all possible ways that DIO can summon.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10\,000$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$) &nbsp;– the number of Stand users initially summoned.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i &lt; 2^8$) &nbsp;– the strength of each Stand user.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output a single integer, maximum <span class="tex-font-style-it">strength</span> of a Stand user among all possible ways that DIO can summon.</p>





```input1|2,3,6,7
3
4
0 2 5 1
3
1 2 3
5
8 2 4 12 1
```




```output1
7
3
14
```



## Note

<p>In the first test case, one of the ways to add new Stand users is as follows:</p><ul><li> Choose $i=n$. Now, $a$ becomes $[0,2,5,1,1]$.</li><li> Choose $i=1$. Now, $a$ becomes $[0,2,5,1,1,7]$. $7$ is the maximum <span class="tex-font-style-it">strength</span> of a Stand user DIO can summon.</li></ul><p>In the second test case, DIO does not need to add more Stand users because $3$ is the maximum <span class="tex-font-style-it">strength</span> of a Stand user DIO can summon. </p>
