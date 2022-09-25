---
layout: post
description: Using HTML fragments and JavaScript data to build a table
author: Vivian Ni
categories: [markdown, week5]
title: Javascript and HTML
comments: true
---
<html>
<body>

<p id="intro">Using HTML fragments and Javascript to build a table.</p>

<button type="button" onclick='document.getElementById("intro").innerHTML = "Keep reading to learn more!"'>Click Me!</button>

<p>Ready to continue?</p>

<button onclick="document.getElementById('myImage').src='/images/yes.png'">yes</button>

<img id="myImage" src="/images/no.png" style="width:100px">

</body>
</html>