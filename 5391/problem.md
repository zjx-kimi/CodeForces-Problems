## Description

<div><p>You have a robot in a two-dimensional labyrinth which consists of <span class="tex-span"><i>N</i> × <i>M</i></span> cells. Some pairs of cells adjacent by side are separated by a wall or a door. The labyrinth itself is separated from the outside with walls around it. Some labyrinth cells are the exits. In order to leave the labyrinth the robot should reach any exit. There are keys in some cells. Any key can open any door but after the door is opened the key stays in the lock. Thus every key can be used only once. There are no labyrinth cells that contain both a key and an exit. Also there can not be both a wall and a door between the pair of adjacent cells.</p><p>Your need to write a program in <span class="tex-span"><i>abc</i></span> language (see the language description below) that will lead the robot to one of the exits. Lets numerate the labyrinth rows from <span class="tex-span">0</span> to <span class="tex-span"><i>N</i> - 1</span> top to bottom and the columns – from <span class="tex-span">0</span> to <span class="tex-span"><i>M</i> - 1</span> left to right.</p><p>In <span class="tex-span"><i>abc</i></span> language the following primary commands are available:</p><ul> <li> <span class="tex-font-style-tt">move-DIR</span> – move to the adjacent cell in the <img align="middle" class="tex-formula" src="file://u9MqgSx6.png" style="max-width: 100.0%;max-height: 100.0%;"> direction. <span class="tex-span"><i>down</i></span> increases the number of the row by 1, <span class="tex-span"><i>right</i></span> increases the number of the column by 1. In case there’s a wall or a closed door in this direction, nothing’s happening. </li><li> <span class="tex-font-style-tt">open-DIR</span> – open the door between the current cell and the adjacent one in <span class="tex-span"><i>DIR</i></span> direction. In case there isn’t any door in this direction or it’s already been opened or the robot doesn’t have a key, nothing’s happening.</li><li> <span class="tex-font-style-tt">take</span> – take the key in the current cell. In case there isn’t any key or the robot has already picked it up, nothing’s happening. The robot is able to carry any number of keys.</li><li> <span class="tex-font-style-tt">terminate</span> – terminate the program. This command is not obligatory to use. In case it’s absent the command is added at the end of the program automatically. </li></ul><p>Also, there are the following control commands in <span class="tex-span"><i>abc</i></span> language: </p><ul> <li> <span class="tex-font-style-tt">for-N OPS end</span> – repeat the sequence of the <span class="tex-span"><i>OPS</i></span> commands <span class="tex-span"><i>N</i></span> times, <span class="tex-span">0 &lt; <i>N</i> ≤ 100000</span>. Each loop counter check counts as a command fulfilled by the robot. </li><li> <span class="tex-font-style-tt">if-ok  OPS1  else  OPS2  endif</span> – carries out the sequence of the <span class="tex-span"><i>OPS</i>1</span> commands, if the previous command of moving, taking the key or opening the door was successful, otherwise the sequence of the <span class="tex-span"><i>OPS</i>2</span> commands is being carried out. Should there be no previous command run, the sequence <span class="tex-span"><i>OPS</i>1</span> will be carried out. If-ok check counts as a command fulfilled by the robot. </li><li> <span class="tex-font-style-tt">break</span> – stops the current <span class="tex-span"><i>for</i></span> loop. </li><li> <span class="tex-font-style-tt">continue</span> – finishes the current <span class="tex-span"><i>for</i></span> loop iterations. </li></ul><p>Note that the control and the primary commands can be fit into each other arbitrarily.</p><p>The robot will fulfill your commands sequentially until it exits the labyrinth, or it runs out of the commands, or the <span class="tex-span"><i>terminate</i></span> command is run, or the quantity of the fulfilled commands exceeds the bound number <span class="tex-span">5·10<sup class="upper-index">6</sup></span>.</p><p>In <span class="tex-span"><i>abc</i></span> language each command is a separate word and should be separated from other commands with at least one space symbol.</p><p>You should write a program that prints the sequence of commands leading the robot out of the labyrinth. Of course, as you are a good programmer, you should optimize these sequence.</p><p>The number of the non-space symbols in the sequence should not exceed <span class="tex-span">10<sup class="upper-index">7</sup></span>. If you succeed in finding the way out of the labyrinth <span class="tex-span"><i>i</i></span> you’ll be granted the number of points equal to: </p><center class="tex-equation"><img align="middle" class="tex-formula" src="file://Vsxw6o8G.png" style="max-width: 100.0%;max-height: 100.0%;"></center> where: <ul> <li> <span class="tex-span"><i>W</i><sub class="lower-index"><i>i</i></sub></span> – labyrinth’s weight, some fixed constant. </li><li> <span class="tex-span"><i>G</i><sub class="lower-index"><i>i</i></sub></span> – number of robots moves. </li><li> <span class="tex-span"><i>O</i><sub class="lower-index"><i>i</i></sub></span> – number of fulfilled commands. Note that this number includes commands like <span class="tex-span"><i>take</i></span> executed in the cells with no key, as well as opening commands applied to the already opened doors. </li><li> <span class="tex-span"><i>L</i><sub class="lower-index"><i>i</i></sub></span> – sequence length in symbols, excluding space symbols and line breaks. </li><li> <span class="tex-span"><i>Q</i> = 10·<i>N</i>·<i>M</i></span>. </li></ul><p>In case your sequence doesn’t lead the robot to the exit you’ll be granted <span class="tex-span">0</span> points. Your programs result will be the sum of all <span class="tex-span"><i>S</i><sub class="lower-index"><i>i</i></sub></span>. You should maximize this total sum.</p><p>All labyrinths will be known and available to you. You can download the archive with labyrinths by any of the given links, password to extract files is <span class="tex-font-style-tt">aimtechiscool</span>:</p><ol> <li> <a href="https://drive.google.com/file/d/1dkIBfW_Gy6c3FJtXjMXZPMsGKRyn3pzp">https://drive.google.com/file/d/1dkIBfW_Gy6c3FJtXjMXZPMsGKRyn3pzp</a> </li><li> <a href="https://www.dropbox.com/s/77jrplnjgmviiwt/aimmaze.zip?dl=0">https://www.dropbox.com/s/77jrplnjgmviiwt/aimmaze.zip?dl=0</a> </li><li> <a href="https://yadi.sk/d/JNXDLeH63RzaCi">https://yadi.sk/d/JNXDLeH63RzaCi</a> </li></ol><p>In order to make local testing of your programs more convenient, the program calculating your results (checker) and the labyrinth visualizer will be available. This program is written in <span class="tex-span"><i>python</i>3</span> programming language, that’s why you’re going to need <span class="tex-span"><i>python</i>3</span> interpreter, as well as <span class="tex-span"><i>pillow</i></span> library, which you can install with the following command <span class="tex-font-style-tt">pip3 install pillow</span>. <span class="tex-span"><i>pip</i>3</span> is a utility program for <span class="tex-span"><i>python</i>3</span> package (library) installation. It will be installed automatically with the <span class="tex-span"><i>python</i>3</span> interpreter.</p><p>Example command to run checker and visualizer: <span class="tex-font-style-tt">python3 aimmaze.py maze.in robot.abc --image maze.png</span>. The checker can be run separately of visualization: <span class="tex-font-style-tt">python3 aimmaze.py maze.in robot.abc</span>. Flag <span class="tex-font-style-tt">--output-log</span> will let you see the information of robots each step: <span class="tex-font-style-tt">python3 aimmaze.py maze.in robot.abc --output-log</span>. Note <span class="tex-span"><i>python</i>3</span> can be installed as <span class="tex-span"><i>python</i></span> on your computer.</p><p>To adjust image settings, you can edit constants at the beginning of the program <span class="tex-span"><i>aimmaze</i>.<i>py</i></span>.</p></div><div class="input-specification"><p>The first line contains integers <span class="tex-span"><i>i</i>, &nbsp;<i>W</i>, &nbsp;<i>N</i>, &nbsp;<i>M</i>, &nbsp;<i>x</i><sub class="lower-index">0</sub>, &nbsp;<i>y</i><sub class="lower-index">0</sub>, &nbsp;<i>C</i>, &nbsp;<i>D</i>, &nbsp;<i>K</i>, &nbsp;<i>E</i></span>. </p><ul> <li> <span class="tex-span">1 ≤ <i>i</i> ≤ 14</span> – labyrinth’s number, which is needed for a checking program. </li><li> <span class="tex-span">1 ≤ <i>W</i> ≤ 10<sup class="upper-index">18</sup></span> – labyrinth’s weight, which is needed for a checking program. </li><li> <span class="tex-span">2 ≤ <i>N</i>, <i>M</i> ≤ 1000</span> – labyrinth’s height and width. </li><li> <span class="tex-span">0 ≤ <i>x</i><sub class="lower-index">0</sub> ≤ <i>N</i> - 1, &nbsp;0 ≤ <i>y</i><sub class="lower-index">0</sub> ≤ <i>M</i> - 1</span> – robot’s starting position <span class="tex-span">(<i>x</i><sub class="lower-index">0</sub>, <i>y</i><sub class="lower-index">0</sub>)</span>. </li><li> <span class="tex-span">0 ≤ <i>C</i> ≤ 2·<i>NM</i></span> – number of walls. </li><li> <span class="tex-span">0 ≤ <i>D</i> ≤ 10<sup class="upper-index">5</sup></span> – number of doors. </li><li> <span class="tex-span">0 ≤ <i>K</i> ≤ 10<sup class="upper-index">5</sup></span> – number of keys. </li><li> <span class="tex-span">1 ≤ <i>E</i> ≤ 1000</span> – number of exits. </li></ul><p>The <span class="tex-span"><i>x</i></span> coordinate corresponds to the row number, <span class="tex-span"><i>y</i></span> – to the column number. <span class="tex-span">(0, 0)</span> cell is located on the left-up corner, so that <span class="tex-span"><i>down</i></span> direction increases the <span class="tex-span"><i>x</i></span> coordinate, while <span class="tex-span"><i>right</i></span> direction increases the <span class="tex-span"><i>y</i></span> coordinate.</p><p>Each of the next <span class="tex-span"><i>C</i></span> lines contains <span class="tex-span">4</span> integers each <span class="tex-span"><i>x</i><sub class="lower-index">1</sub>, <i>y</i><sub class="lower-index">1</sub>, <i>x</i><sub class="lower-index">2</sub>, <i>y</i><sub class="lower-index">2</sub></span> – the coordinates of cells with a wall between them in a zero based indexing. It is guaranteed that <span class="tex-span">|<i>x</i><sub class="lower-index">1</sub> - <i>x</i><sub class="lower-index">2</sub>| + |<i>y</i><sub class="lower-index">1</sub> - <i>y</i><sub class="lower-index">2</sub>| = 1, &nbsp;0 ≤ <i>x</i><sub class="lower-index">1</sub>, <i>x</i><sub class="lower-index">2</sub> ≤ <i>N</i> - 1, &nbsp;0 ≤ <i>y</i><sub class="lower-index">1</sub>, <i>y</i><sub class="lower-index">2</sub> ≤ <i>M</i> - 1</span>. Also there are always walls around the labyrinth’s borders, which are not given in the labyrinths description.</p><p>Each of the next <span class="tex-span"><i>D</i></span> lines contains door description in the same format as walls description. It is guaranteed that doors and walls don’t overlap.</p><p>Each of the next <span class="tex-span"><i>K</i></span> rows contains a pair of integer which are the key coordinates in a zero based indexing.</p><p>Each of the next <span class="tex-span"><i>E</i></span> rows contains a pair of integer which are the exit coordinates in a zero based indexing.</p><p>It is guaranteed that the robots starting position as well as keys and exits are located in pairwise different cells.</p></div><div class="output-specification"><p>Print a program in <span class="tex-span"><i>abc</i></span> language which passes the given labyrinth. Commands have to be separated by at least one space symbol. You can use arbitrary formatting for the program.</p></div>

## Input

<p>The first line contains integers <span class="tex-span"><i>i</i>, &nbsp;<i>W</i>, &nbsp;<i>N</i>, &nbsp;<i>M</i>, &nbsp;<i>x</i><sub class="lower-index">0</sub>, &nbsp;<i>y</i><sub class="lower-index">0</sub>, &nbsp;<i>C</i>, &nbsp;<i>D</i>, &nbsp;<i>K</i>, &nbsp;<i>E</i></span>. </p><ul> <li> <span class="tex-span">1 ≤ <i>i</i> ≤ 14</span> – labyrinth’s number, which is needed for a checking program. </li><li> <span class="tex-span">1 ≤ <i>W</i> ≤ 10<sup class="upper-index">18</sup></span> – labyrinth’s weight, which is needed for a checking program. </li><li> <span class="tex-span">2 ≤ <i>N</i>, <i>M</i> ≤ 1000</span> – labyrinth’s height and width. </li><li> <span class="tex-span">0 ≤ <i>x</i><sub class="lower-index">0</sub> ≤ <i>N</i> - 1, &nbsp;0 ≤ <i>y</i><sub class="lower-index">0</sub> ≤ <i>M</i> - 1</span> – robot’s starting position <span class="tex-span">(<i>x</i><sub class="lower-index">0</sub>, <i>y</i><sub class="lower-index">0</sub>)</span>. </li><li> <span class="tex-span">0 ≤ <i>C</i> ≤ 2·<i>NM</i></span> – number of walls. </li><li> <span class="tex-span">0 ≤ <i>D</i> ≤ 10<sup class="upper-index">5</sup></span> – number of doors. </li><li> <span class="tex-span">0 ≤ <i>K</i> ≤ 10<sup class="upper-index">5</sup></span> – number of keys. </li><li> <span class="tex-span">1 ≤ <i>E</i> ≤ 1000</span> – number of exits. </li></ul><p>The <span class="tex-span"><i>x</i></span> coordinate corresponds to the row number, <span class="tex-span"><i>y</i></span> – to the column number. <span class="tex-span">(0, 0)</span> cell is located on the left-up corner, so that <span class="tex-span"><i>down</i></span> direction increases the <span class="tex-span"><i>x</i></span> coordinate, while <span class="tex-span"><i>right</i></span> direction increases the <span class="tex-span"><i>y</i></span> coordinate.</p><p>Each of the next <span class="tex-span"><i>C</i></span> lines contains <span class="tex-span">4</span> integers each <span class="tex-span"><i>x</i><sub class="lower-index">1</sub>, <i>y</i><sub class="lower-index">1</sub>, <i>x</i><sub class="lower-index">2</sub>, <i>y</i><sub class="lower-index">2</sub></span> – the coordinates of cells with a wall between them in a zero based indexing. It is guaranteed that <span class="tex-span">|<i>x</i><sub class="lower-index">1</sub> - <i>x</i><sub class="lower-index">2</sub>| + |<i>y</i><sub class="lower-index">1</sub> - <i>y</i><sub class="lower-index">2</sub>| = 1, &nbsp;0 ≤ <i>x</i><sub class="lower-index">1</sub>, <i>x</i><sub class="lower-index">2</sub> ≤ <i>N</i> - 1, &nbsp;0 ≤ <i>y</i><sub class="lower-index">1</sub>, <i>y</i><sub class="lower-index">2</sub> ≤ <i>M</i> - 1</span>. Also there are always walls around the labyrinth’s borders, which are not given in the labyrinths description.</p><p>Each of the next <span class="tex-span"><i>D</i></span> lines contains door description in the same format as walls description. It is guaranteed that doors and walls don’t overlap.</p><p>Each of the next <span class="tex-span"><i>K</i></span> rows contains a pair of integer which are the key coordinates in a zero based indexing.</p><p>Each of the next <span class="tex-span"><i>E</i></span> rows contains a pair of integer which are the exit coordinates in a zero based indexing.</p><p>It is guaranteed that the robots starting position as well as keys and exits are located in pairwise different cells.</p>

## Output

<p>Print a program in <span class="tex-span"><i>abc</i></span> language which passes the given labyrinth. Commands have to be separated by at least one space symbol. You can use arbitrary formatting for the program.</p>





```input1
1 1 30 30 1 1 1 1 1 1
1 1 1 2
2 2 2 3
1 4
9 0

```




```output1
for-1111
  take
  open-up
  open-left
  open-right
  open-down
  move-left
  if-ok
    for-11
      move-left
  take
  open-up
  open-left
  open-right
  open-down
    end
  else
    move-right
    if-ok
      for-11
        move-right
  take
  open-up
  open-left
  open-right
  open-down
      end
    else endif
  endif

  move-up
  if-ok
    for-11
      move-up
  take
  open-up
  open-left
  open-right
  open-down
    end
  else
    move-down
    if-ok
      for-11
        move-down
  take
  open-up
  open-left
  open-right
  open-down
      end
    else endif
  endif

end
```


