---
title: Hexo
date: 2020-12-11 10:46:01
tags: #文章标签
---
<a name="Anchor"/>

### Write down in front:

Hexo is a blog framework that I use to construct this blog. I meet many problems when I first deploy it into my computer, so I decide to write down this blog as a manual.

### How to update my blog if I change my computer one day？

Solving this problem is easy by using github. You just need to create a branch in your github.io repository for saving initial file like css file.

So the process is 
- create a repository in github named **yourname.github.io**
- create a branch named hexo for saving file that is for generating page
- set **hexo** branch as default branch.
- using **git clone** command clone repository to your computer and push your file to hexo branch
  ```git
  git add .
  git commit -m "message"
  git push origin hexo
  ```
- And the key is setting your blog push to master branch, the directory is in root directory's *_config.yml* not in theme directory. The detail will be metioned later.

##### Remark: Because there was a accout used before in my computer, how to clear its vestige is very important to ensure our push operation is right.

The process is 
- modify you username and password in your computer by entering some commands in git interface.
```git
git config --glogal user.name "user.name"
git config --global user.email "user.email"
```
- Add privacy key to your computer by entering some commands in git interface
```git
eval `ssh-agent`
ssh-add ~/.ssh/rsa
```
- Add public key to github (refer to [public](https://www.jianshu.com/p/f22d02c7d943))

### Hexo install
Now you have a repository to save your blog file and blog page. Next step is to using Hexo framework to generate your page. Then mainly refer to the site [Use Hexo](https://zhuanlan.zhihu.com/p/26625249)

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

Thirdly, initialize our blog with basic framework.
```git
hexo init blog
```
Remark: you need to initialize the blog in **yourname.github.io** folder, and there should be no file in it.

Then you will get some folder that are scaffolds, source, themes, _config.yml.
