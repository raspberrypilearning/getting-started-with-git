## Adding more books and travelling in time.

- Now that you have set up your repo, it's time to get on with the project. Here, two new files have been created: `snitch-sniffer.py` and `quidditch-rules.json`. Typing `ls` reveals those files.

	```bash
	README.md  quidditch-rules.json  snitch-sniffer.py
	```

- The new files need to be added to the Git repo and then committed.

	```bash
	git add --all
	git commit -am 'add json rules and python program'
	```

- Then you carry on working on your code for a bit. Every time you make a significant change to the file, you can perform a new commit.

	```bash
	git commit -am 'finish find function'
	```

- Now imagine that you've made a horrible mistake. You've been working for a while and you've deleted your `find_snitch()` function, and then performed a commit. With Git, it's easy to go back in time and restore an earlier version of any of your files. Let's first look at the commit history of the file.

	```bash
	git log snitch-sniffer.py
	```

- This produces something like this:

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

- You can see that in that last commit (the one at the top) was where the function was deleted. Luckily the commit message has made it easy to see what was done, which is why commit messages are important. However, typing `git log -p snitch-sniffer.py` would have actually shown the changed contents of the file, if the commit message wasn't clear enough.

- You can now get back the version of the file from the commit before. The long string of characters after the word 'commit' is called a hash, and is used by Git to keep track of files. In this case, the commit that needs to be restored is `5fd772a292c019a7cf3012b1156685280d4a7d2d`. So typing the following will get the file back to the way it was:

	```bash
	git checkout 5fd772a292c019a7cf3012b1156685280d4a7d2d snitch-sniffer.py
	```

- The file will be restored and you can now commit this change.

	```bash
	git commit -am 'restore find function'
	```

