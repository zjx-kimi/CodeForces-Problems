## Description

<div><p>One Martian boy called Zorg wants to present a string of beads to his friend from the Earth — Masha. He knows that Masha likes two colours: blue and red, — and right in the shop where he has come, there is a variety of adornments with beads of these two colours. All the strings of beads have a small fastener, and if one unfastens it, one might notice that all the strings of beads in the shop are of the same length. Because of the peculiarities of the Martian eyesight, if Zorg sees one blue-and-red string of beads first, and then the other with red beads instead of blue ones, and blue — instead of red, he regards these two strings of beads as identical. In other words, Zorg regards as identical not only those strings of beads that can be derived from each other by the string turnover, but as well those that can be derived from each other by a mutual replacement of colours and/or by the string turnover.</p><p>It is known that all Martians are very orderly, and if a Martian sees some amount of objects, he tries to put them in good order. Zorg thinks that a red bead is smaller than a blue one. Let's put 0 for a red bead, and 1 — for a blue one. From two strings the Martian puts earlier the string with a red bead in the <span class="tex-span"><i>i</i></span>-th position, providing that the second string has a blue bead in the <span class="tex-span"><i>i</i></span>-th position, and the first two beads <span class="tex-span"><i>i</i> - 1</span> are identical.</p><p>At first Zorg unfastens all the strings of beads, and puts them into small heaps so, that in each heap strings are identical, in his opinion. Then he sorts out the heaps and chooses the minimum string in each heap, in his opinion. He gives the unnecassary strings back to the shop assistant and says he doesn't need them any more. Then Zorg sorts out the remaining strings of beads and buys the string with index <span class="tex-span"><i>k</i></span>. </p><p>All these manupulations will take Zorg a lot of time, that's why he asks you to help and find the string of beads for Masha.</p></div><div class="input-specification"><p>The input file contains two integers <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>k</i></span> (<span class="tex-span">2 ≤ <i>n</i> ≤ 50;1 ≤ <i>k</i> ≤ 10<sup class="upper-index">16</sup></span>) —the length of a string of beads, and the index of the string, chosen by Zorg. </p></div><div class="output-specification"><p>Output the <span class="tex-span"><i>k</i></span>-th string of beads, putting 0 for a red bead, and 1 — for a blue one. If it s impossible to find the required string, output the only number <span class="tex-font-style-tt">-1</span>.</p></div>

## Input

<p>The input file contains two integers <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>k</i></span> (<span class="tex-span">2 ≤ <i>n</i> ≤ 50;1 ≤ <i>k</i> ≤ 10<sup class="upper-index">16</sup></span>) —the length of a string of beads, and the index of the string, chosen by Zorg. </p>

## Output

<p>Output the <span class="tex-span"><i>k</i></span>-th string of beads, putting 0 for a red bead, and 1 — for a blue one. If it s impossible to find the required string, output the only number <span class="tex-font-style-tt">-1</span>.</p>





```input1
4 4

```




```output1
0101

```



## Note

<p>Let's consider the example of strings of length 4 — 0001, 0010, 0011, 0100, 0101, 0110, 0111, 1000, 1001, 1010, 1011, 1100, 1101, 1110. Zorg will divide them into heaps: {0001, 0111, 1000, 1110}, {0010, 0100, 1011, 1101}, {0011, 1100}, {0101, 1010}, {0110, 1001}. Then he will choose the minimum strings of beads in each heap: 0001, 0010, 0011, 0101, 0110. The forth string — 0101.</p>