<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trang Yêu Thương</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f0f0;
            margin-top: 50px;
        }
        h1 {
            color: #ff3366;
        }
        button {
            background-color: #ff3366;
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 16px;
            cursor: pointer;
            margin: 10px;
            border-radius: 5px;
        }
        button:hover {
            background-color: #ff6699;
        }
        #message {
            font-size: 20px;
            color: #333;
            margin-top: 20px;
        }
        #game {
            margin-top: 30px;
        }
    </style>
</head>
<body>

    <h1>Chào Em Yêu!</h1>
    
    <!-- Nút 1: Hiển thị thông điệp -->
    <button onclick="showMessage()">Hiển Thị Thông Điệp</button>
    
    <!-- Nút 2: Thay đổi màu nền -->
    <button onclick="changeBackground()">Thay Đổi Màu Nền</button>
    
    <!-- Nút 3: Chơi trò chơi nhỏ -->
    <button onclick="startGame()">Bắt Đầu Trò Chơi</button>

    <div id="message"></div>
    <div id="game"></div>

    <script>
        // Hiển thị thông điệp yêu thương
        function showMessage() {
            document.getElementById('message').innerText = 'Anh yêu Quỳnh Anh nhất trên đời. Yêu em nhất ❤️';
        }

        // Thay đổi màu nền ngẫu nhiên
        function changeBackground() {
            const colors = ['#ffccff', '#00ffff', '#ccffcc', '#ffffcc', '#ff6666'];
            const randomColor = colors[Math.floor(Math.random() * colors.length)];
            document.body.style.backgroundColor = randomColor;
        }

        // Trò chơi nhấn nút để hiển thị một thông điệp vui
        function startGame() {
            document.getElementById('game').innerHTML = `
                <p>Chơi trò chơi nào! Nhấn vào đây để nhận thông điệp đặc biệt:</p>
                <button onclick="revealSecret()">Nhấn vào đây!</button>
            `;
        }

        function revealSecret() {
            alert('Anh là người may mắn nhất vì có em bên cạnh! 💕');
        }
    </script>

</body>
</html>