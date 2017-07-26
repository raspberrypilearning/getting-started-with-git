## Making major changes

Imagine you're talking to your friend about your amazing project, and they have a really cool idea for some changes you could make to improve it. Your friend suggests using [Lidar](https://en.wikipedia.org/wiki/Lidar) rather than ultrasonic sensors. The changes are quite large, though, and you're worried that if you make them, you might break the project. You could make a copy of the directory and start working on this copy, but to keep using Git you'd have to make an entirely new repo. This could all get quite confusing. Luckily, Git has a feature called **branches**; using a branch allows you to make copies without losing or altering your original work.

- First, you can have a look at your repo's current status.

	```bash
	git status
	```

	This should show something like this:

	```bash
	On branch master
	nothing to commit, working directory clean
	```

- Now you can make a new branch in the repo, which lets you work on your amazing new adaption.

	```bash
	git checkout -b lidar-version
	```

- Now `git status` will show you something like this:

	```bash
	On branch lidar-version
	nothing to commit, working directory clean
	```

	This tells you that you are on the `lidar-version` branch. To view all the branches in your repo, you can type `git branch` which will show something like this:

	```bash
	* lidar-version
		master
	```

- You can now work on the lidar-version branch without altering your master branch. If you try out the new approach and find it doesn't work, you can simply delete the branch using `git branch -D lidar-version`. However, if it all works well, you can merge the branch back into your master branch.

- First, you'll need to make sure all your changes are committed and then switch back to the master branch.

	```bash
	git checkout master
	```
- Then you can merge the version into the master branch

	```bash
	git merge lidar-version
	```
- **Warning**: you can cause problems with a merge if you're working on two branches at the same time, as Git won't know which changes are the ones you want to keep. For this reason, it's best to just work on one branch at a time.

