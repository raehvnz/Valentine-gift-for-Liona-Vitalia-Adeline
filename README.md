<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surat Valentine untuk Liona</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Patrick+Hand&display=swap');

        body {
            font-family: 'Patrick Hand', cursive;
            text-align: center;
            background-color: #ffecf2;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
            position: relative;
            overflow: hidden;
        }

        .background {
            position: fixed;
            width: 100%;
            height: 100%;
            background: url('https://i.pinimg.com/originals/4d/c9/da/4dc9da45f9b0b6fa4c957e644a25833b.jpg') no-repeat center center/cover;
            z-index: -1;
        }

        .container {
            text-align: center;
            position: relative;
            background: rgba(255, 240, 245, 0.9);
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0px 0px 10px rgba(0,0,0,0.3);
            z-index: 1;
        }

        .speech-bubble {
            background-color: #ffb6c1;
            padding: 15px 25px;
            border-radius: 20px;
            display: inline-block;
            font-size: 20px;
            font-weight: bold;
            box-shadow: 2px 2px 5px rgba(0,0,0,0.2);
            margin-bottom: 20px;
            cursor: pointer;
            transition: transform 0.3s ease-in-out;
        }

        .speech-bubble:hover {
            transform: scale(1.1);
        }

        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: #fffaf0;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0px 0px 10px rgba(0,0,0,0.3);
            text-align: center;
            width: 80%;
            max-width: 400px;
            opacity: 0;
            animation: fadeIn 0.5s ease-in-out forwards;
            z-index: 10;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translate(-50%, -55%); }
            to { opacity: 1; transform: translate(-50%, -50%); }
        }

        .popup p {
            font-size: 18px;
            color: #333;
            margin: 15px 0;
        }

        .button {
            background-color: #ff69b4;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-size: 16px;
            transition: 0.3s ease-in-out;
            margin: 5px;
        }

        .button:hover {
            background-color: #ff1493;
        }

        .final-screen {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: white;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            text-align: center;
            z-index: 100;
            opacity: 0;
            animation: fadeInFinal 1s ease-in-out forwards;
        }

        @keyframes fadeInFinal {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .final-screen img {
            width: 300px;
            animation: popIn 1s ease-in-out;
        }

        .final-screen p {
            font-size: 22px;
            color: #ff1493;
            font-weight: bold;
            margin-top: 10px;
        }

        @keyframes popIn {
            0% { transform: scale(0.5); opacity: 0; }
            100% { transform: scale(1); opacity: 1; }
        }

    </style>
</head>
<body>

    <div class="background"></div>

    <div class="container">
        <div class="speech-bubble" onclick="confirmIdentity()">💌 Hai, ada surat buat kamu!</div>
    </div>

    <!-- Popup Konfirmasi Identitas -->
    <div class="popup" id="confirmPopup">
        <p>Apakah benar ini Liona? 🤔</p>
        <button class="button" onclick="showLetter()">Iya</button>
        <button class="button" onclick="notLiona()">Tidak</button>
    </div>

    <!-- Popup Surat untuk Liona -->
    <div class="popup" id="letterPopup">
        <p>💖 Selamat Hari Valentine, Sayangku! 💖<br>  
        Aku mencintaimu lebih dari yang bisa kau bayangkan. Semoga kita selalu bersama selamanya! 💞</p>
        <button class="button" onclick="showFinalScreen()">OK</button>
    </div>

    <!-- Popup untuk yang bukan Liona -->
    <div class="popup" id="notLionaPopup">
        <p>😢 Maaf, surat ini bukan untukmu...<br>
        Tapi semoga kamu juga mendapatkan cinta dan kebahagiaan hari ini! 💕</p>
        <button class="button" onclick="closePopup('notLionaPopup')">OK</button>
    </div>

    <!-- Tampilan akhir -->
    <div class="final-screen" id="finalScreen">
        <img src="https://i.pinimg.com/originals/71/f7/72/71f77267391e65d770205299a5feab5e.gif" alt="Beruang Peluk">
        <p>I'll always love you, Liona ❤️</p>
    </div>

    <script>
        function confirmIdentity() {
            document.getElementById('confirmPopup').style.display = 'block';
        }

        function showLetter() {
            document.getElementById('confirmPopup').style.display = 'none';
            document.getElementById('letterPopup').style.display = 'block';
        }

        function notLiona() {
            document.getElementById('confirmPopup').style.display = 'none';
            document.getElementById('notLionaPopup').style.display = 'block';
        }

        function showFinalScreen() {
            document.getElementById("letterPopup").style.display = "none";
            
            // Tampilkan layar akhir dengan animasi
            let finalScreen = document.getElementById("finalScreen");
            finalScreen.style.display = "flex";
            setTimeout(() => {
                finalScreen.style.opacity = "1";
            }, 50);
        }

        function closePopup(popupId) {
            document.getElementById(popupId).style.display = 'none';
        }
    </script>

</body>
</html><!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surat Valentine untuk Liona</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Patrick+Hand&display=swap');

        body {
            font-family: 'Patrick Hand', cursive;
            text-align: center;
            background-color: #ffecf2;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
            position: relative;
            overflow: hidden;
        }

        .background {
            position: fixed;
            width: 100%;
            height: 100%;
            background: url('https://i.pinimg.com/originals/4d/c9/da/4dc9da45f9b0b6fa4c957e644a25833b.jpg') no-repeat center center/cover;
            z-index: -1;
        }

        .container {
            text-align: center;
            position: relative;
            background: rgba(255, 240, 245, 0.9);
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0px 0px 10px rgba(0,0,0,0.3);
            z-index: 1;
        }

        .speech-bubble {
            background-color: #ffb6c1;
            padding: 15px 25px;
            border-radius: 20px;
            display: inline-block;
            font-size: 20px;
            font-weight: bold;
            box-shadow: 2px 2px 5px rgba(0,0,0,0.2);
            margin-bottom: 20px;
            cursor: pointer;
            transition: transform 0.3s ease-in-out;
        }

        .speech-bubble:hover {
            transform: scale(1.1);
        }

        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: #fffaf0;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0px 0px 10px rgba(0,0,0,0.3);
            text-align: center;
            width: 80%;
            max-width: 400px;
            opacity: 0;
            animation: fadeIn 0.5s ease-in-out forwards;
            z-index: 10;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translate(-50%, -55%); }
            to { opacity: 1; transform: translate(-50%, -50%); }
        }

        .popup p {
            font-size: 18px;
            color: #333;
            margin: 15px 0;
        }

        .button {
            background-color: #ff69b4;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-size: 16px;
            transition: 0.3s ease-in-out;
            margin: 5px;
        }

        .button:hover {
            background-color: #ff1493;
        }

        .final-screen {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: white;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            text-align: center;
            z-index: 100;
            opacity: 0;
            animation: fadeInFinal 1s ease-in-out forwards;
        }

        @keyframes fadeInFinal {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .final-screen img {
            width: 300px;
            animation: popIn 1s ease-in-out;
        }

        .final-screen p {
            font-size: 22px;
            color: #ff1493;
            font-weight: bold;
            margin-top: 10px;
        }

        @keyframes popIn {
            0% { transform: scale(0.5); opacity: 0; }
            100% { transform: scale(1); opacity: 1; }
        }

    </style>
</head>
<body>

    <div class="background"></div>

    <div class="container">
        <div class="speech-bubble" onclick="confirmIdentity()">💌 Hai, ada surat buat kamu!</div>
    </div>

    <!-- Popup Konfirmasi Identitas -->
    <div class="popup" id="confirmPopup">
        <p>Apakah benar ini Liona? 🤔</p>
        <button class="button" onclick="showLetter()">Iya</button>
        <button class="button" onclick="notLiona()">Tidak</button>
    </div>

    <!-- Popup Surat untuk Liona -->
    <div class="popup" id="letterPopup">
        <p>💖 Selamat Hari Valentine, Sayangku! 💖<br>  
        Aku mencintaimu lebih dari yang bisa kau bayangkan. Semoga kita selalu bersama selamanya! 💞</p>
        <button class="button" onclick="showFinalScreen()">OK</button>
    </div>

    <!-- Popup untuk yang bukan Liona -->
    <div class="popup" id="notLionaPopup">
        <p>😢 Maaf, surat ini bukan untukmu...<br>
        Tapi semoga kamu juga mendapatkan cinta dan kebahagiaan hari ini! 💕</p>
        <button class="button" onclick="closePopup('notLionaPopup')">OK</button>
    </div>

    <!-- Tampilan akhir -->
    <div class="final-screen" id="finalScreen">
        <img src="https://i.pinimg.com/originals/71/f7/72/71f77267391e65d770205299a5feab5e.gif" alt="Beruang Peluk">
        <p>I'll always love you, Liona ❤️</p>
    </div>

    <script>
        function confirmIdentity() {
            document.getElementById('confirmPopup').style.display = 'block';
        }

        function showLetter() {
            document.getElementById('confirmPopup').style.display = 'none';
            document.getElementById('letterPopup').style.display = 'block';
        }

        function notLiona() {
            document.getElementById('confirmPopup').style.display = 'none';
            document.getElementById('notLionaPopup').style.display = 'block';
        }

        function showFinalScreen() {
            document.getElementById("letterPopup").style.display = "none";
            
            // Tampilkan layar akhir dengan animasi
            let finalScreen = document.getElementById("finalScreen");
            finalScreen.style.display = "flex";
            setTimeout(() => {
                finalScreen.style.opacity = "1";
            }, 50);
        }

        function closePopup(popupId) {
            document.getElementById(popupId).style.display = 'none';
        }
    </script>

</body>
</html>
