# Game-for-my-love
Para mi linda novia. From: Dayanna. To: Génesis
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Juego Romántico para Génesis</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #E8DAEF;
            color: #391848;
            text-align: center;
        }
        .question {
            margin: 20px;
            padding: 20px;
            background-color: #ffcccc;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .question h2 {
            color: #391848;
        }
        .options button {
            background-color: #ff9999;
            border: none;
            padding: 10px 20px;
            margin: 10px;
            border-radius: 5px;
            cursor: pointer;
            color: #391848;
        }
        .options button:hover {
            background-color: #ff6666;
        }
        #result {
            margin-top: 20px;
            font-size: 1.2em;
        }
    </style>
    <script>
        function checkAnswer(question, correctOption) {
            const selectedOption = document.querySelector(`input[name="question${question}"]:checked`).value;
            const result = document.getElementById('result');
            if (selectedOption === correctOption) {
                result.innerHTML += `<p>Pregunta ${question}: ¡Correcto!</p>`;
            } else {
                result.innerHTML += `<p>Pregunta ${question}: Incorrecto. La respuesta correcta es ${correctOption}.</p>`;
            }
        }

        function showImage() {
            const image = document.getElementById('loveImage');
            image.style.display = 'block';
        }
    </script>
</head>
<body>
    <h1>Juego Romántico para Génesis</h1>

    <div class="question">
        <h2>¿Cuál es mi cumpleaños?</h2>
        <div class="options">
            <label>
                <input type="radio" name="question1" value="7 de noviembre del 2006"> 7 de noviembre del 2006
            </label>
            <label>
                <input type="radio" name="question1" value="7 de diciembre del 2006"> 7 de diciembre del 2006
            </label>
        </div>
        <button onclick="checkAnswer(1, '7 de noviembre del 2006')">Comprobar Respuesta</button>
    </div>

    <div class="question">
        <h2>¿Cuáles son los nombres de mis gatas?</h2>
        <div class="options">
            <label>
                <input type="radio" name="question2" value="Luna y Zazha"> Luna y Zazha
            </label>
            <label>
                <input type="radio" name="question2" value="Sol y Estrella"> Sol y Estrella
            </label>
        </div>
        <button onclick="checkAnswer(2, 'Luna y Zazha')">Comprobar Respuesta</button>
    </div>

    <div class="question">
        <h2>¿Qué carrera estoy estudiando?</h2>
        <div class="options">
            <label>
                <input type="radio" name="question3" value="Comercio exterior"> Comercio exterior
            </label>
            <label>
                <input type="radio" name="question3" value="Ingeniería informática"> Ingeniería informática
            </label>
        </div>
        <button onclick="checkAnswer(3, 'Comercio exterior')">Comprobar Respuesta</button>
    </div>

    <div class="question">
        <h2>¿Cuál es el nombre de mi mejor amiga?</h2>
        <div class="options">
            <label>
                <input type="radio" name="question4" value="Marylinn"> Marylinn
            </label>
            <label>
                <input type="radio" name="question4" value="Ana"> Ana
            </label>
        </div>
        <button onclick="checkAnswer(4, 'Marylinn')">Comprobar Respuesta</button>
    </div>

    <div id="result"></div>

    <button onclick="showImage()">Ver Imagen Especial</button>
    <img id="loveImage" src="loveee.jpeg" alt="Imagen especial" style="display:none; margin-top:20px; max-width: 100%; border-radius: 10px;">

</body>
</html>
