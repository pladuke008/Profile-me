<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>โปรไฟล์ - อัฟฮัม อินทโช</title>
    <!-- นำเข้าฟอนต์ Kanit เพื่อความทันสมัยตามเทรนด์โมเดิร์นไทย -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600&display=swap" rel="stylesheet">
    <!-- นำเข้าชุดไอคอน Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* กำหนดตัวแปรชุดสีม่วงแบบพรีเมียม */
        :root {
            --primary-purple: #6d28d9;    /* สีม่วงเข้ม */
            --dark-purple: #4c1d95;       /* สีม่วงดีพ */
            --medium-purple: #8b5cf6;     /* สีม่วงสว่าง */
            --accent-purple: #a855f7;     /* สีม่วงอัญมณี */
            --light-purple: #f5f3ff;      /* สีม่วงพาสเทลอ่อน */
            --text-dark: #1e1b4b;         /* สีข้อความเข้ม */
            --text-muted: #6b7280;        /* สีข้อความรอง */
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Kanit', sans-serif;
        }

        body {
            background-color: #faf5ff;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
            position: relative;
            overflow: hidden;
        }

        /* ตกแต่งพื้นหลังด้วย Gradient Blobs เพื่อมิติทางสายตา */
        .bg-blob {
            position: absolute;
            border-radius: 50%;
            filter: blur(80px);
            z-index: 0;
            opacity: 0.5;
        }

        .blob-1 {
            top: -10%;
            left: -10%;
            width: 400px;
            height: 400px;
            background: var(--medium-purple);
        }

        .blob-2 {
            bottom: -10%;
            right: -10%;
            width: 500px;
            height: 500px;
            background: #c084fc;
        }

        .blob-3 {
            top: 40%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 300px;
            height: 300px;
            background: #818cf8;
        }

        /* การ์ดโปรไฟล์สไตล์โปร่งแสงกระจก (Glassmorphism) */
        .profile-container {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.5);
            border-radius: 24px;
            box-shadow: 0 20px 40px rgba(109, 40, 217, 0.1);
            width: 100%;
            max-width: 450px;
            padding: 40px 30px;
            text-align: center;
            z-index: 1;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .profile-container:hover {
            transform: translateY(-8px);
            box-shadow: 0 30px 60px rgba(109, 40, 217, 0.15);
        }

        /* ส่วนจัดวางภาพโปรไฟล์และการสลับไปเป็นไอคอนสำรอง */
        .avatar-area {
            position: relative;
            width: 150px;
            height: 150px;
            margin: 0 auto 25px auto;
        }

        .profile-img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid white;
            box-shadow: 0 10px 25px rgba(109, 40, 217, 0.2);
            display: block;
        }

        .avatar-fallback {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--accent-purple), var(--primary-purple));
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 55px;
            border: 5px solid white;
            box-shadow: 0 10px 25px rgba(109, 40, 217, 0.2);
        }

        /* ข้อมูลส่วนตัว */
        .name {
            font-size: 26px;
            font-weight: 600;
            color: var(--text-dark);
        }

        .student-id-badge {
            background-color: var(--light-purple);
            color: var(--primary-purple);
            font-size: 14px;
            font-weight: 500;
            padding: 6px 16px;
            border-radius: 50px;
            display: inline-block;
            border: 1px solid rgba(109, 40, 217, 0.15);
        }

        /* รายละเอียดข้อมูลเพิ่มเติม */
        .info-list {
            text-align: left;
        }

        .info-card {
            background: rgba(255, 255, 255, 0.6);
            border: 1px solid rgba(109, 40, 217, 0.08);
            border-radius: 16px;
            padding: 16px 20px;
            display: flex;
            align-items: center;
            transition: background 0.2s ease, transform 0.2s ease;
        }

        .info-card:hover {
            background: rgba(255, 255, 255, 0.9);
            transform: translateX(5px);
        }

        .icon-box {
            width: 44px;
            height: 44px;
            border-radius: 12px;
            background: var(--light-purple);
            color: var(--primary-purple);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            flex-shrink: 0;
        }

        .text-box {
            flex-grow: 1;
        }

        .info-label {
            font-size: 12px;
            color: var(--text-muted);
            font-weight: 400;
            display: block;
        }

        .info-value {
            font-size: 15px;
            color: var(--text-dark);
            font-weight: 500;
            display: block;
        }

        .info-value a {
            color: var(--primary-purple);
            text-decoration: none;
            transition: color 0.2s ease;
        }

        .info-value a:hover {
            color: var(--dark-purple);
            text-decoration: underline;
        }

        /* ส่วนของปุ่มกด */
        .button-group {
            display: grid;
            grid-template-columns: 1fr;
        }

        .action-btn {
            background: linear-gradient(135deg, var(--medium-purple), var(--primary-purple));
            color: white;
            border: none;
            border-radius: 12px;
            font-size: 16px;
            font-weight: 500;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(109, 40, 217, 0.25);
            text-decoration: none;
        }

        .action-btn i {
            margin-right: 8px;
        }

        .action-btn:hover {
            background: linear-gradient(135deg, var(--primary-purple), var(--dark-purple));
            box-shadow: 0 6px 20px rgba(109, 40, 217, 0.35);
            transform: translateY(-2px);
        }

        /* ระยะห่างขององค์ประกอบต่างๆ ที่เป็นระเบียบ */
        .spacing-y-md {
            margin-bottom: 20px;
        }

        .spacing-y-lg {
            margin-bottom: 30px;
        }

        .spacing-x-sm {
            margin-right: 15px;
        }

        .btn-padding {
            padding: 14px 20px;
        }
    </style>
</head>
<body>

    <!-- รูปทรงกลมตกแต่งเพื่อความละมุนในพื้นหลัง -->
    <div class="bg-blob blob-1"></div>
    <div class="bg-blob blob-2"></div>
    <div class="bg-blob blob-3"></div>

    <div class="profile-container">
        
        <!-- รูปโปรไฟล์พร้อมระบบ Fallback ดักไว้เมื่อยังไม่มีไฟล์จริง -->
        <div class="avatar-area spacing-y-md">
            <img src="profile.jpg" alt="อัฟฮัม อินทโช" class="profile-img" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
            <div class="avatar-fallback" style="display: none;">
                <i class="fa-solid fa-user-graduate"></i>
            </div>
        </div>

        <!-- หัวข้อโปรไฟล์ -->
        <h1 class="name">คุณอัฟฮัม อินทโช</h1>
        <div class="student-id-badge spacing-y-lg">รหัสนักศึกษา: 694245015</div>

        <!-- รายการข้อมูลที่กระชับ สวยงาม -->
        <div class="info-list spacing-y-lg">
            
            <div class="info-card spacing-y-md">
                <div class="icon-box spacing-x-sm">
                    <i class="fa-solid fa-laptop-code"></i>
                </div>
                <div class="text-box">
                    <span class="info-label">สาขาวิชา</span>
                    <span class="info-value">วิทยาการจัดการคอมพิวเตอร์</span>
                </div>
            </div>

            <div class="info-card spacing-y-md">
                <div class="icon-box spacing-x-sm">
                    <i class="fa-solid fa-university"></i>
                </div>
                <div class="text-box">
                    <span class="info-label">สถาบันการศึกษา</span>
                    <span class="info-value">มหาวิทยาลัยราชภัฏหมู่บ้านจอมบึง</span>
                </div>
            </div>

            <div class="info-card spacing-y-md">
                <div class="icon-box spacing-x-sm">
                    <i class="fa-solid fa-phone"></i>
                </div>
                <div class="text-box">
                    <span class="info-label">เบอร์โทรศัพท์</span>
                    <span class="info-value"><a href="tel:0986979273">098-697-9273</a></span>
                </div>
            </div>

            <div class="info-card">
                <div class="icon-box spacing-x-sm">
                    <i class="fa-solid fa-envelope"></i>
                </div>
                <div class="text-box">
                    <span class="info-label">อีเมล</span>
                    <span class="info-value"><a href="mailto:afham.i@mcru.ac.th">afham.i@example.com</a></span>
                </div>
            </div>

        </div>

        <!-- ปุ่มโทรด่วนที่โดดเด่น -->
        <div class="button-group">
            <a href="tel:0986979273" class="action-btn btn-padding">
                <i class="fa-solid fa-phone-volume"></i> โทรติดต่อฉันตอนนี้
            </a>
        </div>

    </div>

</body>
</html>
