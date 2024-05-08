## Description

<div><p>John is a lead programmer on a destroyer belonging to the space navy of the Confederacy of Independent Operating Systems. One of his tasks is checking if the electronic brains of robots were damaged during battles.</p><p>A standard test is to order the robots to form one or several lines, in each line the robots should stand one after another. After that, each robot reports the number of robots standing in front of it <span class="tex-font-style-bf">in its line</span>.</p><center> <img class="tex-graphics" src="file://knmd65AT.png" style="max-width: 100.0%;max-height: 100.0%;" width="151px"> <span class="tex-font-size-small">An example of robots' arrangement (the front of the lines is on the left). The robots report the numbers above.</span> </center><p>The $i$-th robot reported number $l_i$. Unfortunately, John does not know which line each robot stands in, and can't check the reported numbers. Please determine if it is possible to form the lines in such a way that all reported numbers are correct, or not.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 100$), denoting the number of test cases.</p><p>The first line in each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the number of robots.</p><p>The second line in each test case contains $n$ integers $l_1, l_2, \ldots, l_n$ ($0 \leq l_i &lt; 100$), $l_i$ is equal to the number of robots in front of the $i$-th robot in its line.</p><p>The sum of $n$ over all test cases won't exceed $200$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>", if there exists a robot arrangement consistent with robots' reports. Otherwise, output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 100$), denoting the number of test cases.</p><p>The first line in each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the number of robots.</p><p>The second line in each test case contains $n$ integers $l_1, l_2, \ldots, l_n$ ($0 \leq l_i &lt; 100$), $l_i$ is equal to the number of robots in front of the $i$-th robot in its line.</p><p>The sum of $n$ over all test cases won't exceed $200$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>", if there exists a robot arrangement consistent with robots' reports. Otherwise, output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,6,7,10,11
5
6
0 1 2 0 1 0
9
0 0 0 0 1 1 1 2 2
3
0 0 2
1
99
5
0 1 2 3 4
```




```output1
YES
YES
NO
NO
YES
```



## Note

<p>Example arrangement consistent with robot statements from the first example test case: </p><center> <img class="tex-graphics" src="file://jnOjI51J.png" style="max-width: 100.0%;max-height: 100.0%;" width="151px"> </center><p>Example arrangement consistent with robot statements from the second example is shown in the statement.</p><p>In the third test case, the third robot claims that there are two machines in front of it. In such a case, the robot directly in front of it would have one machine in front. No robot claims that, so there is no valid arrangement.</p>
