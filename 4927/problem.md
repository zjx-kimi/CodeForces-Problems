## Description

<div><p><span class="tex-font-style-bf">This is an interactive task.</span></p><p>Rudolph is a scientist who studies alien life forms. There is a room in front of Rudolph with $n$ different objects scattered around. Among the objects there is <span class="tex-font-style-bf">exactly one</span> amazing creature — a mimic that can turn into any object. He has already disguised himself in this room and Rudolph needs to find him by experiment.</p><p>The experiment takes place in several stages. At each stage, the following happens:</p><ul><li> Rudolf looks at all the objects in the room and writes down their types. The type of each object is indicated by a number; there can be several objects of the same type.</li><li> After inspecting, Rudolph can point to an object that he thinks is a mimic. After that, the experiment ends. Rudolph only has one try, so if he is unsure of the mimic's position, he does the next step instead.</li><li> Rudolf can remove any number of objects from the room (possibly zero). Then Rudolf leaves the room and at this time all objects, including the mimic, <span class="tex-font-style-bf">are mixed</span> with each other, their order is changed, and the <span class="tex-font-style-bf">mimic can transform</span> into any other object (even one that is not in the room).</li><li> After this, Rudolf returns to the room and repeats the stage. The <span class="tex-font-style-bf">mimic may not change appearance</span>, but it can not remain a same object for more than two stages in a row.</li></ul><p>Rudolf's task is to detect mimic in no more than <span class="tex-font-style-bf">five</span> stages.</p></div><div class="input-specification"><p>The first line contains one integer $t$ $(1 \le t \le 1000)$ — the number of test cases.</p><p>The first line of each test case contains one integer $n$ $(2 \le n \le 200)$ — the number of objects in the room.</p><p>The second line of each test case contains $n$ integers $a_1$,$a_2$,...,$a_n$ $(1 \le a_i \le 9)$ — object types.</p></div><div><h2>Interaction</h2><p>After you have read the description of the input data set, you must make no more than <span class="tex-font-style-bf">$5$</span> queries. Reading the input data is considered the beginning of the first stage, and the mimic may already begin to change.</p><p>The request is a line. The first character of the line indicates the request type. To remove objects, print "-". After that print the number $k$ — how many objects you want to remove. Then there are $k$ numbers — indexes of objects in their current location. Indexing starts from one. You can remove the mimic, but in this case you will not be able to point to it and will get "Wrong answer" verdict.</p><p>In response to the request you will receive a line containing integers — the objects remaining in the room after removal and mixing.</p><p>To indicate the position of a mimic, print "!", then print the index of the object that is the mimic.</p><p>The task will be considered solved if the position of the mimic is specified correctly.</p><p>If you make more than five requests, or make an invalid request, the solution will get "Wrong answer" verdict.</p><p>After outputting a query or the answer do not forget to output the end of line and flush the output. Otherwise, you will get "Idleness limit exceeded". To do this, use:</p><ul> <li> fflush(stdout) or cout.flush() in C++; </li><li> System.out.flush() in Java; </li><li> flush(output) in Pascal; </li><li> stdout.flush() in Python; </li><li> see documentation for other languages. </li></ul><p><span class="tex-font-style-bf">Hacks</span></p><p>You can hack a solution with the following input format.</p><p>The first line contains one integer $t$ $(1 \le t \le 1000)$ — the number of test cases.</p><p>The first line of each test case contains two integers $n$, $k$ ($2 \le n \le 200, 1 \le k \le n$)&nbsp;— the number of objects and the position of the mimic.</p><p>The second line contains of each test case $n$ integers $a_1$, $a_2$,...,$a_n$ ($1 \le a_i \le 9$) – initial array of objects.</p></div>

## Input

<p>The first line contains one integer $t$ $(1 \le t \le 1000)$ — the number of test cases.</p><p>The first line of each test case contains one integer $n$ $(2 \le n \le 200)$ — the number of objects in the room.</p><p>The second line of each test case contains $n$ integers $a_1$,$a_2$,...,$a_n$ $(1 \le a_i \le 9)$ — object types.</p>





```input1
3
5
1 1 2 2 3

2 1 1 2

2 2 2

2

8
1 2 3 4 3 4 2 1

4 3 4 3 2 2 1 3
 
2 3 3 2

5 3 2

2 5

15
1 2 3 4 5 6 7 8 7 6 5 4 3 2 1 

1 2 3 4 5 6 7 8 7 9 5 4 3 2 1
```




```output1
- 1 5

- 1 3

- 2 1 2

! 1


- 0

- 4 1 3 7 8

- 1 4

- 1 2

! 2


- 0

! 10
```



## Note

<p>Explanation for the first test: initial array is $x_1$, $x_2$, $x_3$, $x_4$, $x_5$. Mimic is in first position. </p><ul><li> Delete the fifth object. After that, the positions are shuffled, and the mimic chose not to change his appearance. Object positions become $x_4$, $x_1$, $x_2$, $x_3$. </li><li> Delete the third objects. The mimic is forced to turn into another object, because it has already been in the form $1$ for two stages. The mimic chose to transform into $2$, the objects are shuffled and become $x_3$, $x_4$, $x_1$. </li><li> Delete the first and second objects. The objects positions become $x_1$. Only the mimic remains, and it remains an object $2$. </li><li> Point to the first element.</li></ul>
