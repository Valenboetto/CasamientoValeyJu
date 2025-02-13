<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Invitación de Boda</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f8f8f8;
            color: #333;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 600px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1, h2, h3 {
            color: #444;
        }
        .countdown {
            font-size: 24px;
            font-weight: bold;
            margin: 20px 0;
        }
        .button {
            display: inline-block;
            margin: 10px;
            padding: 10px 20px;
            background: #444;
            color: white;
            text-decoration: none;
            border-radius: 5px;
        }
        .gift {
            margin-top: 20px;
            font-size: 18px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Valentina & Julián</h1>
        <h2>¡Nos casamos!</h2>
        <div class="countdown" id="countdown"></div>
        <h3>Ubicación y horario</h3>
        <p>Lugar: [Nombre del lugar]</p>
        <p>Fecha y Hora: [Día, Mes, Año - Hora]</p>
        <h3>Dress Code</h3>
        <p>Elegante</p>
        <h3>Nuestra Historia</h3>
        <p>[Breve resumen de su historia de amor]</p>
        <a href="[link al formulario de asistencia]" class="button">Confirmar Asistencia</a>
        <a href="[link al formulario de sugerencias]" class="button">Sugerir una canción</a>
        <div class="gift">
            <h3>Regalo</h3>
            <p>Si deseas hacernos un regalo, puedes hacerlo al siguiente CBU:</p>
            <p><strong>[Número de CBU]</strong></p>
        </div>
    </div>

    <script>
        function countdown() {
            const weddingDate = new Date("2025-11-01T00:00:00").getTime();
            const now = new Date().getTime();
            const timeLeft = weddingDate - now;
            
            const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
            const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);
            
            document.getElementById("countdown").innerText = `${days} días, ${hours} horas, ${minutes} minutos, ${seconds} segundos`;
        }
        setInterval(countdown, 1000);
    </script>
</body>
</html>
