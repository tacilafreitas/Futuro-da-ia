<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Você decide o futuro da IA</title>
<style>
body {
  font-family: Arial, Helvetica, sans-serif;
  background: linear-gradient(135deg, #0d47a1, #1976d2);
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  margin: 0;
}
.container {
  width: 90%;
  max-width: 700px;
  background: rgba(255,255,255,0.15);
  padding: 30px;
  border-radius: 20px;
  text-align: center;
  backdrop-filter: blur(10px);
}
h1 {
  font-size: 2em;
  margin-bottom: 20px;
}
p { font-size: 1.2em; }
button {
  margin: 10px;
  padding: 12px 25px;
  border: none;
  border-radius: 30px;
  background: #2196f3;
  color: white;
  cursor: pointer;
  font-size: 1em;
  transition: 0.3s;
}
button:hover {
  background: #0d47a1;
  transform: scale(1.05);
}
#resultado {
  margin-top: 20px;
  font-weight: bold;
}
</style>
</head>
<body>
<div class="container">
  <h1>Você decide o futuro da IA</h1>
  <p id="pergunta"></p>
  <div id="opcoes"></div>
  <p id="resultado"></p>
</div>

<script>
const etapas = [
  {
    pergunta: "Assim que saiu da escola, você se depara com um chat de IA que responde tudo, gera imagens e áudios hiper-realistas. Qual o primeiro pensamento?",
    opcoes: [
      { texto: "Isso é assustador!", valor: "assustador" },
      { texto: "Isso é maravilhoso!", valor: "maravilhoso" }
    ]
  },
  {
    pergunta: {
      assustador: "Você acha que a IA pode trazer riscos. O que fazer?",
      maravilhoso: "Você vê a IA como uma oportunidade. Como usá-la?"
    },
    opcoes: {
      assustador: [
        { texto: "Proibir a IA", valor: "proibir" },
        { texto: "Criar leis e controlar", valor: "controlar" }
      ],
      maravilhoso: [
        { texto: "Melhorar a educação", valor: "educacao" },
        { texto: "Criar empresas e ganhar dinheiro", valor: "empresas" }
      ]
    }
  }
];

const resultados = {
  proibir: "🚫 A sociedade decide proibir a IA. Segurança aumentou, mas a evolução diminuiu.",
  controlar: "⚖️ Criaram leis. A IA é usada com responsabilidade em saúde e segurança.",
  educacao: "📚 A IA melhora a educação com tutores digitais personalizados.",
  empresas: "💼 Startups de IA crescem, mas desigualdades surgem."
};

let etapaAtual = 0;
let caminho = [];

function mostrarEtapa() {
  const perguntaEl = document.getElementById('pergunta');
  const opcoesEl = document.getElementById('opcoes');
  const resultadoEl = document.getElementById('resultado');
  resultadoEl.textContent = '';
  opcoesEl.innerHTML = '';

  if (etapaAtual === 0) {
    perguntaEl.textContent = etapas[0].pergunta;
    etapas[0].opcoes.forEach(op => {
      const btn = document.createElement('button');
      btn.textContent = op.texto;
      btn.onclick = () => escolher(op.valor);
      opcoesEl.appendChild(btn);
    });
  } else if (etapaAtual === 1) {
    const primeiraEscolha = caminho[0];
    perguntaEl.textContent = etapas[1].pergunta[primeiraEscolha];
    etapas[1].opcoes[primeiraEscolha].forEach(op => {
      const btn = document.createElement('button');
      btn.textContent = op.texto;
      btn.onclick = () => escolher(op.valor);
      opcoesEl.appendChild(btn);
    });
  } else {
    perguntaEl.textContent = '';
    resultadoEl.textContent = resultados[caminho[1]];
  }
}

function escolher(valor) {
  caminho.push(valor);
  etapaAtual++;
  mostrarEtapa();
}

// Inicializa
mostrarEtapa();
</script>
</body>
</html><!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Você decide o futuro da IA</title>
<style>
body {
  font-family: Arial, Helvetica, sans-serif;
  background: linear-gradient(135deg, #0d47a1, #1976d2);
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  margin: 0;
}
.container {
  width: 90%;
  max-width: 700px;
  background: rgba(255,255,255,0.15);
  padding: 30px;
  border-radius: 20px;
  text-align: center;
  backdrop-filter: blur(10px);
}
h1 {
  font-size: 2em;
  margin-bottom: 20px;
}
p { font-size: 1.2em; }
button {
  margin: 10px;
  padding: 12px 25px;
  border: none;
  border-radius: 30px;
  background: #2196f3;
  color: white;
  cursor: pointer;
  font-size: 1em;
  transition: 0.3s;
}
button:hover {
  background: #0d47a1;
  transform: scale(1.05);
}
#resultado {
  margin-top: 20px;
  font-weight: bold;
}
</style>
</head>
<body>
<div class="container">
  <h1>Você decide o futuro da IA</h1>
  <p id="pergunta"></p>
  <div id="opcoes"></div>
  <p id="resultado"></p>
</div>

<script>
const etapas = [
  {
    pergunta: "Assim que saiu da escola, você se depara com um chat de IA que responde tudo, gera imagens e áudios hiper-realistas. Qual o primeiro pensamento?",
    opcoes: [
      { texto: "Isso é assustador!", valor: "assustador" },
      { texto: "Isso é maravilhoso!", valor: "maravilhoso" }
    ]
  },
  {
    pergunta: {
      assustador: "Você acha que a IA pode trazer riscos. O que fazer?",
      maravilhoso: "Você vê a IA como uma oportunidade. Como usá-la?"
    },
    opcoes: {
      assustador: [
        { texto: "Proibir a IA", valor: "proibir" },
        { texto: "Criar leis e controlar", valor: "controlar" }
      ],
      maravilhoso: [
        { texto: "Melhorar a educação", valor: "educacao" },
        { texto: "Criar empresas e ganhar dinheiro", valor: "empresas" }
      ]
    }
  }
];

const resultados = {
  proibir: "🚫 A sociedade decide proibir a IA. Segurança aumentou, mas a evolução diminuiu.",
  controlar: "⚖️ Criaram leis. A IA é usada com responsabilidade em saúde e segurança.",
  educacao: "📚 A IA melhora a educação com tutores digitais personalizados.",
  empresas: "💼 Startups de IA crescem, mas desigualdades surgem."
};

let etapaAtual = 0;
let caminho = [];

function mostrarEtapa() {
  const perguntaEl = document.getElementById('pergunta');
  const opcoesEl = document.getElementById('opcoes');
  const resultadoEl = document.getElementById('resultado');
  resultadoEl.textContent = '';
  opcoesEl.innerHTML = '';

  if (etapaAtual === 0) {
    perguntaEl.textContent = etapas[0].pergunta;
    etapas[0].opcoes.forEach(op => {
      const btn = document.createElement('button');
      btn.textContent = op.texto;
      btn.onclick = () => escolher(op.valor);
      opcoesEl.appendChild(btn);
    });
  } else if (etapaAtual === 1) {
    const primeiraEscolha = caminho[0];
    perguntaEl.textContent = etapas[1].pergunta[primeiraEscolha];
    etapas[1].opcoes[primeiraEscolha].forEach(op => {
      const btn = document.createElement('button');
      btn.textContent = op.texto;
      btn.onclick = () => escolher(op.valor);
      opcoesEl.appendChild(btn);
    });
  } else {
    perguntaEl.textContent = '';
    resultadoEl.textContent = resultados[caminho[1]];
  }
}

function escolher(valor) {
  caminho.push(valor);
  etapaAtual++;
  mostrarEtapa();
}

// Inicializa
mostrarEtapa();
</script>
</body>
</html>
