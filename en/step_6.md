## Creating your first magic school bag

So you want to start a new project? Maybe it's a special ultrasonic range finder for tracking flying objects in the air. You'll want a directory on your computer for all your files to sit in, so the first thing to do is create that directory.

- In the terminal, you can use the `mkdir` (make directory) command to create a new directory.

	```bash
	mkdir snitch-sniffer
	```

- Now you want to go into that directory. You can use the `cd` (change directory) command to do this.

	```bash
	cd snitch-sniffer
	```

- Next, you can create a file that will tell people what the project is about. You can use any text editor to do this, but in this example `nano` is used to create a file called `README.md`. The `.md` extension stands for **Markdown**, which is a markup language. You can learn more about Markdown [here](https://daringfireball.net/projects/markdown/).


	```bash
	nano README.md
	```

- This should open up the file in the terminal. You can now give the file a title and write a short explanation of what your project is about.

	```markdown
	# The Golden Snitch Sniffer
	This is a project that uses multiple long-range ultrasonic sensors to find and track 
	an object flying in three-dimensional space. It displays the object's coordinates, 
	speed, and trajectory through a VR headset.
	```

- Pressing `Ctrl + X` will cause a save prompt to appear. You can type `Y` to save and then hit `Enter` to close nano.

- Your file should have been created and will now be sitting in your directory. You can type `ls` in the terminal to see a list of files.

	```bash
	ls
	```

- At the moment, the directory is just like any other directory on your system. You now need to make the magical school bag part. This is known as a **Git repository**, and it takes the form of a hidden directory that keeps track of all the changes to the working directory. Type the following to create the repository, which from now on will just be called a **repo**:

	```bash
	git init
	```

- If you type `ls` again, nothing will appear to have changed. You can use `ls -a` to see all the hidden files and directories, though.

	```
	ls -a
	```

- You should now see something like this in your terminal window:

	```bash
	.  ..  .git  README.md
	```

- That `.git` directory is the **repo skeleton**. You can have a look inside it by typing the following.

	```bash
	ls -a .git
	```

- This should bring up something like:

	```bash
	branches  config  description  HEAD  hooks  info  objects  refs
	```

- You don't really need to worry about this directory at all now. Just know that it is there and that it is tracking all the changes to the parent directory `snitch-sniffer`. 

