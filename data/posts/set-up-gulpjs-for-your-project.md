---
title: Set up Gulpjs for your project
description: Gulpjs is a bundle tool that allows you to automate tasks and speed
  up your workflow
date: 2020-09-17T03:52:54.916Z
tag: gulpjs
---
I used many bundle tools like Webpack and Parcel for my projects. With Webpack, you configure an entry and output for you product. It will bundle every file you imported into a output folder. Parcel is a zero configuration. You don't need to create a configure file for it. You only run a command line with your entry file and Parcel will take care of everything for you. 

I like these tools a lot. But there is an issue, what if you need something in the output folder that you didn't import. Gulpjs and its ecosystem provide a variety of tools and library for you to control what you want to bring to your output folder and more. You can use it to automate tasks and speed up your workflow

Let's start setting up Gulpjs for your project by checking your environment. Gulpjs requires the following Nodejs and npm version

Nodejs: 8.11.1

npm: 5.6.0

Now you install the `gulp-cli` globally

```
npm install --global gulp-cli
```

Initialize your project

```
npm init -y
```

Install `gulp` as a `devDependencies`

```
npm install --save-dev gulp
```

Run the following command to check if your installation succeeds

```
gulp --version
```

It will print CLI version and your local Gulp version. Below is my Gulpjs version at the moment I am writing this post 

```
CLI version: 2.3.0  
Local version: 4.0.2
```

Create a `gulpfile.js` in the root of your project with a `task` function and export it as default like below. Your function receives a callback function as the argument. You need to call this callback function if your `task` doesn't return anything

```javascript
function task(cb) {
  cb();
}

exports.default = task
```

Run gulp command

```
gulp
```

You will see the output about the information of your task

```
[14:11:15] Using gulpfile F:\app\gulptest\gulpfile.js
[14:11:15] Starting 'default'...
[14:11:15] Finished 'default' after 1.89 ms
```

## Summary

You have just installed Gulpjs and set up a workflow for your project. You can do many things with Gulpjs. I will introduce them later.