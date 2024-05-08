## Description

<div><p>You have an array $a_1, a_2, \dots, a_n$. Answer $q$ queries of the following form: </p><ul> <li> If we change all elements in the range $a_l, a_{l+1}, \dots, a_r$ of the array to $k$, will the sum of the entire array be odd? </li></ul> Note that queries are <span class="tex-font-style-bf">independent</span> and do not affect future queries.</div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case consists of $2$ integers $n$ and $q$ ($1 \le n \le 2 \cdot 10^5$; $1 \le q \le 2 \cdot 10^5$)&nbsp;— the length of the array and the number of queries.</p><p>The second line of each test case consists of $n$ integers $a_i$ ($1 \le a_i \le 10^9$)&nbsp;— the array $a$.</p><p>The next $q$ lines of each test case consists of $3$ integers $l,r,k$ ($1 \le l \le r \le n$; $1 \le k \le 10^9$)&nbsp;— the queries.</p><p>It is guaranteed that the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$, and the sum of $q$ doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each query, output "<span class="tex-font-style-tt">YES</span>" if the sum of the entire array becomes odd, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case consists of $2$ integers $n$ and $q$ ($1 \le n \le 2 \cdot 10^5$; $1 \le q \le 2 \cdot 10^5$)&nbsp;— the length of the array and the number of queries.</p><p>The second line of each test case consists of $n$ integers $a_i$ ($1 \le a_i \le 10^9$)&nbsp;— the array $a$.</p><p>The next $q$ lines of each test case consists of $3$ integers $l,r,k$ ($1 \le l \le r \le n$; $1 \le k \le 10^9$)&nbsp;— the queries.</p><p>It is guaranteed that the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$, and the sum of $q$ doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each query, output "<span class="tex-font-style-tt">YES</span>" if the sum of the entire array becomes odd, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,4,5,6,7,8
2
5 5
2 2 1 3 2
2 3 3
2 3 4
1 5 5
1 4 9
2 4 3
10 5
1 1 1 1 1 1 1 1 1 1
3 8 13
2 5 10
3 8 10
1 10 2
1 9 100
```




```output1
YES
YES
YES
NO
YES
NO
NO
NO
NO
YES
```



## Note

<p>For the first test case: </p><ul> <li> If the elements in the range $(2, 3)$ would get set to $3$ the array would become $\{2, 3, 3, 3, 2\}$, the sum would be $2+3+3+3+2 = 13$ which is odd, so the answer is "<span class="tex-font-style-tt">YES</span>".</li><li> If the elements in the range $(2, 3)$ would get set to $4$ the array would become $\{2, 4, 4, 3, 2\}$, the sum would be $2+4+4+3+2 = 15$ which is odd, so the answer is "<span class="tex-font-style-tt">YES</span>".</li><li> If the elements in the range $(1, 5)$ would get set to $5$ the array would become $\{5, 5, 5, 5, 5\}$, the sum would be $5+5+5+5+5 = 25$ which is odd, so the answer is "<span class="tex-font-style-tt">YES</span>".</li><li> If the elements in the range $(1, 4)$ would get set to $9$ the array would become $\{9, 9, 9, 9, 2\}$, the sum would be $9+9+9+9+2 = 38$ which is even, so the answer is "<span class="tex-font-style-tt">NO</span>".</li><li> If the elements in the range $(2, 4)$ would get set to $3$ the array would become $\{2, 3, 3, 3, 2\}$, the sum would be $2+3+3+3+2 = 13$ which is odd, so the answer is "<span class="tex-font-style-tt">YES</span>". </li></ul>
