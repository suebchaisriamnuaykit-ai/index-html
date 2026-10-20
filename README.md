<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset=UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> โปรเจ็กแรกของฉัน </title>
    <style>
        /* ส่วนตกแต่งด้วย CSS */
      body {
          font-family: sans-serif;
          background-color: #f0f2f5;
          text-align: center;
          padding-top: 50px ;

        {
        color: #333;
      ton {
       padding: 10px 20px;
       font-size: 16px;
       background-color: #4CAF50;
       color: white;
       border: none;
       border-radius: 5px;
       cursor: pointer;

       ton:hover {
        background-color: #45a049;
        
    </style>
</head>
<body>

  <!-- ส่วนโครงสร้างด้วย HTML -->
  <h1>ยินดีต้อนรับสู่เว็บแรกของผม! 🚀</h1>
  <p>นี่คือโปรเจ็กต์เล็กๆ ที่เขียนเองแสดงผลเอง</p>

  <button id="myButton">คลิกฉันสิ!</button>

  <!-- ส่วนลูกเล่นด้วย JavaSclipt -->
  <script>
      const button = document.getElementById('myButton');
      button.addEventListener('click', function() {
          alert('เย้! คุณกดปุ่มสำเร็จแล้ว 🎉✨️');
      });
  </script>
</body>
