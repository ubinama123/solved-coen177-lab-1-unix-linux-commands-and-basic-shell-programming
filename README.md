Download Link: https://assignmentchef.com/product/solved-coen177-lab-1-unix-linux-commands-and-basic-shell-programming
<br>
<strong>Objectives</strong>

<h5>1.     To learn Unix/ Linux</h5>

<h5>2.     To use command – line programs</h5>

<h5>3.     To develop sample shell programs</h5>

<h5></h5>

<h5><strong>Guidelines</strong></h5>

<h5>Good knowledge in Unix/Linux based C programming is required for all labs. You are highly encouraged to use command line tools in developing, compiling, and running your programs. You may use editors like vi or gedit and gcc compiler. This lab is designed to teach you basics of the Linux technical environment, including tools, commands, and shell scripts.</h5>




<h5>Please pay attention to your coding style and good programming practices, if your program is not worth documenting, it probably isn’t worth running.<a href="#_ftn1" name="_ftnref1">[1]</a> Please follow the GNU coding standards available on: <a href="https://www.gnu.org/prep/standards/html_node/Writing-C.html">https://www.gnu.org/prep/standards/html_node/Writing-C.html</a>.</h5>




<h5><strong>Unix</strong><strong>/ Linux</strong></h5>

<h5>Linux is a Unix-like operating system, following the design principles of Unix monolithic kernel in process control, cpu scheduling, memory management, file systems, networking, and access to the peripherals. Please read details on <a href="https://en.wikipedia.org/wiki/Linux">https://en.wikipedia.org/wiki/Linux</a>.Unix/ Linux has a culture of distinctive art and powerful design philosophy since its inception in 1969. Software technologies come and go but Unix/ Linux remained dominant and continued to evolve on a wide variety of machines ranging from supercomputers and PCs to handheld devices and embedded networking hardware.  C language is ubiquitous and a central technology of Unix/ Linux. It is very hard to imagine developing applications at the core system level without C. The POSIX, Portable Operating System Standard, the Unix API (Application Programming Interface) is used to write truly portable software that can run across a heterogeneous mix of computers. TCP/IP (which you will learn in this class) and Unix represent the core technologies of the Internet. For more details, see <a href="#_ftn2" name="_ftnref2">[2]</a>.</h5>

<h5></h5>

<h5>Please install Linux on your laptop computer, either as a bare operating system or as a virtual machine. For details, please check https://www.linux.com. If you are using Mac OS, you can use Linux commands in a terminal window, including vi and gcc compiler.</h5>




<strong>Command-line programs (utilities)</strong>

<h5>The use of command-line programs is a tradition in UnixLinux. Commands are executable programs that can run with variety of arguments (options). Command-line options are single letters preceded by a single hyphen, including:</h5>

<h5>-a: all, -b: buffer, -c: command, -d: debug, -e: execute, -f: file, -l: list, -o: output, -u: user</h5>

<h5></h5>

Some of the basic commands are:




<ul>

 <li>ls: lists all files and directories (try with options: -a, -al)</li>

 <li>cat: displays file content (try cat file1 file2 &gt; file3)</li>

 <li>mv: moves a file to a new location (try mv file1 file2)</li>

 <li>rm: deletes a file</li>

 <li>cp: copy file</li>

 <li>cmp: compares two files</li>

 <li>man: gives help information on a command</li>

 <li>history: gives a list of past commands</li>

 <li>clear: clear the terminal</li>

 <li>mkdir: creates a new directory</li>

 <li>cd: changes directory</li>

 <li>rmdir: deletes a directory</li>

 <li>chmod: changes the access mode of the specified files to the specified mode</li>

 <li>chown: changes the owner of the specified files to the specified userid</li>

 <li>echo: writes arguments to the standard output (try echo ‘Hello World’ &gt; myfile)</li>

 <li>df: shows disk usage</li>

 <li>apt -get: install and update packages</li>

 <li>mail -s ‘subject’ -c ‘cc-address’ -b ‘bcc-address’ ‘to-address’ &lt; filename: sends email with attachment</li>

 <li>chown/ chmod: change ownership/ permission of file or directory</li>

 <li>date: show the current date and time</li>

 <li>ps: displays active processes</li>

 <li>kill: kills process</li>

 <li>sh: bourne shell – command interpreter (good to learn about shell programming)</li>

 <li>grep: searches for pattern in files</li>

 <li>Ctrl+c: halts current command</li>

 <li>Ctrl+z: stops current command and resumes with foreground</li>

 <li>Ctrl+d (exit): logout of current session</li>

 <li>man: displays the manual page of the specified command</li>

 <li>echo: prints on the screen</li>

</ul>

For more commands, please refer to Linux command quick reference<a href="#_ftn3" name="_ftnref3">[3]</a>.




<strong>Shell programming (aka scripting)</strong>

A shell program (aka script) is a text file (typically has .sh extension, but not required) that contains standard Unix and shell commands. It allows you to execute a series of commands in a shell program simply by running the shell program rather than typing all commands. Shell programs are interpreted not compiled. They are used to automate system administration tasks. In a shell program, you can use

<ol>

 <li>comments,</li>

 <li>variables,</li>

 <li>conditional commands,</li>

 <li>repeated actions of commands, and</li>

 <li></li>

</ol>




Bourne Shell (bsh or sh) is used for this lab. Other Shells are C-Shell – csh, Korn Shell, Born Again Shell – BASH, Thomas C-Shell – tcsh.




<ol>

 <li>Comments: Use the # character to signify comments. Anything after a # character until the end of the line is considered a comment and is ignored by the shell.</li>

</ol>




<ol start="2">

 <li>Variables: Use letters, numbers, and the underscore to define variable names is a shell program. The assigned values to variables are stored internally as strings. To use a variable, precede the name with $. The shell provides the following pre-defined shell variables that may be used to pass parameters to a shell script.</li>

</ol>

$0                     the name of the shell program$1 thru$9          the first thru to ninth parameters$#                     the number of parameters$*                     all parameters passed represented as a single word with individual parameters separated<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="321672">[email protected]</a>                   all the parameters passed with each parameter as a separate word

$?                     hold the exit status of the previous command$$                     the process id of the current process

PATH               the value of the PATH environment variable

HOME              the full path name of your home directory

USER               your user name

PWD                the current directory path




<ol start="3">

 <li>Conditional commands: Use if keyword for a conditional statement in either of the following arrangements:</li>

</ol>

if expression

then

command-list

fi




if expression

then

command-list

elsif expression

command-list2

fi




if expression

then

command-list1

else

command-list2

fi




case keyword can also be used to execute one of several lists of statements depending on the value of a variable.




Expressions (Boolean):

<ul>

 <li>Relational operators:</li>

</ul>

-eq, -ne, -gt, -ge, -lt, -le

<ul>

 <li>File operators:</li>

</ul>

-f <em>file</em>     True if <em>file</em> exists and is not a directory

-d <em>file</em>    True if <em>file</em> exists and <em>is</em> a directory

-s <em>file</em>    True if <em>file</em> exists and has a size &gt; 0

<ul>

 <li>String operators:</li>

</ul>

-z <em>string</em>             True if the length of <em>string</em> is zero

-n <em>string</em>            True if the length of <em>string</em> is nonzero

<em>s1 </em>= <em>s2</em>             True if <em>s1</em> and <em>s2</em> are the same

<em>s1 </em>!= <em>s2</em>             True if <em>s1</em> and <em>s2</em> are different

<em>s1         </em>            True if <em>s1</em> is not the null string

<ul>

 <li>Compound comparison:</li>

</ul>

-a                     And

-o                     Or

!                       Not




The other type of conditional command supported by the shell is the case command. The case command allows the user to compare a single value against multiple values and when a match is found execute the associated command list.




<ol start="4">

 <li>Repeated actions of commands: The Bourne shell provides three repeated action commands: for, while, and until as follows:</li>

</ol>

for variable in word1 word2 word3 … wordn

do

command-list

done




while command

do

command-list

done




until command

do

command-list

done







<ol start="5">

 <li>Functions: shell functions are generally defined in a file as:</li>

</ol>

name () {                                                               add (){

commands;              e.g.                      echo $[$1 + $2]

}                                                                              }







Important notes:

<ul>

 <li>Shell programming is not good in numerical computation, but use can still use some mathematical expressions by using the keyword expr, e.g. i=‘expr $i+1’ or you may close expressions in brackets, e.g. i=$[i+1]</li>

 <li>Use #!/bin/sh as the first line of a shell program to define the path of the command interpreter.</li>

 <li>Use chmod +x &lt;program_name&gt; to make a shell program executable, then run either using sh &lt;program_name&gt;, or ./&lt;program_name&gt;</li>

 <li>Shell metacharacters are:</li>

</ul>

‘…’    takes without interpreting contents

“…”   takes after processing $, `…` and 

       escape, for example c takes character c

`…`   runs enclosed command and replace with output







<strong>Sample shell program</strong>

Demonstrate each of the following steps to the TA to get a grade on this part of the lab assignment

<ul>

 <li>Write the following shell program using vi, emacs, or an editor of your choice</li>

</ul>

#Sample shell programs for Lab assignment

#!/bin/sh

echo Executing $0

echo $(/bin/ls | wc -l) files

wc -l $(/bin/ls)

echo “HOME=”$HOME

echo “USER=”$USER

echo “PATH=”$PATH

echo “PWD=”$PWD

echo “$$”=$$

user=`whoami`

numusers=`who | wc -l`

echo “Hi $user! There are $numusers users logged on.”

if [ $user = “salagtash” ]

then

echo “Now you can proceed!”

else

echo “Check who logged in!”

exit 1

fi




response=”Yes”

while [ $response != “No” ]

do

echo “Enter height of rectangle: ”

read height

echo “Enter width of rectangle: ”

read width

area=`expr $height * $width`

echo “The area of the rectangle is $area”




echo “Would you like to repeat for another rectangle [Yes/No]?”

read response




done







<ul>

 <li>Run the shell program by typing sh &lt;YourProgram.sh&gt;. When it runs without errors or warnings, write down your observations in detail and make a copy of the source file.</li>

</ul>




<ul>

 <li>Rewrite the program in Step 1. so that you compute also the area of a circle, then demonstrate steps 1 – 3 to the TA.</li>

</ul>




When your program runs without errors or warnings, make a copy of the source file

<a href="#_ftnref1" name="_ftn1">[1]</a> Jonathan Nagler, “Coding Style and Good Computing Practices”, <em>PS: Political Science and Politics</em>, Volume 28, Issue 3, 1995, pp. 488-492.

<a href="#_ftnref2" name="_ftn2">[2]</a> Eric S. Raymond, <em>The Art of Unix Programming</em>, Pearson, 2004

<a href="#_ftnref3" name="_ftn3">[3]</a> https://www.oreilly.com/openbook/debian/book/appe_01.html