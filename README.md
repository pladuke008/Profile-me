<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>โปรไฟล์ - อัฟฮัม อินทโช</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #e0eafc, #cfdef3);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .profile-card {
            background: #ffffff;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 450px;
            padding: 40px 30px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .profile-card:hover {
            transform: translateY(-5px);
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid #4a90e2;
            margin-bottom: 20px;
            box-shadow: 0 5px 15px rgba(74, 144, 226, 0.3);
        }

        .name {
            font-size: 24px;
            color: #333333;
            margin-bottom: 5px;
            font-weight: bold;
        }

        .student-id {
            font-size: 16px;
            color: #4a90e2;
            font-weight: 600;
            margin-bottom: 25px;
            letter-spacing: 0.5px;
        }

        .info-section {
            text-align: left;
            background: #f8faac;
            background: rgba(74, 144, 226, 0.05);
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 20px;
        }

        .info-item {
            margin-bottom: 15px;
            display: flex;
            flex-direction: column;
        }

        .info-item:last-child {
            margin-bottom: 0;
        }

        .label {
            font-size: 12px;
            text-transform: uppercase;
            color: #888888;
            margin-bottom: 3px;
            font-weight: bold;
        }

        .value {
            font-size: 16px;
            color: #444444;
        }

        .value a {
            color: #4a90e2;
            text-decoration: none;
        }

        .value a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

    <div class="profile-card">
        <img src="profile.jpg" alt="รูปโปรไฟล์ อัฟฮัม อินทโช" class="profile-img">
        
        <div class="name">คุณอัฟฮัม อินทโช</div>
        <div class="student-id">รหัสนักศึกษา: 694245015</div>
        
        <div class="info-section">
            <div class="info-item">
                <span class="label">สาขาวิชา</span>
                <span class="value">วิทยาการจัดการคอมพิวเตอร์</span>
            </div>
            <div class="info-item">
                <span class="label">สถาบันการศึกษา</span>
                <span class="value">มหาวิทยาลัยราชภัฏหมู่บ้านจอมบึง</span>
            </div>
            <div class="info-item">
                <span class="label">เบอร์โทรศัพท์</span>
                <span class="value"><a href="tel:0986979273">098-697-9273</a></span>
            </div>
            <div class="info-item">
                <span class="label">อีเมล</span>
                <span class="value"><a href="mailto:your-email@example.com">เติมอีเมลของคุณที่นี่</a></span>
            </div>
        </div>
    </div>

</body>
</html>
