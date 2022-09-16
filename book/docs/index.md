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

Type 'git clone' and paste the link copied above into the terminal. Your code should look something like this.

```{code-cell} ipython3
git clone https://github.com/nencarc-digital/template.git
```

```{figure} /_static/lecture_specific/index/screenshot11.png
:scale: 25%
```








### Adding/Editing/Deleting Content From Page

Text will appear here.

### Uploading Page Content 

Text will appear here.



