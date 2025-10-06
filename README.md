<!DOCTYPE html>
<html>
<head>
  <title>B.Tech IT Resume</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 40px; }
    .resume { border: 1px solid #ccc; padding: 20px; max-width: 600px; }
    h2 { color: #2c3e50; }
    label { font-weight: bold; }
  </style>
</head>
<body>
  <h2>Enter Your Resume Details</h2>
  <form onsubmit="generateResume(); return false;">
    <label>Name:</label><br>
    <input type="text" id="name"><br><br>

    <label>Hobbies:</label><br>
    <input type="text" id="hobbies"><br><br>

    <label>Personal Info:</label><br>
    <textarea id="personal" rows="4" cols="50"></textarea><br><br>

    <button type="submit">Generate Resume</button>
  </form>

  <hr>

  <div class="resume" id="resume" style="display:none;">
    <h2>My Resume</h2>
    <p><strong>Name:</strong> <span id="rName"></span></p>
    <p><strong>Hobbies:</strong> <span id="rHobbies"></span></p>
    <p><strong>Personal Info:</strong></p>
    <p id="rPersonal"></p>
  </div>

  <script>
    function generateResume() {
      document.getElementById("rName").innerText = document.getElementById("name").value;
      document.getElementById("rHobbies").innerText = document.getElementById("hobbies").value;
      document.getElementById("rPersonal").innerText = document.getElementById("personal").value;
      document.getElementById("resume").style.display = "block";
    }
  </script>
</body>
</html>
