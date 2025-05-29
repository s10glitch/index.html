# index.html
 <!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <title>جاري الاختراق...</title>
    <style>
        body {
            background-color: black;
            color: #00ff00;
            font-family: monospace;
            font-size: 18px;
            padding: 20px;
            white-space: pre-wrap;
        }

        #msg {
            color: red;
            font-size: 24px;
            margin-top: 30px;
        }
    </style>
</head>
<body>
    <div id="screen">جارِ الاتصال بسيرفر الاختراق...</div>
    <div id="msg"></div>

    <script>
        const fakeLogs = [
            "جارِ الوصول إلى ملفات النظام...",
            "تم الوصول إلى كاميرا الجهاز...",
            "جاري سحب الصور الخاصة...",
            "جارِ رفع الملفات إلى السيرفر الروسي...",
            "تم تفعيل التحكم الكامل بالجهاز...",
            "جارِ إغلاق الحماية...",
            "جارِ مراقبة المايك...",
            "جارِ استدعاء وحدة الهكر العالمية...",
        ];

        let index = 0;
        const screen = document.getElementById("screen");
        const msg = document.getElementById("msg");

        function showLogs() {
            if (index < fakeLogs.length) {
                screen.innerHTML += "\n" + fakeLogs[index];
                index++;
                setTimeout(showLogs, 1500);
            } else {
                msg.innerText = "😈 تم اختراق جهازك بنجاح...\nلا تحاول تهرب.";
            }
        }

        setTimeout(showLogs, 1000);
    </script>
</body>
</html>
