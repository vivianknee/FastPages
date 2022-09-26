---
layout: post
description: Using HTML fragments and JavaScript data to build a table
author: Vivian 
permalink: /frontend/jsTable
categories: [markdown, week5]
title: Javascript and HTML
---
{% include nav_frontend.html %}

<html>
<body>

<div id="myTable"></div>

<script>
    function book(name, author, genre) {
        this.name = name; 
        this.author = author;
        this.genre = genre;
    }

    var books = [ 
        new book("Angels and Demons", "Dan Brown", "Action"),
        new book("Scythe", "Neal Shusterman", "Dystopian Fiction"),
        new book("Inferno", "Dan Brown", "Action"),
        new book("Holes", "Louis Sachar", "Realistic Fiction"),
        new book("Murder on the Orient Express", "Agatha Christie", "Mystery"),
    ];

    // define a library and build Library objects and json
    function library(books){  
        // add each book to library
        this.books = books;
        this.library = [];
        this.books.forEach(book => {this.library.push(book);});
    }
    printBooks = new library(books);

    // HTML Body of Table is build as a series of concatenations (+=)
    var body = "";

    // Heading for Array Columns
    body += "</table>";
    body += "<tr>";
    body += "<td>" + "Title" + "</td>";
    body += "<td>" + "Author" + "</td>";
    body += "<td>" + "Genre" + "</td>";
    body += "</tr>";

    // Data of Array, iterate through each row of vShelf.library
    for (var row of printBooks.library) {
    body += "<tr>";
    body += "<td>" + row.name + "</td>";
    body += "<td>" + row.author + "</td>";
    body += "<td>" + row.genre + "</td>";
    body += "<tr>";
    }
    body += "</table>";

    document.getElementById('myTable').innerHTML = "<p>This is the text which has already been typed into the div</p>";

</script>

</body>
</html>