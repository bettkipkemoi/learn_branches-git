Learning what branches are. I have tried before to understand it but it seemed too complicated. With [Steve's Griffith Video](https://www.youtube.com/watch?v=t4IbjqqW8x0&list=PLyuRouwmQCjmYaG21ijCw0KrFiFEG0Oh9&index=3), I think I am all good now.
For me, the steps were as easy as:
- create a new directory ```mkdir learning_branches && cd learning_branches```
- create a readme file. Use any of the three options:
	- echo "learning git branches" >> README.md, or
	- ```touch README.md```, open and it with vi/vim
	- straightaway open a vi/vim editor and write with ```vim README.md```
All the three are great, depending on how good you are with shell/linux scripting commands. Make sure to use ```i``` for insert when you open vi/vim, and press ```esc```, type ```:wq``` to exit it. ```:wq``` means literally to write and quit!
- To create a new branch, we use either:
	- ```git branch [name]``` which creates the branch but you remain logged in main/master branch
		- you can get into the above branch by using ```git checkout [name]```
	- ```git checkout -b [branchname]``` which is a quick way to create and checkout to the new branch
- Use ```git status``` to see the changes in your directory
