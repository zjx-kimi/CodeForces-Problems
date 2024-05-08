## Description

<div><p>There was a big bank robbery in Tablecity. In order to catch the thief, the President called none other than Albert – Tablecity’s Chief of Police. Albert does not know where the thief is located, but he does know how he moves.</p><p>Tablecity can be represented as <span class="tex-span">1000 × 2</span> grid, where every cell represents one district. Each district has its own unique name “<span class="tex-span">(<i>X</i>, <i>Y</i>)</span>”, where <span class="tex-span"><i>X</i></span> and <span class="tex-span"><i>Y</i></span> are the coordinates of the district in the grid. The thief’s movement is as </p><p>Every hour the thief will leave the district <span class="tex-span">(<i>X</i>, <i>Y</i>)</span> he is currently hiding in, and move to one of the districts: <span class="tex-span">(<i>X</i> - 1, <i>Y</i>)</span>, <span class="tex-span">(<i>X</i> + 1, <i>Y</i>)</span>, <span class="tex-span">(<i>X</i> - 1, <i>Y</i> - 1)</span>, <span class="tex-span">(<i>X</i> - 1, <i>Y</i> + 1)</span>, <span class="tex-span">(<i>X</i> + 1, <i>Y</i> - 1)</span>, <span class="tex-span">(<i>X</i> + 1, <i>Y</i> + 1)</span> as long as it exists in Tablecity. </p><p>Below is an example of thief’s possible movements if he is located in district (7,1):</p><p><img class="tex-graphics" src="file://FPhEmjW1.png" style="max-width: 100.0%;max-height: 100.0%;"></p><p>Albert has enough people so that <span class="tex-font-style-bf">every hour</span> he can pick any <span class="tex-font-style-bf">two</span> districts in Tablecity and fully investigate them, making sure that if the thief is located in one of them, he will get caught. Albert promised the President that the thief will be caught in <span class="tex-font-style-bf">no more</span> than 2015 hours and needs your help in order to achieve that.</p></div><div class="input-specification"><p>There is no input for this problem. </p></div><div class="output-specification"><p>The first line of output contains integer <span class="tex-span"><i>N</i></span> – duration of police search in hours. Each of the following <span class="tex-span"><i>N</i></span> lines contains exactly 4 integers <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i>1</sub></span>, <span class="tex-span"><i>Y</i><sub class="lower-index"><i>i</i>1</sub></span>, <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i>2</sub></span>, <span class="tex-span"><i>Y</i><sub class="lower-index"><i>i</i>2</sub></span> separated by spaces, that represent 2 districts (<span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i>1</sub></span>, <span class="tex-span"><i>Y</i><sub class="lower-index"><i>i</i>1</sub></span>), (<span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i>2</sub></span>, <span class="tex-span"><i>Y</i><sub class="lower-index"><i>i</i>2</sub></span>) which got investigated during i-th hour. Output is given in <span class="tex-font-style-bf">chronological</span> order (i-th line contains districts investigated during i-th hour) and should <span class="tex-font-style-bf">guarantee</span> that the thief is caught in no more than 2015 hours, <span class="tex-font-style-bf">regardless of thief’s initial position and movement</span>.</p><ul> <li> <span class="tex-span"><i>N</i> ≤ 2015</span> </li><li> <span class="tex-span">1 ≤ <i>X</i> ≤ 1000</span> </li><li> <span class="tex-span">1 ≤ <i>Y</i> ≤ 2</span> </li></ul></div>

## Input

<p>There is no input for this problem. </p>

## Output

<p>The first line of output contains integer <span class="tex-span"><i>N</i></span> – duration of police search in hours. Each of the following <span class="tex-span"><i>N</i></span> lines contains exactly 4 integers <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i>1</sub></span>, <span class="tex-span"><i>Y</i><sub class="lower-index"><i>i</i>1</sub></span>, <span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i>2</sub></span>, <span class="tex-span"><i>Y</i><sub class="lower-index"><i>i</i>2</sub></span> separated by spaces, that represent 2 districts (<span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i>1</sub></span>, <span class="tex-span"><i>Y</i><sub class="lower-index"><i>i</i>1</sub></span>), (<span class="tex-span"><i>X</i><sub class="lower-index"><i>i</i>2</sub></span>, <span class="tex-span"><i>Y</i><sub class="lower-index"><i>i</i>2</sub></span>) which got investigated during i-th hour. Output is given in <span class="tex-font-style-bf">chronological</span> order (i-th line contains districts investigated during i-th hour) and should <span class="tex-font-style-bf">guarantee</span> that the thief is caught in no more than 2015 hours, <span class="tex-font-style-bf">regardless of thief’s initial position and movement</span>.</p><ul> <li> <span class="tex-span"><i>N</i> ≤ 2015</span> </li><li> <span class="tex-span">1 ≤ <i>X</i> ≤ 1000</span> </li><li> <span class="tex-span">1 ≤ <i>Y</i> ≤ 2</span> </li></ul>





```input1
В этой задаче нет примеров ввода-вывода.
This problem doesn't have sample input and output.
```




```output1
Смотрите замечание ниже.
See the note below.
```



## Note

<p>Let's consider the following output:</p><p>2</p><p>5 1 50 2</p><p>8 1 80 2</p><p>This output is not guaranteed to catch the thief and is not correct. It is given to you only to show the expected output format. There exists a combination of an initial position and a movement strategy such that the police will not catch the thief.</p><p>Consider the following initial position and thief’s movement:</p><p>In the first hour, the thief is located in district (1,1). Police officers will search districts (5,1) and (50,2) and will not find him.</p><p>At the start of the second hour, the thief moves to district (2,2). Police officers will search districts (8,1) and (80,2) and will not find him.</p><p>Since there is no further investigation by the police, the thief escaped!</p>
