## Description

<div><p>You are given a regular $N$-sided polygon. Label one arbitrary side as side $1$, then label the next sides in clockwise order as side $2$, $3$, $\dots$, $N$. There are $A_i$ special points on side $i$. These points are positioned such that side $i$ is divided into $A_i + 1$ segments with equal length.</p><p>For instance, suppose that you have a regular $4$-sided polygon, i.e., a square. The following illustration shows how the special points are located within each side when $A = [3, 1, 4, 6]$. The uppermost side is labelled as side $1$.</p><center> <img class="tex-graphics" src="file://Niptfojt.png" style="max-width: 100.0%;max-height: 100.0%;" width="189px"> </center><p>You want to create as many <span class="tex-font-style-bf">non-degenerate triangles</span> as possible while satisfying the following requirements. Each triangle consists of $3$ distinct special points (not necessarily from different sides) as its corners. Each special point can only become the corner of at most $1$ triangle. All triangles must not intersect with each other.</p><p>Determine the maximum number of non-degenerate triangles that you can create.</p><p>A triangle is <span class="tex-font-style-bf">non-degenerate</span> if it has a positive area.</p></div><div class="input-specification"><p>The first line consists of an integer $N$ ($3 \leq N \leq 200\,000$).</p><p>The following line consists of $N$ integers $A_i$ ($1 \leq A_i \leq 2 \cdot 10^9$).</p></div><div class="output-specification"><p>Output a single integer representing the maximum number of non-degenerate triangles that you can create.</p></div>

## Input

<p>The first line consists of an integer $N$ ($3 \leq N \leq 200\,000$).</p><p>The following line consists of $N$ integers $A_i$ ($1 \leq A_i \leq 2 \cdot 10^9$).</p>

## Output

<p>Output a single integer representing the maximum number of non-degenerate triangles that you can create.</p>





```input1
4
3 1 4 6
```




```input2
6
1 2 1 2 1 2
```




```input3
3
1 1 1
```




```output1
4
```




```output2
3
```




```output3
1
```



## Note

<p><span class="tex-font-style-it">Explanation for the sample input/output #1</span></p><p>One possible construction which achieves maximum number of non-degenerate triangles can be seen in the following illustration. </p><center> <img class="tex-graphics" src="file://5mhqQbiM.png" style="max-width: 100.0%;max-height: 100.0%;" width="151px"> </center><p><span class="tex-font-style-it">Explanation for the sample input/output #2</span></p><p>One possible construction which achieves maximum number of non-degenerate triangles can be seen in the following illustration. </p><center> <img class="tex-graphics" src="file://aGi9HRs2.png" style="max-width: 100.0%;max-height: 100.0%;" width="151px"> </center>
