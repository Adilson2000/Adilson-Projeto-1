<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Viagem</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f8ff; /* Azul-claro */
            margin: 0;
            padding: 0;
        }

        h1 {
            color: #333;
            text-align: center;
        }

        form {
            max-width: 400px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        label {
            display: block;
            margin-bottom: 5px;
            color: #333;
        }

        input[type="text"],
        input[type="number"] {
            width: 100%;
            padding: 8px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }

        button {
            background-color: #007bff;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }

        button:hover {
            background-color: #0056b3;
        }

        #resultado {
            margin-top: 20px;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        #resultado p {
            margin-bottom: 10px;
            color: #333;
        }
    </style>
</head>
<body>
    <h1>Calculadora de Viagem</h1>
    
    <form id="viagemForm">
        <label for="destino">Destino da viagem:</label>
        <input type="text" id="destino" name="destino" required><br><br>

        <label for="distancia">Distância da viagem (em quilômetros):</label>
        <input type="number" id="distancia" name="distancia" step="0.01" required><br><br>

        <label for="consumoGasolina">Consumo de gasolina do veículo (em km/l):</label>
        <input type="number" id="consumoGasolina" name="consumoGasolina" step="0.01" required><br><br>

        <label for="precoGasolina">Preço da gasolina (por litro):</label>
        <input type="number" id="precoGasolina" name="precoGasolina" step="0.01" required><br><br>

        <label for="velocidade">Velocidade média da viagem (em km/h):</label>
        <input type="number" id="velocidade" name="velocidade" step="0.01" required><br><br>

        <button type="button" onclick="calcularViagem()">Calcular</button>
    </form>

    <div id="resultado"></div>

    <script>
        function calcularViagem() {
            const destino = document.getElementById("destino").value;
            const distancia = parseFloat(document.getElementById("distancia").value);
            const consumoGasolina = parseFloat(document.getElementById("consumoGasolina").value);
            const precoGasolina = parseFloat(document.getElementById("precoGasolina").value);
            const velocidade = parseFloat(document.getElementById("velocidade").value);

            const tempo = distancia / velocidade;

            const custoGasolina = (distancia / consumoGasolina) * precoGasolina;

            document.getElementById("resultado").innerHTML = `
                <p>Gasto com combustível (gasolina): R$ ${custoGasolina.toFixed(2)}</p>
                <p>Tempo estimado de viagem: ${tempo.toFixed(2)} horas</p>
            `;
        }
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Viagem</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f8ff; /* Azul-claro */
            margin: 0;
            padding: 0;
        }

        h1 {
            color: #333;
            text-align: center;
        }

        form {
            max-width: 400px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        label {
            display: block;
            margin-bottom: 5px;
            color: #333;
        }

        input[type="text"],
        input[type="number"] {
            width: 100%;
            padding: 8px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }

        button {
            background-color: #007bff;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }

        button:hover {
            background-color: #0056b3;
        }

        #resultado {
            margin-top: 20px;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        #resultado p {
            margin-bottom: 10px;
            color: #333;
        }
    </style>
</head>
<body>
    <h1>Calculadora de Viagem</h1>
    
    <form id="viagemForm">
        <label for="destino">Destino da viagem:</label>
        <input type="text" id="destino" name="destino" required><br><br>

        <label for="distancia">Distância da viagem (em quilômetros):</label>
        <input type="number" id="distancia" name="distancia" step="0.01" required><br><br>

        <label for="consumoGasolina">Consumo de gasolina do veículo (em km/l):</label>
        <input type="number" id="consumoGasolina" name="consumoGasolina" step="0.01" required><br><br>

        <label for="precoGasolina">Preço da gasolina (por litro):</label>
        <input type="number" id="precoGasolina" name="precoGasolina" step="0.01" required><br><br>

        <label for="velocidade">Velocidade média da viagem (em km/h):</label>
        <input type="number" id="velocidade" name="velocidade" step="0.01" required><br><br>

        <button type="button" onclick="calcularViagem()">Calcular</button>
    </form>

    <div id="resultado"></div>

    <script>
        function calcularViagem() {
            const destino = document.getElementById("destino").value;
            const distancia = parseFloat(document.getElementById("distancia").value);
            const consumoGasolina = parseFloat(document.getElementById("consumoGasolina").value);
            const precoGasolina = parseFloat(document.getElementById("precoGasolina").value);
            const velocidade = parseFloat(document.getElementById("velocidade").value);

            const tempo = distancia / velocidade;

            const custoGasolina = (distancia / consumoGasolina) * precoGasolina;

            document.getElementById("resultado").innerHTML = `
                <p>Gasto com combustível (gasolina): R$ ${custoGasolina.toFixed(2)}</p>
                <p>Tempo estimado de viagem: ${tempo.toFixed(2)} horas</p>
            `;
        }
    </script>
</body>
</html>
