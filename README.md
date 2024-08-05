## Branches in git
Learning what branches are. I have tried before to understand it but it seemed too complicated. With [Steve's Griffith Video](https://www.youtube.com/watch?v=t4IbjqqW8x0&list=PLyuRouwmQCjmYaG21ijCw0KrFiFEG0Oh9&index=3), I think I am all good now.
For me, the steps were as easy as:
- create a new directory `mkdir learning_branches && cd learning_branches`
- create a readme file. Use any of the three options:
	- echo "learning git branches" >> README.md, or
	- `touch README.md`, open and it with vi/vim
	- straightaway open a vi/vim editor and write with `vim README.md`
All the three are great, depending on how good you are with shell/linux scripting commands. Make sure to use `i` for insert when you open vi/vim, and press `esc`, type `:wq` to exit it. `:wq` means literally to write and quit!
- To create a new branch, we use either:
	- `git branch [name]` which creates the branch but you remain logged in main/master branch
		- you can get into the above branch by using `git checkout [name]`
	- `git checkout -b [branchname]` which is a quick way to create and checkout to the new branch
- Use `git status` to see the changes in your directory, and `git branch -a` to see the branches in the working directory and the one with * is where you are currently checked in.
- To merge the changes in the other branches to the main/master, simply use `git merge [branchname]`

## Merging Conflicts 
*Credits to [Net-Ninja](https://www.youtube.com/watch?v=XX-Kct0PfFc)*
Conflicts do emerge if one file is edited on the master/main branch, and a branch concurrently. For instance, let's say there is person a editing [file-1.txt](file-1.txt) from the master/main, and another on test-1 branch, there would be conflicts when merging it.
For instance, edit and commit the changes on the file while both on master/main, and on the branch. You will get a similar response to the following if you try to merge it:
> Auto-merging file-1.txt
> CONFLICT (content): Merge conflict in file-1.txt
> Automatic merge failed; fix conflicts and then commit the result.

To fix it, simply go to the file delete the error messages as seen here:
![screenshot of the error message](/images/image_1.png)
to this:
![screenshot of the fixed error message](/images/image_2.png)
Then `git add .` the changes, do a `git commit`, which opens an vi/vim with tons of errors but just type `:wq` and click enter. Boom! The conflicts have been merged. 
That is it, we have gone through the basics of creating branches, merging them and dealing with any conflicts which may emerge. 

Thank you, and leave a star if impressed. You can email me @ bettkipkemoo@gmail.com
