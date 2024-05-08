## Description

<div><p>There are $2n$ positive integers written on a whiteboard. Being bored, you decided to play a one-player game with the numbers on the whiteboard.</p><p>You start with a score of $0$. You will increase your score by performing the following move <span class="tex-font-style-bf">exactly</span> $n$ times: </p><ul> <li> Choose two integers $x$ and $y$ that are written on the whiteboard. </li><li> Add $\min(x,y)$ to your score. </li><li> Erase $x$ and $y$ from the whiteboard. </li></ul> <p>Note that after performing the move $n$ times, there will be no more integers written on the whiteboard.</p><p>Find the maximum final score you can achieve if you optimally perform the $n$ moves.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 5000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 50$)&nbsp;— the number of integers written on the whiteboard is $2n$.</p><p>The second line of each test case contains $2n$ integers $a_1,a_2,\ldots,a_{2n}$ ($1 \leq a_i \leq 10^7$)&nbsp;— the numbers written on the whiteboard.</p></div><div class="output-specification"><p>For each test case, output the maximum final score that you can achieve.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 5000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 50$)&nbsp;— the number of integers written on the whiteboard is $2n$.</p><p>The second line of each test case contains $2n$ integers $a_1,a_2,\ldots,a_{2n}$ ($1 \leq a_i \leq 10^7$)&nbsp;— the numbers written on the whiteboard.</p>

## Output

<p>For each test case, output the maximum final score that you can achieve.</p>





```input1|2,3,6,7
3
1
2 3
2
1 1 2 1
3
1 1 1 1 1 1
```




```output1
2
2
3
```



## Note

<p>In the first test case, you can only make one move. You select $x=2$ and $y=3$, and your score will be $\min(x,y)=2$.</p><p>In the second test case, the following is a sequence of moves that achieves a final score of $2$:</p><ul> <li> In the first move, select $x=1$ and $y=1$. Then, add $\min(x,y)=1$ to the score. After erasing $x$ and $y$, the integers left on the whiteboard are $1$ and $2$. </li><li> In the second move, select $x=1$ and $y=2$. Then, add $\min(x,y)=1$ to the score. After removing $x$ and $y$, no more integers will be left on the whiteboard. </li></ul> It can be proved that it is not possible to get a score greater than $2$.<p>In the third test case, you will perform the move thrice, adding $1$ to the score each time.</p>
