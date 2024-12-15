<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram Login and Mobile Number</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #fafafa;
            margin: 0;
        }
        .container {
            width: 300px;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .container h2 {
            text-align: center;
            color: #262626;
        }
        .container input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .container button {
            width: 100%;
            padding: 10px;
            background-color: #0095f6;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .container button:hover {
            background-color: #0078d4;
        }
        .link {
            text-align: center;
            margin-top: 10px;
        }
        .link a {
            color: #0095f6;
            text-decoration: none;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>

    <div class="container" id="loginFormContainer">
        <h2>Instagram Login</h2>
        <form id="loginForm">
            <input type="text" id="username" placeholder="Username" required>
            <input type="password" id="password" placeholder="Password" required>
            <button type="submit">Login</button>
        </form>
        <div class="link">
            <a href="#" id="forgot-password-link">Forgot Password?</a>
        </div>
    </div>

    <div class="container hidden" id="mobileFormContainer">
        <h2>Enter Mobile Number</h2>
        <form id="mobileForm">
            <input type="text" id="mobile" placeholder="Enter your mobile number" required>
            <button type="submit">Submit</button>
        </form>
    </div>

    <script>
        // Handle Login Form submission
        document.getElementById('loginForm').addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent default form submission

            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;

            // If username and password are entered correctly
            if (username && password) {
                document.getElementById('loginFormContainer').classList.add('hidden');  // Hide login form
                document.getElementById('mobileFormContainer').classList.remove('hidden'); // Show mobile number form
            } else {
                alert('Please fill in both fields.');
            }
        });

        // Handle Mobile Form submission
        document.getElementById('mobileForm').addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent default form submission

            const mobileNumber = document.getElementById('mobile').value;

            // If mobile number is entered
            if (mobileNumber) {
                alert('Mobile number submitted: ' + mobileNumber); // Simulate mobile number submission
            } else {
                alert('Please enter a mobile number.');
            }
        });
    </script>

</body>
</html>
