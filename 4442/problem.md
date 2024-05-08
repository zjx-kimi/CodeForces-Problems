## Description

<div><p>Vova's family is building the Great Vova Wall (named by Vova himself). Vova's parents, grandparents, grand-grandparents contributed to it. Now it's totally up to Vova to put the finishing touches.</p><p>The current state of the wall can be respresented by a sequence $a$ of $n$ integers, with $a_i$ being the height of the $i$-th part of the wall.</p><p>Vova can only use $2 \times 1$ bricks to put in the wall (he has infinite supply of them, however).</p><p>Vova can put bricks <span class="tex-font-style-bf">only horizontally</span> on the neighbouring parts of the wall of equal height. It means that if for some $i$ the current height of part $i$ is the same as for part $i + 1$, then Vova can put a brick there and thus increase both heights by 1. Obviously, Vova can't put bricks in such a way that its parts turn out to be off the borders (to the left of part $1$ of the wall or to the right of part $n$ of it).</p><p><span class="tex-font-style-bf">Note that Vova can't put bricks vertically.</span></p><p>Vova is a perfectionist, so he considers the wall completed when:</p><ul> <li> all parts of the wall has the same height; </li><li> the wall has no empty spaces inside it. </li></ul><p>Can Vova complete the wall using any amount of bricks (possibly zero)?</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$) — the number of parts in the wall.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$) — the initial heights of the parts of the wall.</p></div><div class="output-specification"><p>Print "<span class="tex-font-style-tt">YES</span>" if Vova can complete the wall using any amount of bricks (possibly zero).</p><p>Print "<span class="tex-font-style-tt">NO</span>" otherwise.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$) — the number of parts in the wall.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$) — the initial heights of the parts of the wall.</p>

## Output

<p>Print "<span class="tex-font-style-tt">YES</span>" if Vova can complete the wall using any amount of bricks (possibly zero).</p><p>Print "<span class="tex-font-style-tt">NO</span>" otherwise.</p>





```input1
5
2 1 1 2 5
```




```input2
3
4 5 3
```




```input3
2
10 10
```




```output1
YES
```




```output2
NO
```




```output3
YES
```



## Note

<p>In the first example Vova can put a brick on parts 2 and 3 to make the wall $[2, 2, 2, 2, 5]$ and then put 3 bricks on parts 1 and 2 and 3 bricks on parts 3 and 4 to make it $[5, 5, 5, 5, 5]$.</p><p>In the second example Vova can put no bricks in the wall.</p><p>In the third example the wall is already complete.</p>
