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

        /* Main Content */
        #main-content {
            opacity: 1;
            display: block;
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

        /* Journey List */
        .journey-list {
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 4px 20px rgba(224, 82, 117, 0.1);
            margin-bottom: 60px;
        }
        .journey-item {
            margin-bottom: 25px;
            border-left: 3px solid var(--primary-pink);
            padding-left: 15px;
        }
        .journey-title {
            font-weight: bold;
            color: var(--dark-pink);
            margin-bottom: 5px;
        }

        /* Gallery Grid */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 25px;
            margin-bottom: 60px;
        }

        .pho
