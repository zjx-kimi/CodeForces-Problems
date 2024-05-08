## Description

<div><p>You are given an array of <span class="tex-font-style-bf">positive</span> integers $a$ of length $n$.</p><p>Let's call an array of <span class="tex-font-style-bf">positive</span> integers $b$ of length $n$ <span class="tex-font-style-it">good</span> if: </p><ol> <li> $a_i \neq b_i$ for <span class="tex-font-style-bf">all</span> $i$ from $1$ to $n$, </li><li> $a_1 + a_2 +\ldots + a_n = b_1 + b_2 + \ldots + b_n$. </li></ol><p>Does a good array exist?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10 ^ 9$)&nbsp;— the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes) if there exists a good array, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>","<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10 ^ 9$)&nbsp;— the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes) if there exists a good array, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>","<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,6,7,10,11
6
3
6 1 2
2
1 1
4
3 1 2 4
1
17
5
1 2 1 1 1
3
618343152 819343431 1000000000
```




```output1
YES
NO
YES
NO
NO
YES
```



## Note

<p>In the first test case, a possible <span class="tex-font-style-it">good</span> array is $[3, 3, 3]$. Some examples of not <span class="tex-font-style-it">good</span> arrays are: </p><ul> <li> $[8, 0, 1]$&nbsp;— the array does not consist of only <span class="tex-font-style-bf">positive</span> integers, </li><li> $[5, 2, 4]$&nbsp;— the array does not have the same sum as the given array, </li><li> $[5, 2, 2]$&nbsp;— the third element is equal to the third element of the given array. </li></ul><p>In the second test case, $[1, 1]$ is the only array of positive integers of length $2$ that has the sum of it's elements equal to $2$. Since $[1, 1]$ is not a <span class="tex-font-style-it">good</span> array, the answer is "<span class="tex-font-style-tt">NO</span>".</p>
