## Description

<div><p>Monocarp is the most famous thief in Berland. This time, he decided to steal two diamonds. Unfortunately for Monocarp, there are $n$ cameras monitoring the diamonds. Each camera has two parameters, $t_i$ and $s_i$. The first parameter determines whether the camera is monitoring the first diamond only ($t_i=1$), the second diamond only ($t_i=2$), or both diamonds ($t_i=3$). The second parameter determines the number of seconds the camera will be disabled after it is hacked.</p><p>Every second, Monocarp can perform one of the following three actions: </p><ul> <li> do nothing; </li><li> choose a camera and hack it; if Monocarp hacks the $i$-th camera, it will be disabled for the next $s_i$ seconds (if the current second is the $T$-th one, the camera will be disabled from the $(T+1)$-th to the $(T+s_i)$-th second, inclusive); </li><li> steal a diamond if all cameras monitoring it are currently disabled. Monocarp cannot steal the second diamond if he hasn't stolen the first diamond yet. </li></ul><p>Note that Monocarp can hack a camera multiple times, even if it is currently disabled.</p><p>Your task is to determine the minimum time it will take Monocarp to steal both diamonds, <span class="tex-font-style-bf">beginning with the first diamond</span>, or report that it is impossible.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($0 \le n \le 1500$)&nbsp;— the number of cameras.</p><p>Then $n$ lines follow, the $i$-th of them contains two integers $t_i$ and $s_i$ ($1 \le t_i \le 3$; $1 \le s_i \le 2n$)&nbsp;— the parameters of the $i$-th camera.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the minimum time it will take for Monocarp to steal <span class="tex-font-style-bf">the first diamond first and then the second diamond</span>. If it is impossible, print <span class="tex-font-style-tt">-1</span>.</p></div>

## Input

<p>The first line contains a single integer $n$ ($0 \le n \le 1500$)&nbsp;— the number of cameras.</p><p>Then $n$ lines follow, the $i$-th of them contains two integers $t_i$ and $s_i$ ($1 \le t_i \le 3$; $1 \le s_i \le 2n$)&nbsp;— the parameters of the $i$-th camera.</p>

## Output

<p>Print a single integer&nbsp;— the minimum time it will take for Monocarp to steal <span class="tex-font-style-bf">the first diamond first and then the second diamond</span>. If it is impossible, print <span class="tex-font-style-tt">-1</span>.</p>





```input1
4
2 6
1 2
1 2
2 1
```




```input2
4
2 8
3 2
3 2
3 5
```




```input3
2
3 2
2 3
```




```input4
1
3 1
```




```input5
8
2 1
2 2
3 5
3 6
1 2
1 3
1 4
1 5
```




```output1
6
```




```output2
9
```




```output3
4
```




```output4
4
```




```output5
11
```


