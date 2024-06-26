During lecture and the lab, I 1have learned many simple filesystem commands such as pwd, which allows us to see the current working directory, cd, which allows us to change the current directory and ls, which lists out the contents of a directory. In Lab1, we had to use and show what each commands did and what output was produced.



#### 1. Share an example of using the command with no arguments.
##### cd:
Absolute path before command was ran: /workspaces/lecture1

This output was produced because changing the cd with no arguments just changes it to /home

This did not produce an error because ‘cd’ means to change the directory. Since there is no argument, it changed the directory to /home/codespace

![Image](cd1.png)
##### ls:
Absolute path before command was ran: /home/codespace

This output was produced because 'ls' lists the contents of what is inside of the working directory.

‘Ls’ did not produce an error because ‘ls’ just produces a list of the contents of the given path since there is no argument, it just list out the contents of the absolute path

![Image](ls1.png)
##### cat: 
Absolute path before command was ran: /home/codespace

This was the output because cat needs an argument of a file name in order to print out the contents of a certtain file.

I believe this produced an error because ‘cat’ means print the contents of one or more files given by the paths. Without an argument, there is nothing to produce.

![Image](cat1.png)

#### 2. Share an example of using the command with a path to a directory as an argument.
##### cd:
Absolute path before command was ran: /workspaces/lecture1

This was the output because ~ is the same as /home which is a directory and the working directory changed to ~

This does not produce an error because it changed the directory to ‘~’ which is the argument which is /home/codespace

![Image](cd2.png)
##### ls:

Absolute path before command was ran: /home/codespace

This is the output because ~ was an argument and it just lists out the contents within ~

This does not produce an error because it list out the content of the directory

![Image](ls2.png)

##### cat:
Absolute path before comand was ran: /home/codespace

I believe this output was produced because in the argument, it looked for a file called /home however it is a directory not a file.

This produced an error because '/home' is a directory not a file and therefore cannot list the contents inside.

![Image](cat2.png)

#### 3. Share an example of using the command with a path to a file as an argument.
##### cd:
Absolute Path before command was ran:/home/codespace

This output was produced because as the argument 'lecture1' it concatanated '~' with lecture1 and changed its directory to that.

This did not produce an error because it changed the directory to ~/lecture1’

![Image](cd3.png)
##### ls:

Absolute path before command was ran: /home/codespace/lecture1

This output was produced because in the argument, it is looking for lecture1 inside of lecture1 however lecture1 does not exist.

This resulted in an error because in the directory ‘/home/codespace/lecture1’ there is no file called lecture1 in lecture1

![Image](ls3.png)
##### cat:
Absolute path before command was ran: /home/codespace/lecture1

This output was produced because it is looking at the contents inside lecture1 however lecture1 does not exist inside lectire1.

This resulted in an error because in the directory ‘/home/codespace/lecture1’ there is no lecture1 and therefore cannot list out the contents that is within ‘lecture1’

![Image](cat3.png)
