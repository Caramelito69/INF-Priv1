<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carta con Efecto de Máquina de Escribir</title>
    <style>
        body {
            background-color: #f4f4f9;
            font-family: 'Courier New', Courier, monospace;
            color: #333;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh; 
            margin: 0;
        }

        .container {
            max-width: 600px;
            width: 90%;
            padding: 40px;
            background-color: #fff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
            text-align: left;
            border: 1px solid #ddd;
        }

        #typing-text {
            font-size: 1.2em;
            white-space: pre-wrap; 
            overflow: hidden;
            border-right: .15em solid orange;
            animation: 
                blink-caret .75s step-end infinite;
            display: inline-block; 
            padding-right: 5px;
        }

        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: orange; }
        }
    </style>
</head>
<body>

    <div class="container">
        <h1 style="text-align: center;">📜 01000001 01101101 01100001 00100000 01110100 01101111 01100100 01101111 00100000 01101100 01101111 00100000 01110001 01110101 01100101 00100000 01101000 01100001 01100011 01100101 01110011</h1>
        <p id="typing-text"></p>
        <p style="text-align: right; margin-top: 30px;">—  Atte: A.N. :) </p>
    </div>

    <script>
      
        const textElement = document.getElementById('typing-text');
        

        const fullText = `
        Wuuenasss joveeeen,
        Primeramente y obviamente felicitarte por tu cumple, y pues por mi parte siempre desearte lo mejor.
        Si de algo que te caracteriza a ti, es justamente esa misma perseverancia que siempre veo que quieres mas
        Y pues la verdad eso mismo es lo que te llevo hasta donde estas ahora,
        Tu sola te animaste a esto, y me atreveria a decir que todo este camino jamas fue facil
        Almenos la constancia que llegaste a tener, muy pocas personas la poseen.
        Parte de mi consejo es que sigas a tu "Instinto", muy probablemente jamas encuentres a otra persona que te entienda... mas que solo tu
        Recuerda que todo este camino lo tienes que hacer solo por ti, persiguiendo lo que amasss
        Aveces quiza lo pintamos como una tonteria, pero alli es donde esta la verdadera grandeza...
        Siempre les dije que jamas es necesario tener "Talento", sino "Obsesion" por lo que tu amas, ese algo por lo que darias toda tu vida
        Y pues al final ese es el sentido de la vida misma,
        No tienes que vivir el sueño de otra persona, sino la tuya, es lo unico que debe importar
        Y obviamente en todo este camino jamas estaras sola, tu elijes las personas que quieres que continuen en tu camino
        Y seran quienes te apoyaran en las buenas y malas situaciones, especialmente en las malas
        Desearte siempre lo mejor, se te quiere muchisiiimoo joven 🫂
        Y Feliz Cumpleaños aunque atrasado XDD
       
        `;

        let index = 0;
        const speed = 50;

        function typeWriter() {
            if (index < fullText.length) {
                textElement.textContent += fullText.charAt(index);
                index++;
                setTimeout(typeWriter, speed);
            } else {
                textElement.style.borderRight = 'none';
            }
        }
        window.onload = typeWriter;
    </script>

</body>
</html>
