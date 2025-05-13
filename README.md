#HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DOM Manipulation Demo</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1 id="title">Welcome to My Page</h1>
  </header>

  <main>
    <section>
      <p id="description">This is a simple example of DOM manipulation.</p>
      <button id="changeTextBtn">Change Text</button>
      <button id="changeStyleBtn">Change Style</button>
      <button id="toggleBoxBtn">Add/Remove Box</button>
    </section>

    <article id="contentArea">
      <!-- Box will be added or removed here -->
    </article>
  </main>

  <footer>
    <p>&copy; 2025 MySite</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
# style.css 
body {
  font-family: Arial, sans-serif;
  padding: 20px;
}

button {
  margin: 5px;
}

.box {
  width: 100px;
  height: 100px;
  background-color: steelblue;
  margin-top: 20px;
}
#script.js 
// Change text content dynamically
document.getElementById("changeTextBtn").addEventListener("click", function () {
  document.getElementById("title").textContent = "Text Changed!";
  document.getElementById("description").textContent = "The content has been updated using JavaScript.";
});

// Modify CSS styles via JavaScript
document.getElementById("changeStyleBtn").addEventListener("click", function () {
  document.body.style.backgroundColor = "#f0f8ff";
  document.getElementById("title").style.color = "darkblue";
});

// Add or remove an element
document.getElementById("toggleBoxBtn").addEventListener("click", function () {
  const contentArea = document.getElementById("contentArea");
  const existingBox = document.getElementById("dynamicBox");

  if (existingBox) {
    contentArea.removeChild(existingBox);
  } else {
    const newBox = document.createElement("div");
    newBox.id = "dynamicBox";
    newBox.className = "box";
    contentArea.appendChild(newBox);
  }
});
