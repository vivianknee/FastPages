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


<div id="myTable"></div>

<script>
function book(name, author) {
    this.name = name; 
    this.author = author;
}

// define a setter for role in Person data
Person.prototype.setGenre = function(genre) {
    this.genre = genre;
}

// define a JSON conversion "method" associated with Person
Person.prototype.toJSON = function() {
    const obj = {name: this.name, author: this.author, genre: this.genre};
    const json = JSON.stringify(obj);
    return json;
}
var books = [ 
    new book("Angels and Demons", "Dan Brown"),
    new book("Scythe", "Neal Shusterman"),
    new book("Inferno", "Dan Brown"),
    new book("Holes", "Louis Sachar"),
    new book("Murder on the Orient Express", "Agatha Christie"),
];

// define a library and build Library objects and json
function (books){  
    // add each book to library
    this.books = books;
    this.book.forEach(book => { book.setGenre("Student"); this.library.push(book); });
    // build json/string format of Classroom
    this.json = [];
    this.library.forEach(book => this.json.push(book.toJSON()));
}

vShelf = new library(genre);

library.prototype._toHtml = function() {
    // HTML Style is build using inline structure
    var style = (
      "display:inline-block;" +
      "border: 2px solid blue;" +
    );
  
    // HTML Body of Table is build as a series of concatenations (+=)
    var body = "";
    
    // Heading for Array Columns
    body += "<tr>";
    body += "<th><mark>" + "Title" + "</mark></th>";
    body += "<th><mark>" + "Author" + "</mark></th>";
    body += "<th><mark>" + "Genre" + "</mark></th>";
    body += "</tr>";

    // Data of Array, iterate through each row of vShelf.library
    for (var row of vShelf.library) {
      // tr for each row, a new line
      body += "<tr>";
      // td for each column of data
      body += "<td>" + row.name + "</td>";
      body += "<td>" + row.author + "</td>";
      body += "<td>" + row.genre + "</td>";
      // tr to end line
      body += "<tr>";
    }
  
     // Build and HTML fragment of div, table, table body
    return (
      "<div style='" + style + "'>" +
        "<table>" +
          body +
        "</table>" +
      "</div>"
    );
  
  };

document.getElementById('myTable').innerHTML = body;

</script>

</body>
</html>