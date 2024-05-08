## Description

<div><p>Talia has just bought an abandoned house in the outskirt of Jakarta. The house has a nice and long yard which can be represented as a one-dimensional grid containing $1 \times N$ cells. To beautify the house, Talia is going to build a terrace on the yard by tiling the cells. Each cell on the yard contains either soil (represented by the character '<span class="tex-font-style-tt">.</span>') or rock (represented by the character '<span class="tex-font-style-tt">#</span>'), and there are at most $50$ cells containing rocks.</p><p>Being a superstitious person, Talia wants to tile the terrace with mystical tiles that have the power to repel ghosts. There are three types of mystical tiles: </p><ul> <li> Type-1: Covers $1 \times 1$ cell and can only be placed on a soil cell ("<span class="tex-font-style-tt">.</span>"). </li><li> Type-2: Covers $1 \times 2$ cells and can only be placed on two consecutive soil cells ("<span class="tex-font-style-tt">..</span>"). </li><li> Type-3: Covers $1 \times 3$ cells and can only be placed on consecutive soil-rock-soil cells ("<span class="tex-font-style-tt">.#.</span>"). </li></ul><p>Each tile of Type-1, Type-2, and Type-3 has the power to repel $G_1$, $G_2$, and $G_3$ ghosts per day, respectively. There are also some mystical rules which must be followed for the power to be effective: </p><ul> <li> There should be no overlapping tiles, i.e. each cell is covered by at most one tile. </li><li> There should be at most $K$ tiles of Type-1, while there are no limitations for tiles of Type-2 and Type-3. </li></ul><p>Talia is scared of ghosts, thus, the terrace (which is tiled by mystical tiles) should be able to repel as many ghosts as possible. Help Talia to find the maximum number of ghosts that can be repelled per day by the terrace. Note that Talia <span class="tex-font-style-bf">does not need</span> to tile all the cells on the yard as long as the number of ghosts that can be repelled by the terrace is maximum.</p></div><div class="input-specification"><p>Input begins with a line containing five integers: $N$ $K$ $G_1$ $G_2$ $G_3$ ($1 \le N \le 100\,000$; $0 \le K \le N$; $0 \le G_1, G_2, G_3 \le 1000$) representing the number of cells, the maximum number of tiles of Type-1, the number of ghosts repelled per day by a tile of Type-1, the number of ghosts repelled per day by a tile of Type-2, and the number of ghosts repelled by a tile of Type-3, respectively. The next line contains a string of $N$ characters representing the yard. Each character in the string is either '<span class="tex-font-style-tt">.</span>' which represents a soil cell or '#' which represents a rock cell. There are at most $50$ rock cells.</p></div><div class="output-specification"><p>Output in a line an integer representing the maximum number of ghosts that can be repelled per day.</p></div>

## Input

<p>Input begins with a line containing five integers: $N$ $K$ $G_1$ $G_2$ $G_3$ ($1 \le N \le 100\,000$; $0 \le K \le N$; $0 \le G_1, G_2, G_3 \le 1000$) representing the number of cells, the maximum number of tiles of Type-1, the number of ghosts repelled per day by a tile of Type-1, the number of ghosts repelled per day by a tile of Type-2, and the number of ghosts repelled by a tile of Type-3, respectively. The next line contains a string of $N$ characters representing the yard. Each character in the string is either '<span class="tex-font-style-tt">.</span>' which represents a soil cell or '#' which represents a rock cell. There are at most $50$ rock cells.</p>

## Output

<p>Output in a line an integer representing the maximum number of ghosts that can be repelled per day.</p>





```input1
6 4 10 25 40
..#...
```




```input2
6 4 10 100 40
..#...
```




```input3
7 2 30 10 100
..#...#
```




```output1
75
```




```output2
210
```




```output3
160
```



## Note

<p><span class="tex-font-style-it">Explanation for the sample input/output #1</span></p><p>Let "<span class="tex-font-style-tt">A</span>" be a tile of Type-1, "<span class="tex-font-style-tt">BB</span>" be a tile of Type-2, and "<span class="tex-font-style-tt">CCC</span>" be a tile of Type-3. The tiling "<span class="tex-font-style-tt">ACCCBB</span>" in this case produces the maximum number of ghosts that can be repelled, i.e. $10 + 40 + 25 = 75$</p><p><span class="tex-font-style-it">Explanation for the sample input/output #2</span></p><p>This sample input has the same yard with the previous sample input, but each tile of Type-2 can repel more ghosts per day. The tiling "<span class="tex-font-style-tt">BB#BBA</span>" or "<span class="tex-font-style-tt">BB#ABB</span>" produces the maximum number of ghosts that can be repelled, i.e. $100 + 100 + 10 = 210$. Observe that the third cell is left untiled.</p><p><span class="tex-font-style-it">Explanation for the sample input/output #3</span></p><p>The tiling "<span class="tex-font-style-tt">ACCCA.#</span>", "<span class="tex-font-style-tt">ACCC.A#</span>", or "<span class="tex-font-style-tt">.CCCAA#</span>" produces the maximum number of ghosts that can be repelled, i.e. $30 + 100 + 30 = 160$. Observe that there is no way to tile the last cell.</p>
