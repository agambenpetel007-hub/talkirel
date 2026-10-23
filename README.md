<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>תל קירל - העיר הרשמית של נועה קירל 🦄</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #ffe6f0, #ffffff, #ffd1dc);
            margin: 0;
            padding: 15px;
            color: #333;
            text-align: center;
        }
        .header {
            background: linear-gradient(90deg, #ff69b4, #ff1493);
            color: white;
            padding: 25px 15px;
            border-radius: 20px;
            box-shadow: 0 4px 15px rgba(255, 105, 180, 0.4);
            margin-bottom: 20px;
        }
        h1 { margin: 0; font-size: 2.2em; text-shadow: 2px 2px 4px rgba(0,0,0,0.2); }
        .card {
            background: white;
            border-radius: 20px;
            padding: 20px;
            margin: 15px auto;
            max-width: 500px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
            border: 2px solid #ffb6c1;
        }
        .unicorn-map {
            width: 100%;
            max-width: 350px;
            margin: 20px auto;
            position: relative;
        }
        .area-btn {
            background: #ff69b4;
            color: white;
            border: none;
            padding: 12px 20px;
            margin: 8px 0;
            width: 100%;
            border-radius: 12px;
            font-size: 1.1em;
            font-weight: bold;
            cursor: pointer;
            transition: transform 0.2s;
        }
        .area-btn:active { transform: scale(0.98); }
        input[type="text"] {
            width: 80%;
            padding: 12px;
            border: 2px solid #ff69b4;
            border-radius: 10px;
            font-size: 1em;
            text-align: center;
            margin-bottom: 10px;
        }
        .id-card {
            background: linear-gradient(135deg, #fff0f5, #ffe4e1);
            border: 3px dashed #ff1493;
            border-radius: 15px;
            padding: 15px;
            display: none;
            margin-top: 15px;
        }
    </style>
</head>
<body>

    <div class="header">
        <h1>🦄 ברוכים הבאים ל-תל קירל! 👑</h1>
        <p>העיר הדיגיטלית הרשמית של נועה קירל והמעריצים</p>
    </div>

    <div class="card">
        <h2>🆔 הנפקת תעודת תושב/ת תל קירל</h2>
        <p>הקלידי את השם שלך כדי לקבל תעודת תושב רשמית:</p>
        <input type="text" id="citizenName" placeholder="הכניסי את שמך כאן...">
        <button class="area-btn" onclick="generateID()">הנפיקי תעודת תושב ✨</button>

        <div id="idCard" class="id-card">
            <h3>🏛️ תעודת תושב/ת רשמית</h3>
            <p><strong>שם התושב/ת:</strong> <span id="displayName"></span></p>
            <p><strong>מספר תושב:</strong> #TK-<span id="idNum"></span></p>
            <p><strong>מעמד:</strong> מעריץ/ה מושבע/ת 💖</p>
            <p>✨ מאושר על ידי עיריית תל קירל ✨</p>
        </div>
    </div>

    <div class="card">
        <h2>🗺️ מפת העיר "תל קירל" (בצורת חד-קרן 🦄)</h2>
        <p>לחצי על השכונות במפת חד-הקרן כדי לגלות את העיר:</p>
        
        <button class="area-btn" onclick="alert('✨ קרן הזהב: מתחם פנומן והאירוויזיון!')">✨ קרן הזהב (מתחם פנומן)</button>
        <button class="area-btn" onclick="alert('🐆 שדרות פנתר: מועדון המוזיקה והשירים!')">🐆 שדרות פנתר (חדר מוזיקה)</button>
        <button class="area-btn" onclick="alert('📸 מוזיאון דובדבן: גלריית הלוקים והתלבושות!')">📸 מוזיאון דובדבן (אופנה וסטייל)</button>
        <button class="area-btn" onclick="alert('🏟️ אצטדיון פארק הירקון: אזור ההופעות החיות!')">🏟️ אצטדיון פארק הירקון (הופעות)</button>
    </div>

    <script>
        function generateID() {
            var name = document.getElementById('citizenName').value;
            if(name.trim() === "") {
                alert("בבקשה הכניסי שם!");
                return;
            }
            document.getElementById('displayName').innerText = name;
            document.getElementById('idNum').innerText = Math.floor(1000 + Math.random() * 9000);
            document.getElementById('idCard').style.display = 'block';
        }
    </script>

</body>
</html>

