<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Special Gift</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f8ff;
            font-family: Arial, sans-serif;
            flex-direction: column;
            text-align: center;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 20px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #ff69b4;
        }
        .buttons {
            margin-top: 20px;
        }
        .btn {
            padding: 10px 20px;
            font-size: 18px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: 0.3s;
        }
        .yes {
            background-color: #4CAF50;
            color: white;
        }
        .yes:hover {
            background-color: #45a049;
        }
        .no {
            background-color: #ff4747;
            color: white;
            position: absolute;
        }
        .panda {
            width: 100px;
            position: absolute;
            bottom: 10px;
            animation: fidget 2s infinite;
        }
        @keyframes fidget {
            0%, 100% { transform: rotate(0); }
            25% { transform: rotate(-10deg); }
            50% { transform: rotate(10deg); }
            75% { transform: rotate(-5deg); }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Will you accept the gift?</h1>
        <div class="buttons">
            <button class="btn yes" onclick="alert('Yay! 🎁')">Yes</button>
            <button class="btn no" id="noBtn">No</button>
        </div>
    </div>
    <img src="https://i.imgur.com/5vDVTUI.png" class="panda" alt="Cute Panda">
    <script>
        const noBtn = document.getElementById("noBtn");
        
        noBtn.addEventListener("mouseover", function() {
            const x = Math.random() * (window.innerWidth - noBtn.clientWidth);
            const y = Math.random() * (window.innerHeight - noBtn.clientHeight);
            noBtn.style.left = `${x}px`;
            noBtn.style.top = `${y}px`;
        });
    </script>
</body>
</html>
