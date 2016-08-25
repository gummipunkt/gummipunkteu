---
layout: post
title: Simpsons CSS
date: '2016-02-02 16:32:05'
---

<div id="simpsons">
  <p title="maggie" id="maggie"></p>
  <p title="homer" id="homer"></p>
  <p title="marge" id="marge"></p>
  <p title="bart" id="bart"></p>
  <p title="lisa" id="lisa"></p>
</div>

##simpsons.css
```
<style>
  #simpsons {
    background-color: #2B2B2B;
    width: 600px;
    height: 300px;
    text-align: center;
  }
  #simpsons p {
    width: 40px;
    height: 40px;
    display: inline-block;
    margin-left: 18px;
    margin-right: 18px;
    transition: 0.1s;
  }
  #simpsons p:hover {
    transform: scale(1.1);
  }
  #maggie {
    background-color: #FFC60A;
  }
  #homer {
    border-top: 40px solid #FFC60A;
    background-color: white;
    border-bottom: 40px solid #008BAA;
  }
  #marge {
    border-top: 40px solid #008BAA;
    background-color: #FFC60A;
    border-bottom: 80px solid #AEC774;
  }
  #bart {
    border-top: 40px solid #FFC60A;
    background-color: #008BAA;
  }
  #lisa {
    border-top: 40px solid #FFC60A;
    background-color: #F25822;
  }
</style>
```

##html
```
<div id="simpsons">
  <p title="maggie" id="maggie"></p>
  <p title="homer" id="homer"></p>
  <p title="marge" id="marge"></p>
  <p title="bart" id="bart"></p>
  <p title="lisa" id="lisa"></p>
</div>

```

[via paulrouget.com](http://paulrouget.com/e/simpsons/)