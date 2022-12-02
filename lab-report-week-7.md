# Part 1 from Vim
*Add a new line to print before File[] paths = f.listfiles()*

Using the shortest sequence of commands:
```
/toString
^ //To reach File[] path, around 3 key presses
shift a
enter //to create blank space above
System.out.println(f.toString() + "is a directory");
esc
:x
```
Effectively, this took me around 1 minute to do. While I'm sure there are better shortcuts, such as /f.listFiles(), I felt the most comfortable and fastest with this method.

To double check my code stayed, I re-typed vim DocSearchServer.java.

![Image](DocSearchServer%20tostring.PNG)