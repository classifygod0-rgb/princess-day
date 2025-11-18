<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Princess Day for My Wifey</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #ffe6f2;
            color: #333;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
        }
        .slide {
            display: none;
            width: 100%;
            max-width: 400px;
            padding: 20px;
            box-sizing: border-box;
            text-align: center;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            margin: 10px;
        }
        .slide.active {
            display: block;
        }
        .letter {
            font-size: 18px;
            line-height: 1.6;
            margin-bottom: 20px;
        }
        .pictures {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin: 20px 0;
        }
        .picture {
            width: 150px;
            height: 150px;
            border: 5px solid #ff69b4;
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }
        .picture img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .flowers {
            position: absolute;
            top: -10px;
            left: -10px;
            right: -10px;
            bottom: -10px;
            background: url('https://example.com/flowers.png') repeat; /* Replace with actual flower image URL */
            pointer-events: none;
            z-index: -1;
        }
        .music-container {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin: 20px 0;
        }
        .song {
            border: 3px solid #ff1493;
            border-radius: 10px;
            padding: 10px;
            background-color: #fff0f5;
        }
        iframe {
            width: 100%;
            height: 200px;
            border: none;
            border-radius: 5px;
        }
        button {
            background-color: #ff69b4;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            border-radius: 5px;
            cursor: pointer;
            margin: 10px;
        }
        button:hover {
            background-color: #ff1493;
        }
        .title {
            font-size: 24px;
            font-weight: bold;
            color: #ff69b4;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <div id="slide1" class="slide active">
        <div class="title">Princess Day</div>
        <div class="letter">
            My dearest Meri sabse Pyaari Pujaa jii,<br><br>
            I wanted to take a moment to tell you how much I love you. You are the light of my life, my everything. Your smile brightens my day, and your love makes every moment special. Happy Princess Day, my love!<br><br>
            With all my heart,<br>Your loving husband
        </div>
        <button onclick="nextSlide(1)">Next</button>
    </div>

    <div id="slide2" class="slide">
        <div class="title">Our Music and Memories</div>
        <div class="music-container">
            <div class="song">
                <p>Song 1: Special for You</p>
                <iframe src="https://www.youtube.com/embed/LH9REAV5UzU?start=103" allowfullscreen></iframe>
            </div>
            <div class="song">
                <p>Song 2: Our Love Song</p>
                <iframe src="https://www.youtube.com/embed/Bn76WLJii2g?start=102" allowfullscreen></iframe>
            </div>
            <div class="song">
                <p>Song 3: Forever Together</p>
                <iframe src="https://www.youtube.com/embed/TlrNxJqODBc?start=8" allowfullscreen></iframe>
            </div>
        </div>
        <div class="pictures">
            <div class="picture">
                <div class="flowers"></div>
                <img src="https://image2url.com/images/1763443324480-571fa192-cd1a-4527-8492-aabf37c89473.jpg" alt="Cute Pic 1"> <!-- Replace with actual image URL -->
            </div>
            <div class="picture">
                <div class="flowers"></div>
                <img src="https://image2url.com/images/1763443394362-a9cce80a-e32a-4d6b-a837-afa68f045a93.jpg" alt="Cute Pic 2"> <!-- Replace with actual image URL -->
            </div>
        </div>
        <button onclick="nextSlide(2)">Next</button>
    </div>

    <div id="slide3" class="slide">
        <div class="title">Our Precious Moments</div>
        <div class="pictures">
            <div class="picture">
                <img src="https://image2url.com/images/1763442369663-b6711193-2747-4973-acb7-2e4b4c462c4e.jpg" alt="Moment 1"> <!-- Replace with actual image URL -->
            </div>
            <div class="picture">
                <img src="https://image2url.com/images/1763442479189-30afe8ad-ee90-4545-953a-e1af340f9f43.jpg" alt="Moment 2"> <!-- Replace with actual image URL -->
            </div>
        </div>
        <button onclick="nextSlide(3)">Next</button>
    </div>

    <div id="slide4" class="slide">
        <div class="title">Duniya ki sabse zyada Khoobsurat Biwi</div>
        <div class="pictures">
            <div class="picture">
                <img src="https://image2url.com/images/1763442587515-66f9d53a-97a6-4e4e-8dca-06ceaa3215a2.jpg" alt="Her Pic 1"> <!-- Replace with actual image URL -->
            </div>
            <div class="picture">
                <img src="https://image2url.com/images/1763442643708-422d35dc-3428-49a1-8afb-825dde64ab29.jpg" alt="Her Pic 2"> <!-- Replace with actual image URL -->
            </div>
        </div>
        <div class="letter">
            My beautiful Pujaa jii,<br><br>
            Thank you for all the efforts you put in every day and for always supporting me. You are my rock, my inspiration, and the most beautiful wife in the world. I love you endlessly.<br><br>
            Forever yours,<br>Your devoted husband
        </div>
        <button onclick="restart()">Restart</button>
    </div>

    <script>
        let currentSlide = 1;
        const totalSlides = 4;

        function nextSlide(current) {
            document.getElementById('slide' + current).classList.remove('active');
            currentSlide++;
            if (currentSlide <= totalSlides) {
                document.getElementById('slide' + currentSlide).classList.add('active');
            }
        }

        function restart() {
            document.querySelectorAll('.slide').forEach(slide => slide.classList.remove('active'));
            currentSlide = 1;
            document.getElementById('slide1').classList.add('active');
        }
    </script>
</body>
</html>
