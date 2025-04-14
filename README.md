<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Botões de Ajuste do Texto</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .text {
            font-size: 16px;
            color: black;
        }
    </style>
</head>
<body>

    <h1>Atividade de ajuste de fonte e estilo de texto</h1>

    <div>
        <button onclick="ajustarTamanhoTexto('aumentar')">Aumentar Fonte</button>
        <button onclick="ajustarTamanhoTexto('diminuir')">Diminuir Fonte</button>
        <button onclick="mudarFonte('serif')">Fonte Normal</button>
        <button onclick="mudarFonte('sans-serif')">Fonte Bonita</button>
    </div>

    <p class="text" id="texto">aki esta o codigo para testar.</p>

    <script>
        let tamanhoFonte = 16;

        function ajustarTamanhoTexto(acao) {
            const texto = document.getElementById('texto');
            if (acao === 'aumentar') {
                tamanhoFonte += 2;
            } else if (acao === 'diminuir') {
                tamanhoFonte -= 2;
            }
            texto.style.fontSize = tamanhoFonte + 'px';
        }

        function mudarCorTexto(cor) {
            const texto = document.getElementById('texto');
            texto.style.color = cor;
        }

        function mudarFonte(fonte) {
            const texto = document.getElementById('texto');
            texto.style.fontFamily = fonte;
        }
    </script>

</body>
</html>
