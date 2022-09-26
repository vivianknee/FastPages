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

<ul id="myList">
</ul>

<script>
const fruits = ["Banana", "Orange", "Mango"];

// Create a document fragment:
const dFrag = document.createDocumentFragment();
for (let x in fruits) {
  const li = document.createElement('li');
  li.textContent = fruits[x];
  dFrag.appendChild(li);
}

// Add fragment to a list: 
document.getElementById('myList').appendChild(dFrag);
</script>

</body>
</html>