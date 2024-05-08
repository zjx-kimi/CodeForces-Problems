## Description

<div><p>Alice has written a program and now tries to improve its readability. One of the ways to improve readability is to give sensible names to the variables, so now Alice wants to rename some variables in her program. In her IDE there is a command called "massive refactoring", which can replace names of many variable in just one run. To use it, Alice needs to select two strings $s$ and $t$ and after that for each variable the following algorithm is performed: if the variable's name contains $s$ as a substring, then the first (and only first) occurrence of $s$ is replaced with $t$. If the name doesn't contain $s$, then this variable's name stays the same.</p><p>The list of variables is known and for each variable both the initial name and the name Alice wants this variable change to are known. Moreover, for each variable the lengths of the initial name and the target name are equal (otherwise the alignment of the code could become broken). You need to perform renaming of all variables in <span class="tex-font-style-bf">exactly one</span> run of the massive refactoring command or determine that it is impossible.</p></div><div class="input-specification"><p>The first line contains the only integer $n$ ($1 \le n \le 3000$)&nbsp;— the number of variables in Alice's program.</p><p>The following $n$ lines contain the initial names of variables $w_1, w_2, \ldots, w_n$, one per line. After that, $n$ more lines go, the $i$-th of them contains the target name $w'_i$ for the $i$-th variable. It is guaranteed that $1 \le |w_i| = |w'_i| \le 3000$.</p><p>It is guaranteed that there is <span class="tex-font-style-bf">at least one</span> variable having its target name <span class="tex-font-style-bf">different</span> from the initial name. Both initial and target names consist of lowercase English letters only. For each variable the length of its initial name is equal to the length of its target name.</p></div><div class="output-specification"><p>If it is impossible to rename all variables with one call of "massive refactoring", print "<span class="tex-font-style-tt">NO</span>" (quotes for clarity).</p><p>Otherwise, on the first line print "<span class="tex-font-style-tt">YES</span>" (quotes for clarity) and on the following lines print $s$ and $t$ ($1 \le |s|, |t| \le 5000$), which should be used for replacement. Strings $s$ and $t$ should consist only of lowercase letters of English alphabet.</p><p>If there are multiple ways to perform a "massive refactoring", you can use any of them.</p></div>

## Input

<p>The first line contains the only integer $n$ ($1 \le n \le 3000$)&nbsp;— the number of variables in Alice's program.</p><p>The following $n$ lines contain the initial names of variables $w_1, w_2, \ldots, w_n$, one per line. After that, $n$ more lines go, the $i$-th of them contains the target name $w'_i$ for the $i$-th variable. It is guaranteed that $1 \le |w_i| = |w'_i| \le 3000$.</p><p>It is guaranteed that there is <span class="tex-font-style-bf">at least one</span> variable having its target name <span class="tex-font-style-bf">different</span> from the initial name. Both initial and target names consist of lowercase English letters only. For each variable the length of its initial name is equal to the length of its target name.</p>

## Output

<p>If it is impossible to rename all variables with one call of "massive refactoring", print "<span class="tex-font-style-tt">NO</span>" (quotes for clarity).</p><p>Otherwise, on the first line print "<span class="tex-font-style-tt">YES</span>" (quotes for clarity) and on the following lines print $s$ and $t$ ($1 \le |s|, |t| \le 5000$), which should be used for replacement. Strings $s$ and $t$ should consist only of lowercase letters of English alphabet.</p><p>If there are multiple ways to perform a "massive refactoring", you can use any of them.</p>





```input1
1
topforces
codecoder

```




```input2
3
bab
cac
cdc
bdb
cdc
cdc

```




```input3
2
you
shal
not
pass

```




```output1
YES
topforces
codecoder

```




```output2
YES
a
d

```




```output3
NO

```


