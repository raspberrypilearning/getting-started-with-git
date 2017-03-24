# Getting Started with Git

## What is Git?

Git is a version control system (VCS) for tracking changes to files and coordinating changes between multiple people who are all working on the same code base.

One way to think about Git, is to imagine a magical school bag. You can pull books out of your bag and do some work anytime you like. Once you've finished you homework, you can put the books back into your school bag, and the bag remembers what changes you made to all the books inside it.

What's even better is that this school bag can be sychronised with another magical school bag that lives in the clouds. Anytime you like, you can tell the bag to copy the contents of all the books to the sky-bag. If you lose your own school bag, you don't have to worry, as you can just get a new one and grab all the books and writing from the sky-bag.

That's not all though. All your friends at school also have magical school bags. They also keep their bags synchronised with the sky-bag. This means that you and your friends can all work on the homework together. If a friend has a better answer to a Science question than you do, you can copy their answer from the sky-bag to your book.

It gets better than that though. Your teacher also has a magical school bag. When she wants to check the homework, she just copies all the books from the sky-bag to her bag. She can then check through the answers from the whole class in one go. If she spots a mistake, she can write a comment in the margin of the book, and then all the magical bags from the whole class will have receive the comment. Only one person in the class needs to correct the mistake though, and then all of a sudden, every one in the class has the correct answer.

## Getting Git.

If you're working on a Raspberry Pi, then congratulations, Git is already installed by default in Raspbian. If you're using MacOS, then you can follow [this quick guide]() to installing git and then return here to learn how to use it. If you're on Windows, then we have a [special guide just for you here](). Lastly, if you're on Linux, and dont' have git installed, then you can just use your package manager to grab the software. Something like this should work:

```bash
sudo apt install git
```

## Setting up Git

You're going to be working in the terminal for the duration of this resource, so open it up by clicking on the icon on the Desktop, or by pressing `ctrl+alt+t` on your keyboard.

1. The first thing to do is to tell Git who you are. This is important, as Git can be used collaboratively by lots of people, so it needs to know who made changes to which files.

```bash
git config --global user.name "Harry Potter"
git config --global user.email "h.potter@hogworts.prof"
```

1. Next you need to tell Git which text editor you want to use. If you don't have any particularly strong feelings about text editors then you can just type:

```bash
git config --global core.editor nano
```

## Creating your first magic school bag

So you want to start a new project; maybe it's a special ultrasonic range finder for tracking flying objects in the air. You'll want a directory on your computer for all your files to sit in, so the first thing to do is to create the directory.

1. In the terminal you can use the `make directory` command to create a new directory.

```bash
mkdir snitch-sniffer
```

1. Now you want to go into that directory. You can used the `change directory` command to do this.

```bash
cd snitch-sniffer
```

1. Next you can create a file to that will tell anyone looking at the project, what it's all about. You can use any text editor to do this, but in this example `nano` is used to create a file called `README.md`. The `.md` extension stands for `markdown`, which is a markup language. [You can learn more about markdown here](https://daringfireball.net/projects/markdown/).


```bash
nano README.md
```

1. This should open up the file in the terminal. You can now give the file a title and a little explanation for what your project is all about.

```markdown
# The Golden Snitch Sniffer
This is a project that uses multiple long range ultrasonic sensors to find and track an object flying in three dimensional space and display the objects coordinates, speed and trajectory through a VR headset.
```

1. Pressing `ctrl`+`x` will cause a save prompt to appear. You can type `y` to save and then hit `enter` to close nano.

1. You file should have been created and now be sitting in your directory. You can type `ls` in the terminal to see a list of files.

```bash
ls
```

1. At the moment, the directory is just like any other directory on your system. You now need to make the magical school bag part. This is known as a `Git Repository`, and it takes the form a a hidden directory that keeps track of all the changes to the working directory. Type the following to create the repository, which from now on will just be called a *repo*.

```bash
git init
```

1. If you type `ls` again, nothing will appear to have changed. You can use `ls -a` though to see all the hidden files and directories.

```
ls -a
```

1. You should now see something like this in your teminal:

```bash
.  ..  .git  README.md
```

1. That `.git` directory is the *repo skeleton*. You can have a look inside it by typing the following.

```bash
ls -a .git
```

1. This should bring up something like:

```bash
branches  config  description  HEAD  hooks  info  objects  refs
```

1. You don't really need to worry about this directory at all now. Just know that it is there and that it is tracking all the changes to the parent directory **snitch-sniffer**. 

## Adding your books

1. So you now have the magic school bag part, but you haven't yet added anything to it. That `README.md` file hasn't been placed into the bag yet. You need to tell git that you want to add the `README.md` file to the repo. To do this you can simply type:

	```bash
	git add README.md
	```

	Sometime it's easier to just add everything to the repo though, rather than adding individual files. To do this you can type:

	```bash
	git add --all
	```

1. Now git knows it needs to keep track of all the changes that happen to the `README.md` file. You can have a look at the status of your repo at any time by typing

```bash
git status
```

You should see something like this

```bash
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   README.md
```

1. The above response is telling you that the `README.md` file has not yet been **comitted**. This means that although Git knows about the file, it doesn't yet have any of the file's contents stored. The simplest way to do a commit is by typing:

	```bash
	git commit -am 'add README.md`
	```

	This commits all changes you have made in the directory to the Git repo, and adds a message saying what you did. The message can be anything really, but it's best to keep it fairly short yet descriptive of what you changed.

## Adding more books and travelling in time.

1. Now that you have set up your repo, it's time to get on with the project. Here two new files have been created - `snitch-sniffer.py` and `quidditch-rules.json`. Typing `ls` reveals those files.

```bash
README.md  quidditch-rules.json  snitch-sniffer.py
```

1. The new files need adding to the git repo and then commiting.

```bash
git add --all
git commit -am 'add json rules and python program'
```

1. Then you carry on working on your code for a bit. Every time you make a significant change to the file, you can perform a new commit.

```bash
git commit -am 'finish find function`
```

1. Now imagine that you've made a horible mistake. You've been working for awhile and you've deleted your `find_snitch()` function, adn then performed a commit. With Git, it's easy to go back in time and restore an earlier version of any of your files. Let's first look at the commit history of the file.

```bash
git log snitch-sniffer.py
```

1. This produces something like this:

```bash
commit 12c4c693e95438ceadcf3f4fb39c83ce1ade712f
Author: Harry Potter <h.potter@hogwarts.prog>
Date:   Fri Mar 3 20:27:17 2017 +0000

    delete find function

commit 5fd772a292c019a7cf3012b1156685280d4a7d2d
Author: Harry Potter <h.potter@hogwarts.prog>
Date:   Fri Mar 3 20:24:52 2017 +0000

    finish find function

commit 127545c19794b5fe869dd22d0cf57bf8820c5794
Author: Harry Potter <h.potter@hogwarts.prog>
Date:   Fri Mar 3 20:20:18 2017 +0000

    add json rules and python program
```

1. You can see that in that last commit (the one at the top) was where the function was deleted. Luckily the commit message has made it easy to see what was done, which is why commit messages are important. However typing `git log -p snitch-sniffer.py` would have actually shown the changed contents of the file, if the commit message wasn't clear enough.

1. You can now get back the version of the file from the commit before. The long string of characters is called a hash, and is used by Git to keep track of files. In this case the commit that needs to be restored is `5fd772a292c019a7cf3012b1156685280d4a7d2d` So typing the following will get the file back to the way it was.

```bash
git checkout 5fd772a292c019a7cf3012b1156685280d4a7d2d snitch-sniffer.py
```

1. The file will be restored and you can now commit this change.

```bash
git commit -am 'restore find function'
```

## 
