<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mensaje Romántico</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: black;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            flex-direction: column;
        }
        .mensaje {
            font-size: 24px;
            line-height: 1.5;
        }
    </style>
</head>
<body>
    <div class="mensaje" id="mensaje"></div>

    <script>
        const mensaje = "MI MOGOSITA HERMOSA, CADA VEZ QUE TE VEO, MI CORAZÓN LATE MÁS RÁPIDO. ERES MI PECECITO GRACIA MI VIDA. NO HAY PALABRAS SUFICIENTES PARA DECIRTE LO MUCHO QUE TE QUIERO, MUCHO MÁS DE LO QUE IMAGINAS. TE QUIERO MUCHO, MI AMOR, Y CADA DÍA QUE PASO CONTIGO ES UN REGALO QUE TENGO QUE AGUANTAR PORQUE TU MAMI NO SE PONE AL DÍA EN EL PAGO. HOY NO ES UN MES MÁS PERO YA PASÓ 30 Y HOY 1 OSEA LIT MUAKITI 31❤️";
        let index = 0;
        let colors = ["#FF0000", "#0000FF"]; // Rojo y Azul
        let colorIndex = 0;

        function escribirMensaje() {
            if (index < mensaje.length) {
                document.getElementById("mensaje").innerHTML += 
                    `<span style="color: ${colors[colorIndex]}">${mensaje[index]}</span>`;
                index++;
                colorIndex = 1 - colorIndex; // Alterna entre rojo y azul
                setTimeout(escribirMensaje, 100); // Llama a la función cada 100ms
            }
        }

        escribirMensaje(); // Inicia la animación
    </script>
</body>
</html>
