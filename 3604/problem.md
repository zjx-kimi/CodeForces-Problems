## Description

<div><p>The new ICPC town has $N$ junctions (numbered from $1$ to $N$) which are connected by $N-1$ roads. It is possible from one junction to go to any other junctions by going through one or more roads. To make sure all the junctions are well-maintained, the government environment agency is planning to deploy their newest advanced cleaning robots. In addition to its cleaning ability, each robot is also equipped with a movement ability such that it can move from one junction to any other junctions connected by roads. However, as you might have guessed, such robots are not cheap. Therefore, the agency is considering the following deployment plan.</p><p>Let $T_k$ be the set of junctions which should be cleaned by the $k^{th}$ robot (also known as, the robot's task), and $|T_k| \ge 1$ be the number of junctions in $T_k$. The junctions in $T_k$ form a <span class="tex-font-style-bf">path</span>, i.e. there exists a sequence of $v_1, v_2, \dots, v_{|T_k|}$ where $v_i \in T_k$ and $v_i \neq v_j$ for all $i \neq j$ such that each adjacent junction in this sequence is connected by a road. The union of $T$ for all robots is equal to the set of all junctions in ICPC town. On the other hand, no two robots share a common junction, i.e. $T_i \cap T_j = \emptyset$ if $i \neq j$.</p><p>To avoid complaints from citizens for an inefficient operation, the deployment plan should be <span class="tex-font-style-it">irreducible</span>; in other words, there should be no two robots, $i$ and $j$, such that $T_i \cup T_j$ forms a (longer) path. Note that the agency does not care whether the number of robots being used is minimized as long as all the tasks are irreducible.</p><p>Your task in this problem is to count the number of feasible deployment plan given the town's layout. A plan is feasible if and only if it satisfies all the above-mentioned requirements.</p><p>For example, let $N = 6$ and the roads are $\{(1,3),(2,3),(3,4),(4,5),(4,6)\}$. There are $5$ feasible deployment plans as shown in the following figure. </p><p><img class="tex-graphics" src="file://i5tfJZUX.png" style="max-width: 100.0%;max-height: 100.0%;"></p><ul> <li> The first plan uses $2$ robots (labeled as A and B in the figure) to clean $\{1,2,3\}$ and $\{4,5,6\}$. </li><li> The second plan uses $3$ robots (labeled as A, B, and C in the figure) to clean $\{1,3,4,6\}$, $\{2\}$, and $\{5\}$. </li><li> The third plan uses $3$ robots to clean $\{1,3,4,5\}$, $\{2\}$, and $\{6\}$. </li><li> The fourth plan uses $3$ robots to clean $\{1\}$, $\{2,3,4,6\}$, and $\{5\}$. </li><li> The fifth plan uses $3$ robots to clean $\{1\}$, $\{2,3,4,5\}$, and $\{6\}$. </li></ul> No other plans are feasible in this case. For example, the plan $\{\{1,3\},\{2\},\{4,5,6\}\}$ is not feasible as the task $\{1,3\}$ and $\{2\}$ can be combined into a longer path $\{1,3,2\}$. The plan $\{\{1,2,3,4\},\{5\},\{6\}\}$ is also not feasible as $\{1,2,3,4\}$ is not a path.</div><div class="input-specification"><p>Input begins with a line containing an integer: $N$ ($1 \le N \le 100\,000$) representing the number of junctions. The next $N-1$ lines each contains two integers: $u_i$ $v_i$ ($1 \le u_i &lt; v_i \le N$) representing a road connecting junction $u_i$ and junction $v_i$. It is guaranteed that it is possible from one junction to go to any other junctions by going through one or more roads.</p></div><div class="output-specification"><p>Output in a line an integer representing the number of feasible deployment plans. As this output can be large, you need to modulo the output by $1\,000\,000\,007$.</p></div>

## Input

<p>Input begins with a line containing an integer: $N$ ($1 \le N \le 100\,000$) representing the number of junctions. The next $N-1$ lines each contains two integers: $u_i$ $v_i$ ($1 \le u_i &lt; v_i \le N$) representing a road connecting junction $u_i$ and junction $v_i$. It is guaranteed that it is possible from one junction to go to any other junctions by going through one or more roads.</p>

## Output

<p>Output in a line an integer representing the number of feasible deployment plans. As this output can be large, you need to modulo the output by $1\,000\,000\,007$.</p>





```input1
6
1 3
2 3
3 4
4 5
4 6
```




```input2
5
1 2
2 3
2 4
4 5
```




```output1
5
```




```output2
3
```



## Note

<p><span class="tex-font-style-it">Explanation for the sample input/output #1</span></p><p>This is the example from the problem description.</p>
