---
layout: post
title:  "Methods HTML in Postman"
date:   2022-04-28 17:02:14 -0500
categories: HTML
---

## What is Postman?

"Postman is an API platform for building and using APIs. Postman simplifies each step of the API lifecycle and streamlines collaboration so you can create better APIs—faster." [1](https://www.postman.com/)

### Methods HTML

#### 1.- GET

This method obtains data by a request done to an API

In Node Express:

```javascript
var express = require('express');
var app = express();

// respond with "hello world" when a GET request is made to the homepage
app.get('/', function(req, res) { // The home page in this case is in /
  res.send('hello world'); //This is the response of the request, in this case the request is just accesing to the homepage /
});
```

#### 2.- POST

#### 3.- PUT

#### 4.- PATCH

#### 5.- DELETE

#### 6.- COPY

#### 7.- HEAD

#### 8.- OPTIONS

#### 9.- LINK

#### 10.- UNLINK

#### 11.- PURGE

#### 12.- LOCK

#### 13.- UNLOCK

#### 14.- PROPFIND

#### 15.- VIEW

Node js Express implementation examples

References

1.- Postman. (s. f.). Postman. Recuperado 28 de abril de 2022, de https://www.postman.com/
