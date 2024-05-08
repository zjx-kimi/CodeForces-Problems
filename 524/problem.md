## Description

<div><p>The array $[a_1, a_2, \dots, a_k]$ is called <span class="tex-font-style-it">beautiful</span> if it is possible to remove several (maybe zero) elements from the beginning of the array and insert all these elements to the back of the array in the same order in such a way that the resulting array is sorted in non-descending order.</p><p>In other words, the array $[a_1, a_2, \dots, a_k]$ is <span class="tex-font-style-it">beautiful</span> if there exists an integer $i \in [0, k-1]$ such that the array $[a_{i+1}, a_{i+2}, \dots, a_{k-1}, a_k, a_1, a_2, \dots, a_i]$ is sorted in non-descending order.</p><p>For example:</p><ul> <li> $[3, 7, 7, 9, 2, 3]$ is <span class="tex-font-style-it">beautiful</span>: we can remove four first elements and insert them to the back in the same order, and we get the array $[2, 3, 3, 7, 7, 9]$, which is sorted in non-descending order; </li><li> $[1, 2, 3, 4, 5]$ is <span class="tex-font-style-it">beautiful</span>: we can remove zero first elements and insert them to the back, and we get the array $[1, 2, 3, 4, 5]$, which is sorted in non-descending order; </li><li> $[5, 2, 2, 1]$ is not <span class="tex-font-style-it">beautiful</span>. </li></ul><p><span class="tex-font-style-bf">Note that any array consisting of zero elements or one element is <span class="tex-font-style-it">beautiful</span></span>.</p><p>You are given an array $a$, which is initially <span class="tex-font-style-bf">empty</span>. You have to process $q$ queries to it. During the $i$-th query, you will be given one integer $x_i$, and you have to do the following:</p><ul> <li> if you can append the integer $x_i$ to the <span class="tex-font-style-bf">back</span> of the array $a$ so that the array $a$ stays <span class="tex-font-style-it">beautiful</span>, you have to append it; </li><li> otherwise, do nothing. </li></ul><p>After each query, report whether you appended the given integer $x_i$, or not.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of two lines. The first line contains one integer $q$ ($1 \le q \le 2 \cdot 10^5$) — the number of queries. The second line contains $q$ integers $x_1, x_2, \dots, x_q$ ($0 \le x_i \le 10^9$).</p><p>Additional constraint on the input: the sum of $q$ over all test cases does not exceed $2 \cdot 10^5$).</p></div><div class="output-specification"><p>For each test case, print one string consisting of exactly $q$ characters. The $i$-th character of the string should be <span class="tex-font-style-tt">1</span> if you appended the integer during the $i$-th query; otherwise, it should be <span class="tex-font-style-tt">0</span>.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of two lines. The first line contains one integer $q$ ($1 \le q \le 2 \cdot 10^5$) — the number of queries. The second line contains $q$ integers $x_1, x_2, \dots, x_q$ ($0 \le x_i \le 10^9$).</p><p>Additional constraint on the input: the sum of $q$ over all test cases does not exceed $2 \cdot 10^5$).</p>

## Output

<p>For each test case, print one string consisting of exactly $q$ characters. The $i$-th character of the string should be <span class="tex-font-style-tt">1</span> if you appended the integer during the $i$-th query; otherwise, it should be <span class="tex-font-style-tt">0</span>.</p>





```input1|2,3,6,7
3
9
3 7 7 9 2 4 6 3 4
5
1 1 1 1 1
5
3 2 1 2 3
```




```output1
111110010
11111
11011
```



## Note

<p>Consider the first test case of the example. Initially, the array is $[]$.</p><ul> <li> trying to append an integer $3$. The array $[3]$ is beautiful, so we append $3$; </li><li> trying to append an integer $7$. The array $[3, 7]$ is beautiful, so we append $7$; </li><li> trying to append an integer $7$. The array $[3, 7, 7]$ is beautiful, so we append $7$; </li><li> trying to append an integer $9$. The array $[3, 7, 7, 9]$ is beautiful, so we append $9$; </li><li> trying to append an integer $2$. The array $[3, 7, 7, 9, 2]$ is beautiful, so we append $2$; </li><li> trying to append an integer $4$. The array $[3, 7, 7, 9, 2, 4]$ is not beautiful, so we don't append $4$; </li><li> trying to append an integer $6$. The array $[3, 7, 7, 9, 2, 6]$ is not beautiful, so we don't append $6$; </li><li> trying to append an integer $3$. The array $[3, 7, 7, 9, 2, 3]$ is beautiful, so we append $3$; </li><li> trying to append an integer $4$. The array $[3, 7, 7, 9, 2, 3, 4]$ is not beautiful, so we don't append $4$. </li></ul>
