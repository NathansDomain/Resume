# How to forge a website!

  

## Purpose:

* This read me is for those out there trying to host a resume on a static site generator, in this case Pellican, and tracking any changes made to it via a forge, github

* It is indeed for individuals with little to no experience in this field.

* The methodologies and main ideas used will be from Modern Technical Writing: An Introduction to Software Documentation

  

## Prerequisites

* A lightweight markup languages, such as Markdown, reStructuredTextt, AsciiDoc, etc

* A static site generator, such as Pelican, Sphinx, Hugo, etc

* A forge account to host and track any changes made to the static site generator, such as GitHub
* A Distributed version control system, such as git
* Internet connection, at least for committing changes to the forge and getting started.

### Getting started
##
* Download a lightweight markup language, Etter recommends using either Markdown, reStructuredTextt, or AsciiDoc.
* Download python, this can be done through Microsoft store or going to [Python](https://www.python.org/downloads).
* Ensure the version is not too out of date. Etter’s mentions you should not use out of date tools as it admits to contributors that you can not be bothered to use modern tools.
	* Check your PATH variable was properly set after downloading Python if you are on Windows.
	* Open cmd and type in python
	* Read the terminal, if the cmd terminal says that python is not a recognized command refer to "setting PATHS", otherwise follow the next step.
	* Type into cmd python -m pip install "pelican[markdown]", If you see an error message pelican-quickstart is not on PATH, C:\Users\user\AppData\... and so on refer to "setting PATHS". Etter says static site generators are great for their speed, simplicity, portability, and security.
* Make a forge account
* Create a repository, the home page should direct you on the steps to take but if you encounter issues refer to "Creating a repository"
* Download git a distributed version control systems (DVCS). Etter says that they are generally most important in the context of documentation because developers prefer them.

### Creating a repository
##
* We will first create a single repository, Etter states a single repository makes writing more cohesive.
* Navigate to the home page of github.com, in the top left corner it is under the three barred menu, below Home there is a menu create a repository.
* Type in the empty field Resume, then click create new repository, name it Resume. 
* Create a folder to store the repository.
* Navigate to the folder through cmd.
* Clone the repository to you machine by using the command, 
   git clone https://github.com/UserName/Resume.git.
* The repository is now ready for changes to be pushed to.
### First static site
##
* Now we will create a static site, Etter mentions that static site generators are great, because you have everything you need to write, build, and review changes locally.
* Open cmd and navigate to the folder you created for the git repository using cd C:\.... 
* Run pelican-quickstart through cmd .
* Hit enter for the first prompt, the title should be "Insert name" Resume, the author is your name, hit y for enter url prefix, it should be the same url you used for your repository.
* Hit enter for all other prompts, this should have created a new project.
* Type in pelican content, it should give you a list of empty content, if you type in pelican --listen it will let you locally host your empty site.
### Converting resume to markdown
##
* We use a lightweight markup, as Etter says because, you can pipe to a more complex format like xml and never need to write it by hand.
* Open which ever lightweight markup you have downloaded.
* Slowly convert your Resume to follow markdown syntax, note that lightweight markups tend to have heavy restrictions on special formatting.
* At the top of the Resume include Title: "insert a title".
* Save the new markdown folder, preferably as resume.
* Open the folder you had used for pelican and your repository through file manager
* Create a pages folder under content if one does not exist.
* Move your resume to the pages folder, if you now call pelican content in the directory you called pelican quick start you should see it counts 1 page.
### Pushing changes to forge
##
* Etter claims that publishing should not be a special event, so you will be pushing many commits to the forge.
* Use the command git add  .; git commit -am "First commit".
* Then call pelican  content -s publishconf.py.
* Then call ghp-import output -b gh-pages.
* Finally push the changes using git push  origin gh-pages.
* Now if you got the your repository on forge you will see that the changes have been made.
### setting PATHS
##
* Find the directory that the application you can't call was installed, if the issue was with pelican it should have printed the directory path so copy that. The installer should have told you the directory.
* Once you have the directory open up Edit the system environment through the search bar.
* Navigate to the advanced tab and cline on Environment Variables.
* Click Path then edit, now click new and enter in the directory, hit enter then okay.
* Restart the computer if the computer still can not find the application.
### Further resources/readings
##
* https://www.computerhope.com/issues/ch000549.htm
* https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-your-personal-account/managing-multiple-accounts
* https://www.markdownguide.org/basic-syntax/
* https://linuxize.com/post/how-to-configure-git-username-and-email/
* https://dev.to/mahbubumithu/a-complete-markdown-tutorial-from-basics-to-advanced-41nb
* https://getpelican.com/
* https://git-scm.com/downloads
### FAQ
## 
* Why is Markdown better than  writing raw HTML
	* Markdown is better for a few reassons, one is it is very human readable so it is easy to understand.
	Html also has a ton of boiler plate code that static cite generator can produce for you. 
* I changed the Markdown version of my resume, so why don’t I see the  
changes when I refresh the website in my browser?
	* The changes you made were local and based on your computer, you need to make sure to commit the changes by using git commit 
### Credits
##
* Modern Technical Writing: An Introduction to Software Documentation
* Class mates: Ashek A Zaman and Shreshth Tyagi
* Professor: Tristan Miller
* Tutorials: Stack overflow
