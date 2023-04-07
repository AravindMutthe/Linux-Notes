# Internal vs External commands:

- Internal cmds are directly executed by the shell. No separate process is there to run these commands.
- External cmds are executed by the kernel. Each command has its unique process id.

*UNIX commands are classified into two types*
1. Internal Commands - Ex: cd, source, fg
2. External Commands - Ex: ls, cat

## Internal Commands
- Internal commands are something which is built into the shell
- For the shell built in commands, the execution speed is really high
- It is because no process needs to be born for executing it:
- in the sense that the shell doesn’t have to search the given path for them in the PATH variable, and also no process needs to be spawned for executing it.
*For example, when using the "cd" command*
- To get the list of Internal commands?
**Note**You can get only if you are in bash shell. Bash shell has a command called "help" which will list out all the built-in shell commands.

## External Commands:
- External commands are not built into the shell.
- These are executables present in a separate file. 
- When an external command has to be executed, a new process has to be spawned(born) and the command gets executed.
- When an external command has to be executed, the shell looks for its path given in the PATH variable, 
- and also a new process has to be spawned and the command gets executed. They are usually located in /bin or /usr/bin.
*For example, when you execute the "cat" command*
- which usually is at /usr/bin, the executable /usr/bin/cat gets executed.


## internal vs external

1. Internal commands are commands that are already loaded in the system
2. They can be executed any time and are independent.
3. Internal commands don’t require a separate process to execute them.
4. Internal commands are a part of the shell.while external commands require a Path

- If the path files for the command are not present in the path, the external command won’t execute.
- external commands are loaded when the user requests for them.
- External commands will have an individual process.
- External commands are those command which are stored as a separate binaries.
- Shell starts separate sub-process to execute them.
- Most external commands are stored in the form of binaries in /bin directory.
- To execute external command shell check $PATH variable . 
- If command present in the location mentioned in $PATH variable shell will execute it , otherwise it will give error.


#### 1. How to find out whether a command is internal or external?
type command:
$ type cd
cd is a shell builtin
$ type cat
cat is /bin/cat
- For the internal commands, the type command will clearly say its shell built-in, 
- however for the external commands, it gives the path of the command from where it is executed.

## 2. DIFFERENCE
- The big difference in internal vs external command is 'performance' 
- Internal command are much much faster compared to external for the simple reason that no process needs to be spawned for an internal command since it is all built-into the shell. 
- So, as the size of a script gets bigger, using external commands a lot does adds to its performance.

## 3. WHEN TO CHOOSE:
-  Not always we get a choice to choose an internal over an external command.
- However, a careful look at our scripting practices, we might find quite a few places where we can avoid external commands.
- Eg: Say to add 2 numbers say x & y:
1. 	z=`expr $x+$y`
2. 	let z=x+y
- let is a shell built-in command, whereas expr is an external command.
- Using expr will be slower.