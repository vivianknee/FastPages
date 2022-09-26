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


<div id="myTable">
</div>

<script>
function Person(name, ghID, classOf) {
    this.name = name; 
    this.ghID = ghID;
    this.classOf = classOf;
    this.role = "";
}

// define a setter for role in Person data
Person.prototype.setRole = function(role) {
    this.role = role;
}

// define a JSON conversion "method" associated with Person
Person.prototype.toJSON = function() {
    const obj = {name: this.name, ghID: this.ghID, classOf: this.classOf, role: this.role};
    const json = JSON.stringify(obj);
    return json;
}

var teacher = new Person("Mr M", "jm1021", 1977);

var students = [ 
    new Person("Vivian", "vivanknee", 2024),
    new Person("Emma", "e-shen", 2024),
    new Person("Amay", "amayadvani", 2024),
    new Person("Sarah", "sarahliu", 2024),
];

// define a classroom and build Classroom objects and json
function Classroom(teacher, students){ // 1 teacher, many student
    // start Classroom with Teacher
    teacher.setRole("Teacher");
    this.teacher = teacher;
    this.classroom = [teacher];
    // add each Student to Classroom
    this.students = students;
    this.students.forEach(student => { student.setRole("Student"); this.classroom.push(student); });
    // build json/string format of Classroom
    this.json = [];
    this.classroom.forEach(person => this.json.push(person.toJSON()));
}

// make a CompSci classroom from formerly defined teacher and students
compsci = new Classroom(teacher, students);

Classroom.prototype._toHtml = function() {
    // HTML Style is build using inline structure
    var style = (
      "display:inline-block;" +
      "border: 2px solid blue;" +
      "box-shadow: 0.8em 0.4em 0.4em black;"
    );
  
    // HTML Body of Table is build as a series of concatenations (+=)
    var body = "";
    
    // Heading for Array Columns
    body += "<tr>";
    body += "<th><mark>" + "Name" + "</mark></th>";
    body += "<th><mark>" + "GitHub ID" + "</mark></th>";
    body += "<th><mark>" + "Class Of" + "</mark></th>";
    body += "<th><mark>" + "Role" + "</mark></th>";
    body += "</tr>";

    // Data of Array, iterate through each row of compsci.classroom 
    for (var row of compsci.classroom) {
      // tr for each row, a new line
      body += "<tr>";
      // td for each column of data
      body += "<td>" + row.name + "</td>";
      body += "<td>" + row.ghID + "</td>";
      body += "<td>" + row.classOf + "</td>";
      body += "<td>" + row.role + "</td>";
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

// Create a document fragment:
const dFrag = document.createDocumentFragment();

dFrag.appendChild(compsci._toHtml);


// Add fragment to a list: 
document.getElementById('myTable').appendChild(dFrag);
</script>

</body>
</html>