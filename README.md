<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List</title>
  <!-- <link rel="stylesheet" href="styles.css"> -->
</head>
<body>
  <div class="container">
    <h1>To-Do List</h1>
    <p>Tom stinks</p> <!-- NOT -->
    <p>tOM EATS bnanas</p>
    <input type="text" id="task-input" placeholder="Add a new task">
    <input type="text" id="details-input" placeholder="Add task details (optional)">
    <button onclick="addTask()">Add</button>
    <ul id="task-list"></ul>
  </div>
  <script>
    function addTask() {
      let element = document.getElementById("task-list");
      var entry = document.createElement('li');
      let inputText = document.getElementById('task-input').value;
      entry.appendChild(document.createTextNode(inputText));
      element.appendChild(entry);
      inputText = " "
      entry.appendChild(document.createTextNode(inputText));
      let inputTexts = document.getElementById('details-input').value;
      entry.appendChild(document.createTextNode(inputTexts));
      element.appendChild(entry);
    }
  </script>
</body>
</html>
