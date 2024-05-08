## Description

<div><p><span class="tex-font-style-it">The only difference between the two versions is that in this version, the constraints are lower.</span></p><p>Initially, array $a$ contains just the number $1$. You can perform several operations in order to change the array. In an operation, you can select some subsequence$^{\dagger}$ of $a$ and add into $a$ an element equal to the sum of all elements of the subsequence. </p><p>You are given a final array $c$. Check if $c$ can be obtained from the initial array $a$ by performing some number (possibly 0) of operations on the initial array.</p><p>$^{\dagger}$ A sequence $b$ is a subsequence of a sequence $a$ if $b$ can be obtained from $a$ by the deletion of several (possibly zero, but not all) elements. In other words, select $k$ ($1 \leq k \leq |a|$) distinct indices $i_1, i_2, \dots, i_k$ and insert anywhere into $a$ a new element with the value equal to $a_{i_1} + a_{i_2} + \dots + a_{i_k}$.</p></div><div class="input-specification"><p>The first line of the input contains an integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 5000$) &nbsp;— the number of elements the final array $c$ should have.</p><p>The second line of each test case contains $n$ space-separated integers $c_i$ ($1 \leq c_i \leq 5000$) &nbsp;— the elements of the final array $c$ that should be obtained from the initial array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5000$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes) if such a sequence of operations exists, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line of the input contains an integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 5000$) &nbsp;— the number of elements the final array $c$ should have.</p><p>The second line of each test case contains $n$ space-separated integers $c_i$ ($1 \leq c_i \leq 5000$) &nbsp;— the elements of the final array $c$ that should be obtained from the initial array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5000$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes) if such a sequence of operations exists, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,3,6,7,10,11
6
1
1
1
2
5
5 1 3 2 1
5
7 1 5 2 1
3
1 1 1
5
1 1 4 2 1
```




```output1
YES
NO
YES
NO
YES
YES
```



## Note

<p>For the first test case, the initial array $a$ is already equal to $[1]$, so the answer is "<span class="tex-font-style-tt">YES</span>".</p><p>For the second test case, performing any amount of operations will change $a$ to an array of size at least two which doesn't only have the element $2$, thus obtaining the array $[2]$ is impossible and the answer is "<span class="tex-font-style-tt">NO</span>".</p><p>For the third test case, we can perform the following operations in order to obtain the final given array $c$:</p><ul><li> Initially, $a = [1]$. </li><li> By choosing the subsequence $[1]$, and inserting $1$ in the array, $a$ changes to $[1, 1]$. </li><li> By choosing the subsequence $[1, 1]$, and inserting $1+1=2$ in the middle of the array, $a$ changes to $[1, 2, 1]$.</li><li> By choosing the subsequence $[1, 2]$, and inserting $1+2=3$ after the first $1$ of the array, $a$ changes to $[1, 3, 2, 1]$.</li><li> By choosing the subsequence $[1, 3, 1]$ and inserting $1+3+1=5$ at the beginning of the array, $a$ changes to $[5, 1, 3, 2, 1]$ (which is the array we needed to obtain).</li></ul>
