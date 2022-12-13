---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# NENCARC Example Project

This is an example project designed and written by Conor Wall.

This will include additional information when required. The Github repo can be found [here](https://github.com/nencarc-digital/template).

```{figure} /_static/lecture_specific/index/banner.jpeg
:scale: 45%
```

## Overview

This section will cover how to create your own book using this template. 

You will need a GitHub account setup for this process (if not using the nencarc.digital@gmail.com account) which can be done by clicking on this [link](https://github.com/join).

You will learn how to

1.  install the relevant packages required for github
2.  setup a new github repository and github page
3.  add/edit/delete content from the book 
4.  push the content to the github repository and live github page 

### Packages Needed

To begin, Git is required to be installed on your system. Depending if you are on a Windows device or MAC OS device, there are different installation methods to use. 

#### Windows Installation

For Windows, the following [link](https://github.com/git-for-windows/git/releases/download/v2.37.3.windows.1/Git-2.37.3-32-bit.exe) will lead you to the installation package. 

#### Mac OS Installation

For Mac OS, I would recommend the use of Homebrew for the installation, which can be installed via entering the following code into terminal.

```{code-cell} ipython3
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Once Homebrew is installed, git can then be installed via the following command.

```{code-cell} ipython3
brew install git.
```

### Anaconda Installation

Although the use of Git is possible without any python installation, the use of a python environment manager ensures the process is a lot simpler and more convenient. 

Therefore, on a Windows machine the installation of Anaconda is required. 

The link to the download page can be found [here](https://repo.anaconda.com/archive/Anaconda3-2022.05-Windows-x86_64.exe). The following screenshots will help you with the installation process.



### Setting Up New Page

#### Downloading Template

Download the template zip file from GitHub using this [link](https://github.com/nencarc-digital/template/raw/main/book/_static/lecture_specific/index/template.zip). Unzip the file and then export the folder to a desired location and save the folder name.

#### Creating New Repository 

Sign into GitHub using the user credentials. Create a new repository using the following screenshots as a guide. 

Click on the button in the red circle.

```{figure} /_static/lecture_specific/index/screenshot1.png
:scale: 25%
```

Enter a repository name and click on the 'Add a README File' checkbox.

```{figure} /_static/lecture_specific/index/screenshot2.png
:scale: 25%
```

Click on the 'Create Repository' Button.

```{figure} /_static/lecture_specific/index/screenshot3.png
:scale: 25%
```

#### Configuring Repository 

GitHub Pages is required to be enabled within each repository. To achieve this, use the following screenshots as a guide.

First click onto the repository.

```{figure} /_static/lecture_specific/index/screenshot4.png
:scale: 25%
```

Click on the repository settings.

```{figure} /_static/lecture_specific/index/screenshot5.png
:scale: 25%
```

Click on 'Pages'.

```{figure} /_static/lecture_specific/index/screenshot6.png
:scale: 25%
```

To enable GitHub Pages, click on 'None'.

```{figure} /_static/lecture_specific/index/screenshot7.png
:scale: 25%
```

Then proceed to click on 'Main'. This source will change to 'gh-pages' at a later date but for now but 'Main' is the only option.

```{figure} /_static/lecture_specific/index/screenshot8.png
:scale: 25%
```

Following this step, GitHub Pages is enabled.

#### Setting Up Github Credentials

To perform any Git related actions on terminal, it is required that your Github credentials are verified first. 

Enter your Github username first, which in our case as an example is the 'nencarc-digital'.

```{code-cell} ipython3
git config --global user.name nencarc-digital
```

Then enter your Github email, which  in our case will be 'nencarc.digital@gmail.com'.

```{code-cell} ipython3
git config --global user.name nencarc.digital@gmail.com
```

```{figure} /_static/lecture_specific/index/screenshot12.png
:scale: 45%
```

At this stage it may ask for your Github password, which will be sent privately. If this does not work, a Github personal access token may be required. It also may ask for your password at a later stage, for example, when pushing to the repository. Here is an example of what that may look like.

```{figure} /_static/lecture_specific/index/screenshot21.png
:scale: 45%
```

#### Generating Personal Access Token

Click on the user icon in the top right and then click on settings. 

```{figure} /_static/lecture_specific/index/screenshot14.png
:scale: 25%
```

Scroll down to the bottom of the page and click 'Developer Options' on the left-hand side.

```{figure} /_static/lecture_specific/index/screenshot15.png
:scale: 25%
```

Click on 'Personal access tokens'.

```{figure} /_static/lecture_specific/index/screenshot16.png
:scale: 25%
```

Click 'Generate new token'

```{figure} /_static/lecture_specific/index/screenshot17.png
:scale: 25%
```

Enter a token note. 

```{figure} /_static/lecture_specific/index/screenshot18.png
:scale: 25%
```

Check every box and click on the 'Generate token' button. 

```{figure} /_static/lecture_specific/index/screenshot19.png
:scale: 25%
```

A new token should be generated in the red circle. For the sake of security, the token created in this example is covered by a red rectangle. Paste this new password in the terminal if prompted by an error previously.

```{figure} /_static/lecture_specific/index/screenshot20.png
:scale: 25%
```

#### Setting Up New Page With Template

To upload the template to the new GitHub Page, you first need to clone the new repository. This should be done using the terminal/Git Bash terminal depending if you are on Mac OS or Windows. 

First, you need the corrent link to clone the repository. On the repository main page, click on the 'Code' button. 

```{figure} /_static/lecture_specific/index/screenshot9.png
:scale: 25%
```

Then click on 'HTTPS' and then copy the link via the button on the right circled. 

```{figure} /_static/lecture_specific/index/screenshot10.png
:scale: 25%
```

Type 'git clone' and paste the link copied above into the terminal. Your code should look something like this (the repo name being the name you used earlier and not 'testrepo').

```{code-cell} ipython3
git clone https://github.com/nencarc-digital/reponame.git
```

```{figure} /_static/lecture_specific/index/screenshot11.png
:scale: 45%
```

You should now have a folder in your directory named the same as the repository name. Type 'ls' or 'dir' (depending if you're on MAC OS or Windows) to see new directory.  

```{figure} /_static/lecture_specific/index/screenshot23.png
:scale: 35%
```

Replace the contents of that folder with the contents in the 'template' zip file that was downloaded earlier in the tutorial.

### Adding/Editing/Deleting Content From Page

Text will appear here.

### Uploading Page Content 

Text will appear here.



