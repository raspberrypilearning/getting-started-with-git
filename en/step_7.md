## Adding your books

- So you now have the magic school bag part, but you haven't yet added anything to it. That `README.md` file hasn't been placed into the bag yet. You need to tell Git that you want to add the `README.md` file to the repo. To do this you can simply type:

	```bash
	git add README.md
	```

	Sometime it's easier to just add everything to the repo though, rather than adding individual files. To do this you can type:

	```bash
	git add --all
	```

- Now Git knows it needs to keep track of all the changes that happen to the `README.md` file. You can have a look at the status of your repo at any time by typing the following: 

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

- The above response is telling you that the `README.md` file has not yet been **committed**. This means that although Git knows about the file, it doesn't yet have any of the file's contents stored. The simplest way to do a commit is by typing:

	```bash
	git commit -am 'add README.md'
	```

	This commits all changes you have made in the directory to the Git repo, and adds a message saying what you did. The message can be anything really, but it's best to keep it fairly short yet descriptive of what you changed.

