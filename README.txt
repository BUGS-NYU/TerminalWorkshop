### TerminalWorkshop 
### http://bit.ly/BugsTerminal
### cd ~/Desktop
### $ git clone https://github.com/BUGS-NYU/TerminalWorkshop

Hey, could you help me with some things? Nadira gave me these simple computer tasks to do but I’m terrible with computers. I had Ana write up this up for me because I don’t even know how to do that. I could really use your help with these tasks. Thanks a lot! 
- David (written by Ana)
____________________
0: First find out who and where you are…

$ whoami
$ pwd
$ ls
$ ls -F
$ ls -F -a OR $ ls -Fa
$ ls -l -h OR $ ls -lh

Navigate to the TerminalWorkshop folder.

$ cd directory
$ cd ..
____________________
____________________
1: Read my jokes in the joke.txt file! I think they’re funny.
Can you add one more joke to the text file jokes.txt please?

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
2: Create a new folder called ‘publish’, pick three images from the ‘sort’ folder, and move them into the ‘publish’ folder so we can publish our latest funny pictures on our website. Also make two new folders, ‘memes’ and ‘comics’, and sort the rest of the images appropriately.

$ mkdir publish
$ mv sort/comic_triumphant.jpg publish

Go to the ‘delete’ directory and delete any pictures that have titles suggesting they don’t work. Don’t delete any text files, they could be important for someone else! Let’s copy any text files to the folder ‘data’ just in case. I heard Ana was looking for a file named ‘important_do_not_delete.txt’, if you find it she wants it renamed ‘numbers.txt’.

$ rm -r -i delete
$ cp delete/animals.txt data
$ mv important_do_not_delete.txt numbers.txt
____________________
____________________
3: Can you make two new folders, ‘memes’ and ‘comics’, and sort the rest of the images in the ‘sort’ directory appropriately.

$ mkdir memes
$ mv sort/meme*.jpg memes

Go to the ‘data’ directory and tell me how many amino acids there are, I’m supposed to start learning this for Biochemistry D: yikes. Then save the word count information to a file called ‘lengths.txt’, Ana wants to make sure her research data is all there.

$ wc amino-acids.txt
$ wc *.txt
$ wc *.txt > lengths.txt

____________________
____________________
More learning: https://swcarpentry.github.io/shell-novice/
Decipher confusing command lines: https://explainshell.com/
