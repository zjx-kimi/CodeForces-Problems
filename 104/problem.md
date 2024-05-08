## Description

<div><p>In the long-forgotten halls of Kombinatoria's ancient academy, a gifted mathematician named Kim is faced with an unusual challenge. They found an old sequence of integers, which is believed to be a cryptic message from the legendary Kombinatoria's Oracle, and Kim wants to decipher its hidden meaning.</p><p>Kim's mission is to find specific patterns within the sequence, known as <span class="tex-font-style-underline">Harmonious Subsequences</span>. These are extraordinary subsequences where the sum of every three consecutive numbers is even, and each subsequence must be at least three numbers in length. </p><p>Given a sequence $a_i$ ($1 \le i \le n$) of length $n$, its <span class="tex-font-style-underline">subsequence</span> of length $m$ is equal to $a_{b_1}, a_{b_2}, \ldots, a_{b_m}$ and is uniquely defined by a set of $m$ indices $b_j$, such that $1 \le b_1 &lt; b_2 &lt; \ldots &lt; b_m \le n$. Subsequences given by different sets of indices $b_j$ are considered different.</p><p>There's a twist in Kim's quest: the number of these Harmonious Subsequences could be overwhelming. To report the findings effectively, Kim must calculate the total number of these subsequences, presenting the answer as a remainder after dividing by the number $998\,244\,353$.</p></div><div class="input-specification"><p>The first line contains a single integer $n$&nbsp;— the length of the sequence ($3 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ space-separated integers $a_i$&nbsp;— the elements of the sequence ($1 \le a_i \le 2 \cdot 10^5$).</p></div><div class="output-specification"><p>Output one number&nbsp;— the number of Harmonious Subsequences, modulo $998\,244\,353$.</p></div>

## Input

<p>The first line contains a single integer $n$&nbsp;— the length of the sequence ($3 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ space-separated integers $a_i$&nbsp;— the elements of the sequence ($1 \le a_i \le 2 \cdot 10^5$).</p>

## Output

<p>Output one number&nbsp;— the number of Harmonious Subsequences, modulo $998\,244\,353$.</p>





```input1|
3
1 2 3
```




```input2|
5
2 8 2 6 4
```




```input3|
5
5 7 1 3 5
```




```input4|
11
3 1 4 1 5 9 2 6 5 3 6
```




```input5
54
2 1 1 1 1 2 1 2 2 2 2 1 1 1 2 1 1 2
2 1 2 2 2 2 2 2 2 1 1 1 2 2 1 1 1 1
2 2 1 1 2 2 2 2 2 1 1 1 2 2 1 2 1 1
```




```output1
1
```




```output2
16
```




```output3
0
```




```output4
386
```




```output5
0
```



## Note

<p>In the provided input data for the fifth sample, the sequence of numbers is split into three separate lines for clarity, but it should be understood that in the actual test data, the sequence is given in one line. The actual number of Harmonious Subsequences in this example is $4\,991\,221\,765 = 5 \times 998\,244\,353$, hence the output is zero as a result of finding its remainder after dividing by the number $998\,244\,353$.</p>
