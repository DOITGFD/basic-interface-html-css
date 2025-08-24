<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Login Page</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .box {
      border: 1px solid #ccc;
      padding: 20px;
      border-radius: 8px;
      text-align: center;
    }
    input {
      display: block;
      margin: 10px auto;
      padding: 8px;
      width: 80%;
    }
    button {
      padding: 8px 15px;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <div class="box">
    <h2>Login</h2>
    <input type="text" id="user" placeholder="Username">
    <input type="password" id="pass" placeholder="Password">
    <button onclick="login()">Login</button>
    <p id="msg"></p>
  </div>

  <script>
    function login() {
      let u = document.getElementById("user").value;
      let p = document.getElementById("pass").value;
      let msg = document.getElementById("msg");

      if (u === "admin" && p === "1234") {
        msg.style.color = "green";
        msg.textContent = "Login successful!";
      } else {
        msg.style.color = "red";
        msg.textContent = "Wrong username or password!";
      }
    }
  </script>

</body>
</html>

