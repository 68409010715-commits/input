<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>My Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 40px;
        }
        input {
            padding: 8px;
            width: 250px;
        }
        button {
            padding: 10px 20px;
            margin-top: 10px;
        }
        #result {
            margin-top: 20px;
            font-weight: bold;
            color: green;
        }
    </style>
</head>
<body>

    <h2>แบบฟอร์มกรอกชื่อ</h2>

    <form onsubmit="showData(); return false;">
        <label>First name:</label><br>
        <input type="text" id="fname" placeholder="กรอกชื่อจริง" required><br><br>

        <label>Last name:</label><br>
        <input type="text" id="lname" placeholder="กรอกนามสกุล" required><br><br>

        <button type="submit">Submit</button>
    </form>

    <div id="result"></div>

    <script>
        function showData() {
            const fname = document.getElementById("fname").value;
            const lname = document.getElementById("lname").value;

            document.getElementById("result").innerHTML =
                "คุณกรอกชื่อ: " + fname + " " + lname;
        }
    </script>

</body>
</html>
