<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine Confession for Andine</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #ffe6f2;
            color: #333;
            text-align: center;
            padding: 20px;
            transition: all 0.5s ease;
        }
        .page {
            display: none;
        }
        .page.active {
            display: block;
        }
        button {
            background-color: #ff69b4;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            margin: 10px;
            border-radius: 5px;
        }
        button:hover {
            background-color: #ff1493;
        }
        input {
            padding: 10px;
            font-size: 16px;
            margin: 10px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        .options {
            margin: 20px;
        }
        .option {
            display: inline-block;
            padding: 10px 20px;
            margin: 10px;
            background-color: #f0f0f0;
            border-radius: 5px;
            cursor: pointer;
        }
        .option.selected {
            background-color: #ff69b4;
            color: white;
        }
        .letter {
            background-color: #fff;
            border: 2px solid #ff69b4;
            padding: 20px;
            margin: 20px auto;
            width: 300px;
            cursor: pointer;
            position: relative;
        }
        .letter:hover {
            box-shadow: 0 0 10px rgba(0,0,0,0.2);
        }
        .reveal {
            display: none;
            margin-top: 20px;
        }
        .love {
            font-size: 48px;
            color: #ff1493;
            opacity: 0;
            animation: fadeIn 2s forwards;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
    </style>
</head>
<body>
    <div id="page1" class="page active">
        <h1>Hai Andine!</h1>
        <button onclick="nextPage(2)">Start</button>
    </div>

    <div id="page2" class="page">
        <h2>Perasaan mu ke aku 1-100 berapa sih?</h2>
        <input type="number" id="feeling" min="1" max="100" placeholder="Masukkan angka 1-100">
        <button onclick="checkFeeling()">Lanjut</button>
    </div>

    <div id="page3" class="page">
        <h2>Kamu kalau aku tembak mau atau tidak?</h2>
        <div class="options">
            <div class="option" id="iya" onclick="selectOption('iya')">Iya</div>
            <div class="option" id="tidak" onclick="selectOption('tidak')">Tidak</div>
        </div>
        <button id="lanjutkan" style="display:none;" onclick="nextPage(4)">Lanjutkan</button>
    </div>

    <div id="page4" class="page">
        <div class="letter" onclick="revealLetter()">
            <p>Click di sini</p>
            <div class="reveal" id="revealText">I will keep trying, because I like you</div>
        </div>
        <div class="love" id="loveText" style="display:none;">I Love You</div>
        <button id="lanjutkanLove" style="display:none;" onclick="nextPage(5)">Lanjutkan</button>
    </div>

    <div id="page5" class="page">
        <h2>Semangat ya sekolanya kamu tuh random banget kalau di sekolah</h2>
        <button onclick="nextPage(6)">Lanjut</button>
    </div>

    <div id="page6" class="page">
        <h2>Aku suka kok ke randoman mu, jangan gampang insecure ya karena semua itu sempurna</h2>
        <button onclick="nextPage(7)">Lanjut</button>
    </div>

    <div id="page7" class="page">
        <h2>Kamu tuh kayak lagu Sempurna tau nggak sih, hmm coba deh cari di Spotify itu ngambarin kamu banget loh</h2>
        <button onclick="endConfession()">Selesai</button>
    </div>

    <script>
        function nextPage(pageNum) {
            try {
                document.querySelectorAll('.page').forEach(page => page.classList.remove('active'));
                const targetPage = document.getElementById('page' + pageNum);
                if (targetPage) {
                    targetPage.classList.add('active');
                } else {
                    console.error('Page ' + pageNum + ' not found');
                }
            } catch (e) {
                console.error('Error in nextPage:', e);
            }
        }

        function checkFeeling() {
            try {
                const feelingInput = document.getElementById('feeling');
                const feeling = parseInt(feelingInput.value);
                if (isNaN(feeling) || feeling < 50 || feeling > 100) {
                    alert('Jawaban harus angka antara 50-100 dan tidak boleh kosong!');
                    feelingInput.focus();
                } else {
                    nextPage(3);
                }
            } catch (e) {
                console.error('Error in checkFeeling:', e);
            }
        }

        function selectOption(choice) {
            try {
                document.querySelectorAll('.option').forEach(opt => opt.classList.remove('selected'));
                document.getElementById(choice).classList.add('selected');
                if (choice === 'iya') {
                    document.getElementById('lanjutkan').style.display = 'inline-block';
                } else if (choice === 'tidak') {
                    alert('Haha, aku tahu kamu bohong! Lanjut ya?');
                    document.getElementById('lanjutkan').style.display = 'inline-block';
                }
            } catch (e) {
                console.error('Error in selectOption:', e);
            }
        }

        function revealLetter() {
            try {
                document.getElementById('revealText').style.display = 'block';
                setTimeout(() => {
                    document.getElementById('loveText').style.display = 'block';
                    setTimeout(() => {
                        document.getElementById('lanjutkanLove').style.display = 'inline-block';
                    }, 500);
                }, 2000);
            } catch (e) {
                console.error('Error in revealLetter:', e);
            }
        }

        function endConfession() {
            try {
                alert('Terima kasih sudah membaca! Semoga harimu indah, Andine. 💕');
                location.reload();
            } catch (e) {
                console.error('Error in endConfession:', e);
            }
        }
    </script>
</body>
</html>
