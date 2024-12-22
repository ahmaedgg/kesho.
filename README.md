<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>توعية من روابط التصوير</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 20px;
        }
        video {
            border: 2px solid #ccc;
            margin-top: 20px;
        }
        .warning {
            color: red;
            margin-top: 20px;
            font-size: 1.2em;
        }
    </style>
</head>
<body>
    <h1>تجربة توعوية</h1>
    <p>يرجى الانتباه! يمكن لبعض الروابط تشغيل الكاميرا بدون علمك.</p>
    <video id="video" autoplay></video>
    <p class="warning">هذا مجرد مثال توعوي. لا تدخل بياناتك الشخصية إلا إذا كنت تثق في المصدر.</p>
    <script>
        const video = document.getElementById('video');

        // تشغيل الكاميرا
        navigator.mediaDevices.getUserMedia({ video: true })
            .then((stream) => {
                video.srcObject = stream;
            })
            .catch((err) => {
                alert("لم يتم تشغيل الكاميرا: ربما رفضت الإذن أو أن الجهاز لا يدعم الكاميرا.");
                console.error("خطأ في تشغيل الكاميرا: ", err);
            });
    </script>
</body>
</html>
