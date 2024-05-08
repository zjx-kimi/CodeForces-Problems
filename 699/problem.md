## Description

<div><center> <img class="tex-graphics" height="189px" src="file://SpXmxPkZ.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>Galaxy Luck, a well-known casino in the entire solar system, introduces a new card game.</p><p>In this game, there is a deck that consists of $n$ cards. Each card has $m$ numbers written on it. Each of the $n$ players receives exactly one card from the deck.</p><p>Then all players play with each other in pairs, and each pair of players plays exactly once. Thus, if there are, for example, four players in total, then six games are played: the first against the second, the first against the third, the first against the fourth, the second against the third, the second against the fourth and the third against the fourth.</p><p>Each of these games determines the winner in some way, but the rules are quite complicated, so we will not describe them here. All that matters is how many chips are paid out to the winner. Let the first player's card have the numbers $a_1, a_2, \dots, a_m$, and the second player's card&nbsp;— $b_1, b_2, \dots, b_m$. Then the winner of the game gets $|a_1 - b_1| + |a_2 - b_2| + \dots + |a_m - b_m|$ chips from the total pot, where $|x|$ denotes the absolute value of $x$.</p><p>To determine the size of the total pot, it is necessary to calculate the winners' total winnings for all games. Since there can be many cards in a deck and many players, you have been assigned to write a program that does all the necessary calculations.</p></div><div class="input-specification"><p>Each test consists of several test cases. The first line contains one integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n \cdot m \le 3\cdot 10^5$)&nbsp;— the number of cards in the deck and the count of numbers on the one card.</p><p>Each of the following $n$ lines of the test case set contains $m$ integers $c_{i,j}$ ($1 \le c_{i,j} \le 10^6$)&nbsp;— a description of the $i$-th card.</p><p>It is guaranteed that the total $n \cdot m$ in all tests does not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print one number&nbsp;— the total amount of winnings from all games.</p></div>

## Input

<p>Each test consists of several test cases. The first line contains one integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n \cdot m \le 3\cdot 10^5$)&nbsp;— the number of cards in the deck and the count of numbers on the one card.</p><p>Each of the following $n$ lines of the test case set contains $m$ integers $c_{i,j}$ ($1 \le c_{i,j} \le 10^6$)&nbsp;— a description of the $i$-th card.</p><p>It is guaranteed that the total $n \cdot m$ in all tests does not exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print one number&nbsp;— the total amount of winnings from all games.</p>





```input1|2,3,4,5,8,9,10,11,12
3
3 5
1 4 2 8 5
7 9 2 1 4
3 8 5 3 1
1 4
4 15 1 10
4 3
1 2 3
3 2 1
1 2 1
4 2 7
```




```output1
50
0
31
```



## Note

<p>Consider the first test case.</p><p>In the game between the first and second player, the winner receives $|1-7| + |4-9| + |2-2| + |8-1| + |5-4| = 19$ chips.</p><p>In the game between the first and third player, the winner receives $|1-3| + |4-8| + |2-5| + |8-3| + |5-1| = 18$ in chips.</p><p>In the game between the second and third player, the winner receives $|7-3| + |9-8| + |2-5| + |1-3| + |4-1| = 13$ chips.</p><p>The total is $19 + 18 + 13 = 50$ chips.</p>
