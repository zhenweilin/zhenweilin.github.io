---
title: Hexo
date: 2020-12-11 10:46:01
tags: #文章标签
---
<a name="Hexo"/>

### Write down in front:

Hexo is a blog framework that I use to construct this blog. I meet many problems when I first deploy it into my computer, so I decide to write down this blog as a manual.

### How to update my blog if I change my computer one day？

Solving this problem is easy by using GitHub. It would be best to create a branch in your github.io repository for saving initial files like CSS files.

So the process is 
- create a repository in GitHub named **yourname.github.io**
- create a branch named 'hexo' for saving files that are for generating page
- set **hexo** branch as the default branch.
- using **git clone** command clone repository to your computer and push your file to 'hexo' branch
  ```git
  git add .
  git commit -m "message"
  git push origin hexo
  ```
- The key is setting your blog push to the master branch, and the directory is in the root directory's *_config.yml*, not in the theme directory. The detail will be mentioned later.

##### Remark: Because there was an account used before in my computer, how to clear its vestige is very important to ensure our push operation is right.

The process is 
- modify your username and password on your computer by entering some commands in the git interface.
```git
git config --global user.name "user.name"
git config --global user.email "user.email"
```
- Add privacy key to your computer by entering some commands in the git interface.
```git
eval `ssh-agent`
ssh-add ~/.ssh/rsa
```
- Add public key to GitHub (refer to [public](https://www.jianshu.com/p/f22d02c7d943))

### Hexo install
Now you have a repository to save your blog file and blog page. The next step is to using Hexo framework to generate your page. Then mainly refer to the site [Use Hexo](https://zhuanlan.zhihu.com/p/26625249)

Firstly, download and install [Node.js](https://nodejs.org/en/download/)

Enter some commands in your command windows to test whether it is installed successfully.

```git
node -v
npm -v
```

Secondly, install Hexo

```git
npm install -g hexo-cli 
```

Thirdly, initialize our blog with the basic framework.
```git
hexo init blog
```
Remark: you need to initialize the blog in **yourname.github.io** folder, and there should be no file in it.

Then you will get some folders that are scaffolds, source, themes, _config.yml.

- scaffolds folder: this folder is to save your page's module file.
- source folder: this folder is to save your resource for the page like a markdown file.
- themes folder: this folder to keep your themes file, you can search theme file in [theme](https://hexo.io/themes/) 
- _config.yml: this file is used to record some fundamental configurations.

### How to generate your blog page?
```bash
hexo clean
```
This command could be used for the first time.

```bash
hexo g
```
g is an abbreviation of the generating.
And you can preview it by using 

```bash
hexo s
```
s is an abbreviation of the server.

So I always use 
```bash
hexo g
hexo s
```

### How to change the theme in Hexo?
- Download theme module in the site [theme](https://hexo.io/themes/)
- Put the theme file under the theme folder in the root directory.
- Modify _config.yml file theme to your theme, like academia in my blog.
```
theme: academia
```
- Next, a few configurations are mainly based on your theme documentation.

### How to deploy your page to website?
- add deployment message in _config.yml from the **root** dir.

the pattern is like 
``` 
deploy:
  type: git
  repo: git@github.com:zhenweilin/zhenweilin.github.io.git
  branch: master
```

**Remark**: 
> the branch is the master (Had better choose this. It seems that github.io will find the branch named automatically. Of course, it's my pure surmise)
> 
> the **https** may be invalid sometimes, so that ssh may be the right choice here.

- one command helps you deploy the page to a website in command windows in the root directory.
```
hexo d
```

**Remark**
> Some problems maybe will come up in website though the page is well on your computer.
> you need to change your **url** and **root** in _config.yml from root dir. There is an example
```
url: https://github.com/zhenweilin/zhenweilin.github.io/tree/master
root: /
```
The url could be copied by the path of GitHub's branch.

### How to set hyperlink or anchor in page?
- URL:
```
[theme](https://hexo.io/themes/)
```
- Anchor: set an anchor in pageA
```
<a name="Anchor"/>
```
refer it in page B
```
[pageA](./articleA#Anchor)
```
A key to use this method is to set permalink in _config.yml from root dir.
```
permalink: :title/
```