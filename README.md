<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Paywall</title>
    <style>
        body {
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #000;
      flex-direction: column;
        }

        #paywall {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            color: white;
            padding: 20px;
            z-index: 1;
        }

        .paywall-content {
            background-color: #333;
            border-radius: 10px;
            padding: 20px;
            max-width: 400px;
            margin: 50px auto;
        }

        .hidden {
            display: none;
        }

        .image-container {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
            overflow: hidden;
        }

        .image-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            position: absolute;
            opacity: 0;
            transition: opacity 1s ease-in-out;
        }

        .image-container img.active {
            opacity: 1;
        }

        .chat-widget {
            position: fixed;
            top: 40%;
            left: 30%;
            transform: translate(-50%, -50%);
            width: 450px;
            height: 500px;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            background-color: transparent;
            z-index: 1;
        }
    </style>
</head>
<body>
    <div class="image-container">
        <img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExd2VtcHdiZHpjMmgybTl5eWtvMjdnMnVzbmU3eG80OW5kemJsOGc0NiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/wuU9Hvp5wF7xe/giphy.webp" class="active">
        <img src="https://i.pinimg.com/originals/32/64/5e/32645e1a0642ce7fc4d952dde6e598a8.gif">
        <img src="https://i.giphy.com/1qErVv5GVUac8uqBJU.webp">
        <img src="https://i.giphy.com/BWD3CtcudWL28.webp">
    </div>

    <div class="chat-widget">
        <elevenlabs-convai id="chat-agent" agent-id="sNEfrsQUklzPW2Hu6VGg"></elevenlabs-convai>
        <script src="https://elevenlabs.io/convai-widget/index.js" async></script>
    </div>

    <div id="paywall">
        <div class="paywall-content">
            <h2>Purchase More Conversation Time</h2>
            <p>Select your desired time extension:</p>
            <ul>
                <li>10 minutes: 15 lei - <a href="https://revolut.me/r/9ouIF7WVBU" target="_blank">Pay Now</a></li>
                <li>30 minutes: 25 lei - <a href="https://revolut.me/r/qTzpX33NT1" target="_blank">Pay Now</a></li>
                <li>60 minutes: 50 lei - <a href="https://revolut.me/r/Z0QtuDZnEQ" target="_blank">Pay Now</a></li>
            </ul>
            <p>After payment, enter the code received on Revolut to unlock access:</p>
            <input type="text" id="code-input" placeholder="Enter your code">
            <button onclick="validateCode()">Unlock</button>
            <p id="error-message" class="hidden">Invalid code. Please try again.</p>
        </div>
    </div>

    <script>
        const validCodes = {
            "1234": 10,
            "2345": 30,
            "3456": 60
        };

        const images = document.querySelectorAll('.image-container img');
        let currentIndex = 0;

        function showNextImage() {
            images[currentIndex].classList.remove('active');
            currentIndex = (currentIndex + 1) % images.length;
            images[currentIndex].classList.add('active');
        }

        setInterval(showNextImage, 4000);

        let countdown;

        function showPaywall() {
            document.getElementById('paywall').style.display = 'block';
            const chatAgent = document.getElementById('chat-agent');
            if (chatAgent) {
                chatAgent.setAttribute('agent-id', '');
            }
        }

        function hidePaywall() {
            document.getElementById('paywall').style.display = 'none';
            const chatAgent = document.getElementById('chat-agent');
            if (chatAgent) {
                chatAgent.setAttribute('agent-id', 'sNEfrsQUklzPW2Hu6VGg');
            }
        }

        function validateCode() {
            const code = document.getElementById('code-input').value;
            const errorMessage = document.getElementById('error-message');
            
            if (validCodes[code]) {
                errorMessage.classList.add('hidden');
                hidePaywall();
                startTimer(validCodes[code]);
            } else {
                errorMessage.classList.remove('hidden');
            }
        }

        function startTimer(minutes) {
            const endTime = Date.now() + minutes * 60000;

            if (countdown) clearInterval(countdown);

            countdown = setInterval(() => {
                const timeLeft = endTime - Date.now();

                if (timeLeft <= 0) {
                    clearInterval(countdown);
                    showPaywall();
                }
            }, 1000);
        }

        setTimeout(showPaywall, 10000); // Show paywall after 10 seconds
    </script>
</body>
</html>
