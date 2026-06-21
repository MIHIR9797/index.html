<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To My Beautiful Wife</title>
    <style>
        :root {
            --primary-pink: #ff7597;
            --dark-pink: #e05275;
            --soft-bg: #fff5f7;
            --text-color: #4a4a4a;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--soft-bg);
            color: var(--text-color);
            margin: 0;
            padding: 0;
            overflow: hidden; /* Locks scrolling until unlocked */
        }

        /* Password Overlay Screen */
        #password-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: var(--soft-bg);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            transition: opacity 0.8s ease, visibility 0.8s;
        }

        .lock-box {
            background: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(224, 82, 117, 0.15);
            text-align: center;
            max-width: 350px;
            width: 90%;
        }

        .lock-box h2 {
            margin-top: 0;
            font-size: 1.8rem;
        }

        .lock-box input {
            width: 80%;
            padding: 12px;
            font-size: 1.1rem;
            border: 2px solid #ffd0dc;
            border-radius: 25px;
            text-align: center;
            margin-bottom: 15px;
            outline: none;
            transition: border-color 0.3s;
        }

        .lock-box input:focus {
            border-color: var(--primary-pink);
        }

        #error-msg {
            color: var(--dark-pink);
            font-size: 0.9rem;
            margin-bottom: 10px;
            height: 18px;
        }

        /* Main Content (Hidden until unlocked) */
        #main-content {
            opacity: 0;
            transition: opacity 1s ease;
        }

        /* Hero Section */
        header {
            height: 80vh;
            background: linear-gradient(rgba(255, 117, 151, 0.4), rgba(255, 117, 151, 0.2)), 
                        url('couple-bg.jpg') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.3);
            padding: 20px;
        }

        header h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
        }

        header p {
            font-size: 1.5rem;
            font-style: italic;
            margin-top: 0;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        h2 {
            text-align: center;
            color: var(--dark-pink);
            font-size: 2.2rem;
            margin-bottom: 30px;
            position: relative;
        }

        h2::after {
            content: '❤️';
            display: block;
            font-size: 1.2rem;
            margin-top: 5px;
        }

        /* Gallery Grid */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-bottom: 60px;
        }

        .photo-card {
            background: white;
            padding: 12px;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s ease;
            text-align: center;
        }

        .photo-card:hover {
            transform: scale(1.03) rotate(1deg);
        }

        .photo-card img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            border-radius: 4px;
        }

        .photo-card p {
            font-style: italic;
            margin: 10px 0 0 0;
            color: #666;
        }

        /* Timeline Section */
        .timeline {
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.05);
            margin-bottom: 60px;
        }

        .timeline-item {
            border-left: 3px solid var(--primary-pink);
            padding-left: 20px;
            margin-bottom: 30px;
            position: relative;
        }

        .timeline-item::before {
            content: '✨';
            position: absolute;
            left: -11px;
            top: 0;
            background: var(--soft-bg);
            border-radius: 50%;
            padding: 2px;
        }

        .timeline-date {
            font-weight: bold;
            color: var(--dark-pink);
        }

        /* Surprise Section */
        .surprise-box {
            text-align: center;
            margin-top: 40px;
        }

        .btn {
            background-color: var(--dark-pink);
            color: white;
            border: none;
            padding: 15px 35px;
            font-size: 1.2rem;
            border-radius: 30px;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(224, 82, 117, 0.4);
            transition: background 0.3s, transform 0.2s;
        }

        .btn:hover {
            background-color: #c43b5c;
            transform: translateY(-2px);
        }

        .love-letter {
            display: none;
            background: #fffdf9;
            border-left: 5px solid var(--primary-pink);
            padding: 30px;
            margin-top: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            text-align: left;
            line-height: 1.8;
            font-size: 1.1rem;
        }

        footer {
            text-align: center;
            padding: 40px;
            color: #999;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <div id="password-screen">
        <div class="lock-box">
            <h2>Enter Secret Code 🌹</h2>
            <input type="password" id="password-input" placeholder="Type password here...">
            <div id="error-msg"></div>
            <button class="btn" onclick="checkPassword()">Unlock</button>
        </div>
    </div>

    <div id="main-content">
        <header>
            <h1>Happy Special Day, My Love!</h1>
            <p>To the most beautiful woman in the world, inside and out.</p>
        </header>

        <div class="container">
            <h2>Beautiful Memories</h2>
            <div class="gallery">
                <div class="photo-card">
                    <img src="wife1.jpg" alt="My Beautiful Wife">
                    <p>Your smile lights up my whole world.</p>
                </div>
                <div class="photo-card">
                    <img src="couple1.jpg" alt="Our Moment">
                    <p>One of my absolute favorite days with you.</p>
                </div>
                <div class="photo-card">
                    <img src="couple2.jpg" alt="Another Memory">
                    <p>Forever looks incredibly good with you.</p>
                </div>
            </div>

            <h2>Our Beautiful Journey</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-date">The Day We Met</div>
                    <p>The moment my life changed for the better. I still remember what you wore and how nervous I was!</p>
                </div>
                <div class="timeline-item">
                    <div class="timeline-date">Our Wedding Day</div>
                    <p>The easiest 'Yes' of my life. Walking alongside you as your husband is my greatest honor.</p>
                </div>
                <div class="timeline-item">
                    <div class="timeline-date">Right Now & Forever</div>
                    <p>Every single day, I love you more than the day before. Thank you for being my rock and my home.</p>
                </div>
            </div>

            <div class="surprise-box">
                <h2>A Little Message For You</h2>
                <button class="btn" id="reveal-btn">Click to Open Your Letter</button>
                
                <div class="love-letter" id="love-letter">
                    <p>My Dearest,</p>
                    <p>I wanted to make something unique just to tell you how incredibly special you are to me. Words truly fail to describe how much I love you, so I built this little corner of the internet just for us.</p>
                    <p>Thank you for your kindness, your endless support, and the love you pour into my life every single day. You are my best friend, my soulmate, and my favorite adventure.</p>
                    <p>Forever and always Yours,</p>
                    <p><strong>[Your Name]</strong></p>
                </div>
            </div>
        </div>

        <footer>
            <p>Made with ❤️ by [Your Name] | 2026</p>
        </footer>
    </div>

    <script>
        function checkPassword() {
            const input = document.getElementById('password-input').value;
            const errorMsg = document.getElementById('error-msg');
            const lockScreen = document.getElementById('password-screen');
            const mainContent = document.getElementById('main-content');

            // Password is set to 2506
            if (input === "2506") {
                lockScreen.style.opacity = '0';
                lockScreen.style.visibility = 'hidden';
                mainContent.style.opacity = '1';
                document.body.style.overflow = 'auto'; // Enable scrolling
            } else {
                errorMsg.innerText = "Wrong password, my love! Try again 😉";
            }
        }

        // Allow pressing 'Enter' key to unlock
        document.getElementById('password-input').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                checkPassword();
            }
        });

        // Love Letter Toggle Button
        const btn = document.getElementById('reveal-btn');
        const letter = document.getElementById('love-letter');

        btn.addEventListener('click', () => {
            if (letter.style.display === 'none' || letter.style.display === '') {
                letter.style.display = 'block';
                btn.innerText = 'Close Letter';
                letter.scrollIntoView({ behavior: 'smooth' });
            } else {
                letter.style.display = 'none';
                btn.innerText = 'Click to Open Your Letter';
            }
        });
    </script>
</body>
</html>
