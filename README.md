# Telvin-s-award
my awards
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Telvin's awards</title>
    <link href="https://fonts.googleapis.com/css2?family=French+Script+MT:wght@700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'French Script MT', cursive;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            text-align: center;
            padding: 50px;
        }
        h1 {
            font-size: 48px;
            color: #4a90e2;
            text-shadow: 2px 2px 5px #000;
            font-weight: bold;
        }
        label {
            font-size: 36px;
            color: #fff;
            font-weight: bold;
        }
        input[type="text"] {
            padding: 10px;
            font-size: 24px;
            border: none;
            border-radius: 10px;
            margin: 20px 0;
            width: 50%;
            font-family: 'French Script MT', cursive;
        }
        button {
            background-color: #4a90e2;
            color: #fff;
            padding: 15px 30px;
            font-size: 20px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.3);
        }
    </style>
</head>
<body>
    <h1>Welcome to Telvin's awards</h1>
    <form id="nameForm">
        <label for="name">Enter your name:</label><br>
        <input type="text" id="name" name="name" required><br>
        <button type="submit">Get Certificate</button>
    </form>

    <script>
        document.getElementById('nameForm').addEventListener('submit', function(event) {
            event.preventDefault();
            var name = document.getElementById('name').value.trim();
            if (name) {
                // Capitalize the first letter of the name
                name = name.charAt(0).toUpperCase() + name.slice(1).toLowerCase();
                localStorage.setItem('cookName', name);
                window.location.href = 'certificate.html';
            }
        });
    </script>
</body>
</html>
