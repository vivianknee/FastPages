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

    library.prototype._toHtml = function() {
    var style = (
        "display:inline-block;" +
        "border: 2px solid blue;" +
    );

    // HTML Body of Table is build as a series of concatenations (+=)
    var body = "";

    // Heading for Array Columns
    body += "<tr>";
    body += "<th>" + "Title" + "</th>";
    body += "<th>" + "Author" + "</th>";
    body += "<th>" + "Genre" + "</th>";
    body += "</tr>";

    for (var row of printBooks.library) {
    body += "<tr>";
    body += "<td>" + row.name + "</td>";
    body += "<td>" + row.author + "</td>";
    body += "<td>" + row.genre + "</td>";
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
    
    document.getElementById('myTable').innerHTML = printBooks._toHtml();

</script>

</body>
</html>