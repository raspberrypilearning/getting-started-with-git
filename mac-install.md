# Installing Git on MacOS

Getting Git setup on MacOS is easy, with the added benefit that you gain a package manager to install lots of other awesome and open source software.

1. You're going to need to start by typing a command into the Terminal on MacOS. This will install the [Homebrew package manager](https://brew.sh/), which is pretty similar to **apt** on Linux.

	![homebrew](images/homebrew.png)

1. Open up a Terminal window by typing `cmd + space` to open *Spotlight* and then type `Terminal` into the search field.

	![spotlight](images/spotlight.png)
	
1. Now copy and past the following command into the Terminal window to install Homebrew.

	```bash
	/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
	```
	
	![terminal](images/terminal.png)
	
1. You can hit `Return` at the prompts and allow Homebrew to install. Once it is finished, you'll have Git installed on MacOS, as it's an integral part of Homebrew. You can return to the [main worksheet](worksheet.md), and carry on following the guide.

	![installed](images/installed-git.png)
	
1. As an added bonus, you now have an amazing package manager that you can use to install software. For instance, you can install Emacs, just by typing `brew install emacs` into a Terminal window.
