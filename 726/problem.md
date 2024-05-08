## Description

<div><p>Annie is an amateur photographer. She likes to take pictures of giant residential buildings at night. She just took a picture of a huge rectangular building that can be seen as a table of $n \times m$ windows. That means that the building has $n$ floors and each floor has exactly $m$ windows. Each window is either dark or bright, meaning there is light turned on in the room behind it.</p><p>Annies knows that each apartment in this building is either one-bedroom or two-bedroom. Each one-bedroom apartment has exactly one window representing it on the picture, and each two-bedroom apartment has exactly two <span class="tex-font-style-bf">consecutive</span> windows on the same floor. Moreover, the value of $m$ is guaranteed to be divisible by $4$ and it is known that each floor has exactly $\frac{m}{4}$ two-bedroom apartments and exactly $\frac{m}{2}$ one-bedroom apartments. The actual layout of apartments is unknown and can be different for each floor.</p><p>Annie considers an apartment to be occupied if <span class="tex-font-style-bf">at least one</span> of its windows is bright. She now wonders, what are the minimum and maximum possible number of occupied apartments if judged by the given picture?</p><p>Formally, for each of the floors, she comes up with some particular apartments layout with exactly $\frac{m}{4}$ two-bedroom apartments (two consecutive windows) and $\frac{m}{2}$ one-bedroom apartments (single window). She then counts the total number of apartments that have at least one bright window. What is the minimum and maximum possible number she can get?</p></div><div class="input-specification"><p>The first line of the input contains two positive integers $n$ and $m$ ($1 \leq n \cdot m \leq 5 \cdot 10^5$)&nbsp;— the number of floors in the building and the number of windows per floor, respectively. It is guaranteed that $m$ is divisible by $4$.</p><p>Then follow $n$ lines containing $m$ characters each. The $j$-th character of the $i$-th line is "<span class="tex-font-style-tt">0</span>" if the $j$-th window on the $i$-th floor is dark, and is "<span class="tex-font-style-tt">1</span>" if this window is bright.</p></div><div class="output-specification"><p>Print two integers, the minimum possible number of occupied apartments and the maximum possible number of occupied apartments, assuming each floor can have an individual layout of $\frac{m}{4}$ two-bedroom and $\frac{m}{2}$ one-bedroom apartments.</p></div>

## Input

<p>The first line of the input contains two positive integers $n$ and $m$ ($1 \leq n \cdot m \leq 5 \cdot 10^5$)&nbsp;— the number of floors in the building and the number of windows per floor, respectively. It is guaranteed that $m$ is divisible by $4$.</p><p>Then follow $n$ lines containing $m$ characters each. The $j$-th character of the $i$-th line is "<span class="tex-font-style-tt">0</span>" if the $j$-th window on the $i$-th floor is dark, and is "<span class="tex-font-style-tt">1</span>" if this window is bright.</p>

## Output

<p>Print two integers, the minimum possible number of occupied apartments and the maximum possible number of occupied apartments, assuming each floor can have an individual layout of $\frac{m}{4}$ two-bedroom and $\frac{m}{2}$ one-bedroom apartments.</p>





```input1
5 4
0100
1100
0110
1010
1011
```




```input2
1 8
01011100
```




```output1
7 10
```




```output2
3 4
```



## Note

<p>In the first example, each floor consists of one two-bedroom apartment and two one-bedroom apartments.</p><p>The following apartment layout achieves the minimum possible number of occupied apartments equal to $7$. </p><pre class="verbatim"><br>|0 1|0|0|<br>|1 1|0|0|<br>|0|1 1|0|<br>|1|0 1|0|<br>|1|0|1 1|<br></pre><p>The following apartment layout achieves the maximum possible number of occupied apartments equal to $10$. </p><pre class="verbatim"><br>|0 1|0|0|<br>|1|1 0|0|<br>|0 1|1|0|<br>|1|0 1|0|<br>|1 0|1|1|<br></pre>
