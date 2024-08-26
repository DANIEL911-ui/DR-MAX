<!DOCTYPE html>
<html lang="sk">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registrácia klubovej kartičky Dr.Max</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f5f5f5; /* Svetlošedé pozadie pre kontrast */
        }
        .container {
            max-width: 500px;
            margin: auto;
            background-color: #ffffff;
            padding: 20px;
            border-radius: 5px;
            border-top: 10px solid #7db343; /* Zelený horný okraj */
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: #4d4d4d; /* Tmavošedá farba pre text */
        }
        input[type="text"], input[type="date"], input[type="email"], input[type="tel"], input[type="number"], input[type="checkbox"], input[type="submit"] {
            width: 100%;
            padding: 10px;
            margin: 5px 0 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        input[type="submit"] {
            background-color: #7db343; /* Zelené tlačidlo */
            color: white;
            cursor: pointer;
            border: none;
        }
        input[type="submit"]:hover {
            background-color: #6aa535; /* Tmavšia zelená pri hover */
        }
        .header {
            text-align: center;
            margin-bottom: 20px;
        }
        .header img {
            width: 150px; /* Nastaviť šírku loga */
        }
    </style>
</head>
<body>

<div class="container">
    <div class="header">
        <img src="https://www.drmax.sk/images/logo.svg" alt="Logo Dr.Max">
        <h2 style="color: #7db343;">Registrácia klubovej kartičky Dr.Max</h2>
    </div>
    <form id="registrationForm">
        <div class="form-group">
            <label for="cardNumber">Číslo karty:</label>
            <input type="number" id="cardNumber" name="cardNumber" required>
        </div>
        <div class="form-group">
            <label for="name">Meno:</label>
            <input type="text" id="name" name="name" required>
        </div>
        <div class="form-group">
            <label for="surname">Priezvisko:</label>
            <input type="text" id="surname" name="surname" required>
        </div>
        <div class="form-group">
            <label for="birthdate">Dátum narodenia:</label>
            <input type="date" id="birthdate" name="birthdate" required>
        </div>
        <div class="form-group">
            <label for="address">Bydlisko:</label>
            <input type="text" id="address" name="address" required>
        </div>
        <div class="form-group">
            <label for="phone">Tel. číslo:</label>
            <input type="tel" id="phone" name="phone" required pattern="[0-9]{3} [0-9]{3} [0-9]{3}">
        </div>
        <div class="form-group">
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>
        </div>
        <div class="form-group">
            <label for="signature">Podpis:</label>
            <input type="text" id="signature" name="signature" required>
        </div>
        <div class="form-group">
            <label for="registered">Zaregistrovaný:</label>
            <input type="checkbox" id="registered" name="registered">
        </div>
        <div class="form-group">
            <input type="submit" value="Vytvoriť kartičku">
        </div>
    </form>
</div>

<script>
    document.getElementById('registrationForm').addEventListener('submit', function(event) {
        event.preventDefault(); // Zabraň odoslaniu formulára

        // Validácia vstupov
        const cardNumber = document.getElementById('cardNumber').value;
        const name = document.getElementById('name').value;
        const surname = document.getElementById('surname').value;
        const birthdate = document.getElementById('birthdate').value;
        const address = document.getElementById('address').value;
        const phone = document.getElementById('phone').value;
        const email = document.getElementById('email').value;
        const signature = document.getElementById('signature').value;
        const registered = document.getElementById('registered').checked;

        if (!cardNumber || !name || !surname || !birthdate || !address || !phone || !email || !signature) {
            alert('Vyplňte všetky polia!');
            return;
        }

        // Tu môžeš pridať ďalšie kroky na spracovanie formulára
        alert('Kartička bola úspešne vytvorená! Stav zaregistrovania: ' + (registered ? 'Áno' : 'Nie'));
    });
</script>

</body>
</html>
