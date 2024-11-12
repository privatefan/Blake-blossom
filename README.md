<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fan Club Login</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f5f5f5;
            text-align: center;
        }
        .container {
            background-color: #ffffff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            width: 300px;
            text-align: center;
        }
        header {
            font-size: 24px;
            font-weight: bold;
            color: #333;
            margin-bottom: 20px;
        }
        .hidden {
            display: none;
        }
        h2 {
            margin: 0 0 20px;
        }
        input[type="text"], input[type="password"] {
            width: 100%;
            padding: 10px;
            margin: 8px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }
        button:hover {
            background-color: #45a049;
        }
        .toggle-password {
            display: inline-block;
            cursor: pointer;
            color: #007BFF;
            font-size: 14px;
            margin-top: 5px;
        }
        .forgot-password {
            display: block;
            margin-top: 10px;
            color: #007BFF;
            text-decoration: none;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Page Header -->
        <header>BLAKE BLOSSOM</header>

        <!-- Welcome Message -->
        <div id="welcomeMessage" class="hidden">
            <h2>Welcome!</h2>
            <p>Thank you for your love and support! We’re thrilled to have you here and deeply appreciate the passion and enthusiasm you bring. Your presence means the world to us, and we're excited to take this journey with you.</p>
            <p>Thank you for being an incredible fan!</p>
            <button onclick="showNextContent()">Next</button>
        </div>

        <!-- Login Form -->
        <div id="loginFormContainer">
            <h2>Fan Club Login</h2>
            <form id="loginForm">
                <input type="text" id="username" placeholder="Username" required>
                <input type="password" id="password" placeholder="Fan ID" required>
                <span class="toggle-password" onclick="togglePassword()">Show Password</span>
                <button type="submit">Login</button>
                <a href="#" class="forgot-password">Forgot Password?</a>
            </form>
            <p id="error-message" style="color: red; display: none;">Incorrect username or fan ID.</p>
        </div>

        <!-- Exclusive Benefits Content -->
        <div id="additionalContent" class="hidden">
            <h2>❤️‍🔥What my superfans grant ⬇️</h2>
            <ul style="text-align: left;">
                <li>📍Daily New Content (over 500 sexy & nude pics including videos you get immediate access to upon subscription)</li>
                <li>📍B/G and Solo content (PPV)</li>
                <li>📌I sell my panties</li>
                <li>📍Twerk videos</li>
                <li>❣️Video call</li>
                <li>❤️Hookup</li>
                <li>🥰 Unlimited talk</li>
                <li>❣️Masturbating video</li>
                <li>❣️Random meeting</li>
                <li>📌One-on-one messaging 24/7 with you</li>
            </ul>
            <button onclick="showFinalPage()">Next</button>
        </div>

        <!-- Final Connection Page -->
        <div id="finalPage" class="hidden">
            <h2>You are fully connected to BLAKE BLOSSOM</h2>
        </div>
    </div>

    <script>
        function togglePassword() {
            const passwordField = document.getElementById("password");
            const toggleText = document.querySelector(".toggle-password");
            if (passwordField.type === "password") {
                passwordField.type = "text";
                toggleText.textContent = "Hide Password";
            } else {
                passwordField.type = "password";
                toggleText.textContent = "Show Password";
            }
        }

        document.getElementById("loginForm").addEventListener("submit", function(event) {
            event.preventDefault();
            const username = document.getElementById("username").value;
            const password = document.getElementById("password").value;

            const correctUsername = "Kevin";
            const correctPassword = "XX28P622";

            if (username === correctUsername && password === correctPassword) {
                document.getElementById("loginFormContainer").classList.add("hidden");
                document.getElementById("welcomeMessage").classList.remove("hidden");
            } else {
                document.getElementById("error-message").style.display = "block";
            }
        });

        function showNextContent() {
            document.getElementById("welcomeMessage").classList.add("hidden");
            document.getElementById("additionalContent").classList.remove("hidden");
        }

        function showFinalPage() {
            document.getElementById("additionalContent").classList.add("hidden");
            document.getElementById("finalPage").classList.remove("hidden");
        }
    </script>
</body>
</html>
