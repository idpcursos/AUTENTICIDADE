<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Autenticação Válida</title>
    <style>
        body {
            background-color: #000;
            color: #fff;
            font-family: 'Arial', sans-serif;
            text-align: center;
            padding: 50px;
        }
        h1 {
            color: #00ff00; /* Cor verde em hexadecimal */
        }
        .legislacao-text {
            font-size: 18px;
            max-width: 600px;
            margin: 0 auto;
        }
        .emissor-text {
            font-size: 24px;
            font-weight: bold;
            color: #00ff00; /* Cor verde em hexadecimal */
        }
        #serial-code {
            font-size: 18px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Autenticação Válida</h1>
    <p class="emissor-text">Emitido por: IDPCURSOS</p>
    <p class="legislacao-text">
        Este certificado é reconhecido como válido de acordo com a Lei nº 9.394/96 (Lei da Educação Nacional), o Decreto nº 5.154/04 (Decreto de Reconhecimento de Certificados), a Portaria MEC nº 1.428/2018 (regulamentação EAD) e a Resolução CNE/CEB nº 04/1999 (normas para cursos profissionalizantes).
    </p>
    <div id="serial-code"></div>

    <script>
        // Função para gerar um código de série aleatório
        function gerarCodigoSerie() {
            const caracteres = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789';
            let codigo = '';
            for (let i = 0; i < 10; i++) {
                const indice = Math.floor(Math.random() * caracteres.length);
                codigo += caracteres.charAt(indice);
            }
            return codigo;
        }

        // Exibir o código de série na página
        document.getElementById("serial-code").innerText = "Código de Série: " + gerarCodigoSerie();
    </script>
</body>
</html>
