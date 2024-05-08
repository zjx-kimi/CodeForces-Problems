## Description

<div><p>You have been invited as a production process optimization specialist to some very large company. The company has $n$ machines at its factory, standing one behind another in the production chain. Each machine can be described in one of the following two ways: $(+,~a_i)$ or $(*,~a_i)$.</p><p>If a workpiece with the value $x$ is supplied to the machine of kind $(+,~a_i)$, then the output workpiece has value $x + a_i$.</p><p>If a workpiece with the value $x$ is supplied to the machine of kind $(*,~a_i)$, then the output workpiece has value $x \cdot a_i$.</p><p>The whole production process is as follows. The workpiece with the value $1$ is supplied to the first machine, then the workpiece obtained after the operation of the first machine is supplied to the second machine, then the workpiece obtained after the operation of the second machine is supplied to the third machine, and so on. The company is not doing very well, so now the value of the resulting product does not exceed $2 \cdot 10^9$.</p><p>The directors of the company are not satisfied with the efficiency of the production process and have given you a budget of $b$ coins to optimize it.</p><p>To optimize production you can change the order of machines in the chain. Namely, by spending $p$ coins, you can take any machine of kind $(+,~a_i)$ and move it to any place in the chain without changing the order of other machines. Also, by spending $m$ coins, you can take any machine of kind $(*,~a_i)$ and move it to any place in the chain.</p><p>What is the maximum value of the resulting product that can be achieved if the total cost of movements that are made should not exceed $b$ coins?</p></div><div class="input-specification"><p>The first line contains four integers $n$, $b$, $p$ and $m$ ($1 \le n \le 10^6$, $1 \le b, p, m \le 10^9$)&nbsp;— the number of machine at the factory, your budget and costs of movements of both kinds of machines.</p><p>Each of the following $n$ lines contains description of a machine. The description begins with one of the following characters: "<span class="tex-font-style-tt">+</span>" or "<span class="tex-font-style-tt">*</span>", that denotes the kind of the machine. Then an integer $a_i$ follows ($1 \le a_i \le 2 \cdot 10^9$).</p><p>It's guaranteed that the current value of the resulting product does not exceed $2 \cdot 10^9$.</p></div><div class="output-specification"><p>Print one integer&nbsp;— the maximum value of the resulting product that can be achieved if the total cost of movements that are made does not exceed $b$ coins.</p></div>

## Input

<p>The first line contains four integers $n$, $b$, $p$ and $m$ ($1 \le n \le 10^6$, $1 \le b, p, m \le 10^9$)&nbsp;— the number of machine at the factory, your budget and costs of movements of both kinds of machines.</p><p>Each of the following $n$ lines contains description of a machine. The description begins with one of the following characters: "<span class="tex-font-style-tt">+</span>" or "<span class="tex-font-style-tt">*</span>", that denotes the kind of the machine. Then an integer $a_i$ follows ($1 \le a_i \le 2 \cdot 10^9$).</p><p>It's guaranteed that the current value of the resulting product does not exceed $2 \cdot 10^9$.</p>

## Output

<p>Print one integer&nbsp;— the maximum value of the resulting product that can be achieved if the total cost of movements that are made does not exceed $b$ coins.</p>





```input1
3 2 1 3
* 2
+ 1
+ 1
```




```input2
4 2 2 2
* 2
+ 1
* 3
+ 2
```




```input3
8 2 1 1
* 2
+ 1
* 4
+ 1
+ 1
+ 1
* 5
+ 3
```




```output1
6
```




```output2
21
```




```output3
240
```



## Note

<p>In the first example our budget is too low to move machine $(*,~2)$, but we can move both machines $(+,~1)$ to the beginning of the chain. So the final chain will be $(+,~1)$ $(+,~1)$ $(*,~2)$. If the workpiece with the value $1$ is supplied to the first machine, its value will be changed in the following way: $1, 2, 3, 6$.</p><p>In the second example we can move only one machine. Let's move machine $(+,~2)$ to the beginning of the chain. The final chain will be $(+,~2)$ $(*,~2)$ $(+,~1)$ $(*,~3)$. The value of the workpiece will be changed in the following way: $1, 3, 6, 7, 21$.</p><p>In the third example we can place machine $(*,~4)$ before the machine $(*,~5)$, and move machine $(+,~3)$ to the beginning of the chain. The final chain will be $(+,~3)$ $(*,~2)$ $(+,~1)$ $(+,~1)$ $(+,~1)$ $(+,~1)$ $(*,~4)$ $(*,~5)$. The value of the workpiece will be changed in the following way: $1, 4, 8, 9, 10, 11, 12, 48, 240$.</p>
