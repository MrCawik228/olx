# olx
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Сайт объявлений</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #ff9f00;
            padding: 10px;
            text-align: center;
            color: white;
        }
        .ad-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            padding: 20px;
        }
        .ad-item {
            background-color: white;
            margin: 10px;
            padding: 20px;
            width: 250px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .ad-item img {
            width: 100%;
            height: auto;
            border-radius: 8px;
        }
        .ad-item h3 {
            margin: 10px 0;
        }
        .ad-item p {
            color: gray;
        }
        .ad-item .price {
            font-weight: bold;
            color: #ff9f00;
        }
    </style>
</head>
<body>
    <header>
        <h1>Добро пожаловать на сайт объявлений!</h1>
    </header>

    <div class="ad-list">
        <div class="ad-item">
            <img src="https://via.placeholder.com/250" alt="Объявление 1">
            <h3>Продажа смартфона</h3>
            <p>Продам новый смартфон Samsung Galaxy S20.</p>
            <p class="price">10 000 грн</p>
        </div>
        <div class="ad-item">
            <img src="https://via.placeholder.com/250" alt="Объявление 2">
            <h3>Продаю велосипед</h3>
            <p>Велосипед в хорошем состоянии, почти не использовался.</p>
            <p class="price">2 500 грн</p>
        </div>
        <!-- Можно добавить больше объявлений -->
    </div>

    <footer>
        <p style="text-align: center; padding: 10px; background-color: #ff9f00; color: white;">© 2025 Сайт объявлений</p>
    </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Добавить объявление</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            padding: 20px;
        }
        .form-container {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 500px;
            margin: 0 auto;
        }
        input, textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            border: 1px solid #ddd;
        }
        button {
            padding: 10px 20px;
            background-color: #ff9f00;
            border: none;
            color: white;
            font-size: 16px;
            cursor: pointer;
            border-radius: 5px;
        }
        button:hover {
            background-color: #e68900;
        }
    </style>
</head>
<body>
    <div class="form-container">
        <h2>Добавить объявление</h2>
        <form id="ad-form">
            <label for="title">Заголовок</label>
            <input type="text" id="title" name="title" required>

            <label for="description">Описание</label>
            <textarea id="description" name="description" rows="4" required></textarea>

            <label for="price">Цена</label>
            <input type="number" id="price" name="price" required>

            <label for="image">Изображение URL</label>
            <input type="text" id="image" name="image" required>

            <button type="submit">Разместить объявление</button>
        </form>
    </div>

    <script>
        document.getElementById('ad-form').addEventListener('submit', function(event) {
            event.preventDefault();

            // Получаем данные из формы
            const title = document.getElementById('title').value;
            const description = document.getElementById('description').value;
            const price = document.getElementById('price').value;
            const image = document.getElementById('image').value;

            // Здесь можно добавить логику для отправки данных на сервер или в базу данных

            alert(`Объявление "${title}" успешно добавлено!`);
        });
    </script>
</body>
</html>
