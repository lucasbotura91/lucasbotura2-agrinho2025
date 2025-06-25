<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8" />
    <title>Quiz Interativo - Campo x Cidade</title>
    <link rel="stylesheet" href="style.css" />
    <style>
        /* Estilos CSS */
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f8e0;
            text-align: center;
            padding: 20px;
        }

        .container {
            max-width: 600px;
            margin: auto;
            background-color: white;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 0 10px gray;
        }

        button {
            margin-top: 10px;
            padding: 10px;
            border: none;
            border-radius: 8px;
            background-color: #4CAF50;
            color: white;
            cursor: pointer;
        }

        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🌾🏙️ Quiz: Campo x Cidade</h1>
        <div id="quiz">
            <p id="pergunta"></p>
            <div id="opcoes"></div>
            <button onclick="proximaPergunta()">Próxima</button>
        </div>
        <div id="resultado" class="hidden"></div>
    </div>

    <script>
        // Array de perguntas
        const perguntas = [
            {
                pergunta: "Qual destes alimentos é mais comum ser produzido no campo?",
                opcoes: ["Cenoura", "Refrigerante", "Pizza", "Chocolate"],
                correta: 0
            },
            {
                pergunta: "Qual equipamento é mais comum nas grandes cidades?",
                opcoes: ["Trator", "Semáforo", "Plantadeira", "Arado"],
                correta: 1
            },
            {
                pergunta: "O que é uma feira agroecológica?",
                opcoes: [
                    "Um local de venda de celulares",
                    "Uma feira de produtos agrícolas com práticas sustentáveis",
                    "Uma exposição de tratores antigos",
                    "Um mercado apenas de produtos industrializados"
                ],
                correta: 1
            },
            {
                pergunta: "Qual atitude fortalece a conexão entre campo e cidade?",
                opcoes: [
                    "Troca de produtos regionais",
                    "Conflitos por território",
                    "Isolamento das áreas rurais",
                    "Falta de transporte"
                ],
                correta: 0
            },
            {
                pergunta: "Qual desses profissionais atua mais no campo?",
                opcoes: ["Agricultor", "Piloto de avião", "Bombeiro urbano", "Porteiro de prédio"],
                correta: 0
            },
            {
                pergunta: "Como o pensamento computacional pode ajudar na agricultura?",
                opcoes: [
                    "Apenas com jogos",
                    "Controlando pragas com mágica",
                    "Usando dados para melhorar a produção",
                    "Não pode ajudar em nada"
                ],
                correta: 2
            }
        ];

        let indiceAtual = 0;
        let pontuacao = 0;

        // Função para exibir a pergunta atual
        function mostrarPergunta() {
            const q = perguntas[indiceAtual];
            document.getElementById("pergunta").textContent = q.pergunta;
            const opcoesDiv = document.getElementById("opcoes");
            opcoesDiv.innerHTML = "";

            q.opcoes.forEach((opcao, i) => {
                const bot
