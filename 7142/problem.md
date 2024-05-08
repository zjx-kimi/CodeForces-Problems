## Description

<div><p>Little Vova studies programming in an elite school. Vova and his classmates are supposed to write <span class="tex-span"><i>n</i></span> progress tests, for each test they will get a mark from 1 to <span class="tex-span"><i>p</i></span>. Vova is very smart and he can write every test for any mark, but he doesn't want to stand out from the crowd too much. If the sum of his marks for all tests exceeds value <span class="tex-span"><i>x</i></span>, then his classmates notice how smart he is and start distracting him asking to let them copy his homework. And if the median of his marks will be lower than <span class="tex-span"><i>y</i></span> points <span class="tex-font-style-it">(the definition of a median is given in the notes)</span>, then his mom will decide that he gets too many bad marks and forbid him to play computer games.</p><p>Vova has already wrote <span class="tex-span"><i>k</i></span> tests and got marks <span class="tex-span"><i>a</i><sub class="lower-index">1</sub>, ..., <i>a</i><sub class="lower-index"><i>k</i></sub></span>. He doesn't want to get into the first or the second situation described above and now he needs to determine which marks he needs to get for the remaining tests. Help him do that.</p></div><div class="input-specification"><p>The first line contains 5 space-separated integers: <span class="tex-span"><i>n</i></span>, <span class="tex-span"><i>k</i></span>, <span class="tex-span"><i>p</i></span>, <span class="tex-span"><i>x</i></span> and <span class="tex-span"><i>y</i></span> (<span class="tex-span">1 ≤ <i>n</i> ≤ 999</span>, <span class="tex-span"><i>n</i></span> is odd, <span class="tex-span">0 ≤ <i>k</i> &lt; <i>n</i></span>, <span class="tex-span">1 ≤ <i>p</i> ≤ 1000</span>, <span class="tex-span"><i>n</i> ≤ <i>x</i> ≤ <i>n</i>·<i>p</i></span>, <span class="tex-span">1 ≤ <i>y</i> ≤ <i>p</i></span>). Here <span class="tex-span"><i>n</i></span> is the number of tests that Vova is planned to write, <span class="tex-span"><i>k</i></span> is the number of tests he has already written, <span class="tex-span"><i>p</i></span> is the maximum possible mark for a test, <span class="tex-span"><i>x</i></span> is the maximum total number of points so that the classmates don't yet disturb Vova, <span class="tex-span"><i>y</i></span> is the minimum median point so that mom still lets him play computer games.</p><p>The second line contains <span class="tex-span"><i>k</i></span> space-separated integers: <span class="tex-span"><i>a</i><sub class="lower-index">1</sub>, ..., <i>a</i><sub class="lower-index"><i>k</i></sub></span> (<span class="tex-span">1 ≤ <i>a</i><sub class="lower-index"><i>i</i></sub> ≤ <i>p</i></span>)&nbsp;— the marks that Vova got for the tests he has already written.</p></div><div class="output-specification"><p>If Vova cannot achieve the desired result, print "<span class="tex-font-style-tt">-1</span>".</p><p>Otherwise, print <span class="tex-span"><i>n</i> - <i>k</i></span> space-separated integers&nbsp;— the marks that Vova should get for the remaining tests. If there are multiple possible solutions, print any of them.</p></div>

## Input

<p>The first line contains 5 space-separated integers: <span class="tex-span"><i>n</i></span>, <span class="tex-span"><i>k</i></span>, <span class="tex-span"><i>p</i></span>, <span class="tex-span"><i>x</i></span> and <span class="tex-span"><i>y</i></span> (<span class="tex-span">1 ≤ <i>n</i> ≤ 999</span>, <span class="tex-span"><i>n</i></span> is odd, <span class="tex-span">0 ≤ <i>k</i> &lt; <i>n</i></span>, <span class="tex-span">1 ≤ <i>p</i> ≤ 1000</span>, <span class="tex-span"><i>n</i> ≤ <i>x</i> ≤ <i>n</i>·<i>p</i></span>, <span class="tex-span">1 ≤ <i>y</i> ≤ <i>p</i></span>). Here <span class="tex-span"><i>n</i></span> is the number of tests that Vova is planned to write, <span class="tex-span"><i>k</i></span> is the number of tests he has already written, <span class="tex-span"><i>p</i></span> is the maximum possible mark for a test, <span class="tex-span"><i>x</i></span> is the maximum total number of points so that the classmates don't yet disturb Vova, <span class="tex-span"><i>y</i></span> is the minimum median point so that mom still lets him play computer games.</p><p>The second line contains <span class="tex-span"><i>k</i></span> space-separated integers: <span class="tex-span"><i>a</i><sub class="lower-index">1</sub>, ..., <i>a</i><sub class="lower-index"><i>k</i></sub></span> (<span class="tex-span">1 ≤ <i>a</i><sub class="lower-index"><i>i</i></sub> ≤ <i>p</i></span>)&nbsp;— the marks that Vova got for the tests he has already written.</p>

## Output

<p>If Vova cannot achieve the desired result, print "<span class="tex-font-style-tt">-1</span>".</p><p>Otherwise, print <span class="tex-span"><i>n</i> - <i>k</i></span> space-separated integers&nbsp;— the marks that Vova should get for the remaining tests. If there are multiple possible solutions, print any of them.</p>





```input1
5 3 5 18 4
3 5 4

```




```input2
5 3 5 16 4
5 5 5

```




```output1
4 1

```




```output2
-1

```



## Note

<p>The median of sequence <span class="tex-span"><i>a</i><sub class="lower-index">1</sub></span>,&nbsp;...,&nbsp;<span class="tex-span"><i>a</i><sub class="lower-index"><i>n</i></sub></span> where <span class="tex-span"><i>n</i></span> is odd (in this problem <span class="tex-span"><i>n</i></span> is always odd) is the element staying on <span class="tex-span">(<i>n</i> + 1) / 2</span> position in the sorted list of <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span>.</p><p>In the first sample the sum of marks equals 3 + 5 + 4 + 4 + 1 = 17, what doesn't exceed 18, that means that Vova won't be disturbed by his classmates. And the median point of the sequence {1, 3, 4, 4, 5} equals to 4, that isn't less than 4, so his mom lets him play computer games.</p><p>Please note that you do not have to maximize the sum of marks or the median mark. Any of the answers: "<span class="tex-font-style-tt">4&nbsp;2</span>", "<span class="tex-font-style-tt">2&nbsp;4</span>", "<span class="tex-font-style-tt">5&nbsp;1</span>", "<span class="tex-font-style-tt">1&nbsp;5</span>", "<span class="tex-font-style-tt">4&nbsp;1</span>", "<span class="tex-font-style-tt">1&nbsp;4</span>" for the first test is correct.</p><p>In the second sample Vova got three '5' marks, so even if he gets two '1' marks, the sum of marks will be 17, that is more than the required value of 16. So, the answer to this test is "<span class="tex-font-style-tt">-1</span>".</p>
