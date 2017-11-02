# Welcome to our Terminal Workshop 
### Learn a little history here: https://bit.ly/BugsTerminal
### Begin this by opening your Terminal application for Mac and Linux users or download Git Bash for windows users
We use the dollar sign $ to indicate this is the start of a command line. 
The term "directory" is synonymous with "folder".

- [ ] Type each of the commands below into your Terminal application and click Enter each time
	```
	$ cd ~/Desktop
	$ git clone https://github.com/BUGS-NYU/TerminalWorkshop
	```
____________________
____________________

Hey, could you help me with some things? Nadira gave me these simple computer tasks to do but I’m terrible with computers. I had Joanna write this up for me because I don’t even know how to do that. I could really use your help with these tasks. Thanks a lot! 
- David (written by Joanna)
____________________
____________________
### 0. whoami, pwd, ls, cd, man

- [ ] First find out who and where you are…

	```
	This command tells you which account on your computer you are using.
	$ whoami
	This command tells you what folder you are currently located in. It stands for 'print working directory'.
	$ pwd
	This command lists all files and folders in the current folder you are in.
	$ ls
	You can change a command by adding what we call a Flag to it like below. For the list command -F puts a slash after every folder when it lists everything.
	$ ls -F
	$ ls -F -a 
		OR 
		$ ls -Fa
	$ ls -l -h 
		OR 
		$ ls -lh
	The 'man' command means manual and only works on Mac and Linux computers. Windows computers use the command 'help'. It tells you what any command you use it on does, and all the flags you can use with them and their functions
	$ man ls
	```

- [ ] Navigate to the TerminalWorkshop folder.

	```
	This command lets you go into a directory you specify. Replace 'directory' with an actual folder name that exists in your current location.
	$ cd directory
	This command below lets you step back one directory.
	$ cd ..
	```
- [ ] Nadira told me about these shortcuts, you should try them out.

	```
	You can get your last command by click the up keyboard button.
	You can auto-complete a filename or directory name if it's unique by using tab.
	$ history
	$ !your_number
	$ clear
	With your volume on do this command below.
	$ say "hello"
	```
____________________
____________________
### 1. cat, head, tail, nano, touch, rm

- [ ] Read my jokes in the 'jokes.txt' file! I think they're funny.
Can you add one more joke to the text file 'jokes.txt' please?

	```
	$ cat jokes.txt
	$ head jokes.txt
	$ head -15 jokes.txt
	$ tail -5 jokes.txt
	For Mac and Linux users you can use the 'nano' command, which opens a simple text editor, like a Microsoft Word but even more simple. Windows, Mac, and Linux users can use 'vi' or 'vim', which are other text editors.
	$ nano jokes.txt
		OR $ vi jokes.txt
		OR $ vim jokes.txt
	Exit nano with Control+X (control is also known as Ctrl or ^, so ^X), y, then Enter.
	Edit text in 'vi' or 'vim' by going into 'INSERT' mode by clicking 'i'. Then exit by clicking Escape, then ':x'.
	```

- [ ] We also need a new text file named "report_" and your name, like "report_nadiradewji.txt". Then delete the similar file that already exists.

	```
	$ touch report_name.txt 
	$ rm report_nadiradewji.txt
	Use the remove command carefully because there's no way to get back what you removed. You'll learn below how to delete in a more safe way.
	```
____________________
____________________
### 2. mkdir, mv, rm, cp

- [ ] Create a new folder called 'publish', pick three images from the 'sort' folder, and move them into the 'publish' folder so we can publish our latest funny pictures on our website.

	```
	$ mkdir publish
	For move you first tell the computer where the file is in relation to you and its name, then separate by a space you tell the computer where you want to put it. Below our file is located in the 'sort/' directory and is called 'comic_triumphant.jpg', then we're telling it to move it to the directory 'publish'. 
	$ mv sort/comic_triumphant.jpg publish
	```

- [ ] Go to the 'delete' directory and delete any pictures that have titles suggesting they don’t work. Don’t delete any text files, they could be important for someone else! Let's copy any text files to the folder 'data' just in case. I heard Ana was looking for a file named 'important_do_not_delete.txt', if you find it she wants it renamed 'numbers.txt'.

	```
	$ rm -r -i delete
	$ cp delete/animals.txt data
	The mv command lets you rename files or move them elsewhere.
	$ mv important_do_not_delete.txt numbers.txt
	```
____________________
____________________
### 3. wild card regular expressions, >, wc, diff, |

- [ ] Can you make two new folders, 'memes' and 'comics', and sort the rest of the images in the 'sort' directory appropriately?

	```
	$ mkdir memes
	Asterisk * works like a wild card, it says there can by any amount of any character here. So below 'meme*.jpg' means the files must start with 'meme', end with '.jpg', and can have any characters in between.
	$ mv sort/meme*.jpg memes
	```

- [ ] We want to post the first joke from the jokes.txt text file onto our website. Can you make a text file with that first joke, call it 'first_joke.txt', and save it in the 'publish' directory? Navigate to the 'TerminalWorkshop' directory and try.

	```
	We can redirect the output of a command so it goes into a text file instead of onto the screen.
	$ head -3 jokes.txt > first_joke.txt
	$ mv first_joke.txt publish
	```

- [ ] Go to the 'data' directory and tell me how many amino acids there are, I'm supposed to start learning this for Biochemistry D: yikes! Then save the word count information to a file called 'lengths.txt', Ana wants to make sure her research data is all there. She’d like it sorted as well.

	```
	$ wc amino-acids.txt
	$ wc *.txt
	$ wc -w *.txt > lengths.txt
	$ sort lengths.txt
	We can have one command pass along its output to another command using what we call Pipes.
	$ sort -n lengths.txt | head -n 1
	$ wc -w *.txt | sort -n
	$ wc -w *.txt | sort -n | head -n 1
	```

- [ ] Ana ran a couple experiments two months apart, the data she got is shown in the text files '09-10-2017.txt' and '10-10-2017.txt'. She wants to know if she got the same data each time otherwise there may be a problem she’ll have to check.

	```
	$ diff 09-10-2017.txt 10-10-2017.txt
	```
____________________
____________________
### 4. .sh, python, javac, java

- [ ] Nadira asked me to write some computer thingy? A program or something, that lets us see only the third joke from the 'jokes.txt' text file? Well I know the third joke is on lines 8 and 9. Can you help? Navigate to the 'TerminalWorkshop' directory and try.

	```
	$ nano third_joke.sh
	Inside nano type the follow line.
		head -n 9 jokes.txt | tail -n 2
	Then exit nano and run the next line.
	$ bash third_joke.sh
	```

- [ ] Nadira asked me to run her Intro to Programming homework written in python from the file 'poem.py' and another homework written in java from the file 'poem.java'. They're located in the 'code' directory.

	```
	$ python poem.py
	$ javac poem.java
	$ java poem
	```
____________________
____________________
### 5. git

- [ ] We want to know who helped us complete these tasks! Is there a way you can let us know with your name and email? Nagivate to the 'TerminalWorkshop' directory and try.

	```
	$ git add report_name.txt
	$ git commit -m "I contributed!"
	$ git push
	```
____________________
____________________
More learning: https://swcarpentry.github.io/shell-novice/
Decipher confusing command lines: https://explainshell.com/
