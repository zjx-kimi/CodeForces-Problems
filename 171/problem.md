## Description

<div><p>Theofanis easily gets obsessed with problems before going to sleep and often has nightmares about them. To deal with his obsession he visited his doctor, Dr. Emix.</p><p>In his latest nightmare, he has an array $a$ of size $n$ and wants to divide it into non-empty subarrays$^{\dagger}$ such that every element is in exactly one of the subarrays.</p><p>For example, the array $[1,-3,7,-6,2,5]$ can be divided to $[1] [-3,7] [-6,2] [5]$. </p><p>The Cypriot value of such division is equal to $\Sigma_{i=1}^{k} i \cdot \mathrm{sum}_i$ where $k$ is the number of subarrays that we divided the array into and $\mathrm{sum}_i$ is the sum of the $i$-th subarray.</p><p>The Cypriot value of this division of the array $[1] [-3,7] [-6,2] [5] = 1 \cdot 1 + 2 \cdot (-3 + 7) + 3 \cdot (-6 + 2) + 4 \cdot 5 = 17$. </p><p>Theofanis is wondering what is the <span class="tex-font-style-bf">maximum</span> Cypriot value of any division of the array.</p><p>$^{\dagger}$ An array $b$ is a subarray of an array $a$ if $b$ can be obtained from $a$ by deletion of several (possibly, zero or all) elements from the beginning and several (possibly, zero or all) elements from the end. In particular, an array is a subarray of itself.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Each test case consists of two lines. </p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^{5}$)&nbsp;— the size of the array. </p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^8 \le a_i \le 10^{8}$)&nbsp;— the elements of the array.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^{5}$.</p></div><div class="output-specification"><p>For each test case, print one integer&nbsp;— the <span class="tex-font-style-bf">maximum</span> Cypriot value of the array $a$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Each test case consists of two lines. </p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^{5}$)&nbsp;— the size of the array. </p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^8 \le a_i \le 10^{8}$)&nbsp;— the elements of the array.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^{5}$.</p>

## Output

<p>For each test case, print one integer&nbsp;— the <span class="tex-font-style-bf">maximum</span> Cypriot value of the array $a$.</p>





```input1|2,3,6,7
4
6
1 -3 7 -6 2 5
4
2 9 -5 -3
8
-3 -4 2 -5 1 10 17 23
1
830
```




```output1
32
4
343
830
```



## Note

<p>In the first test case, to get the maximum Cypriot value we divide the array into $[1][-3][7][-6][2][5]$ which gives us: $\Sigma_{i=1}^{k} i \cdot \mathrm{sum}_i = 1 \cdot 1 + 2 \cdot (-3) + 3 \cdot 7 + 4 \cdot (-6) + 5 \cdot 2 + 6 \cdot 5 = 32$</p><p>Similarly, in the second test case we divide the array into $[2][9,-5,-3]$ which gives us $\Sigma_{i=1}^{k} i \cdot \mathrm{sum}_i = 1 \cdot 2 + 2 \cdot (9 + (-5) + (-3)) = 4$.</p>
