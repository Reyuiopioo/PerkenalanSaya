<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Perkenalan Diri</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f8ff;
            text-align: center;
            margin: 0;
            padding: 50px;
        }
        .fade {
            opacity: 0;
            transform: scale(0.8);
            transition: opacity 0.8s ease, transform 0.8s ease;
        }
        .show {
            opacity: 1;
            transform: scale(1);
        }
        .content {
            font-size: 2em;
            margin: 20px 0;
            display: inline-block;
            filter: blur(10px);
            transition: filter 0.8s ease;
        }
        .show-filter {
            filter: blur(0);
        }
    </style>
</head>
<body>

    <div id="intro" class="content fade">Turama T nya apa? Teknik dan Teknologi</div>
    <div id="name" class="content fade">Saya Turama!</div>
    <div id="origin" class="content fade">Saya dari kelas 9B.</div>
    <div id="hobby" class="content fade">Nomor absen: 12.</div>
    <div id="goal" class="content fade">Saat ini, saya fokus pada pendidikan.</div>
    <div id="future" class="content fade">Saya berharap dapat jadi lebih baik.</div>
    <div id="thankyou" class="content fade">Terima kasih sudah mengenal saya!</div>

    <script>
        const elements = [
            'intro',
            'name',
            'origin',
            'hobby',
            'goal',
            'future',
            'thankyou'
        ];

        let index = 0;

        function showNext() {
            if (index < elements.length) {
                const element = document.getElementById(elements[index]);
                element.classList.add('show');
                element.classList.add('show-filter');
                index++;
                setTimeout(showNext, 3000); // Ganti setiap 3 detik
            }
        }

        showNext();
    </script>

</body>
</html>
