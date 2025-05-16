<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Telegram Bot Guide</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;

background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: white;
            padding: 1rem;
            text-align: center;
        }
        main {
            padding: 2rem;
            background-color: white;
            margin: 2rem auto;
            max-width: 1000px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1, h2 {
            color: #333;
        }
        pre {
            background-color: #eee;
            padding: 1rem;
            border-radius: 5px;
            overflow-x: auto;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1rem;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
</head>
<body>

<header>
    <h1>Guide to Creating a Telegram Bot with Python</h1>
</header>

<main>
    <h2>Step 1: Create Your Telegram Bot</h2>
    <p>To create a new bot, follow these steps:</p>
    <ol>
        <li>Open <a href="https://t.me/BotFather" target="_blank">BotFather</a> on Telegram.</li>
        <li>Type <code>/newbot</code> and follow the instructions to create a new bot.</li>

       <li>After creating the bot, you will receive a <strong>token</strong>. Keep this safe, as you'll use it in your Python code.</li>
    </ol>

    <h2>Step 2: Install the Required Libraries</h2>
    <p>To interact with Telegram's Bot API, you'll need to install the <code>pyTelegramBotAPI</code> library.</p>
    <pre>
pip install pyTelegramBotAPI
    </pre>

    <h2>Step 3: Write Your Python Code</h2>
    <p>Now that you have your bot token, you can write a simple Python script to get started.</p>
    <pre>
import telebot

TOKEN = 'YOUR_BOT_TOKEN'
bot = telebot.TeleBot(TOKEN)

@bot.message_handler(commands=['start'])
def start(message):
    bot.send_message(message.chat.id, "Hello, welcome to your new Telegram bot!")

bot.polling()
    </pre>

    <h2>Step 4: Run Your Bot</h2>
    <p>Save your code in a file called <code>bot.py</code> and run it:</p>
    <pre>
python bot.py
    </pre>
    <p>Now your bot will start, and you can interact with it on Telegram by typing <code>/start</code>.</p>

    <h2>Step 5: Keep Your Bot Running</h2>
    <p>If you want your bot to run continuously, you can use <strong>screen</strong> or <strong>tmux</strong> in Termux (on Android) to keep the script running even if you close the app.</p>

</main>

<footer>

<p>&copy; 2024 Your Name. All Rights Reserved.</p>
</footer>

</body>
</html>
