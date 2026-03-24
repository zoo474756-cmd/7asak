<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>7asak- هدايا روبوكس</title>
    <style>
        body, html {
            margin: 0; padding: 0; width: 100%; height: 100%;
            display: flex; justify-content: center; align-items: center;
            background-color: white; overflow: hidden; font-family: sans-serif;
        }
        /* تصميم الزر */
        #btn {
            padding: 20px 40px; font-size: 25px;
            background-color: #2ecc71; color: white;
            border: none; border-radius: 15px;
            font-weight: bold; box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            cursor: pointer;
        }
        /* الصورة المخيفة */
        #scaryImg {
            display: none; position: fixed; top: 0; left: 0;
            width: 100%; height: 100%; object-fit: cover; z-index: 999;
        }
    </style>
</head>
<body>

    <!-- الزر اللي يظهر في البداية -->
    <button id="btn">تبي روبوكس أخضر؟ 💸</button>

    <!-- الصورة المخيفة (تقدر تغير الرابط اللي بين القوسين بصورتك) -->
    <img id="scaryImg" src="https://i.imgur.com/5u9gB9P.jpg">

    <!-- الصوت المرعب -->
    <audio id="scarySound">
        <source src="https://www.soundboard.com/handler/DownLoadTrack.ashx?cliptoken=646461-9f93-4e4f-9e6b-0b5c5e5e5e5e" type="audio/mpeg">
    </audio>

    <script>
        const btn = document.getElementById('btn');
        const img = document.getElementById('scaryImg');
        const sound = document.getElementById('scarySound');

        btn.onclick = function() {
            // تشغيل الصوت
            sound.play();
            // إظهار الصورة
            img.style.display = 'block';
            // إخفاء الزر
            btn.style.display = 'none';
            
            // اهتزاز خفيف (اختياري)
            if (navigator.vibrate) navigator.vibrate(500);
        };
    </script>
</body>
</html>
