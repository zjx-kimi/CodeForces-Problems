## Description

<div><p>There are $n$ food items lying in a row on a long table. Each of these items is either a loaf of bread (denoted as a capital Latin letter '<span class="tex-font-style-tt">L</span>' with ASCII code 76) or an onion (denoted as a capital Latin letter '<span class="tex-font-style-tt">O</span>' with ASCII code 79). There is at least one loaf of bread and at least one onion on the table.</p><p>You and your friend want to divide the food on the table: you will take a prefix of this row (several leftmost items), and the friend will take the rest. However, there are several restrictions: </p><ol> <li> Each person should have at least one item. </li><li> The number of your loaves should differ from the number of your friend's loaves. </li><li> The number of your onions should differ from the number of your friend's onions. </li></ol> Find any correct division and print the number of items you take or report that there is no answer.</div><div class="input-specification"><p>The first line contains one integer $n$ ($2 \le n \le 200$)&nbsp;— the number of food items on the table. The second line contains a string of length $n$ consisting of letters '<span class="tex-font-style-tt">L</span>' and '<span class="tex-font-style-tt">O</span>'. $i$-th symbol represents the type of the $i$-th food item on the table: '<span class="tex-font-style-tt">L</span>' stands for a loaf of bread, and '<span class="tex-font-style-tt">O</span>' stands for an onion. It is guaranteed that this string contains at least one letter '<span class="tex-font-style-tt">L</span>' and at least one letter '<span class="tex-font-style-tt">O</span>'.</p></div><div class="output-specification"><p>Print one integer&nbsp;— a number $k$ such that, if you take $k$ leftmost items and your friend takes the remaining $n - k$ items, each of you and your friend get at least one item, your number of loaves is different from your friend's, and your number of onions is different from your friend's. If there are several possible answers, print any of them. If there are no possible answers, print the number $-1$.</p></div>

## Input

<p>The first line contains one integer $n$ ($2 \le n \le 200$)&nbsp;— the number of food items on the table. The second line contains a string of length $n$ consisting of letters '<span class="tex-font-style-tt">L</span>' and '<span class="tex-font-style-tt">O</span>'. $i$-th symbol represents the type of the $i$-th food item on the table: '<span class="tex-font-style-tt">L</span>' stands for a loaf of bread, and '<span class="tex-font-style-tt">O</span>' stands for an onion. It is guaranteed that this string contains at least one letter '<span class="tex-font-style-tt">L</span>' and at least one letter '<span class="tex-font-style-tt">O</span>'.</p>

## Output

<p>Print one integer&nbsp;— a number $k$ such that, if you take $k$ leftmost items and your friend takes the remaining $n - k$ items, each of you and your friend get at least one item, your number of loaves is different from your friend's, and your number of onions is different from your friend's. If there are several possible answers, print any of them. If there are no possible answers, print the number $-1$.</p>





```input1|
3
LOL
```




```input2|
2
LO
```




```input3|
4
LLLO
```




```input4|
4
OLOL
```




```input5|
10
LLOOOOLLLO
```




```output1
-1
```




```output2
1
```




```output3
1
```




```output4
-1
```




```output5
5
```



## Note

<p>In the first example, in any division the left and the right part contain one loaf of bread.</p><p>In the second example, the division is '<span class="tex-font-style-tt">L</span>' and '<span class="tex-font-style-tt">O</span>', and in these two strings the number of loaves is different (1 and 0) and the number of onions is different (0 and 1).</p><p>In the third example, any number 1, 2 or 3 is a correct answer.</p><p> </p>
