# Project-X
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Легенды</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: white;
            color: black;
            margin: 0;
            padding: 0;
            transition: background-color 0.3s, color 0.3s;
        }

        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: black;
            padding: 15px;
            color: white;
        }

        .menu-icon, .search-icon, .moon-icon {
            cursor: pointer;
        }

        .menu {
            position: absolute;
            top: 0;
            left: -200px;
            width: 200px;
            background-color: black;
            height: 100%;
            padding-top: 60px;
            color: white;
            transition: left 0.3s;
        }

        .menu ul {
            list-style: none;
            padding: 0;
        }

        .menu li {
            padding: 10px;
            text-align: center;
        }

        .menu li:hover {
            background-color: #555;
        }

        .circle-button {
            display: block;
            width: 150px;
            height: 150px;
            background-color: red;
            color: black;
            border-radius: 50%;
            border: none;
            font-size: 20px;
            font-weight: bold;
            cursor: pointer;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        #image-popup {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
        }

        #image-popup img {
            max-width: 90%;
            max-height: 90%;
        }

        .dark-mode {
            background-color: black;
            color: white;
        }
    </style>
</head>
<body>

    <!-- Шапка сайта -->
    <header>
        <div class="menu-icon" onclick="toggleMenu()">☰ MENU</div>
        <div>ЛЕГЕНДЫ</div>
        <div class="moon-icon" onclick="toggleTheme()">🌙</div>
    </header>

    <!-- Меню -->
    <div id="menu" class="menu">
        <ul>
            <li>Видео</li>
            <li>Фото</li>
            <li>Амир байдын баласы</li>
            <li>Асан дотер</li>
            <li>Кука алкаш</li>
        </ul>
    </div>

    <!-- Центральная кнопка -->
    <button class="circle-button" onclick="showImage()">НЕ НАЖИМАЙ</button>

    <!-- Всплывающее окно с изображением -->
    <div id="image-popup" onclick="hideImage()">
        <img src="/mnt/data/0BE7B379-7998-4E72-A29B-E9525B5A6C21.jpeg" alt="Изображение">
    </div>

    <script>
        // Функция для показа и скрытия меню
        function toggleMenu() {
            var menu = document.getElementById('menu');
            if (menu.style.left === '0px') {
                menu.style.left = '-200px';
            } else {
                menu.style.left = '0px';
            }
        }

        // Функция для показа изображения
        function showImage() {
            document.getElementById('image-popup').style.display = 'flex';
        }

        // Функция для скрытия изображения
        function hideImage() {
            document.getElementById('image-popup').style.display = 'none';
        }

        // Функция для переключения темы
        function toggleTheme() {
            document.body.classList.toggle('dark-mode');
        }
    </script>
</body>
</html>
