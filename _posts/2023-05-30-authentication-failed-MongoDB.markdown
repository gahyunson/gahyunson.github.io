---
layout: post
title:  "'authentication-failed' solved-MongoDB"
date:   2023-05-30
categories: MongoDB Node.js
---
I connected MySQL to NodeJS server. But I realized my app's datas are JSON type.
So, I decided to change from MySQL to MongoDB.
There was a problem which is 'authentication-failed'.
I try to figure out WHAT IS THE CAUSE. And I was able to remove '<>' characters.

For example, This is a code for authentication. 
You can see a part `<password>`.

`"mongodb+srv://username:<password>@cluster0.btzwq0y.mongodb.net/?retryWrites=true&w=majority";`

I undersood I have to include <> characters. But, I'd got error.

It worked when I removed characters.
`"mongodb+srv://username:password@cluster0.btzwq0y.mongodb.net/?retryWrites=true&w=majority";`


If there were other problems. You can check NodeJS version in MongoDB with your local NodeJS version.
