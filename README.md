<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday My Wifeyyy! 🥺💗</title>
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
            color: var(--dark-pink);
        }

        .lock-box h2::after {
            content: none;
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

        .lock-box button {
            background-color: var(--primary-pink);
            color: white;
            border: none;
            padding: 10px 25px;
            font-size: 1rem;
            border-radius: 25px;
            cursor: pointer;
            transition: background 0.3s;
        }

        .lock-box button:hover {
            background-color: var(--dark-pink);
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
            display: none;
            transition: opacity 1s ease;
        }

        /* Hero Section */
        header {
            height: 80vh;
            background: linear-gradient(rgba(255, 117, 151, 0.5), rgba(255, 117, 151, 0.3)), 
                        url('https://images.unsplash.com/photo-1518199266791-5375a83190b7?q=80&w=1200') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.4);
            padding: 20px;
        }

        header h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            line-height: 1.2;
        }

        header p {
            font-size: 1.5rem;
            font-style: italic;
            margin-top: 0;
        }

        .container {
            max-width: 800px;
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

        /* Love Letter Style */
        .love-letter {
            background: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 4px 20px rgba(224, 82, 117, 0.1);
            line-height: 1.8;
            font-size: 1.15rem;
            white-space: pre-line;
            margin-bottom: 60px;
            border-left: 5px solid var(--primary-pink);
        }

        /* Gallery Grid */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-bottom: 60px;
        }

        .photo-card {
            background: white;
            padding: 15px;
            border-radius: 12px;
            box-shadow: 0 6px 20px rgba(0,0,0,0.06);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-align: center;
        }

        .photo-card:hover {
            transform: scale(1.04) rotate(1deg);
            box-shadow: 0 10px 25px rgba(224, 82, 117, 0.15);
        }

        .photo-card img {
            width: 100%;
            height: 340px;
            object-fit: cover;
            border-radius: 8px;
        }

        .photo-card p {
            font-style: italic;
            font-weight: 500;
            margin: 15px 0 5px 0;
            color: var(--dark-pink);
            font-size: 1.1rem;
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
            margin-bottom: 5px;
        }
        
        footer {
            text-align: center;
            padding: 30px;
            color: #888;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <div id="password-screen">
        <div class="lock-box">
            <h2>Enter Password 🔑</h2>
            <p style="font-size: 0.9rem; color:#888; margin-bottom: 15px;">Hint: A special date or phrase only we know!</p>
            <input type="password" id="password-input" placeholder="Password..." onkeypress="handleKeyPress(event)">
            <div id="error-msg"></div>
            <button onclick="checkPassword()">Unlock</button>
        </div>
    </div>

    <div id="main-content">
        <header>
            <h1>Happy birthday my wifeyyy! 🥺💗</h1>
            <p>To the most beautiful person in my life 🙂😭</p>
        </header>

        <div class="container">
            
            <h2>A Message For You</h2>
            <div class="love-letter">
My dear wifey,

I wanted to make something unique to express how much I love you. It took a lott of time but it's definitely worth it if you are happy 👉🏻👈 continuum

Words truly fail to describe how much I love you so I built this little corner of the internet just for us..

Thank you for being mine, supporting me, loving me. You are my best friend, my wifeyy, my soulmate, my everything.. You are the most precious thing of my life..

Forever and always yourss,
<strong>Mihirrr from your heartt 💋</strong>
            </div>

            <h2>Our Beautiful Journey</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-date">The Day We Met</div>
                    <p>Where our incredible story first started...</p>
                </div>
                <div class="timeline-item">
                    <div class="timeline-date">Our Wedding Day (Coming Very Soon In Sha Allah) 💝</div>
                    <p>Our wedding day wish will change into reality very soon in sha Allah, and it would be the best day of my life!</p>
                </div>
            </div>

            <h2>Our Precious Memories</h2>
            <div class="gallery">
                <div class="photo-card">
                    <img src="data:image/jpeg;base64,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
                    
