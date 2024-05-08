## Description

<div><p>Vasya plays a popular game the Gnomes of Might and Magic.</p><p>In this game Vasya manages the kingdom of gnomes, consisting of several castles, connected by bidirectional roads. The kingdom road network has a special form. The kingdom has <span class="tex-span"><i>m</i></span> main castles <span class="tex-span"><i>a</i><sub class="lower-index">1</sub>, <i>a</i><sub class="lower-index">2</sub>, ..., <i>a</i><sub class="lower-index"><i>m</i></sub></span>, which form the Good Path. This path consists of roads between the castles <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub>, <i>a</i><sub class="lower-index"><i>i</i> + 1</sub></span> <span class="tex-span">(1 ≤ <i>i</i> &lt; <i>m</i>)</span> as well as the road between <span class="tex-span"><i>a</i><sub class="lower-index"><i>m</i></sub></span> and <span class="tex-span"><i>a</i><sub class="lower-index">1</sub></span>. There are no other roads between the castles of the Good Path.</p><p>In addition, for each pair of neighboring Good Path castles <span class="tex-span"><i>u</i></span> and <span class="tex-span"><i>v</i></span> there is exactly one Evil Shortcut — a path that goes along the roads leading from the first castle <span class="tex-span">(<i>u</i>)</span> to the second one <span class="tex-span">(<i>v</i>)</span> and not having any common vertexes with the Good Path except for the vertexes <span class="tex-span"><i>u</i></span> and <span class="tex-span"><i>v</i></span>. It is known that there are no other roads and castles in the kingdom there, that is, every road and every castle lies either on the Good Path or the Evil Shortcut (castles can lie in both of them). In addition, no two Evil Shortcuts have any common castles, different than the castles of the Good Path.</p><p>At the beginning of each week in the kingdom appears one very bad gnome who stands on one of the roads of the kingdom, and begins to rob the corovans going through this road. One road may accumulate multiple very bad gnomes. Vasya cares about his corovans, so sometimes he sends the Mission of Death from one castle to another.</p><p>Let's suggest that the Mission of Death should get from castle <span class="tex-span"><i>s</i></span> to castle <span class="tex-span"><i>t</i></span>. Then it will move from castle <span class="tex-span"><i>s</i></span> to castle <span class="tex-span"><i>t</i></span>, destroying all very bad gnomes, which are on the roads of the Mission's path. Vasya is so tough that his Mission of Death can destroy any number of gnomes on its way. However, Vasya is very kind, so he always chooses such path between castles <span class="tex-span"><i>s</i></span> and <span class="tex-span"><i>t</i></span>, following which he will destroy the smallest number of gnomes. If there are multiple such paths, then Vasya chooses the path that contains the smallest number of roads among them. If there are multiple such paths still, Vasya chooses the lexicographically minimal one among them.</p><p>Help Vasya to simulate the life of the kingdom in the Gnomes of Might and Magic game.</p><p>A path is a sequence of castles, such that each pair of the neighboring castles on the path is connected by a road. Also, path <span class="tex-span"><i>x</i><sub class="lower-index">1</sub>, <i>x</i><sub class="lower-index">2</sub>, ... , <i>x</i><sub class="lower-index"><i>p</i></sub></span> is lexicographically less than path <span class="tex-span"><i>y</i><sub class="lower-index">1</sub>, <i>y</i><sub class="lower-index">2</sub>, ... , <i>y</i><sub class="lower-index"><i>q</i></sub></span>, if either <span class="tex-span"><i>p</i> &lt; <i>q</i></span> and <span class="tex-span"><i>x</i><sub class="lower-index">1</sub> = <i>y</i><sub class="lower-index">1</sub>, <i>x</i><sub class="lower-index">2</sub> = <i>y</i><sub class="lower-index">2</sub>, ... , <i>x</i><sub class="lower-index"><i>p</i></sub> = <i>y</i><sub class="lower-index"><i>p</i></sub></span>, or exists such number <span class="tex-span"><i>r</i></span> <span class="tex-span">(<i>r</i> &lt; <i>p</i>, <i>r</i> &lt; <i>q</i>)</span>, that <span class="tex-span"><i>x</i><sub class="lower-index">1</sub> = <i>y</i><sub class="lower-index">1</sub>, <i>x</i><sub class="lower-index">2</sub> = <i>y</i><sub class="lower-index">2</sub>, ... , <i>x</i><sub class="lower-index"><i>r</i></sub> = <i>y</i><sub class="lower-index"><i>r</i></sub></span> and <span class="tex-span"><i>x</i><sub class="lower-index"><i>r</i> + 1</sub> &lt; <i>y</i><sub class="lower-index"><i>r</i> + 1</sub></span>.</p></div><div class="input-specification"><p>The first line contains two integers <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>m</i></span> <span class="tex-span">(3 ≤ <i>m</i> ≤ <i>n</i> ≤ 100000)</span> — the number of castles in the kingdom, and the number of castles on the Good Path, respectively.</p><p>The second line contains <span class="tex-span"><i>m</i></span> integers, which are numbers of Good Path castles (the castles are numbered from <span class="tex-span">1</span> to <span class="tex-span"><i>n</i></span>) in the order of occurrence on the Path, starting with some castle. All Good Path castles are different.</p><p>Each of the following <span class="tex-span"><i>m</i></span> lines describes an Evil Shortcut. First a line contains an integer <span class="tex-span"><i>k</i><sub class="lower-index"><i>i</i></sub></span> <span class="tex-span">(3 ≤ <i>k</i><sub class="lower-index"><i>i</i></sub> ≤ 100000)</span> — the number of castles on the corresponding Evil Shortcut (with the two castles which are on the Good Path), followed by a <span class="tex-span"><i>k</i><sub class="lower-index"><i>i</i></sub></span> integers — number of castles in the order of occurrence in the given Shortcut. All castles in one Evil Shortcut are different. It is guaranteed that the first and the last castles from the Shortcut are on the Good Path and the first castles in the Evil Shortcuts form the Good Path and are presented in the same order in which the Path was represented on the second line.</p><p>The next line contains an integer <span class="tex-span"><i>q</i></span> <span class="tex-span">(1 ≤ <i>q</i> ≤ 100000)</span> — the number of events in the life of the kingdom. Each of the following <span class="tex-span"><i>q</i></span> lines describes a single event. An event is described by the symbol <span class="tex-span"><i>c</i><sub class="lower-index"><i>j</i></sub></span> and two numbers or castles <span class="tex-span"><i>s</i><sub class="lower-index"><i>j</i></sub></span> and <span class="tex-span"><i>t</i><sub class="lower-index"><i>j</i></sub></span> (the character and numbers of castles are separated by a single space). If the character of <span class="tex-span"><i>c</i><sub class="lower-index"><i>j</i></sub></span> is equal to "<span class="tex-font-style-tt">+</span>" (a plus), it means that a very bad gnome (probably not the first one) has appeared on the road between castles <span class="tex-span"><i>s</i><sub class="lower-index"><i>j</i></sub></span> and <span class="tex-span"><i>t</i><sub class="lower-index"><i>j</i></sub></span>. If <span class="tex-span"><i>c</i><sub class="lower-index"><i>j</i></sub></span> equals "<span class="tex-font-style-tt">?</span>" (a question), then Vasya sent a Mission of Death from castle <span class="tex-span"><i>s</i><sub class="lower-index"><i>j</i></sub></span> to castle <span class="tex-span"><i>t</i><sub class="lower-index"><i>j</i></sub></span>. It is guaranteed that for each request "<span class="tex-font-style-tt">+</span>", the road between castles <span class="tex-span"><i>s</i><sub class="lower-index"><i>j</i></sub></span> and <span class="tex-span"><i>t</i><sub class="lower-index"><i>j</i></sub></span> exists. The events are given in chronological order, starting with the earliest one. Initially there are no very bad gnomes on the roads.</p><p>All numbers in all lines are separated by single spaces. It is guaranteed that all the given Evil Shortcuts and Good Path fit in the limitations given in the problem statement.</p></div><div class="output-specification"><p>For each query "<span class="tex-font-style-tt">?</span>" print a single number on a single line — the number of very bad gnomes destroyed by the corresponding Mission of Death. Print the answers to queries in the chronological order.</p></div>

## Input

<p>The first line contains two integers <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>m</i></span> <span class="tex-span">(3 ≤ <i>m</i> ≤ <i>n</i> ≤ 100000)</span> — the number of castles in the kingdom, and the number of castles on the Good Path, respectively.</p><p>The second line contains <span class="tex-span"><i>m</i></span> integers, which are numbers of Good Path castles (the castles are numbered from <span class="tex-span">1</span> to <span class="tex-span"><i>n</i></span>) in the order of occurrence on the Path, starting with some castle. All Good Path castles are different.</p><p>Each of the following <span class="tex-span"><i>m</i></span> lines describes an Evil Shortcut. First a line contains an integer <span class="tex-span"><i>k</i><sub class="lower-index"><i>i</i></sub></span> <span class="tex-span">(3 ≤ <i>k</i><sub class="lower-index"><i>i</i></sub> ≤ 100000)</span> — the number of castles on the corresponding Evil Shortcut (with the two castles which are on the Good Path), followed by a <span class="tex-span"><i>k</i><sub class="lower-index"><i>i</i></sub></span> integers — number of castles in the order of occurrence in the given Shortcut. All castles in one Evil Shortcut are different. It is guaranteed that the first and the last castles from the Shortcut are on the Good Path and the first castles in the Evil Shortcuts form the Good Path and are presented in the same order in which the Path was represented on the second line.</p><p>The next line contains an integer <span class="tex-span"><i>q</i></span> <span class="tex-span">(1 ≤ <i>q</i> ≤ 100000)</span> — the number of events in the life of the kingdom. Each of the following <span class="tex-span"><i>q</i></span> lines describes a single event. An event is described by the symbol <span class="tex-span"><i>c</i><sub class="lower-index"><i>j</i></sub></span> and two numbers or castles <span class="tex-span"><i>s</i><sub class="lower-index"><i>j</i></sub></span> and <span class="tex-span"><i>t</i><sub class="lower-index"><i>j</i></sub></span> (the character and numbers of castles are separated by a single space). If the character of <span class="tex-span"><i>c</i><sub class="lower-index"><i>j</i></sub></span> is equal to "<span class="tex-font-style-tt">+</span>" (a plus), it means that a very bad gnome (probably not the first one) has appeared on the road between castles <span class="tex-span"><i>s</i><sub class="lower-index"><i>j</i></sub></span> and <span class="tex-span"><i>t</i><sub class="lower-index"><i>j</i></sub></span>. If <span class="tex-span"><i>c</i><sub class="lower-index"><i>j</i></sub></span> equals "<span class="tex-font-style-tt">?</span>" (a question), then Vasya sent a Mission of Death from castle <span class="tex-span"><i>s</i><sub class="lower-index"><i>j</i></sub></span> to castle <span class="tex-span"><i>t</i><sub class="lower-index"><i>j</i></sub></span>. It is guaranteed that for each request "<span class="tex-font-style-tt">+</span>", the road between castles <span class="tex-span"><i>s</i><sub class="lower-index"><i>j</i></sub></span> and <span class="tex-span"><i>t</i><sub class="lower-index"><i>j</i></sub></span> exists. The events are given in chronological order, starting with the earliest one. Initially there are no very bad gnomes on the roads.</p><p>All numbers in all lines are separated by single spaces. It is guaranteed that all the given Evil Shortcuts and Good Path fit in the limitations given in the problem statement.</p>

## Output

<p>For each query "<span class="tex-font-style-tt">?</span>" print a single number on a single line — the number of very bad gnomes destroyed by the corresponding Mission of Death. Print the answers to queries in the chronological order.</p>





```input1
6 3
1 2 3
3 1 4 2
3 2 5 3
3 3 6 1
10
+ 1 2
+ 4 2
+ 1 3
+ 2 3
? 1 2
+ 2 5
? 1 2
? 1 2
+ 1 2
? 1 2

```




```output1
0
1
0
1

```



## Note

<p>In the example after the first four requests there is only one path from castle 1 to castle 2, which does not contain roads with very bad gnomes: 1 <img align="middle" class="tex-formula" src="file://37L7aOza.png" style="max-width: 100.0%;max-height: 100.0%;"> 6 <img align="middle" class="tex-formula" src="file://1kjlIFS1.png" style="max-width: 100.0%;max-height: 100.0%;"> 3 <img align="middle" class="tex-formula" src="file://qksOS3Qj.png" style="max-width: 100.0%;max-height: 100.0%;"> 5 <img align="middle" class="tex-formula" src="file://JGYgMjDv.png" style="max-width: 100.0%;max-height: 100.0%;"> 2.</p><p>After a gnome stood on the road (2, 5), the next Mission of Death moves along path 1 <img align="middle" class="tex-formula" src="file://Lfxlnw0r.png" style="max-width: 100.0%;max-height: 100.0%;"> 2, and destroys the gnome, who was on the road (1, 2). The next Mission of Death follows the same path which is already free of gnomes.</p><p>After yet another gnome stood on the road (1, 2), the next Mission of Death goes on the path 1 <img align="middle" class="tex-formula" src="file://lE0N2xxd.png" style="max-width: 100.0%;max-height: 100.0%;"> 2, and kills the gnome.</p>