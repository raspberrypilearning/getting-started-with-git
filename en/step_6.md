## Setting up Git

You're going to be working in a terminal window for the duration of this resource, so open it up by clicking on the icon on the desktop, or by pressing `Ctrl + Alt + T` on your keyboard.

- The first thing to do is to tell Git who you are. This is important, as Git can be used collaboratively by lots of people, so it needs to know who made changes to which files. You can use your own username and email address, unless you are in fact the Boy Who Lived. 

	```bash
	git config --global user.name "Harry Potter"
	git config --global user.email "h.potter@hogwarts.prof"
	```

- Next you need to tell Git which text editor you want to use. If you don't have any particularly strong feelings about text editors, then you can just type:

	```bash
	git config --global core.editor nano
	```

