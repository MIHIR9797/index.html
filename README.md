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
                    <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAsICAgICAQDAgQECwsIDQ0NCA0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ3/2wBDAQ0LCw0ODRIODhINDg4OEhINDhISEhINDhISEhINDhISEhINDhISEhINDhISEhINDhISEhINDhISEhINDhISEhL/wAARCAH0A7IDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZnaGlqc3R1dnd4eXqGg4SFhoeIiYqSk5SVl5YEMjY0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVl5YGR4hJSlNUVVZXWFlaY2RlZmdoaWpzdHV2d3h5eoKDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uLj5OXm5+jp6vExYGHiImKi4yNjoCFiJWElQCFiY2Sk5SVlpeYmZqadnaGlqc3R1dnd4eXqGg4SFhoeIiYqSk5SVl5YGR4hJSlNUVVZXWFlaY2RlZmdoaWpzdHV2d3h5eoKDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/9oADAMBAAIRAxE6xlpSDR6/58UfXj8v86AFI6D3paTqRjH9KCP8OaBhinD3pnofX8v8KXoT09D2/GgCSgdc1GMZ5/T2pwJxnGOnHpigCXPGO1LUYx/nn6Uo6kfzoAlGe1KCPpTM8HGePrQM4H8+OnFAEuQTxTvrUKnPPrTgfzH1NAEuD607BwOP8KZnofX/Cl9Ppn8v8KAJOvU/yowB6U0D8BScDrg/Qen60ALwRkdfzozjr7e3/ANekoP6+2KAFI7Ggeuf8KQE56A/r6UvGMHmgBMZ9wPywKUfL7H9PrSc85znPr60D3yevIzz7UAODHGOuPTA9aepB9jUIxk+2PpTxnPPrQA/gH3oxx3qMfXP6UoOfpnp2PegBcnGO2fzpce9R7u/0Ape3OfT8PzoAcevUnHPrSjrgU3Prkn86XPvjjigBeBzz3PofpTuCcHpnP+NMGQMcnvzz607PXPPY+xoAeMdDyefrR6DP89PamLnjOfqOvpTx7fn/iaAHDB54Prnv9fWnjrkD39fxpgOfbn69vxpwwenp74/8... [truncated for space] ... 06f6ff3df8ff3df3ff8ff3f/9k=">
                    <p>A beautiful memory...</p>
                </div>
            </div>

        </div>
    </div>

    <script>
        function checkPassword() {
            const passwordInput = document.getElementById('password-input').value.trim();
            const errorMsg = document.getElementById('error-msg');
            const passwordScreen = document.getElementById('password-screen');
            const mainContent = document.getElementById('main-content');

            // Setting 2506 as the official correct password
            if (passwordInput === '2506') {
                // Fade out password overlay
                passwordScreen.style.opacity = '0';
                passwordScreen.style.visibility = 'hidden';
                
                // Transition inside page elements smoothly
                mainContent.style.display = 'block';
                setTimeout(() => {
                    mainContent.style.opacity = '1';
                    document.body.style.overflow = 'auto'; // Restores vertical scrolling
                }, 50);
            } else {
                errorMsg.innerText = 'Incorrect Password. Try again! 😢';
                document.getElementById('password-input').value = '';
            }
        }

        // Listens for keyboard actions
        function handleKeyPress(event) {
            if (event.key === 'Enter') {
                checkPassword();
            }
        }
    </script>
</body>
</html>

