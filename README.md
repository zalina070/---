<!DOCTYPE html>
<html lang="ru">

<head>
    <meta charset="UTF-8">
    <title>Калькулятор возраста</title>
</head>

<body>
    <h2>Калькулятор возраста</h2>

    <label for="birthYear">Введите год рождения:</label>
    <input type="number" id="birthYear" placeholder="Например, 2008">

    <button onclick="calculateAge()">Вычислить возраст</button>

    <p id="result"></p>

    <script>
        function calculateAge() {
            const currentYear = new Date().getFullYear(); // текущий год
            const birthYear = parseInt(document.getElementById('birthYear').value);

            if (isNaN(birthYear) || birthYear > currentYear || birthYear < 1900) {
                document.getElementById('result').textContent = "Пожалуйста, введите корректный год рождения.";
                return;
            }

            const age1 = currentYear - birthYear;
            const age2 = age1 - 1;

            document.getElementById('result').textContent = `Они либо ${age2}, либо ${age1}`;
        }
    </script>
</body>

</html># ---
