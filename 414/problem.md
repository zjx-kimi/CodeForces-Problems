## Description

<div><p>Monocarp had an array $a$ consisting of integers. Initially, <span class="tex-font-style-bf">this array was empty</span>.</p><p>Monocarp performed three types of queries to this array:</p><ul> <li> choose an integer and append it <span class="tex-font-style-bf">to the end of the array</span>. Each time Monocarp performed a query of this type, he wrote out a character <span class="tex-font-style-tt">+</span>; </li><li> remove <span class="tex-font-style-bf">the last element</span> from the array. Each time Monocarp performed a query of this type, he wrote out a character <span class="tex-font-style-tt">-</span>. Monocarp never performed this query on an empty array; </li><li> check if the array is sorted in non-descending order, i.,e. $a_1 \le a_2 \le \dots \le a_k$, where $k$ is the number of elements in the array currently. <span class="tex-font-style-bf">Every array with less than $2$ elements is considered sorted</span>. If the array was sorted by the time Monocarp was performing that query, he wrote out a character <span class="tex-font-style-tt">1</span>. Otherwise, he wrote out a character <span class="tex-font-style-tt">0</span>. </li></ul><p>You are given a sequence $s$ of $q$ characters <span class="tex-font-style-tt">0</span>, <span class="tex-font-style-tt">1</span>, <span class="tex-font-style-tt">+</span> and/or <span class="tex-font-style-tt">-</span>. These are the characters that were written out by Monocarp, given in the exact order he wrote them out.</p><p>You have to check if this sequence is consistent, i. e. it was possible for Monocarp to perform the queries so that the sequence of characters he wrote out is exactly $s$.</p></div><div class="input-specification"><p>The first line of the input contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of one line containing the string $s$ ($1 \le |s| \le 2 \cdot 10^5$). This string consists of characters <span class="tex-font-style-tt">0</span>, <span class="tex-font-style-tt">1</span>, <span class="tex-font-style-tt">+</span> and/or <span class="tex-font-style-tt">-</span>. This is the sequence of characters written by Monocarp, in the order he wrote them.</p><p>Additional constraints on the input: </p><ul> <li> for every prefix of $s$, the number of characters <span class="tex-font-style-tt">+</span> on it is not less than the number of characters <span class="tex-font-style-tt">-</span> on it. In other words, if Monocarp actually performed these queries, he would never try to remove the last element from the empty array; </li><li> the sum of $|s|$ over all test cases does not exceed $2 \cdot 10^5$. </li></ul></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">YES</span> if it was possible for Monocarp to perform the queries so that the sequence of characters he wrote is exactly $s$. Otherwise, print <span class="tex-font-style-tt">NO</span>.</p><p>You can print each letter in any register.</p></div>

## Input

<p>The first line of the input contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of one line containing the string $s$ ($1 \le |s| \le 2 \cdot 10^5$). This string consists of characters <span class="tex-font-style-tt">0</span>, <span class="tex-font-style-tt">1</span>, <span class="tex-font-style-tt">+</span> and/or <span class="tex-font-style-tt">-</span>. This is the sequence of characters written by Monocarp, in the order he wrote them.</p><p>Additional constraints on the input: </p><ul> <li> for every prefix of $s$, the number of characters <span class="tex-font-style-tt">+</span> on it is not less than the number of characters <span class="tex-font-style-tt">-</span> on it. In other words, if Monocarp actually performed these queries, he would never try to remove the last element from the empty array; </li><li> the sum of $|s|$ over all test cases does not exceed $2 \cdot 10^5$. </li></ul>

## Output

<p>For each test case, print <span class="tex-font-style-tt">YES</span> if it was possible for Monocarp to perform the queries so that the sequence of characters he wrote is exactly $s$. Otherwise, print <span class="tex-font-style-tt">NO</span>.</p><p>You can print each letter in any register.</p>





```input1|2,4,6,8
7
++1
+++1--0
+0
0
++0-+1-+0
++0+-1+-0
+1-+0
```




```output1
YES
NO
NO
NO
YES
NO
NO
```



## Note

<p>In the first test case, Monocarp could perform the following sequence of queries:</p><ul> <li> add the integer $13$; </li><li> add the integer $37$; </li><li> check that the current array $[13, 37]$ is sorted in non-descending order (and it is sorted). </li></ul><p>In the fifth test case, Monocarp could perform the following sequence of queries:</p><ul> <li> add the integer $3$; </li><li> add the integer $2$; </li><li> check that the current array $[3, 2]$ is sorted (it is not); </li><li> remove the last element; </li><li> add the integer $3$; </li><li> check that the current array $[3, 3]$ is sorted (it is); </li><li> remove the last element; </li><li> add the integer $-5$; </li><li> check that the current array $[3, -5]$ is sorted (it is not). </li></ul><p>In all other test cases of the example test, it is impossible for Monocarp to write the sequence $s$ when performing the queries according to the statement.</p>
