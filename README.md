<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ยินดีต้อนรับสู่เว็บไซต์ของฉัน</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            font-family: sans-serif;
            background-color: #0f172a;
            color: #f8fafc;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }
        .card {
            background-color: #1e293b;
            border: 1px solid #334155;
            border-radius: 16px;
            padding: 40px;
            max-width: 450px;
            width: 100%;
            text-align: center;
            box-shadow: 0 10px 25px rgba(0,0,0,0.3);
        }
        .profile-img {
            width: 110px;
            height: 110px;
            border-radius: 50%;
            background-color: #38bdf8;
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 48px;
        }
        h1 {
            font-size: 24px;
            margin-bottom: 8px;
            color: #f3f4f6;
        }
        .bio {
            color: #94a3b8;
            font-size: 14px;
            margin-bottom: 24px;
            line-height: 1.5;
        }
        .section-title {
            font-size: 16px;
            color: #38bdf8;
            margin-bottom: 12px;
            text-align: left;
        }
        .links {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        .link-btn {
            display: block;
            padding: 12px;
            background-color: #334155;
            color: #fff;
            text-decoration: none;
            border-radius: 8px;
            font-weight: bold;
            transition: 0.2s;
        }
        .link-btn:hover {
            background-color: #38bdf8;
            color: #0f172a;
        }
    </style>
</head>
<body>

    <div class="card">
        <!-- รูปโปรไฟล์ (ใส่อิโมจิหรือเปลี่ยนเป็นรูปภาพได้) -->
        <div class="profile-img">👨‍💻</div>
        
        <!-- ชื่อและคำอธิบายสั้นๆ -->
        <h1>ยินดีต้อนรับครับ!</h1>
        <p class="bio">พื้นที่เก็บผลงานและเรื่องราวส่วนตัวของผม ยินดีที่ได้รู้จักทุกคนครับ 🚀</p>

        <!-- ช่องทางติดต่อ / ผลงาน -->
        <div class="section-title">📌 ช่องทางการติดตาม & ผลงาน</div>
        <div class="links">
            <a href="https://facebook.com" target="_blank" class="link-btn">Facebook</a>
            <a href="https://github.com" target="_blank" class="link-btn">GitHub ของฉัน</a>
            <a href="mailto:example@email.com" class="link-btn">ส่งอีเมลหาผม</a>
        </div>
    </div>

</body>
</html>
