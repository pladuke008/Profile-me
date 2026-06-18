<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>โปรไฟล์ - อัฟฮัม อินทโช</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary-purple: #7c3aed;    
            --dark-purple: #5b21b6;       
            --medium-purple: #a78bfa;     
            --accent-purple: #c084fc;     
            --light-purple: #f5f3ff;      
            --text-dark: #1e1b4b;         
            --text-muted: #6b7280;        
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Kanit', sans-serif;
        }

        body {
            background-color: #f5f3ff;
            background: linear-gradient(135deg, #f5f3ff 0%, #edd9ff 100%);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
            position: relative;
            overflow-x: hidden;
        }

        .bg-blob {
            position: absolute;
            border-radius: 50%;
            filter: blur(80px);
            z-index: 0;
            opacity: 0.6;
        }

        .blob-1 {
            top: -10%;
            left: -10%;
            width: 350px;
            height: 350px;
            background: var(--medium-purple);
        }

        .blob-2 {
            bottom: -10%;
            right: -10%;
            width: 450px;
            height: 450px;
            background: var(--accent-purple);
        }

        .profile-container {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.6);
            border-radius: 24px;
            box-shadow: 0 20px 40px rgba(124, 58, 237, 0.12);
            width: 100%;
            max-width: 430px;
            padding: 40px 24px;
            text-align: center;
            z-index: 1;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .profile-container:hover {
            transform: translateY(-5px);
            box-shadow: 0 25px 50px rgba(124, 58, 237, 0.18);
        }

        .avatar-area {
            position: relative;
            width: 140px;
            height: 140px;
            margin: 0 auto 25px auto;
            cursor: pointer;
        }

        .profile-img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid white;
            box-shadow: 0 8px 20px rgba(124, 58, 237, 0.2);
            display: block;
        }

        .avatar-fallback {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--medium-purple), var(--primary-purple));
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            border: 4px solid white;
            box-shadow: 0 8px 20px rgba(124, 58, 237, 0.2);
            animation: pulse-border 2s infinite;
        }

        .avatar-fallback i {
            font-size: 40px;
            margin-bottom: 5px;
        }

        .avatar-fallback span {
            font-size: 11px;
            font-weight: bold;
            background: rgba(255, 255, 255, 0.2);
            padding: 2px 8px;
            border-radius: 10px;
        }

        @keyframes pulse-border {
            0% { box-shadow: 0 0 0 0 rgba(124, 58, 237, 0.6); }
            70% { box-shadow: 0 0 0 15px rgba(124, 58, 237, 0); }
            100% { box-shadow: 0 0 0 0 rgba(124, 58, 237, 0); }
        }

        .camera-badge {
            position: absolute;
            bottom: 5px;
            right: 5px;
            background: var(--primary-purple);
            color: white;
            width: 36px;
            height: 36px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 14px;
            border: 3px solid white;
            box-shadow: 0 4px 10px rgba(124, 58, 237, 0.3);
            transition: transform 0.2s ease;
        }

        .avatar-area:hover .camera-badge {
            transform: scale(1.15);
        }

        .name {
            font-size: 24px;
            font-weight: 600;
            color: var(--text-dark);
            margin-bottom: 6px;
        }

        .student-id-badge {
            background-color: var(--light-purple);
            color: var(--primary-purple);
            font-size: 14px;
            font-weight: 500;
            padding: 6px 18px;
            border-radius: 50px;
            display: inline-block;
            border: 1px solid rgba(124, 58, 237, 0.2);
            margin-bottom: 25px;
        }

        .info-list {
            text-align: left;
            margin-bottom: 25px;
        }

        .info-card {
            background: rgba(255, 255, 255, 0.5);
            border: 1px solid rgba(124, 58, 237, 0.08);
            border-radius: 16px;
            padding: 14px 18px;
            display: flex;
            align-items: center;
            margin-bottom: 12px;
            transition: background 0.2s ease, transform 0.2s ease;
        }

        .info-card:last-child {
            margin-bottom: 0;
        }

        .info-card:hover {
            background: rgba(255, 255, 255, 0.95);
            transform: translateX(4px);
        }

        .icon-box {
            width: 40px;
            height: 40px;
            border-radius: 12px;
            background: var(--light-purple);
            color: var(--primary-purple);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 16px;
            margin-right: 15px;
            flex-shrink: 0;
        }

        .text-box {
            flex-grow: 1;
        }

        .info-label {
            font-size: 11px;
            color: var(--text-muted);
            font-weight: 400;
            display: block;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .info-value {
            font-size: 14px;
            color: var(--text-dark);
            font-weight: 500;
            display: block;
            word-break: break-word;
        }

        .info-value a {
            color: var(--primary-purple);
            text-decoration: none;
            transition: color 0.2s;
        }

        .info-value a:hover {
            color: var(--dark-purple);
            text-decoration: underline;
        }

        .button-group {
            display: grid;
            grid-template-columns: 1fr;
            margin-bottom: 15px;
        }

        .action-btn {
            background: linear-gradient(135deg, var(--medium-purple), var(--primary-purple));
            color: white;
            border: none;
            border-radius: 14px;
            font-size: 15px;
            font-weight: 500;
            padding: 14px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(124, 58, 237, 0.25);
            text-decoration: none;
        }

        .action-btn i {
            margin-right: 8px;
        }

        .action-btn:hover {
            background: linear-gradient(135deg, var(--primary-purple), var(--dark-purple));
            box-shadow: 0 6px 20px rgba(124, 58, 237, 0.35);
            transform: translateY(-2px);
        }

        .instruction-box {
            background: rgba(255, 255, 255, 0.9);
            border-left: 4px solid var(--primary-purple);
            border-radius: 12px;
            padding: 15px;
            width: 100%;
            max-width: 430px;
            margin-top: 20px;
            z-index: 1;
            font-size: 13px;
            color: var(--text-dark);
            box-shadow: 0 10px 20px rgba(0,0,0,0.05);
            text-align: left;
        }

        .instruction-box p {
            margin-bottom: 5px;
        }

        .instruction-box ol {
            padding-left: 20px;
            color: var(--text-muted);
        }

        .instruction-box li {
            margin-bottom: 3px;
        }

        .highlight-text {
            color: var(--primary-purple);
            font-weight: bold;
        }
    </style>
</head>
<body>

    <!-- Background decoration blobs -->
    <div class="bg-blob blob-1"></div>
    <div class="bg-blob blob-2"></div>

    <div class="profile-container">
        
        <!-- Profile Image & Fallback mechanism -->
        <div class="avatar-area" onclick="document.getElementById('image-uploader').click();" title="คลิกเพื่อเลือกรูปภาพของคุณ">
            <img src="f15e75df-5cc0-4133-9c0f-ff1cedd104ec.jpg" alt="คุณอัฟฮัม อินทโช" class="profile-img" id="avatar-img" onerror="handleImageError();">
            
            <div class="avatar-fallback" id="fallback-icon" style="display: none;">
                <i class="fa-solid fa-graduation-cap"></i>
                <span>คลิกเพื่อใส่รูป</span>
            </div>
            
            <div class="camera-badge">
                <i class="fa-solid fa-camera"></i>
            </div>
        </div>

        <!-- Hidden file uploader for live previewing -->
        <input type="file" id="image-uploader" accept="image/*" style="display: none;">

        <!-- Header information -->
        <h1 class="name">คุณอัฟฮัม อินทโช</h1>
        <div class="student-id-badge">รหัสนักศึกษา: 694245015</div>

        <div class="info-list">
            
            <div class="info-card">
                <div class="icon-box">
                    <i class="fa-solid fa-laptop-code"></i>
                </div>
                <div class="text-box">
                    <span class="info-label">สาขาวิชา</span>
                    <span class="info-value">วิทยาการจัดการคอมพิวเตอร์</span>
                </div>
            </div>

            <div class="info-card">
                <div class="icon-box">
                    <i class="fa-solid fa-university"></i>
                </div>
                <div class="text-box">
                    <span class="info-label">สถาบันการศึกษา</span>
                    <span class="info-value">มหาวิทยาลัยราชภัฏหมู่บ้านจอมบึง</span>
                </div>
            </div>

            <div class="info-card">
                <div class="icon-box">
                    <i class="fa-solid fa-phone"></i>
                </div>
                <div class="text-box">
                    <span class="info-label">เบอร์โทรศัพท์</span>
                    <span class="info-value"><a href="tel:0986979273">098-697-9273</a></span>
                </div>
            </div>

            <div class="info-card">
                <div class="icon-box">
                    <i class="fa-solid fa-envelope"></i>
                </div>
                <div class="text-box">
                    <span class="info-label">อีเมล</span>
                    <span class="info-value"><a href="mailto:afham.i@mcru.ac.th">afham.i@mcru.ac.th</a></span>
                </div>
            </div>

        </div>

        <!-- Call Action Button -->
        <div class="button-group">
            <a href="tel:0986979273" class="action-btn">
                <i class="fa-solid fa-phone-volume"></i> โทรติดต่อฉันตอนนี้
            </a>
        </div>

    </div>

    <!-- Help instruction box -->
    <div class="instruction-box" id="guide-box">
        <p>💡 <span class="highlight-text">หากรูปภาพด้านบนไม่ยอมแสดงผล:</span></p>
        <ol>
            <li><strong>วิธีที่ง่ายที่สุด:</strong> <span class="highlight-text">คลิกที่วงกลมรูปโปรไฟล์ด้านบน</span> แล้วเลือกไฟล์รูป <code style="background:#eee; padding:1px 4px; border-radius:4px;">f15e75df-5cc0-4133-9c0f-ff1cedd104ec.jpg</code> จากเครื่องของคุณ รูปจะปรากฏทันที!</li>
            <li><strong>หากใช้งานในเครื่องคอมพิวเตอร์ของคุณ:</strong> ตรวจสอบให้แน่ใจว่าไฟล์รูปภาพถูกเซฟไว้ใน <strong>"โฟลเดอร์เดียวกัน"</strong> กับไฟล์ <code style="background:#eee; padding:1px 4px; border-radius:4px;">index.html</code> นี้นะครับ</li>
        </ol>
    </div>

    <script>
        const uploader = document.getElementById('image-uploader');
        const avatarImg = document.getElementById('avatar-img');
        const fallbackIcon = document.getElementById('fallback-icon');
        const guideBox = document.getElementById('guide-box');

        // Handles initial image load failure gracefully
        function handleImageError() {
            avatarImg.style.display = 'none';
            fallbackIcon.style.display = 'flex';
            guideBox.style.display = 'block'; 
        }

        // Handles client-side live image upload previewing
        uploader.addEventListener('change', function(e) {
            const file = e.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(event) {
                    avatarImg.src = event.target.result;
                    avatarImg.style.display = 'block'; 
                    fallbackIcon.style.display = 'none'; 
                }
                reader.readAsDataURL(file);
            }
        });
    </script>

</body>
</html>
