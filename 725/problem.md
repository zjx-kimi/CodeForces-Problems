## Description

<div><p>Ada operates a network that consists of $n$ servers and $m$ direct connections between them. Each direct connection between a pair of distinct servers allows bidirectional transmission of information between these two servers. Ada knows that these $m$ direct connections allow to directly or indirectly transmit information between any two servers in this network. We say that server $v$ is a neighbor of server $u$ if there exists a direct connection between these two servers.</p><p>Ada needs to configure her network's WRP (Weird Routing Protocol). For each server $u$ she needs to select exactly one of its neighbors as an auxiliary server $a(u)$. After all $a(u)$ are set, routing works as follows. Suppose server $u$ wants to find a path to server $v$ (different from $u$). </p><ol> <li> Server $u$ checks all of its direct connections to other servers. If it sees a direct connection with server $v$, it knows the path and the process terminates. </li><li> If the path was not found at the first step, server $u$ asks its auxiliary server $a(u)$ to find the path. </li><li> Auxiliary server $a(u)$ follows this process starting from the first step. </li><li> After $a(u)$ finds the path, it returns it to $u$. Then server $u$ constructs the resulting path as the direct connection between $u$ and $a(u)$ plus the path from $a(u)$ to $v$. </li></ol><p>As you can see, this procedure either produces a correct path and finishes or keeps running forever. Thus, it is critically important for Ada to configure her network's WRP properly.</p><p>Your goal is to assign an auxiliary server $a(u)$ for each server $u$ in the given network. Your assignment should make it possible to construct a path from any server $u$ to any other server $v$ using the aforementioned procedure. Or you should report that such an assignment doesn't exist.</p></div><div class="input-specification"><p>The first line of the input contains two integers $n$ and $m$ ($2 \leq n \leq 20$, $n - 1 \leq m \leq \frac{n \cdot (n - 1)}{2}$)&nbsp;— the number of servers and the number of direct connections in the given network.</p><p>Then follow $m$ lines containing two integers $u_i$ and $v_i$ ($1 \leq u_i, v_i \leq n$, $u_i \ne v_i$) each, the $i$-th line describes the $i$-th direct connection.</p><p>It is guaranteed that there is no more than one direct connection between any two servers. It is guaranteed that there is a direct or indirect route (consisting only of the given direct connections) between any two servers.</p></div><div class="output-specification"><p>If there is no way to assign an auxiliary server $a(u)$ for each server $u$ in such a way that WRP will be able to find a path from any server $u$ to any other server $v$, print "<span class="tex-font-style-tt">No</span>" in the only line of the output.</p><p>Otherwise, print "<span class="tex-font-style-tt">Yes</span>" in the first line of the output. In the second line of the output print $n$ integers, the $i$-th of these integers should be equal to $a(i)$&nbsp;– the index of the auxiliary server for server $i$. Do not forget that there must be a direct connection between server $i$ and server $a(i)$.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>The first line of the input contains two integers $n$ and $m$ ($2 \leq n \leq 20$, $n - 1 \leq m \leq \frac{n \cdot (n - 1)}{2}$)&nbsp;— the number of servers and the number of direct connections in the given network.</p><p>Then follow $m$ lines containing two integers $u_i$ and $v_i$ ($1 \leq u_i, v_i \leq n$, $u_i \ne v_i$) each, the $i$-th line describes the $i$-th direct connection.</p><p>It is guaranteed that there is no more than one direct connection between any two servers. It is guaranteed that there is a direct or indirect route (consisting only of the given direct connections) between any two servers.</p>

## Output

<p>If there is no way to assign an auxiliary server $a(u)$ for each server $u$ in such a way that WRP will be able to find a path from any server $u$ to any other server $v$, print "<span class="tex-font-style-tt">No</span>" in the only line of the output.</p><p>Otherwise, print "<span class="tex-font-style-tt">Yes</span>" in the first line of the output. In the second line of the output print $n$ integers, the $i$-th of these integers should be equal to $a(i)$&nbsp;– the index of the auxiliary server for server $i$. Do not forget that there must be a direct connection between server $i$ and server $a(i)$.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1
6 7
1 2
2 3
3 1
4 5
5 6
4 6
2 5
```




```input2
3 2
1 2
2 3
```




```input3
4 4
1 3
2 3
4 1
4 2
```




```input4
6 5
1 2
2 3
3 4
4 5
5 6
```




```output1
Yes
2 5 2 5 2 5
```




```output2
Yes
2 1 2
```




```output3
Yes
3 3 1 1
```




```output4
No
```


