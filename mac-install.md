# Installing Git on Mac OS

Getting Git set up on Mac OS is easy, and has the added benefit of giving you a package manager to install lots of other awesome and open-source software.

1. You're going to need to start by typing a command into a terminal window on Mac OS. This will install the [Homebrew package manager](https://brew.sh/), which is pretty similar to **apt** on Linux.

	![homebrew](images/homebrew.png)

1. Open up a terminal window by typing `cmd + space` to open Spotlight and then type `terminal` into the search field.

	![spotlight](images/spotlight.png)
	
1. Now copy and past the following command into the terminal window to install Homebrew.

	```bash
	/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
	```
	
	![terminal](images/terminal.png)
	
1. You can hit `Return` at the prompts and allow Homebrew to install. Once it is finished, you'll have Git installed on Mac OS, as it's an integral part of Homebrew. You can return to the [main worksheet](worksheet.md), and carry on following the guide.

	![installed](images/installed-git.png)
	
1. As an added bonus, you now have an amazing package manager which you can use to install software. For instance, you can install Emacs just by typing `brew install emacs` into a terminal window.
