## Description

<div><p>You are designing a new video game. It has $n$ scenarios, which the player may play in any order, but each scenario must be played exactly once. When a player switches from a scenario to another scenario, the game shows a specially crafted transition video to make it all feel part of one big story. This video is specific to a pair of scenarios, but not to their order, in other words, the video playing when switching from scenario $a$ to scenario $b$ is the same as the video playing when switching from scenario $b$ to scenario $a$. Therefore, you need to create $\frac{n(n-1)}{2}$ different transition videos, one for each possible pair of different scenarios.</p><p>Each transition video can be either <span class="tex-font-style-underline">funny</span> or <span class="tex-font-style-underline">scary</span>. It is boring to see too many funny videos or too many scary videos in a row. Therefore, your goal is to create the videos in such a way that no matter in which order does the player approach the scenarios, they will never see more than $\lceil \frac{3n}{4} \rceil$ transition videos of the same type in a row.</p><p>You have already come up with ideas for at most $\lfloor \frac{n}{2} \rfloor$ of the transition videos, and therefore already know if those will be funny or scary. Now you need to choose funny or scary for all other transition videos in such a way that the above requirement is satisfied.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($2 \le n \le 24$)&nbsp;— the number of scenarios in the game.</p><p>The next $n$ lines describe the partial transition video plan. Each of those lines contains $n$ characters. The $j$-th character of the $i$-th line corresponds to the transition video between the $i$-th and the $j$-th scenarios. It will be <span class="tex-font-style-tt">F</span> if the corresponding transition video will be funny, <span class="tex-font-style-tt">S</span> if the corresponding transition video will be scary, <span class="tex-font-style-tt">?</span> if the corresponding transition video is still undecided, or&nbsp;<span class="tex-font-style-tt">.</span>&nbsp;if $i=j$.</p><p>It is guaranteed that the $i$-th character of the $j$-th line and the $j$-th character of the $i$-th line will be the same for all $i$ and $j$. It is guaranteed that at most $\lfloor \frac{n}{2} \rfloor$ ($n$ divided by 2, rounded down) transition videos will already be decided, in other words, that at most $2\lfloor \frac{n}{2} \rfloor$ characters in the input will be <span class="tex-font-style-tt">F</span> or <span class="tex-font-style-tt">S</span>.</p></div><div class="output-specification"><p>Print $n$ lines describing the full transition video plan in the same format as the input. Each of those lines must contain $n$ characters. The $j$-th character of the $i$-th line must be <span class="tex-font-style-tt">F</span> if the corresponding transition video is funny, <span class="tex-font-style-tt">S</span> if the corresponding transition video is scary, or&nbsp;<span class="tex-font-style-tt">.</span>&nbsp;if $i=j$.</p><p>Each <span class="tex-font-style-tt">?</span> character from the input must be replaced with either <span class="tex-font-style-tt">F</span> or <span class="tex-font-style-tt">S</span>, and all other characters from the input must remain unchanged. It must still hold that the $i$-th character of the $j$-th line and the $j$-th character of the $i$-th line are the same for all $i$ and $j$.</p><p>For each permutation of the $n$ scenarios, it must hold that the transition videos corresponding to playing the scenarios in this order do not have more than $\lceil \frac{3n}{4} \rceil$ ($3n$ divided by 4, rounded up) videos of the same type consecutively.</p><p>If there are multiple solutions, print any of them. It can be proven that for all inputs satisfying the constraints of this problem a solution always exists.</p></div>

## Input

<p>The first line contains a single integer $n$ ($2 \le n \le 24$)&nbsp;— the number of scenarios in the game.</p><p>The next $n$ lines describe the partial transition video plan. Each of those lines contains $n$ characters. The $j$-th character of the $i$-th line corresponds to the transition video between the $i$-th and the $j$-th scenarios. It will be <span class="tex-font-style-tt">F</span> if the corresponding transition video will be funny, <span class="tex-font-style-tt">S</span> if the corresponding transition video will be scary, <span class="tex-font-style-tt">?</span> if the corresponding transition video is still undecided, or&nbsp;<span class="tex-font-style-tt">.</span>&nbsp;if $i=j$.</p><p>It is guaranteed that the $i$-th character of the $j$-th line and the $j$-th character of the $i$-th line will be the same for all $i$ and $j$. It is guaranteed that at most $\lfloor \frac{n}{2} \rfloor$ ($n$ divided by 2, rounded down) transition videos will already be decided, in other words, that at most $2\lfloor \frac{n}{2} \rfloor$ characters in the input will be <span class="tex-font-style-tt">F</span> or <span class="tex-font-style-tt">S</span>.</p>

## Output

<p>Print $n$ lines describing the full transition video plan in the same format as the input. Each of those lines must contain $n$ characters. The $j$-th character of the $i$-th line must be <span class="tex-font-style-tt">F</span> if the corresponding transition video is funny, <span class="tex-font-style-tt">S</span> if the corresponding transition video is scary, or&nbsp;<span class="tex-font-style-tt">.</span>&nbsp;if $i=j$.</p><p>Each <span class="tex-font-style-tt">?</span> character from the input must be replaced with either <span class="tex-font-style-tt">F</span> or <span class="tex-font-style-tt">S</span>, and all other characters from the input must remain unchanged. It must still hold that the $i$-th character of the $j$-th line and the $j$-th character of the $i$-th line are the same for all $i$ and $j$.</p><p>For each permutation of the $n$ scenarios, it must hold that the transition videos corresponding to playing the scenarios in this order do not have more than $\lceil \frac{3n}{4} \rceil$ ($3n$ divided by 4, rounded up) videos of the same type consecutively.</p><p>If there are multiple solutions, print any of them. It can be proven that for all inputs satisfying the constraints of this problem a solution always exists.</p>





```input1|
5
.?F??
?.???
F?.S?
??S.?
????.
```




```input2|
12
.???????????
?.??????????
??.?????????
???.????????
????.???????
?????.??????
??????.?????
???????.????
????????.???
?????????.??
??????????.?
???????????.
```




```output1
.FFFF
F.FFF
FF.SF
FFS.F
FFFF.
```




```output2
.SSSFFSSSSFS
S.SFFSFSFFFS
SS.SFFFSSSFS
SFS.FFSSSSFS
FFFF.FFFFFSF
FSFFF.SFFSFF
SFFSFS.SSSFS
SSSSFFS.SSFS
SFSSFFSS.SFS
SFSSFSSSS.FS
FFFFSFFFFF.F
SSSSFFSSSSF.
```



## Note

<p>In the <span class="tex-font-style-bf">first sample</span>: We are allowed $\lceil \frac{3\cdot 5}{4} \rceil=4$ transition videos of the same type in a row, but for any permutation of the 5 scenarios the player will see only 4 transition videos in total, therefore we can choose funny or scary freely. We must still respect the already chosen types.</p><p>In the <span class="tex-font-style-bf">second sample</span>: One of the 479001600 possible permutations of scenarios is 1, 7, 4, 12, 9, 8, 2, 6, 10, 3, 11, 5. The player will get the following sequence of transition videos for this permutation: <span class="tex-font-style-tt">SSSSSSSSSFS</span>. Even though this sequence has 10 scary transition videos in total, it has only 9 scary transition videos in a row, which is the maximum allowed amount ($\lceil \frac{3\cdot 12}{4} \rceil=9$). </p>
