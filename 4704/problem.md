## Description

<div><p>It is the year 2969. 1000 years have passed from the moon landing. Meanwhile, the humanity colonized the Hyperspace™ and lived in harmony.</p><p>Until we realized that we were not alone.</p><p>Not too far away from the Earth, the massive fleet of aliens' spaceships is preparing to attack the Earth. For the first time in a while, the humanity is in real danger. Crisis and panic are everywhere. The scientists from all around the solar system have met and discussed the possible solutions. However, no progress has been made.</p><p>The Earth's last hope is YOU!</p><p>Fortunately, the Earth is equipped with very powerful defense systems made by MDCS. There are $N$ aliens' spaceships which form the line. The defense system consists of three types of weapons: </p><ul> <li> SQL rockets – every SQL rocket can destroy at most one spaceship in the given set.</li><li> Cognition beams – every Cognition beam has an interval $[l,r]$ and can destroy at most one spaceship in that interval.</li><li> OMG bazooka – every OMG bazooka has three possible targets, however, each bazooka can destroy either zero or exactly two spaceships. In addition, due to the smart targeting system, the sets of the three possible targets of any two different OMG bazookas are disjoint (that means that every ship is targeted with at most one OMG bazooka). </li></ul><p>Your task is to make a plan of the attack which will destroy the largest possible number of spaceships. Every destroyed spaceship should be destroyed with exactly one weapon.</p></div><div class="input-specification"><p>The first line contains two integers: the number of your weapons $N$ $(1\leq N\leq 5000)$ and the number of spaceships $M$ $(1\leq M\leq 5000)$.</p><p>In the next $N$ lines, each line starts with one integer that represents type (either 0, 1 or 2). If the type is 0, then the weapon is SQL rocket, the rest of the line contains strictly positive number $K$ $(\sum{K} \leq 100 000)$ and array $k_i$ $(1\leq k_i\leq M)$ of $K$ integers. If the type is 1, then the weapon is Cognition beam, the rest of the line contains integers $l$ and $r$ $(1\leq l\leq r\leq M)$. If the type is 2 then the weapon is OMG bazooka, the rest of the line contains distinct numbers $a$, $b$ and $c$ $ (1 \leq a,b,c \leq M)$.</p></div><div class="output-specification"><p>The first line should contain the maximum number of destroyed spaceships — $X$.</p><p>In the next $X$ lines, every line should contain two numbers $A$ and $B$, where $A$ is an index of the weapon and $B$ is an index of the spaceship which was destroyed by the weapon $A$.</p></div>

## Input

<p>The first line contains two integers: the number of your weapons $N$ $(1\leq N\leq 5000)$ and the number of spaceships $M$ $(1\leq M\leq 5000)$.</p><p>In the next $N$ lines, each line starts with one integer that represents type (either 0, 1 or 2). If the type is 0, then the weapon is SQL rocket, the rest of the line contains strictly positive number $K$ $(\sum{K} \leq 100 000)$ and array $k_i$ $(1\leq k_i\leq M)$ of $K$ integers. If the type is 1, then the weapon is Cognition beam, the rest of the line contains integers $l$ and $r$ $(1\leq l\leq r\leq M)$. If the type is 2 then the weapon is OMG bazooka, the rest of the line contains distinct numbers $a$, $b$ and $c$ $ (1 \leq a,b,c \leq M)$.</p>

## Output

<p>The first line should contain the maximum number of destroyed spaceships — $X$.</p><p>In the next $X$ lines, every line should contain two numbers $A$ and $B$, where $A$ is an index of the weapon and $B$ is an index of the spaceship which was destroyed by the weapon $A$.</p>





```input1
3 5
0 1 4
2 5 4 1
1 1 4

```




```output1
4
2 1
3 2
1 4
2 5

```



## Note

<p>SQL rocket can destroy only 4th spaceship. OMG Bazooka can destroy two of 1st, 4th or 5th spaceship, and Cognition beam can destroy any spaceship from the interval $[1,4]$. The maximum number of destroyed spaceship is 4, and one possible plan is that SQL rocket should destroy 4th spaceship, OMG bazooka should destroy 1st and 5th spaceship and Cognition beam should destroy 2nd spaceship.</p>
