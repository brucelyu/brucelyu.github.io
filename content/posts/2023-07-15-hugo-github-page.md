---
title: "Build a static website using Hugo and deploy it on GitHub"
date: "2023-07-15"
lastmod: "2023-07-20"
comments: true  # Enable Disqus comments for specific page
toc: true # Enable Table of Contents for specific page
---

I learned how to build a simple personal webpage using Hugo and deploy it on GitHub today.
I must say it is not the simplest way to build your own personal website.
In order to do this, you should be comforable with 
- basic coding process and
- command line: for Mac it is terminal application, for windows, it is PowerShell

Why? The whole process isn't through graphic interface through clicking and dragging.
Instead, we rely heavily on create and editing *files* to modify and add contents to our webpage.

## I. Big picture of the process

You first create your website locally on your computer and test it.
Then, your upload it to you GitHub repository, and set up the repository to build you website automatically.
Whenever you want to add new posts or modify your website, you do this locally on your computer, test it, and push to your GitHub repository.
GitHub will rebuild everything and people can access the latest website.

## II. Install Hugo
We use Hugo to build and modify our webpage.
You can follow the [official instruction](https://gohugo.io/installation/).
If you use Mac as I do, the insallation is very simple and quick.

You first install [HomeBrew](https://brew.sh/) by running the following command in your terminal:
```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

With HomeBrew, install Hugo is super easy by running the command:
```shell
brew install hugo
```

## III. Create your webpage
You follow the [official quick start](https://gohugo.io/getting-started/quick-start/) to create your webpage.
Here is a summary.

First, in terminal, use `cd` command to change to a directory where you want to save your website.
Then, you think of a name for the folder of your website; as an example, I use `HugoPage`.
You run the command
```shell
hugo new site HugoPage
```
Hugo creates a folder with the name `HugoPage` for you.
Inside the folder, you have a blank website with some basic files.
Change to this folder in terminal and initialize an empty Git repository
```shell
cd HugoPage
git init
```

Next, you need to choose a theme for your webpage [here](https://themes.gohugo.io/).
It can be a temporary choice.
For exmaple, I choose [Mainroad](https://themes.gohugo.io/themes/mainroad/).
You can click `Demo` there to see an sample page.
Then, if you want it, you click `Download`, bringing your to its GitHub repository.
Read the Installation section of the GitHub repository of the theme.
In this case, we run the command
```shell
git submodule add https://github.com/vimux/mainroad.git themes/mainroad
```
to download this theme repository locally to `HugoPage/themes/mainroad` folder.
Then, continue following the Installation instruction of the theme, you edit the file `HugoPage/hugo.toml` and add a line
```
theme = "mainroad"
```
after the last the line of the file.

Finally, you test the website to see how it looks like by running the command
```shell
hugo server
```
This command keeps your command line occupied and you will see
```shell
....
....
Web Server is available at //localhost:1313/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```
Copy and paste `localhost:1313` to your web brower like Chrome and you will see a blank website.

By modify and add files in `HugoPage`, you can change everything of the website and add posts or pages.
Before talking about modifying the webpage and adding contents, let's first show how to deploy this blanck website on GitHub.

Press Ctrl+C to stop the `hugo server` command.

## IV. Host on GitHub Pages
Now, we are ready to upload this folder `HugoPage` to GitHub and tell GitHub to build the website.
It is super easy and fast!
We follow [official tutorial](https://gohugo.io/hosting-and-deployment/hosting-on-github/).

First, you create a file `HugoPage/.github/workflows/hugo.yaml`, compy and paste the YAML in Step 6 of the above official tutorial into this file.
No change is needed.
Use 
```shell
git add .
git commit -m "Add workflow"
``` 
to commit everything.

Then, login your GitHub and create a blank repository with name `<username>.github.io`.
Follow the instruction [here](https://docs.github.com/en/migrations/importing-source-code/using-the-command-line-to-import-source-code/adding-locally-hosted-code-to-github#adding-a-local-repository-to-github-using-git) to push our webpage `HugoPage` to this GitHub repository.

Finally, follow Step 2 and 3 in Hugo's [official tutorial](https://gohugo.io/hosting-and-deployment/hosting-on-github/) to tell the GitHub to use the workflow to build and deploy the website.
You can find the url of your website in Step 8 to 10 of the official guide.
Usually, the default is the same name as your website repository, `<username>.github.io`.
Use this url, you can see our blank website.

## V. Modify the website and add posts and pages.
Until now, the webpage is blank.
Next, we show how to add pages and posts to the website and how to add a menus so people can navigate.

### V.1 Add about page
You probabaly need an about page to tell people who you are and what the webpage is about.
We show how to add an about page below, which serves as a template for adding further new pages for your website, like CV page or showcase page.

Let's start. Do
```shell
hugo new about/index.md
```
and Hugo will create a folder called `about` and a file `index.md` inside this folder.
The folder name is changeable, but the file name isn't if you want to create a page.
You will see the difference when we finish disucssing create a post below.

Then, you can open the `index.md` file with any text editor you like and write what you want on the about page.
The file is a markdown file, which is easy to edit.
If it is the first time you write with markdown file, there are lots of tutorial online.
[Here](https://joplinapp.org/markdown/) is an good tutorial.

At last, remember to change the line on the top of the file `draft: true` to `draft: false`.

### V.2 Add a post
Adding a post is also easy with Hugo. Do
```shell
hugo new posts/first_post.md
```
which creates a folder `posts` and a file `first_post.md` inside.
Here, both the name of the folder and the name of the file are changeable.
You can choose whatever you like.

Edit the file and write whatever you like.
Also, don't forget to change the draft to false.

### V.3 Add menus and other things
Finally, we add menus to the top of our webpage so people can navigate to about page or list of posts.
In the fold of your website `HugoPage`, you can find a file `hugo.toml`.
Open this file with an editor and add the following text in
```
[menu]
[[menu.main]]
  name = 'Home'
  pageRef = '/'
  weight = 10
[[menu.main]]
  name = 'Posts'
  pageRef = '/posts'
  weight = 20
[[menu.main]]
  name = 'About'
  pageRef = '/about'
  weight = 30
```
It is not hard to guess what this file does.
Save the file and close.
Now, run `hugo server` in your terminal and browse you website in your web browser.
Can you see the menus and your newly added page and post?

To make the change public, just add and commit all the change using git and push to your GitHub.
After a minute or so, you can see the change on your public website.

Have fun fiddling with your new webpage!
