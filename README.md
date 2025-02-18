# horoscope-site![Leonardo_Phoenix_09_A_mystical_and_fascinating_cover_for_a_web_3](https://github.com/user-attachments/assets/bd8bd37f-ce6b-47a2-98a5-5c30c8f9a218)
file:///C:/Users/valer/OneDrive/Документы/index.html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Персональный гороскоп</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
            padding: 20px;
        }
        .container {
            max-width: 400px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        input, button {
            width: 100%;
            margin: 10px 0;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background-color: #007bff;
            color: white;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
        #result {
            margin-top: 20px;
        }
        .premium {
            margin-top: 20px;
            padding: 15px;
            background: #ffcc00;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Получите ваш персональный гороскоп</h2>
        <form id="horoscopeForm">
            <input type="date" id="birthDate" required>
            <input type="time" id="birthTime" required>
            <input type="text" id="birthPlace" placeholder="Место рождения" required>
            <button type="submit">Получить гороскоп</button>
        </form>
        <div id="result"></div>
        <div class="premium">
            <h3>Получите детальный гороскоп!</h3>
            <p>Расшифровка натальной карты, прогнозы на будущее и многое другое.</p>
            <form action="https://pay.alfabank.ru/payment" method="POST">
                <input type="hidden" name="amount" value="299">
                <input type="hidden" name="description" value="Детальный гороскоп">
                <button type="submit">Купить за 299 руб.</button>
            </form>
        </div>
    </div>

    <script>
        document.getElementById('horoscopeForm').addEventListener('submit', function(event) {
            event.preventDefault();
            let date = document.getElementById('birthDate').value;
            let time = document.getElementById('birthTime').value;
            let place = document.getElementById('birthPlace').value;
            
            document.getElementById('result').innerHTML = `Ваш гороскоп рассчитывается... <br>Дата: ${date} <br>Время: ${time} <br>Место: ${place}`;
            
            // Здесь можно добавить логику для расчета гороскопа через API
        });
    </script>
</body>
</html>
