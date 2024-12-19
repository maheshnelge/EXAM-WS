# EXAM-WS
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exam Login/Register</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <div class="logo">Logo</div>
        <div class="exam-name">Exam Name</div>
        <button class="home-button">Home Screen</button>
    </header>

    <div id="content">
        <div class="container" id="loginPage">
            <div class="box">
                <h3>Enter Number to Login/Register</h3>
                <form id="loginForm">
                    <input type="text" id="phone" placeholder="Enter phone number" required>
                    <input type="text" id="otpLogin" placeholder="Enter the OTP" required>
                    <button type="button" onclick="showRegisterPage()">Login</button>
                </form>
            </div>
        </div>

        <div class="container" id="registerPage" style="display: none;">
            <div class="box">
                <h3>Verify your number to register</h3>
                <form id="registerForm">
                    <input type="text" id="name" placeholder="Enter name" required>
                    <input type="email" id="email" placeholder="Enter email" required>
                    <input type="text" id="otpRegister" placeholder="OTP" required>
                    <button type="button" onclick="register()">Verify</button>
                </form>
            </div>
        </div>
    </div>

    <script>
        function showRegisterPage() {
            document.getElementById('loginPage').style.display = 'none';
            document.getElementById('registerPage').style.display = 'flex';
        }

        function register() {
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const otpRegister = document.getElementById('otpRegister').value;

            if (name && email && otpRegister) {
                alert(`Registered with name: ${name}, email: ${email}`);
            } else {
                alert('Please fill in all fields for registration!');
            }
        }
    </script>
</body>
</html>
