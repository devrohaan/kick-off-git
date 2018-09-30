
[![Wisdomic Panda](https://github.com/robagwe/wisdomic-panda/blob/master/imgs/panda.png)](http://www.rohanbagwe.com/)  **Wisdomic Panda**
> *Hold the Vision, Trust the Process.*


# Beginner's guide to Git & GitHub! [![Latest Status](https://img.shields.io/badge/git-2.19.0-brightgreen.svg)](https://git-scm.com/)

*... a version control system for tracking changes in computer files and coordinating work on those files among multiple people.*
###### KSD, Open Friday, Dec 2015.

### :coffee: Ingredients:

- GitHub Profile
- git
- Ubuntu 16.4

## Cooking the Cookbook: git

#### Version Control System is a system that records changes to a file or set of files over time so that you can recall specific versions later. 

> For example, if you are a Software Developer and want to keep every change in the source code of your project that you/your organization has developed, in this case, a Version Control System (VCS) is a very wise thing to use. 

> - It allows you to revert selected files back to a previous state, revert the entire project back to a previous state, compare changes over time, see who last modified something that might be causing a problem, who introduced an issue and when, and more. Using a VCS also generally means that if you screw things up or lose files, you can easily recover.

> - In scenarios in which hundreds of people are working on the same project, a lack of management and coordination can have drastic implications on the project’s completion. By tracking and updating the changes every contributor makes to the ‘big picture,’ there is less room for error and more room for productivity and success.

> - Every time someone goes to work on the project, they should know exactly what has already been completed, added, changed, and so on. Otherwise, they might end up working on something that’s already been finished – or worse, something that has no applicability to the project anymore.

#### So in nutshell, it is a means of tracking collaborative changes to a project so that each collaborator is constantly aware of, or has access to, the most recent state of the project. Any and all updates are recorded instantly by means of version control software (VCS) and consolidated so that the version of the project everyone has access to is as up-to-date and dynamic as possible.

> The crux of the matter is that you just cannot mark yourself **safe** in case of any system failure because of **Your Faulty Code**.  :grin::grin:
Luckily, I have not screwed up any of such patches till date. But I have been through such unexpected system failures because of irresponsible code commits, Very tough times Buddy!!

*:pushpin: Git is always compared with SVN (Apache Subversion) which is a centralized VCS, but we are not going deep into it! We are focusing only on Git. So this write-up is for those who have just started their career in Software Development.)*

###### Git is a distributed version control system. But, Centralized Vs. Distributed ... What?

Well, a central version control system is located in one place so people can check out from the central location to make their changes and then check everything back in.

But this can be problematic if  you can't get access to that central  server or that central repository so for example **if that server is offline or  you're working somewhere that doesn't have a network connection then you'll only be able to see the files that you've checked out from that repository and no additional information about that central remote repository also if something happens to that central repository or that somehow gets corrupted then you've got to hope that there's a backup of that code somewhere.**

#### Now on the other hand, a distributed version control system like Git, everybody has a local replica of the remote repository so you can have the option to have that central remote repository cloned to your local machine. Also, your local repository has all of the information that your remote repository has based on the last time that you sync those two together.


![git](https://github.com/robagwe/wisdomic-panda/blob/master/imgs/git1.png) 
:paperclip: [Source](https://www.git-tower.com/learn/git/ebook/en/desktop-gui/appendix/from-subversion-to-git)


So the good thing about this is that if you don't have access to that remote repository then you can still view every single change that's been made to that  repository since it was created so in a  way it's almost like every developer has  an entire backup of the repository so in  the worst case scenario of something  happening to the remote repository every  developer has a copy of that same  repository on their machine so that's  why it's called a distributed version  control.

![git](https://github.com/robagwe/wisdomic-panda/blob/master/imgs/git2.png) 
:paperclip: [Source](https://www.git-tower.com/learn/git/ebook/en/desktop-gui/appendix/from-subversion-to-git)


> You have a local replica of the remote repository on your machine and then you can keep committing the files in your local repository and then later on you can merge/push the changes into the remote. But in case of SVN for check-ins you have to connect to central repository every time. 

###### GitHub is the largest community of developers in the world, where people share their projects. Well, I guess Microsoft is behind GitHub. Watch out People!!!

## Cookbook: git

**Here is a curated list of git commands to get you going.
For more information about this great tool, visit [here](https://git-scm.com/docs).**


### Installation: Command_Line

	 sudo apt install git-all

> **Check Version:**

	 git --version

> **Set Config:**

	 git config --global user.name "Username"

	 git config --global user.email "username@email.com"

	 git config --list

> **Cloning a Remote Repo (GitHub):**

	git clone https://github.com/robagwe/kick-off-git.git .

:bulb: *For those who are new to linux/unix " . at the end of the command indicates the current working directory.*

### Tracking The Activites:

	git status

	git log

	git diff

### Finally, Pushing the Changes To Github Account:

	git add -A
	
	git add filename

:bulb: *Above command adds the modified file/files to staging.*

	git commit -m "message"

	git pull origin master

:pencil2: *Always make a habit of synchronizing the local repo with a remote one before pushing the changes.*

	git push origin master

:pushpin: *But, What I Feel is, Creating Your Own Branch is a Good Practice while working on a production trunk. Create your own branch and now you are coding safe.:grin:*

	git branch testbranch
	
> **To switch to the newly created local branch.**

	git checkout testbranch

> **Make changes and commit to newly created branch and then push this newly craeted branch to remote repo..**

	git push origin -u testbranch 

> **To See all branches.**
	
	git branch -a
:pushpin: *'\*' in the output indicates the current working branch.*

> **Now, we have to sync up our remotely pushed branch with our remote master branch. Hoping your code worked well and cleared all test cases with flying colors.**

> **To swith to the master local branch.**
	
	git checkout master

	git pull origin master

	git branch --merged

	git merge testbranch

	git push origin master


### Initializing a Local repository from Existing repository:

> **cd to your local repo first.**

	git init

> **Adding an existing project to GitHub using the command line.**


	git add .

	git commit -m "First commit"

	git remote add origin remote_repository_URL
	 eg. git remote add origin https://github.com/robagwe/kick-off-git.git


	git remote -v

	git push origin master
	
	Or git push -u --force origin master
	
### Deleting Local Git Repo:

:exclamation: *Be careful, dangerous command, it will erase your repository. Make sure you run **rm -rf** from correct directory.*

	 rm -rf .git


#### :construction: Get hands on: [Kick-off](https://github.com/robagwe/kick-off-git/blob/master/CookBook.txt)

## <img src="https://github.com/robagwe/wisdomic-panda/blob/master/imgs/acr.png" width="50">   Hey Buddy!</img>

> This repository explains the rationale for git and gives examples. If you have any suggestions for more commands that should be on this page, let me know or consider submitting a pull request so others can benefit from your work. 
Thank you very much for reaching out! Please follow if you find it handy and hit :star: to get more kick-off repo updates.

:email: [Drop In!!](https://www.rohanbagwe.com/profile) Seriously, it'd be great to discuss Technology.

> *"Keep learning, you're never really done" - X*

					
            
            
            
