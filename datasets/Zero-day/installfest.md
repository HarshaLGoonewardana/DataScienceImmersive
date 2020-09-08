---
title: DSI Installfest
duration: "1:30"
creator:
    name: Marc Harper + DSI-DC
    city: LA + DC
---

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Data Science Immersive "Installfest"

## DSI Computer Setup

Welcome to GA's Data Science Immersive! Before you start class, you'll need to download and install a few tools. Follow this guide to get your computer all set up, and let us know if you have any questions.

## Part 0. While we're waiting...

1. Please also download a **reasonably professional** headshot from your LinkedIn, your Facebook, etc. for use on Slack and Github. (More about these later.) If you do not have a headshot, you'll want to take one before the class starts and post it on both Slack and Github.

## Part 1. Operating System

While you can be a data scientist on any operating system, most practicing data scientists choose a Unix-type operating system, typically either Apple's OS X or a popular Linux distribution such as [Ubuntu](http://www.ubuntu.com/) or [Linux Mint](https://www.linuxmint.com/).

 * If you are already using Mac or Linux, great! Skip ahead to **Part 2** and get started with your installs.
 * If you are using a Windows machine, follow the instructions below.

#### For Windows Users
If you are running Windows, you will need to install a virtual machine that runs Linux. We're recommending that you use [VirtualBox](https://www.virtualbox.org/wiki/Downloads) with [Ubuntu](http://www.ubuntu.com/). Here's how to get started:

1. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
 * **Note**: Make sure to also install the "Extension Pack" for your version!
2. Download our [Ubuntu starter image](https://www.dropbox.com/sh/3mp1p3av2k6be4y/AADstHqUMSPRyYPWuk_C3XAJa?dl=0) labeled "For PCs only"
 * **Note**: You'll need at least 2-3 GBs of free disk space.
3. Open VirtualBox and import the image
4. Double-click the Virtual Machine on the left; the password is "**ilovedatascience**"

## Part 2. Anaconda and Python

In our class, we'll be working closely with tools that utilize the Python programming language. [Anaconda](https://docs.continuum.io/anaconda/index) is a popular cross-platform tool that helps install and manage Python-related data science libraries.

1. [Download Anaconda](https://docs.continuum.io/anaconda/install) and follow the installation instructions package for your operating system. When the option arises, **DOWNLOAD PYTHON 3.6**. (Whether you do the graphical installer or command-line installer is irrelevant.)

2. Agree to the terms and let Anaconda go through its default installation. (This will likely take a few minutes.)

3. Anaconda should install several packages by default, including:

  * **jupyter**: an interface for creating interactive python notebooks, great for sharing analyses
  * **python**: a programming language very popular with data scientists
  * **matplotlib**: a plotting library for python
  * **nltk**: a toolkit for natural language processing
  * **numpy**: a linear algebra library
  * **pip** & **setuptools**: software to manage and install python packages
  * **scikit-learn**: a toolkit for machine learning algorithms
  * **scipy** and **statsmodels**: statistical packages for python
  * **sqlite**: a popular, easy to use database
  * **seaborn**: plotting and basic statistical package for python

4. To confirm, run the following at the command line (remember, you don't need to type the `$`):

 ```bash
 $ conda install jupyter python matplotlib nltk numpy pip setuptools scikit-learn scipy statsmodels sqlite seaborn
 ```

5. Once Anaconda is installed, you can add additional python packages from the command line as follows:

 ```bash
 $ conda install gensim spacy sqlalchemy psycopg2
 ```

Anaconda may also update your packages at this time - this is perfectly okay!

#### Just For Linux Users

On Ubuntu, if the `conda install` command fails for some reason, restart your or source your `.bashrc` like so

```bash
$ source ~/.bashrc
```

## Part 3. Confirm Your Python Installation

1. When you've gotten this far, open up a terminal and enter the Python interpreter:

 ```
 $ python3
 ```

 Depending on your operating system, your terminal should return something like this:

 ```bash
 user@vbox:~/Downloads$ python
 Python 3.6.1 :: Anaconda 4.4.0 (x86_64)| (default, Sep 18 2017, 18:08:45)
 [GCC 4.4.7 20120313 (Red Hat 4.4.7-1)] on linux2
 Type "help", "copyright", "credits" or "license" for more information.
 Anaconda is brought to you by Continuum Analytics.
 Please check out: http://continuum.io/thanks and https://anaconda.org
 >>>
 ```

2. Next, make sure that the necessary packages are installed. For example, to check that `matplotlib` is installed, type in your terminal:

 ```bash
 >>>> import matplotlib
 >>>> print(matplotlib.__version__)
 1.5.1
 ```

 You may see another version, which is okay. If you get an error like this:

 ```bash
 $ import matplotlib
 ImportError: No module named matplotlib
 ```

 then you'll need to try to install the Python packages again.

3. Finally, you can check the installation and versions of *all* the python libraries. You can do this a couple of different ways, but we'll simply use `pip freeze`.

 * Open a terminal window

 ```bash
 $ pip freeze
 ```

 You will see a list of all the python packages currently installed with their version numbers in the terminal window.

4. Sometimes, it might be beneficial for us to run things using Python 2.7 instead of Python 3.6. We'll try to stick with Python 3.6 as much as possible, but we can get our computer to also have 2.7 installed on the chance that we'll use it. In the terminal, type:

  ```bash
 $ conda create -n py27 python=2.7 anaconda
 $ source activate py27
 $ python -m ipykernel install --user --name py27 --display-name "Python 2.7"
 $ source deactivate py27
 ```

## Part 4. Homebrew (MacOS Only!)

We'll also install Homebrew, a great package management tool. To understand Homebrew's utility, it's useful to know a bit about packages and libraries.

Packages are executable bits of source code. In other words, they're kind of like an zipped/archived movie you downloaded. (I'm sure you downloaded it legally.) A package requires that you have necessary pre-requisites to run a given piece of software (like the right OS, other package dependencies, etc). A library is a set of files that can be used by other software programs. Much like packages, they have dependencies you need to satisfy.

Here's a [good resource](http://knowpapa.com/modpaclib-py/) discussing the differences among packages, libraries, and modules.

What does a package manager do, exactly? The premise is simple:

1. Takes a single command as input and figures out which software package you want installed.

2. Downloads the source code of the package.

3. Figures out if any dependencies exist and, if so, downloads them as well.

4. Compiles (builds) the dependencies from the source code files and installs them.

5. Builds your requested software.

6. Installs it.

Adapted from [this resource](http://computers.tutsplus.com/tutorials/homebrew-demystified-os-xs-ultimate-package-manager--mac-44884).

Installing is simple:
```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Further [documentation](https://git.io/brew-docs) for Homebrew.

## Part 5. Git

Throughout this course, we'll be using three closely related entities:
- git: a popular version control system used to share code with others
- GitHub: a popular software development platform that interfaces well with git. (This is free and public.)
- GitHub Enterprise: a version of GitHub for private organizations. (This is paid for by GA and is private.)

1. Travel to [Github](https://github.com/) and [Github Enterprise](https://git.generalassemb.ly) and set up a new account **on each** if you don't already have one.

2. Go to the [installation instructions](https://help.github.com/articles/set-up-git/) and walk through step 1.

3. To [check if your git installation is successful](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup), open a new terminal window and try to run `git` from the command line:

 ```
 $ git --version
 ```

 The output should be something like this:

 ```bash
 $ git --version
 git version 2.11.0
 ```

4. Next, you'll need to tell git your name and email. Make sure to use the same email address that you use for github:

 ```bash
 $ git config --global user.name "Ben Shaver"
 $ git config --global user.email benpshaver@gmail.com
 ```

 Note that user.name means the name of the user, **not** the username you used when setting up your account!

 These identifiers will be added to your commits and show up when you push your changes to github from the command line!

5. To expedite the process of logging in, we can get our GitHub Enterprise to remember our password by connecting to GitHub through SSH keys. (These instructions are adapted from the [incredible walkthrough posted on GitHub](https://help.github.com/articles/connecting-to-github-with-ssh/).)

 Step 1: First, we check for existing SSH keys.
 ```bash
 $ ls -al ~/.ssh
 ```

  If you see something like "id_rsa.pub" or "id_ecdsa.pub," you have an existing SSH key. Take note of the name and skip step 2. If you do not see something like id_rsa.pub, or you get an error, then move to step 2.

  Step 2: Next, we have to generate an SSH key.

  ```bash
  $ ssh-keygen -t rsa -b 4096 -C "benpshaver@gmail.com"
  ```
  When prompted to "Enter a file in which to save the key," hit Enter. Select any password; you'll have to enter it twice.

  Step 3: Add your SSH key to the ssh-agent.

  ```bash
  $ eval "$(ssh-agent -s)"
  $ nano ~/.ssh/config
  ```

  At this point, a box should open up. Paste this inside:

  ```
  Host *
   AddKeysToAgent yes
   UseKeychain yes
   IdentityFile ~/.ssh/id_rsa
  ```

  Save the file by hitting Ctrl + X (to exit), Y (to save), Enter (to confirm location).

  Then, run this command.

  ```bash
  $ ssh-add -K ~/.ssh/id_rsa
  ```

  Step 4: Finally, head to [this page](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/) and follow the last set of instructions to add the SSH key to your GitHub account!

## Part 6. PostgreSQL

PostgreSQL is a database management system, similar to MySQL, that we'll be using throughout the class. Install Postgres with the following steps:

1. Follow the instructions for your operating system below.

 #### Mac Users

  * Download Postgres.app from [www.postgresapp.com](http://postgresapp.com)
  * Move the Postgres.app to your 'Applications' folder.
  * Open the Postgres.app (using "right-click + open" since it is an application that isn't from the Mac App Store)
  * Look for the elephant in the the menu bar.

 #### Linux Users
  * [Download Postgres](http://www.postgresql.org/download/linux/ubuntu/)
  * On Ubuntu, you can also [install Postgres](https://help.ubuntu.com/community/PostgreSQL) from the package manager:

  ```bash
  $ sudo apt-get install postgresql postgresql-contrib postgresql-client
  ```

2. You need to add yourself as a user in postgres so you can access the `psql` console seamlessly. Following the commands below, replace `dsi-student` with *your own username* and type *your own password* when prompted.

If you are running Ubuntu, use "**ilovedatascience**" as your password.

```bash
$ sudo -i su - postgres
$ createuser dsi-student --superuser --password
$ createdb dsi-student
$ exit
```

Test that this works by typing `psql`. You should be presented with the postgres shell. To exit type `\q`.

## Part 7. Additional Required Tools

1. We'll be using [Slack](https://slack.com/), a popular messaging platform, for our class communications. Click on the [installation instructions for your platform](https://slack.com/downloads) to install the Slack desktop app. You can also sign into Slack using a web interface or via their mobile app. I recommend using the mobile app and the desktop app.

2. [Chrome](https://www.google.com/chrome/) is Google's popular web browser, and it comes with a complete set of developer tools built-in. We'll use Chrome to examine code, debug scripts, and view back-end processes. If you don't already have Chrome, make sure to download and install it now.

3. [Tableau](http://www.tableau.com/) is a popular dashboard creation system for visualizing data. As a data scientist you'll need to create visualizations that make your analyses accessible to colleagues, stakeholders, and decision makers. Install the correct [Tableau Public](https://public.tableau.com/en-us/s/) version for your operating system.

## Part 8. Text Editors

A data scientist frequently writes scripts to process data, perform analysis, and create visualizations, webpages, and other end products, so you'll need a good text editor. If you don't already have a preference, we recommend [VS Code](https://code.visualstudio.com/). Other popular choices are [Atom](https://atom.io/) and [Sublime](http://www.sublimetext.com/). All three editors are available for most platforms.

1. Download the editor of your choice from their website.
2. Install the package by double clicking the file icon or from the command line.
3. Run your editor from the applications menu, or from the command line, like so:


```bash
$ code
$ subl
$ atom
```

If your terminal does not recognize the above command, you may need to add an alias to your bash profile so that your terminal recognizes your chosen text editor.

If you installed VS Code:
1. Launch VS Code
2. Open the VS Code Command Palette (Command + Shift + P) and type "Shell Command: Install 'code' command in PATH"
3. Restart the terminal and check to see that the `code` alias works

This example would open up VS Code, Sublime, or Atom, respectively. Whichever editor you choose, be sure to practice using it!

#### Configure Git with your Text Editor

Finally, you'll want to tell `git` to use the `nano` text editor. To do this, run the following code:

 ```bash
 $ git config --global core.editor "nano"
 ```

---

That's it! Now you're ready to begin GA's Data Science Immersive. Next, we'll have a review of Command Line, Git, and a short introduction to Jupyter Notebooks.
