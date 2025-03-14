<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cardápio - Pesque e Pague União</title>
    <style>
        body {
            background: url('https://source.unsplash.com/1600x900/?restaurant,food') no-repeat center center fixed;
            background-size: cover;
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 20px;
        }
        h1 {
            font-size: 36px;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
        }
        .container {
            max-width: 800px;
            margin: auto;
            background: rgba(0, 0, 0, 0.8);
            padding: 20px;
            border-radius: 10px;
        }
        .categoria {
            font-size: 24px;
            background: white;
            color: black;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s;
        }
        .categoria:hover {
            background: #e0e0e0;
        }
        .itens {
            display: none;
            margin-top: 10px;
        }
        .item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 20px;
            margin: 10px 0;
            padding: 5px 0;
            border-bottom: 1px solid #444;
            transition: background 0.3s;
            cursor: pointer;
        }
        .item:hover {
            background: rgba(255, 255, 255, 0.2);
        }
        .preco {
            font-weight: bold;
            color: white;
        }
        .descricao {
            display: none;
            font-size: 16px;
            color: #ddd;
            padding-top: 5px;
        }
        .rodape {
            margin-top: 30px;
            font-size: 16px;
            color: #bdbdbd;
            border-top: 1px solid #444;
            padding-top: 10px;
        }
    </style>
    <script>
        function toggleCategoria(id) {
            var itens = document.getElementById(id);
            itens.style.display = itens.style.display === "block" ? "none" : "block";
        }

        function toggleDescricao(id) {
            var descricao = document.getElementById(id);
            descricao.style.display = descricao.style.display === "block" ? "none" : "block";
        }
    </script>
</head>
<body>

    <div class="container">
        <h1>Pesque e Pague União</h1>

        <div class="categoria" onclick="toggleCategoria('refeicoes')">🍽️ Refeições</div>
        <div id="refeicoes" class="itens">
            <div class="item" onclick="toggleDescricao('desc1')"><span>Peixe Frito</span> <span class="preco">R$ 65,00</span></div>
            <div id="desc1" class="descricao">Peixe frito crocante servido com acompanhamentos.</div>

            <div class="item" onclick="toggleDescricao('desc2')"><span>Carne de Sol</span> <span class="preco">R$ 60,00</span></div>
            <div id="desc2" class="descricao">Carne de sol macia com arroz, feijão e farofa.</div>

            <div class="item" onclick="toggleDescricao('desc3')"><span>Panelada</span> <span class="preco">R$ 45,00</span></div>
            <div id="desc3" class="descricao">Prato típico nordestino com miúdos e temperos especiais.</div>

            <div class="item" onclick="toggleDescricao('desc4')"><span>Galinha Caipira</span> <span class="preco">R$ 160,00</span></div>
            <div id="desc4" class="descricao">Galinha caipira cozida lentamente com temperos caseiros.</div>

            <div class="item" onclick="toggleDescricao('desc5')"><span>Peixada União</span> <span class="preco">R$ 120,00</span></div>
            <div id="desc5" class="descricao">Peixada especial da casa com molho e acompanhamentos.</div>
        </div>

        <div class="categoria" onclick="toggleCategoria('petiscos')">🍢 Tira-Gosto/Petiscos</div>
        <div id="petiscos" class="itens">
            <div class="item" onclick="toggleDescricao('desc6')"><span>Tábua de Frios</span> <span class="preco">R$ 35,00</span></div>
            <div id="desc6" class="descricao">Queijos, embutidos e azeitonas.</div>

            <div class="item" onclick="toggleDescricao('desc7')"><span>Calabresa</span> <span class="preco">R$ 30,00</span></div>
            <div id="desc7" class="descricao">Linguiça calabresa acebolada.</div>
        </div>

        <div class="categoria" onclick="toggleCategoria('sobremesas')">🍮 Sobremesas</div>
        <div id="sobremesas" class="itens">
            <div class="item" onclick="toggleDescricao('desc8')"><span>Pudim de Leite</span> <span class="preco">R$ 5,00</span></div>
            <div id="desc8" class="descricao">Pudim cremoso com calda de caramelo.</div>
        </div>

        <div class="categoria" onclick="toggleCategoria('adicionais')">🍚 Adicionais</div>
        <div id="adicionais" class="itens">
            <div class="item" onclick="toggleDescricao('desc9')"><span>Porção de Arroz</span> <span class="preco">R$ 10,00</span></div>
            <div id="desc9" class="descricao">Arroz branco soltinho.</div>
        </div>

        <div class="categoria" onclick="toggleCategoria('bebidas')">🥤 Bebidas</div>
        <div id="bebidas" class="itens">
            <div class="item" onclick="toggleDescricao('desc10')"><span>Heineken 600ml</span> <span class="preco">R$ 14,00</span></div>
            <div id="desc10" class="descricao">Cerveja premium puro malte.</div>
        </div>

        <div class="categoria" onclick="toggleCategoria('aguas')">💧 Águas</div>
        <div id="aguas" class="itens">
            <div class="item" onclick="toggleDescricao('desc11')"><span>Água Mineral 510ml</span> <span class="preco">R$ 4,00</span></div>
            <div id="desc11" class="descricao">Água pura e refrescante.</div>
        </div>

        <div class="rodape">
            <p><strong>Formas de pagamento:</strong> Aceitamos Pix, cartão de crédito e débito.</p>
            <p><strong>Horário de funcionamento:</strong> Terça a domingo, das 10h às 22h.</p>
        </div>
    </div>

</body>
</html>
