# My-<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>تسجيل الدخول</title>
  <style>
    body {font-family: Tahoma, sans-serif; text-align: center; background: #f5f5f5;}
    .login-box {margin: 100px auto; padding: 20px; background: #fff; width: 300px; border-radius: 10px; box-shadow: 0 0 10px #aaa;}
    input {display: block; margin: 10px auto; padding: 10px; width: 90%;}
    button {padding: 10px 20px; background: #28a745; color: #fff; border: none; border-radius: 5px; cursor: pointer;}
    button:disabled {background: #aaa;}
  </style>
</head>
<body>
  <div class="login-box">
    <h2>تسجيل الدخول</h2>
    <input type="text" id="username" placeholder="اسم المستخدم">
    <input type="password" id="password" placeholder="كلمة المرور">
    <button onclick="login()">دخول</button>
    <p id="msg"></p>
  </div>

  <script>
    let attempts = 3;
    function login() {
      const user = document.getElementById("username").value;
      const pass = document.getElementById("password").value;

      const correctUser = "user";
      const correctPass = "1234";

      if (user === correctUser && pass === correctPass) {
        window.location.href = "https://htmlpreview.github.io/?https://gist.githubusercontent.com/openai-user-examples/xxxxx/raw/index.html";
      } else {
        attempts--;
        if (attempts > 0) {
          document.getElementById("msg").innerText = "بيانات غير صحيحة. متبقي " + attempts + " محاولة.";
        } else {
          document.getElementById("msg").innerText = "تم قفل الحساب بعد 3 محاولات.";
          document.querySelector("button").disabled = true;
        }
      }
    }
  </script>
</body>
</html>
-dom
