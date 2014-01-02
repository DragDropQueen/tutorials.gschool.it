#Setting up your computer

You will be spending a lot of time in front of a computer using many different, unfamiliar tools during your time at gSchool. This tutorial will guide you through installing the basic tools we will use. In addition to simply installing the tools, you should take a little time reading each website to understand where each tool fits into your toolbox (also called the toolchain) as a developer. This will help you long term as you form a mental model of the world of software development.

## <a name="workDirectory"></a>Story - Create directory that will house all of your classwork.

As developers, we collect a lot of source code and artifacts for our various projects. Knowing where to easily find everything is a good skill to have, just like when you go looking for that pair of shoes. If you know they are in a specific closet and that closet is clean, they are easy to find. If you have no idea which closet they are in and each closet is messy, they will take a long time to find. 

As a starting point, you should use one [directory](http://en.wikipedia.org/wiki/Directory_(computing)){:target="_blank"} to house all of your code for gSchool. You will develop your own organizational structure within this directory throughout the class. Remember your goal is to easily find things as we go through class.

Use [this tutorial](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line){:target="_blank"} to create a new directory called "gSchoolWork" in your [home directory](http://en.wikipedia.org/wiki/Home_directory){:target="_blank"}, also known as home folder, using the command line interface.

When you are done, you can confirm that you did it properly by typing `ls -l ~` at the command line and seeing the gSchoolWork directory listed. If you see the directory, you can mark the story as completed in Tracker.

{% terminal %}
$ ls -l ~
total 0
drwx------+  4 user  staff   136 Dec 24 10:50 Desktop
drwx------+  3 user  staff   102 Dec 20 15:36 Documents
drwx------+  4 user  staff   136 Dec 20 15:36 Downloads
drwx------@ 39 user  staff  1326 Dec 31 08:27 Library
drwx------+  3 user  staff   102 Dec 20 15:36 Movies
drwx------+  3 user  staff   102 Dec 20 15:36 Music
drwx------+  3 user  staff   102 Dec 20 15:36 Pictures
drwxr-xr-x+  5 user  staff   170 Dec 20 15:36 Public
drwxr-xr-x   2 user  staff    68 Dec 31 09:03 gSchoolWork
{% endterminal %}

## <a name="homebrew"></a>Story - Install Homebrew

[Homebrew](http://brew.sh/){:target="_blank"} is a tool that will allow you to easily install development tools to your Mac from source code. We will be using it throughout the class to install various tools as we need them.

You will follow the instructions on the website to get it installed. When promptped to enter your password, use the password that you use to unlock your computer. When you are asked to install the command line tools, click the "Install" button. You do not need to install a full copy of XCode.

{% terminal %}
$ ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"
==> This script will install:
< lots of output >
You should run `brew doctor' *before* you install anything.
Now type: brew help
{% endterminal %}

You can get an idea of what Homebrew offers you as far as commands by running `brew help`.

{% terminal %}
$ brew help
Example usage:
< lots of output >
{% endterminal %}

When the installation is complete, you should use `brew doctor` to make sure everything is running smoothly.

{% terminal %}
$ brew doctor
Your system is ready to brew.
{% endterminal %}

## <a name="rvm"></a>Story - Install RVM

[RVM](http://rvm.io/){:target="_blank"} (Ruby Version Manager) is a program that allows you to easily install and manage Ruby versions and installed Ruby libraries, called [Gems](http://en.wikipedia.org/wiki/RubyGems){:target="_blank"} . These libraries are managed via a site called [RubyGems.org](http://rubygems.org/){:target="_blank"}.

{% terminal %}
$ \curl -sSL https://get.rvm.io | bash -s stable
Downloading https://github.com/wayneeseguin/rvm/archive/stable.tar.gz
< lots of output >
{% endterminal %}

After the installation completes, close the Terminal program using the keys <command>-q (hold down command key while you hit the q key) and reopen the terminal to confirm that the installation completed properly.

{% terminal %}
$ rvm info
< lots of output >
system:
    uname: "Darwin Users-Mac.local 13.0.0 Darwin Kernel Version 13.0.0: Thu Sep 19 22:22:27 PDT 2013; ...
    system: "osx/10.9/x86_64"
    bash: "/bin/bash => GNU bash, version 3.2.51(1)-release (x86_64-apple-darwin13)"
    zsh: "/bin/zsh => zsh 5.0.2 (x86_64-apple-darwin13.0)"
< lots of output >
{% endterminal %}

## <a name="ruby21"></a>Story - Install Ruby 2.1

OS X Mavericks, the [operating system](http://en.wikipedia.org/wiki/Operating_system){:target="_blank"} for you Mac, comes with a version of Ruby installed but it is not the latest and greatest. We will use RVM to install the latest version of Ruby, 2.1. If prompted for a password, use the password you use to unlock your computer. While you are waiting for Ruby to compile, read about Ruby:

* https://www.ruby-lang.org/en/about/
* http://en.wikipedia.org/wiki/Ruby_(programming_language)

{% terminal %}
$ rvm install ruby-2.1.0
Searching for binary rubies, this might take some time.
Found remote file https://rvm.io/binaries/osx/10.9/x86_64/ruby-2.1.0.tar.bz2
< lots of output >
{% endterminal %}

To confirm that Ruby 2.1.0 is installed correctly, ask for the version at the command line.

{% terminal %}
$ ruby --version
ruby 2.1.0p0 (2013-12-25 revision 44422) [x86_64-darwin12.0]
{% endterminal %}

## <a name="chrome"></a>Story - Install Chrome browser

Chrome will be our primary development browser because of the great built in [development tools](https://developers.google.com/chrome-developer-tools/){:target="_blank"}. If you typically use another browser, please get familiar with Chrome.

To confirm successful installation, open up the Chrome browser from the Applications directory and set it as your default browser.



## <a name="screenhero"></a>Story - Install ScreenHero

We will be doing a lot of pair programming throughout the course. We will start out using [ScreenHero](http://screenhero.com/){:target="_blank"} to support pair programming.

To confirm proper installation, add mgehard@pivotallabs.com as a contact. 

First start ScreenHero:

![ScreenHero Started](/images/computerSetup/screenheroStarted.png)

Then add the contact:

![Add ScreenHero Contact](/images/computerSetup/addContact.png)

## <a name="githubGui"></a>Story - Install GitHub git GUI client

We will be using [Git](http://git-scm.com/){:target="_blank"} as our [version control](http://en.wikipedia.org/wiki/Revision_control){:target="_blank"} software. In order to easily interact with Git early in the class, we will use a [GUI](http://en.wikipedia.org/wiki/Graphical_user_interface){:target="_blank"} client from GitHub.

First you will download the client from [http://mac.github.com](http://mac.github.com){:target="_blank"} and open it from the Downloads folder.

![Open GitHub client](/images/computerSetup/openGithubClient.png)

You should allow it to move the application to your Applications directory. Remember it is a good idea to keep your computer clean.

![Move GitHub client](/images/computerSetup/moveGithubClient.png)

Use the client to help set up Git configuration file (.gitconfig).

![Git Setup](/images/computerSetup/gitSetup1.png)

Enter in your GitHub username and password. These are the ones that you set up for the pre-requisites for gSchool.

![Git Setup](/images/computerSetup/gitSetup2.png)

![Git Setup](/images/computerSetup/gitSetup3.png)

Make sure your name and email address are correct.

![Git Setup](/images/computerSetup/gitSetup4.png)

No need to set up local repositories since you do not have any.

![Git Setup](/images/computerSetup/gitSetup5.png)

When the main window appears, you are all done.

![Git Setup](/images/computerSetup/gitSetupDone.png)

## <a name="sshKey"></a>Story - Generate an SSH key

There are many ways to prove your identity to a remote website. The predominant way is by using a username/password combination. Another way it to use something called an [SSH Key](https://wiki.archlinux.org/index.php/SSH_Keys){:target="_blank"}. We will use SSH keys when communicating with various servers on the Internet.

The first step in using SSH keys is to generate one. GitHub provides a great tutorial on how to generate an SSH key and how to associate it with your GitHub account. Please follow [this tutorial](https://help.github.com/articles/generating-ssh-keys){:target="_blank"} all the way through step 4. Also, please add a password to your ssh key as outlined in step 2.

If you run the `cd ~/.ssh` command and you get the message that looks like `-bash: cd: /Users/user/.ssh: No such file or directory`, you don't have an ssh key and you can continue to step 2. When you get to step 2, the ssh-add command should look like this:

{% terminal %}
$ ssh-add ~/.ssh/id_rsa
{% endterminal %}

If you already have an SSH key as identified by step 1, please make sure that you add a password to the key using [this guide](https://help.github.com/articles/working-with-ssh-key-passphrases){:target="_blank"} before continuing to step 3.

## <a name="heroku"></a>Story - Create Heroku account

We will be using [Heroku](http://heroku.com){:target="_blank"} to quickly and easily deploy applications to the Web. You should sign up for an account on their site.

Remember your username and password. You will need that any time you want to access the Heroku website. 

The next step is to install the [Heroku toolbelt](http://toolbelt.heroku.com){:target="_blank"}, software that allows you to easily deploy appilications to Heroku. Download and install the toolbelt from the welcome screen that you get when you create your account.

You will then need to open a terminal window and log into Heroku for the first time.

{% terminal %}
$ heroku login
Enter your Heroku credentials.
Email: user@example.com
Password (typing will be hidden): 
Found existing public key: /Users/user/.ssh/id_rsa.pub
Uploading SSH public key /Users/user/.ssh/id_rsa.pub... done
Authentication successful.
{% endterminal %}

You should also push a test application from Heroku just to make sure that everything is wired up properly. 

{% terminal %}
$ cd gSchoolWork
$ git clone git://github.com/heroku/ruby-sample.git
Cloning into 'ruby-sample'...
remote: Reusing existing pack: 16, done.
remote: Total 16 (delta 0), reused 0 (delta 0)
Receiving objects: 100% (16/16), done.
Resolving deltas: 100% (1/1), done.
Checking connectivity... done
$ cd ruby-sample/
Users-Mac:ruby-sample user$ heroku create
Creating afternoon-harbor-4586... done, stack is cedar
http://afternoon-harbor-4586.herokuapp.com/ | git@heroku.com:afternoon-harbor-4586.git
Git remote heroku added
$ git push heroku master
The authenticity of host 'heroku.com (50.19.85.132)' can't be established.
RSA key fingerprint is 8b:48:5e:67:0e:c9:16:47:32:f2:87:0c:1f:c8:60:ad.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'heroku.com,50.19.85.132' (RSA) to the list of known hosts.
Initializing repository, done.
Counting objects: 16, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (13/13), done.
Writing objects: 100% (16/16), 1.94 KiB | 0 bytes/s, done.
Total 16 (delta 1), reused 16 (delta 1)
-----> Ruby app detected
< lots of output >
To git@heroku.com:afternoon-harbor-4586.git
 * [new branch]      master -> master
$ heroku open
Opening afternoon-harbor-4586... done
{% endterminal %}

When you see "Hello, world" in the newly opened browser window your Heroku installation is complete and working. You can delete the ruby-sample directory using `rm -rf`.

![Heroku setup complete](/images/computerSetup/herokuInstalled.png)

{% terminal %}
$ rm -rf ~/gSchoolWork/ruby-sample
{% endterminal %}

Congratulations, you now have a basic Ruby tool chain installed on your computer!