<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday My Love ❤️</title>
    <style>
        :root {
            --primary-color: #ff477e;
            --secondary-color: #ff85a1;
            --bg-color: #fff0f3;
            --text-color: #4a4a4a;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            overflow-x: hidden;
        }

        /* --- Fullpage Sections --- */
        section {
            min-height: 100vh;
            width: 100vw;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 40px 20px;
            text-align: center;
            position: relative;
        }

        h2 {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 30px;
        }

        /* --- 1. Birthday Cake & Candle Animation --- */
        #birthday-intro {
            background: linear-gradient(135deg, #ffe5ec, #ffc2d1);
        }

        .cake-container {
            position: relative;
            margin-bottom: 30px;
        }

        /* Pure CSS Candle & Flame Animation */
        .candle {
            width: 16px;
            height: 60px;
            background: linear-gradient(to top, #ffb3c1, #fff);
            border-radius: 4px;
            margin: 0 auto;
            position: relative;
        }

        .flame {
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
            width: 14px;
            height: 24px;
            background: #ffb703;
            border-radius: 50% 50% 20% 20%;
            box-shadow: 0 0 10px #ffb703, 0 0 20px #fb8500;
            animation: flicker 1s ease-in-out infinite alternate;
        }

        .cake-text {
            font-size: 2.5rem;
            color: var(--primary-color);
            font-weight: bold;
            margin-top: 20px;
            animation: popIn 1.5s ease;
        }

        /* --- 2. Home & Countdown --- */
        #home {
            background-color: #fff0f3;
        }

        .countdown-container {
            background: white;
            padding: 35px 40px;
            border-radius: 30px;
            box-shadow: 0 10px 30px rgba(255, 71, 126, 0.15);
            margin-top: 20px;
            max-width: 500px;
            width: 90%;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        /* Couple Image Styling */
        .couple-pic {
            width: 130px;
            height: 130px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--secondary-color);
            margin-bottom: 20px;
            box-shadow: 0 8px 20px rgba(255, 71, 126, 0.2);
        }

        #timer {
            font-size: 1.6rem;
            font-weight: bold;
            color: var(--primary-color);
            margin-top: 15px;
            line-height: 1.4;
        }

        /* --- 3. Memory Gallery --- */
        #gallery {
            background-color: #ffe5ec;
        }

        .gallery-container {
            display: flex;
            flex-direction: column;
            gap: 40px;
            width: 100%;
            max-width: 600px;
        }

        .gallery-card {
            background: white;
            padding: 20px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
            transition: transform 0.4s;
        }

        .gallery-card:hover {
            transform: scale(1.03) rotate(1deg);
        }

        .gallery-card img {
            width: 100%;
            max-height: 550px;
            object-fit: cover;
            border-radius: 15px;
        }

        .gallery-caption {
            margin-top: 15px;
            font-size: 1.1rem;
            font-style: italic;
            color: #555;
            line-height: 1.4;
        }

        /* --- 4. Love Letter --- */
        #letter {
            background-color: #fff0f3;
        }

        .btn {
            background: var(--primary-color);
            color: white;
            border: none;
            padding: 15px 35px;
            font-size: 1.2rem;
            border-radius: 30px;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(255, 71, 126, 0.4);
            transition: 0.3s;
        }

        .btn:hover {
            background: #ff0a54;
            transform: translateY(-3px);
        }

        .hidden-letter {
            display: none;
            max-width: 550px;
            width: 90%;
            background: white;
            padding: 35p
