# Ex03 To-Do List using JavaScript
## Name: HASMITHA V NANCY
## Reg No: 212224040111
## Date: 3-9-2025

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
~~~
<!DOCTYPE html>
<html>
<head>
  <title>Complete To-Do List</title>
  <style>
    body {
      font-family: Arial, georgia;
      background: #e8b4b8;
      text-align: center;
      padding-top: 50px;
    }

    input, button {
      padding: 8px;
      font-size: 16px;
      margin: 5px;
    }

    ul {
      list-style: none;
      padding: 0;
    }

    li {
      background: white;
      padding: 10px;
      margin: 8px auto;
      width: 320px;
      border-radius: 5px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .completed {
      text-decoration: line-through;
      color: green;
    }

    .left-part {
      flex-grow: 1;
      text-align: left;
    }

    .right-part button {
      margin-left: 5px;
    }
  </style>
</head>
<body>

  <h2> To-Do List</h2>

  <input type="text" id="taskInput" placeholder="Enter task">
  <button onclick="addTask()">Add</button>

  <ul id="taskList"></ul>

  <script>
    function addTask() {
      const taskText = document.getElementById("taskInput").value.trim();
      if (taskText === "") return;

      const li = document.createElement("li");
      const span = document.createElement("span");
      span.textContent = taskText;
      span.className = "left-part";

     
      const completeBtn = document.createElement("button");
      completeBtn.textContent = "Complete";
      completeBtn.onclick = function () {
        span.classList.toggle("completed");
      };

     
      const editBtn = document.createElement("button");
      editBtn.textContent = "Edit";
      editBtn.onclick = function () {
        const newText = prompt("Edit your task:", span.textContent);
        if (newText !== null && newText.trim() !== "") {
          span.textContent = newText.trim();
        }
      };

      
      const delBtn = document.createElement("button");
      delBtn.textContent = "Delete";
      delBtn.onclick = function () {
        li.remove();
      };

      const rightPart = document.createElement("div");
      rightPart.className = "right-part";
      rightPart.appendChild(completeBtn);
      rightPart.appendChild(editBtn);
      rightPart.appendChild(delBtn);

      li.appendChild(span);
      li.appendChild(rightPart);

      document.getElementById("taskList").appendChild(li);
      document.getElementById("taskInput").value = "";
    }
  </script>

</body>
</html>

~~~

## OUTPUT
<img width="1919" height="1129" alt="image" src="https://github.com/user-attachments/assets/3be4bf7a-f66e-47c3-b1df-d542db0d6b60" />



## RESULT
The program for creating To-do list using JavaScript is executed successfully.
