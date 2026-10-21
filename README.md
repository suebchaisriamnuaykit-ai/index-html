<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>เกมคลิกวัดดวง ⚡</title>
    <style>
        body {
            font-family: sans-serif;
            text-align: center;
            background-color: #222;
            color: white;
            padding-top: 50px;
        }
        button {
            padding: 15px 30px;
            font-size: 20px;
            background-color: #ff4757;
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
        }
        button:hover { background-color: #ff6b81; }
    </style>
</head>
<body>

    <h1>⚡ เกมคลิกรัวๆ ใน 5 วิ!</h1>
    <p>คะแนนของคุณ: <span id="score">0</span></p>
    
    <button onclick="countClick()">คลิกเลย!</button>

    <script>
        let score = 0;

        function countClick() {
            score = score + 1; // เพิ่มคะแนนทีละ 1 ทุกครั้งที่กด
            document.getElementById('score').innerText = score; // แสดงผลคะแนนบนหน้าจอ
        }
    </script>

</body>
</html>
