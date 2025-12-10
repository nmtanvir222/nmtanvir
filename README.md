<!DOCTYPE html>
<html>
<head>
    <title>Stylish Login</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .login-container {
            background-color: #ffffff;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }

        h2 {
            color: #333;
            margin-bottom: 30px;
            font-size: 24px;
            border-bottom: 2px solid #5cb85c;
            padding-bottom: 10px;
        }

        .input-group {
            margin-bottom: 20px;
            text-align: left;
        }

        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: #555;
        }

        input[type="text"],
        input[type="password"] {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-sizing: border-box;
        }

        input[type="submit"] {
            width: 100%;
            padding: 10px;
            background-color: #5cb85c;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            margin-top: 10px;
            transition: background-color 0.3s;
        }

        input[type="submit"]:hover {
            background-color: #4cae4c;
        }

        .forgot-password {
            display: block;
            margin-top: 15px;
            font-size: 12px;
        }

        .forgot-password a {
            color: #5cb85c;
            text-decoration: none;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <form action="#" onsubmit="return validateLogin()">
            <h2>Login</h2>
            
            <div class="input-group">
                <label for="username">Username:</label>
                <input type="text" id="username" name="username" placeholder="Enter your username" required>
            </div>

            <div class="input-group">
                <label for="password">Password:</label>
                <input type="password" id="password" name="password" placeholder="Enter your password" required>
            </div>

            <input type="submit" value="Submit">
        </form>

        <div class="forgot-password">
            <a href="forgot.html">Forgot Password?</a>
        </div>
    </div>
    
    <script>
        function validateLogin() {
            const correctUsername = "tanvir";
            const correctPassword = "1234";

            const inputUsername = document.getElementById('username').value;
            const inputPassword = document.getElementById('password').value;

            if (inputUsername === correctUsername && inputPassword === correctPassword) {
                alert("Login successful! Going to the welcome page.");
                window.location.href = "welcome.html?username=" + inputUsername; 
                return false;
            } else {
                alert("Invalid Username or Password. Please try again.");
                return false;
            }
        }
    </script>
</body>
</html>
