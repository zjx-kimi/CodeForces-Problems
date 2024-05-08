## Description

<div><p>You are currently researching the Merge Sort algorithm. Merge Sort is a sorting algorithm that is based on the principle of Divide and Conquer. It works by dividing an array into two subarrays of equal length, sorting each subarrays, then merging the sorted subarrays back together to form the final sorted array.</p><p>You are particularly interested in the merging routine. Common merge implementation will combine two subarrays by iteratively comparing their first elements, and move the smaller one to a new merged array. More precisely, the merge algorithm can be presented by the following pseudocode.</p><pre class="verbatim"><br>    Merge(A[1..N], B[1..N]):<br>        C = []<br>        i = 1<br>        j = 1<br>        while i &lt;= N AND j &lt;= N:<br>            if A[i] &lt; B[j]:<br>                append A[i] to C<br>                i = i + 1<br>            else:<br>                append B[j] to C<br>                j = j + 1 <br>        while i &lt;= N:<br>            append A[i] to C<br>            i = i + 1 <br>        while j &lt;= N:<br>            append B[j] to C<br>            j = j + 1 <br>        return C<br></pre><p>During your research, you are keen to understand the behaviour of the merge algorithm when arrays $A$ and $B$ are not necessarily sorted. For example, if $A = [3, 1, 6]$ and $B = [4, 5, 2]$, then $\text{Merge}(A, B) = [3, 1, 4, 5, 2, 6]$.</p><p>To further increase the understanding of the merge algorithm, you decided to work on the following problem. You are given an array $C$ of length $2 \cdot N$ such that it is a permutation of $1$ to $2 \cdot N$. Construct any two arrays $A$ and $B$ of the <span class="tex-font-style-bf">same length</span> $N$, such that $\text{Merge}(A, B) = C$, or determine if it is impossible to do so.</p></div><div class="input-specification"><p>The first line consists of an integer $N$ ($1 \leq N \leq 1000$).</p><p>The following line consists of $2 \cdot N$ integers $C_i$. The array $C$ is a permutation of $1$ to $2 \cdot N$.</p></div><div class="output-specification"><p>If it is impossible to construct two arrays $A$ and $B$ of length $N$ such that $\text{Merge}(A, B) = C$, then output <span class="tex-font-style-tt">-1</span>.</p><p>Otherwise, output the arrays $A$ and $B$ in two lines. The first line consists of $N$ integers $A_i$. The second line consists of $N$ integers $B_i$. If there are several possible answers, output any of them.</p></div>

## Input

<p>The first line consists of an integer $N$ ($1 \leq N \leq 1000$).</p><p>The following line consists of $2 \cdot N$ integers $C_i$. The array $C$ is a permutation of $1$ to $2 \cdot N$.</p>

## Output

<p>If it is impossible to construct two arrays $A$ and $B$ of length $N$ such that $\text{Merge}(A, B) = C$, then output <span class="tex-font-style-tt">-1</span>.</p><p>Otherwise, output the arrays $A$ and $B$ in two lines. The first line consists of $N$ integers $A_i$. The second line consists of $N$ integers $B_i$. If there are several possible answers, output any of them.</p>





```input1
3
3 1 4 5 2 6
```




```input2
4
1 2 3 4 5 6 7 8
```




```input3
2
4 3 2 1
```




```output1
3 1 6
4 5 2
```




```output2
2 3 5 7
1 4 6 8
```




```output3
-1
```



## Note

<p><span class="tex-font-style-it">Explanation for the sample input/output #1</span></p><p>The solution $A = [3, 1, 4]$ and $B = [5, 2, 6]$ is also correct. </p><p><span class="tex-font-style-it">Explanation for the sample input/output #2</span></p><p>The solution $A = [1, 2, 3, 4]$ and $B = [5, 6, 7, 8]$ is also correct. </p>
