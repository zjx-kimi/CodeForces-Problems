## Description

<div><p>After a probationary period in the game development company of IT City Petya was included in a group of the programmers that develops a new turn-based strategy game resembling the well known "Heroes of Might &amp; Magic". A part of the game is turn-based fights of big squadrons of enemies on infinite fields where every cell is in form of a hexagon.</p><p>Some of magic effects are able to affect several field cells at once, cells that are situated not farther than <span class="tex-span"><i>n</i></span> cells away from the cell in which the effect was applied. The distance between cells is the minimum number of cell border crosses on a path from one cell to another.</p><p>It is easy to see that the number of cells affected by a magic effect grows rapidly when <span class="tex-span"><i>n</i></span> increases, so it can adversely affect the game performance. That's why Petya decided to write a program that can, given <span class="tex-span"><i>n</i></span>, determine the number of cells that should be repainted after effect application, so that game designers can balance scale of the effects and the game performance. Help him to do it. Find the number of hexagons situated not farther than <span class="tex-span"><i>n</i></span> cells away from a given cell.</p><center> <img class="tex-graphics" src="file://g19OzQv7.png" style="max-width: 100.0%;max-height: 100.0%;"> </center></div><div class="input-specification"><p>The only line of the input contains one integer <span class="tex-span"><i>n</i></span> (<span class="tex-span">0 ≤ <i>n</i> ≤ 10<sup class="upper-index">9</sup></span>).</p></div><div class="output-specification"><p>Output one integer — the number of hexagons situated not farther than <span class="tex-span"><i>n</i></span> cells away from a given cell.</p></div>

## Input

<p>The only line of the input contains one integer <span class="tex-span"><i>n</i></span> (<span class="tex-span">0 ≤ <i>n</i> ≤ 10<sup class="upper-index">9</sup></span>).</p>

## Output

<p>Output one integer — the number of hexagons situated not farther than <span class="tex-span"><i>n</i></span> cells away from a given cell.</p>





```input1
2

```




```output1
19
```


