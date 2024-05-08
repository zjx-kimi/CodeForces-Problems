## Description

<div><p>Polycarp has an integer $n$ that doesn't contain the digit <span class="tex-font-style-tt">0</span>. He can do the following operation with his number several (possibly zero) times:</p><ul><li> Reverse the prefix of length $l$ (in other words, $l$ leftmost digits) of $n$. So, the leftmost digit is swapped with the $l$-th digit from the left, the second digit from the left swapped with ($l-1$)-th left, etc. For example, if $n=123456789$ and $l=5$, then the new value of $n$ will be $543216789$.</li></ul><p>Note that for different operations, the values of $l$ can be different. The number $l$ can be equal to the length of the number $n$&nbsp;— in this case, the whole number $n$ is reversed.</p><p>Polycarp loves even numbers. Therefore, he wants to make his number even. At the same time, Polycarp is very impatient. He wants to do as few operations as possible.</p><p>Help Polycarp. Determine the minimum number of operations he needs to perform with the number $n$ to make it even or determine that this is impossible.</p><p>You need to answer $t$ independent test cases.</p></div><div class="input-specification"><p>The first line contains the number $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Each of the following $t$ lines contains one integer $n$ ($1 \le n &lt; 10^9$). It is guaranteed that the given number doesn't contain the digit <span class="tex-font-style-tt">0</span>.</p></div><div class="output-specification"><p>Print $t$ lines. On each line print one integer&nbsp;— the answer to the corresponding test case. If it is impossible to make an even number, print <span class="tex-font-style-tt">-1</span>.</p></div>

## Input

<p>The first line contains the number $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Each of the following $t$ lines contains one integer $n$ ($1 \le n &lt; 10^9$). It is guaranteed that the given number doesn't contain the digit <span class="tex-font-style-tt">0</span>.</p>

## Output

<p>Print $t$ lines. On each line print one integer&nbsp;— the answer to the corresponding test case. If it is impossible to make an even number, print <span class="tex-font-style-tt">-1</span>.</p>





```input1
4
3876
387
4489
3
```




```output1
0
2
1
-1
```



## Note

<p>In the first test case, $n=3876$, which is already an even number. Polycarp doesn't need to do anything, so the answer is $0$.</p><p>In the second test case, $n=387$. Polycarp needs to do $2$ operations:</p><ol><li> Select $l=2$ and reverse the prefix $\underline{38}7$. The number $n$ becomes $837$. This number is odd.</li><li> Select $l=3$ and reverse the prefix $\underline{837}$. The number $n$ becomes $738$. This number is even.</li></ol><p>It can be shown that $2$ is the minimum possible number of operations that Polycarp needs to do with his number to make it even.</p><p>In the third test case, $n=4489$. Polycarp can reverse the whole number (choose a prefix of length $l=4$). It will become $9844$ and this is an even number.</p><p>In the fourth test case, $n=3$. No matter how hard Polycarp tried, he would not be able to make an even number.</p>
