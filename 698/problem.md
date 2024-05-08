## Description

<div><p><span class="tex-font-style-it">In this problem, unlike problem A, you need to look for <span class="tex-font-style-bf">unluckiest number</span>, not the luckiest one.</span></p><p><span class="tex-font-style-bf">Note that the constraints of this problem differ from such in problem A.</span></p><p>Olympus City recently launched the production of personal starships. Now everyone on Mars can buy one and fly to other planets inexpensively.</p><p>Each starship has a number&nbsp;—some positive integer $x$. Let's define the <span class="tex-font-style-it">luckiness</span> of a number $x$ as the difference between the largest and smallest digits of that number. For example, $142857$ has $8$ as its largest digit and $1$ as its smallest digit, so its luckiness is $8-1=7$. And the number $111$ has all digits equal to $1$, so its luckiness is zero.</p><p>Hateehc is a famous Martian blogger who often flies to different corners of the solar system. To release interesting videos even faster, he decided to buy himself a starship. When he came to the store, he saw starships with numbers from $l$ to $r$ inclusively. While in the store, Hateehc wanted to find a starship with the <span class="tex-font-style-bf">unluckiest</span> number.</p><p>Since there are a lot of starships in the store, and Hateehc can't program, you have to help the blogger and write a program that answers his question.</p><center> <img class="tex-graphics" src="file://hD8djdKj.png" style="max-width: 100.0%;max-height: 100.0%;"> </center></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 600$)&nbsp;—the number of test cases.</p><p>Each of the following $t$ lines contains a description of the test case. The description consists of two integers $l$, $r$ ($1 \le l \le r \le 10^{18}$)&nbsp;— the largest and smallest numbers of the starships in the store.</p></div><div class="output-specification"><p>Print $t$ lines, one line for each test case, containing the unluckiest starship number in the store.</p><p>If there are several ways to choose the unluckiest number, output any of them.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 600$)&nbsp;—the number of test cases.</p><p>Each of the following $t$ lines contains a description of the test case. The description consists of two integers $l$, $r$ ($1 \le l \le r \le 10^{18}$)&nbsp;— the largest and smallest numbers of the starships in the store.</p>

## Output

<p>Print $t$ lines, one line for each test case, containing the unluckiest starship number in the store.</p><p>If there are several ways to choose the unluckiest number, output any of them.</p>





```input1|2,4,6
5
59 63
42 49
48 53
90 90
1 100
```




```output1
63
44
53
90
1
```



## Note

<p>Let's look at two test examples: </p><ul> <li> the luckiness of the number $59$ is $9 - 5 = 4$; </li><li> the luckiness of $60$ equals $6 - 0 = 6$; </li><li> the luckiness of $61$ equals $6 - 1 = 5$; </li><li> the luckiness of $62$ equals $6 - 2 = 4$; </li><li> the luckiness of $63$ is $6 - 3 = 3$. </li></ul> So the unluckiest number is $63$.<p>In the fifth test case, the unluckiest numbers are $1$, $2$, $3$, $4$, $5$, $6$, $7$, $8$, $9$, $11$, $22$, $33$, $44$, $55$, $66$, $77$, $88$, $99$, so you are allowed to choose any of them.</p>
