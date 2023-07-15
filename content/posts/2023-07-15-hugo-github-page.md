---
title: "Build a static website using Hugo and deploy it on GitHub"
date: "2023-07-15"
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

### V.1 Add about page
### V.2 Add a post
### V.3 Add menus and other things
