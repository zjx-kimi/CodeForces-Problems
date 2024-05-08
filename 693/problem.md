## Description

<div><p>You have a garland consisting of $4$ colored light bulbs, the color of the $i$-th light bulb is $s_i$.</p><p>Initially, all the light bulbs are turned off. Your task is to turn all the light bulbs on. You can perform the following operation any number of times: select a light bulb and switch its state (turn it on if it was off, and turn it off if it was on). The only restriction on the above operation is that you can apply the operation to a light bulb only if the previous operation was applied to a light bulb of a different color (the first operation can be applied to any light bulb).</p><p>Calculate the minimum number of operations to turn all the light bulbs on, or report that this is impossible.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The single line of each test case contains $s$&nbsp;— a sequence of $4$ characters, where each character is a decimal digit. The $i$-th character denotes the color of the $i$-th light bulb.</p></div><div class="output-specification"><p>For each test case, print one integer&nbsp;— the minimum number of operations to turn all the light bulbs on. If it is impossible to turn all the bulbs on, print <span class="tex-font-style-tt">-1</span>.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The single line of each test case contains $s$&nbsp;— a sequence of $4$ characters, where each character is a decimal digit. The $i$-th character denotes the color of the $i$-th light bulb.</p>

## Output

<p>For each test case, print one integer&nbsp;— the minimum number of operations to turn all the light bulbs on. If it is impossible to turn all the bulbs on, print <span class="tex-font-style-tt">-1</span>.</p>





```input1|2,4
3
9546
0000
3313
```




```output1
4
-1
6
```



## Note

<p>In the first example, all the colors are different, so you can just turn all the bulbs on in $4$ operations.</p><p>In the second example, it is impossible to turn all the bulbs on, because after you switch one light bulb, it is impossible to turn the others on.</p><p>In the third example, you can proceed as follows: turn the first light bulb on, turn the third light bulb on, turn the fourth light bulb on, turn the third light bulb off, turn the second light bulb on, turn the third light bulb on.</p>
