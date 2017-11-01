### TerminalWorkshop 
### http://bit.ly/BugsTerminal
### cd ~/Desktop
### $ git clone https://github.com/BUGS-NYU/TerminalWorkshop

Hey, could you help me with some things? Nadira gave me these simple computer tasks to do but I’m terrible with computers. I had Joanna write up this up for me because I don’t even know how to do that. I could really use your help with these tasks. Thanks a lot! 
- David (written by Joanna)
____________________
____________________
### 0. whoami, pwd, ls, cd, man

First find out who and where you are…

$ whoami
$ pwd
$ ls
$ ls -F
$ ls -F -a OR $ ls -Fa
$ ls -l -h OR $ ls -lh
$ man ls

Navigate to the TerminalWorkshop folder.

$ cd directory
$ cd ..
____________________
____________________
### 1. cat, head, tail, nano, touch, rm

Read my jokes in the 'joke.txt' file! I think they’re funny.
Can you add one more joke to the text file 'jokes.txt' please?

$ cat jokes.txt
$ head jokes.txt
$ head -15 jokes.txt
$ tail -5 jokes.txt
$ nano jokes.txt
	Exit nano with Control+X (control is also known as Ctrl or ^, so ^X), y, then Enter

We also need a new text file named “report_” and your name, like “report_nadiradewji.txt”.
Write your NYU email inside and delete the similar file that already exists.

$ touch report_name.txt OR $ nano report_name.txt
$ rm report_nadiradewji.txt
____________________
____________________
### 2. mkdir, mv, rm, cp

Create a new folder called ‘publish’, pick three images from the ‘sort’ folder, and move them into the ‘publish’ folder so we can publish our latest funny pictures on our website.

$ mkdir publish
$ mv sort/comic_triumphant.jpg publish

Go to the ‘delete’ directory and delete any pictures that have titles suggesting they don’t work. Don’t delete any text files, they could be important for someone else! Let’s copy any text files to the folder ‘data’ just in case. I heard Ana was looking for a file named ‘important_do_not_delete.txt’, if you find it she wants it renamed ‘numbers.txt’.

$ rm -r -i delete
$ cp delete/animals.txt data
$ mv important_do_not_delete.txt numbers.txt
____________________
____________________
### 3. wild card regular expressions, >, wc, diff, |

Can you make two new folders, ‘memes’ and ‘comics’, and sort the rest of the images in the ‘sort’ directory appropriately.

$ mkdir memes
$ mv sort/meme*.jpg memes

We want to post the first joke from the jokes.txt text file onto our website. Can you make a text file with that first joke, call it ‘first_joke.txt’, and save it in the ‘publish’ directory?

$ head -3 jokes.txt > first_joke.txt
$ mv first_joke.txt publish

Go to the ‘data’ directory and tell me how many amino acids there are, I’m supposed to start learning this for Biochemistry D: yikes! Then save the word count information to a file called ‘lengths.txt’, Ana wants to make sure her research data is all there. She’d like it sorted as well.

$ wc amino-acids.txt
$ wc *.txt
$ wc -w *.txt > lengths.txt
$ sort lengths.txt
$ sort -n lengths.txt | head -n 1
$ wc -w *.txt | sort -n
$ wc -w *.txt | sort -n | head -n 1

Ana ran an experiment two months apart, the data she got is shown in the text files ’09-10-2017.txt’ and ’10-10-2017.txt’. She wants to know if she got the same data each time otherwise there may be a problem she’ll have to check.

$ diff 09-10-2017.txt 10-10-2017.txt
____________________
____________________
### 4. .sh, python, javac, java

Nadira asked me to write some computer thingy? A program or something, that lets us see only the third joke from the ‘jokes.txt’ text file? Well I know the third joke is on lines 8 and 9. Can you help?

$ nano third_joke.sh
	head -n 9 jokes.txt | tail -n 2

Nadira asked me to run her Intro to Programming homework written in python from the file ‘poem.py’ and another homework written in java from the file ‘poem.java’.

$ python poem.py
$ javac poem.java
$ java poem
____________________
____________________
### 5. git

We want to know who helped us complete these tasks! Is there a way you can let us know with your name and email?

$ git add report_name.txt
$ git commit -m “I contributed!”
$ git push
____________________
____________________
More learning: https://swcarpentry.github.io/shell-novice/
Decipher confusing command lines: https://explainshell.com/
