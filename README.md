# Mautic Documentation

### Introduction
This book serves as the [documentation for Mautic](https://mautic.org/docs/), the open source marketing automation system. Just as the code is open source and available for everyone, so is the documentation. Everyone is welcome to help make this information better and improve as needed.

### Download as PDF!

[Click here](https://mautic.org/docs/mautic_docs_en.pdf) to download these docs as a PDF in English.

[Click here](https://mautic.org/docs/mautic_docs_fr.pdf) to download these docs as a PDF in French.

[Click here](https://mautic.org/docs/mautic_docs_jp.pdf) to download these docs as a PDF in Japanese.



### How to contribute to the docs

This repository is the source code for [Gitbook](https://www.gitbook.com/) published at [www.mautic.org/docs](https://www.mautic.org/docs). The source code is shared [here on GitHub](https://github.com/mautic/documentation) so anyone can contribute to the documentation in the same way the programmers do with the actual Mautic code. 

#### Why is git used for the documentation

- *versions*. Anyone can go back and look at what the text looked like.
- *authorship*. Not only every file, but every line has its author.
- *community contributions*. No need to worry about deleting someone else's work while working on the same document.

Although some git knowledge is required to clone, modify, commit and push changes, there is a way to avoid that and edit the files directly in the GitHub web interface. If you know git, use the workflow you like. If not, the following guide will show you how to contribute easily.

#### Edit documents in browser

1. [Fork](https://github.com/mautic/documentation#fork-destination-box) this repository under your account so you'll have permission to edit.
2. Select a file to edit. The file structure is explained below. Now, let's edit the *README.md* file to show the principles. Click on it.
3. The content of *README.md* should be visible and the *Edit* button (the pencil icon) above as well. Hit it.
4. The content is written in [Markdown markup](https://daringfireball.net/projects/markdown/). Very simple text-based formatting.
5. Make a change to the file. For example, add to the end `This is my first contribution`.
6. When you have made a change, scroll down and notice the form called *Commit changes*. This is important. To save a change, you have to describe what you've changed and why. Write for example `A new line added for testing purposes`. Do not save yet!
7. Because the GitHub web interface does not provide all features of git, we won't have an easy way to revert our change back to the original state. We'd have to create another commit where we'd delete the added line. That would make a mess in the commit history. So instead, we create a new branch. There is a checkbox for it "Creates a new branch...". The branch has to have a name. `{yourusername}-patch-1` will be prefilled. Let's change it to `{yourusername}-testing`. Click the *Propose file change* button now.
8. Ok, so the change exists in your repository now. To propose the change to the official repository, you have to send a pull request (PR). You've been redirected to do just that. Here you describe your proposed change and click (please don't send the testing PRs) the *Create pull request* button.

If you want to clean up after the testing, go to the *Branches* section and delete the testing branch.

#### The File Structure

We've worked with the *README.md* file in the previous section. This file is shown in the home page of a GitHub repository and you are reading its content right now. It doesn't have anything to do with the Mautic documentation.

The *SUMMARY.md* file defines the menu of the documentation. If you add a new page to the documentation, you'll have to also add a new line there defining the title and the link to the file. It's pretty straightforward when you see the current menu items.

The folders are here to group the topics together. Open for example the *asset* folder. You'll see it has its own *README.md* file. It is the main content when you click on the Asset menu item. The *manage_assets.md* file is a subitem. The *media* subfolder contains all the images used in the *md* files.

#### Links

Often you'll want to make a link to another place in the documentation. In Markdown, the link looks like this:

```
[link title](http://example.com)
```

This will create an external link with absolute URL. If you want to create an internal link, use a relative URL like this:

```
[these steps](./../plugins/integration_test.html)
```
This will link to `plugins/integration_test.html` on the documentation website created from the *md* source file.

#### Images

As noted above, the images can be placed in the media subfolders. The images probably aren't possible to upload via the GitHub web interface, but you can upload them to any public URL and link them from there.

```
![alternative text here](http://example.com/images/apple.png "Tooltip text here")
```
Or, if you want to display an image already uploaded to the documentation repository, you can use a relative path:

```
![alternative text here](/assets/media/assets-newcategory.png "Tooltip text here")
```
