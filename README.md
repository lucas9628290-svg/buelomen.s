
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ENEM 2026 | Seu Futuro Começa Aqui</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    font-family: Arial, sans-serif;
    background: #080f20;
    color: white;
}

/* INTRODUÇÃO */
.intro-screen {
    position: fixed;
    inset: 0;
    z-index: 9999;
    background:
        radial-gradient(circle at 50% 45%, #103b70, transparent 55%),
        linear-gradient(135deg, #020817, #071a36, #020817);
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    overflow: hidden;
    transition: opacity 1s, visibility 1s;
}

.intro-screen::before {
    content: "✦";
    position: absolute;
    top: 12%;
    left: 12%;
    color: #28baff;
    font-size: 65px;
    animation: flutuar 3s infinite ease-in-out;
}

.intro-screen::after {
    content: "✎";
    position: absolute;
    bottom: 12%;
    right: 12%;
    color: #28baff;
    font-size: 75px;
    animation: flutuar 3s infinite ease-in-out;
}

.intro-content {
    position: relative;
    z-index: 2;
    width: 90%;
    max-width: 750px;
    animation: aparecer 1.5s ease;
}

.intro-tag {
    color: #43caff;
    letter-spacing: 4px;
    font-weight: bold;
}

.intro-content h1 {
    font-size: clamp(65px, 13vw, 120px);
    color: white;
    text-shadow: 0 0 15px #008cff, 0 0 45px #006eff;
    margin: 20px 0;
    animation: brilho 2s infinite alternate;
}

.intro-content h2 {
    color: white;
    font-size: clamp(20px, 4vw, 32px);
}

.intro-content p {
    color: #b8d9ff;
    margin: 20px 0 30px;
    line-height: 1.6;
}

.intro-btn {
    background: transparent;
    border: 2px solid #16aaff;
    color: white;
    padding: 17px 35px;
    border-radius: 50px;
    font-size: 17px;
    box-shadow: 0 0 20px #008cff;
    cursor: pointer;
}

.intro-btn:hover {
    background: #008cff;
}

.intro-bar {
    width: 230px;
    height: 6px;
    background: #173455;
    margin: 35px auto 10px;
    border-radius: 20px;
    overflow: hidden;
}

.intro-progress {
    height: 100%;
    width: 0;
    background: #20baff;
    box-shadow: 0 0 15px #00aaff;
    animation: carregar 2.5s forwards;
}

.intro-screen.saindo {
    opacity: 0;
    visibility: hidden;
    pointer-events: none;
}

body:not(.started) > header,
body:not(.started) > main,
body:not(.started) > footer {
    visibility: hidden;
}

@keyframes carregar {
    to { width: 100%; }
}

@keyframes aparecer {
    from { opacity: 0; transform: translateY(35px); }
    to { opacity: 1; transform: translateY(0); }
}

@keyframes brilho {
    from { text-shadow: 0 0 15px #008cff; }
    to { text-shadow: 0 0 40px #00aaff, 0 0 70px #006eff; }
}

@keyframes flutuar {
    50% { transform: translateY(-20px) rotate(10deg); }
}

/* CABEÇALHO */
header {
    background: #101d38;
    padding: 20px 8%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;
    border-bottom: 1px solid #243b65;
}

.logo {
    font-size: 25px;
    font-weight: bold;
    color: #42d9ff;
}

nav a {
    color: white;
    text-decoration: none;
    margin: 10px;
    transition: .3s;
}

nav a:hover {
    color: #42d9ff;
}

button {
    border: none;
    padding: 12px 18px;
    border-radius: 9px;
    cursor: pointer;
    font-weight: bold;
    transition: .3s;
    margin: 4px;
}

button:hover {
    transform: translateY(-3px);
    filter: brightness(1.15);
}

.mochila {
    background: #00bfff;
    color: #061326;
}

.download {
    background: #20c997;
    color: #061326;
}

.salvar {
    background: #ffc857;
    color: #172033;
}

/* PÁGINA PRINCIPAL */
.hero {
    min-height: 520px;
    padding: 100px 10%;
    display: flex;
    align-items: center;
    background:
    radial-gradient(circle at 80% 30%, #164c82 0%, transparent 35%),
    linear-gradient(120deg, #081326, #10294b);
}

.hero-content {
    max-width: 700px;
}

.hero h1 {
    font-size: clamp(35px, 6vw, 65px);
    margin-bottom: 20px;
}

.hero h1 span {
    color: #42d9ff;
}

.hero p {
    color: #c3d4e8;
    font-size: 18px;
    line-height: 1.7;
    margin-bottom: 25px;
}

section {
    padding: 75px 9%;
}

h2 {
    font-size: 32px;
    margin-bottom: 20px;
    color: #42d9ff;
}

.intro-text {
    text-align: center;
    max-width: 850px;
    margin: auto;
    line-height: 1.8;
    color: #c6d2e4;
}

.cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 22px;
    margin-top: 35px;
}

.card {
    background: #132340;
    padding: 28px;
    border-radius: 15px;
    border: 1px solid #28436d;
    transition: .3s;
}

.card:hover {
    transform: translateY(-7px);
    border-color: #42d9ff;
}

.card h3 {
    color: #42d9ff;
    margin-bottom: 12px;
}

.card p {
    color: #c4d0e1;
    line-height: 1.6;
}

.dicas {
    background: #101d35;
}

.cta {
    text-align: center;
    background: linear-gradient(120deg, #123c68, #10203d);
    border-radius: 20px;
    padding: 45px 20px;
}

.cta p {
    margin: 15px 0 25px;
    color: #cbd9e9;
}

/* CENTRAL DO PROJETO */
.central {
    background: #09162b;
    padding: 70px 8%;
}

.central-intro {
    text-align: center;
    max-width: 800px;
    margin: auto;
    line-height: 1.7;
    color: #cbd9e9;
}

.central-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
    gap: 20px;
    margin-top: 30px;
}

.central-card {
    background: #132744;
    border: 1px solid #28517c;
    border-radius: 15px;
    padding: 25px;
    line-height: 1.7;
    margin-top: 15px;
}

.central-card h3 {
    color: #42d9ff;
    margin-bottom: 12px;
}

.central-card p,
.central-card li {
    color: #d0ddec;
}

.central-card ul {
    padding-left: 20px;
}

.central-card a {
    color: #42d9ff;
    display: inline-block;
    margin: 5px 0 15px;
}

.qr-area {
    background: #102b4d;
    border: 1px solid #42d9ff;
    border-radius: 20px;
    padding: 35px;
    text-align: center;
    margin-top: 35px;
    overflow-wrap: anywhere;
}

.qr-area img {
    width: 210px;
    height: 210px;
    object-fit: contain;
    background: white;
    padding: 10px;
    border-radius: 12px;
    margin: 20px auto;
    display: block;
}

.pergunta {
    background: #142943;
    padding: 20px;
    border-radius: 12px;
    margin: 15px 0;
    line-height: 1.6;
}

.pergunta strong {
    color: #42d9ff;
}

.creditos {
    text-align: center;
    padding: 35px;
    color: #a9bed6;
}

footer {
    text-align: center;
    padding: 30px;
    color: #91a4bf;
    background: #050b17;
    line-height: 1.8;
}

/* RESPONSIVIDADE */
@media(max-width: 650px) {
    header {
        justify-content: center;
        text-align: center;
    }

    nav {
        width: 100%;
    }

    nav a {
        display: inline-block;
        margin: 6px;
    }

    .hero {
        padding: 70px 7%;
    }

    .qr-area {
        padding: 20px;
    }
}

/* IMPRESSÃO */
@media print {
    .intro-screen,
    header,
    footer,
    button {
        display: none !important;
    }

    body {
        background: white;
        color: black;
    }

    .hero, section, .central {
        background: white !important;
        color: black;
    }

    h1, h2, h3, p, li, a, strong {
        color: black !important;
    }

    .card, .central-card, .pergunta, .qr-area {
        background: white !important;
        color: black;
        border: 1px solid #888;
        break-inside: avoid;
    }

    .card p, .central-card p, .central-card li {
        color: black;
    }
}
</style>
</head>

<body>

<!-- INTRODUÇÃO -->
<div class="intro-screen" id="intro">
    <div class="intro-content">

        <div class="intro-tag">
            EDUCAÇÃO • CONHECIMENTO • FUTURO
        </div>

        <h1>ENEM</h1>

        <h2>Seu futuro começa aqui...</h2>

        <p>
            Mais que uma prova, uma oportunidade
            de transformar seus sonhos em realidade!
        </p>

        <button class="intro-btn" onclick="entrarSite()">
            CLIQUE PARA CONTINUAR →
        </button>

        <div class="intro-bar">
            <div class="intro-progress"></div>
        </div>

        <p>PREPARANDO SEU FUTURO...</p>

        <div style="font-size:35px; margin-top:20px">
            📚 ✏️ 🎓 📝
        </div>

    </div>
</div>

<!-- CABEÇALHO -->
<header>
    <div class="logo">ENEM 2026</div>

    <nav>
        <a href="#inicio">Início</a>
        <a href="#importancia">Importância</a>
        <a href="#oportunidades">Oportunidades</a>
        <a href="#dicas">Dicas</a>
        <a href="#projeto">Projeto</a>
    </nav>

    <button class="mochila" onclick="irMochila()">
        🎒 Minha Mochila
    </button>
</header>

<main>

<!-- INÍCIO -->
<div class="hero" id="inicio">
    <div class="hero-content">

        <h1>
            Seu futuro começa com uma
            <span>oportunidade.</span>
        </h1>

        <p>
            O ENEM é muito mais que uma prova.
            É uma oportunidade de conquistar seus objetivos,
            entrar na universidade e construir um futuro melhor.
        </p>

        <button class="download" onclick="baixarSite()">
            ⬇ Baixar este site
        </button>

        <button class="salvar" onclick="salvarConteudo()">
            ★ Salvar conteúdo
        </button>

        <button class="mochila" onclick="irMochila()">
            🎒 Minha Mochila
        </button>

    </div>
</div>

<!-- IMPORTÂNCIA -->
<section id="importancia">
    <div class="intro-text">
        <h2>Qual é a importância do ENEM?</h2>

        <p>
            O Exame Nacional do Ensino Médio (ENEM) avalia
            os conhecimentos dos estudantes e permite que
            eles utilizem suas notas para buscar vagas
            em universidades. Também pode ajudar no acesso
            a bolsas e programas de financiamento estudantil.
            Por isso, é uma etapa importante para quem deseja
            continuar os estudos.
        </p>
    </div>
</section>

<!-- OPORTUNIDADES -->
<section id="oportunidades">
    <h2>🎓 Oportunidades que o ENEM oferece</h2>

    <div class="cards">

        <div class="card">
            <h3>🏫 SISU</h3>
            <p>
                Utiliza a nota do ENEM para selecionar
                estudantes para vagas em universidades
                e instituições públicas participantes.
            </p>
        </div>

        <div class="card">
            <h3>📚 PROUNI</h3>
            <p>
                Oferece bolsas de estudo integrais ou parciais
                em instituições particulares, conforme os critérios.
            </p>
        </div>

        <div class="card">
            <h3>💻 FIES</h3>
            <p>
                Programa de financiamento estudantil
                para cursos em instituições particulares,
                conforme as regras do programa.
            </p>
        </div>

        <div class="card">
            <h3>🌎 Futuro</h3>
            <p>
                A nota também pode ser aceita por universidades
                portuguesas participantes de acordos com o INEP.
            </p>
        </div>

    </div>
</section>

<!-- DICAS -->
<section class="dicas" id="dicas">
    <h2>📖 Como se preparar para o ENEM?</h2>

    <div class="cards">

        <div class="card">
            <h3>01. Organização</h3>
            <p>
                Monte um cronograma e organize
                seus horários de estudo.
            </p>
        </div>

        <div class="card">
            <h3>02. Redação</h3>
            <p>
                Pratique a escrita e desenvolva
                seus argumentos.
            </p>
        </div>

        <div class="card">
            <h3>03. Exercícios</h3>
            <p>
                Resolva questões de provas anteriores.
            </p>
        </div>

        <div class="card">
            <h3>04. Revisão</h3>
            <p>
                Revise os conteúdos e acompanhe
                seu aprendizado.
            </p>
        </div>

    </div>
</section>

<!-- MENSAGEM FINAL -->
<section>
    <div class="cta">

        <h2>O seu esforço de hoje constrói o amanhã!</h2>

        <p>
            Acredite no seu potencial.
            Cada aprendizado é um passo em direção aos seus sonhos.
        </p>

        <button class="mochila" onclick="irMochila()">
            🎒 Acessar minha mochila
        </button>

    </div>
</section>

<!-- CENTRAL DO PROJETO -->
<section class="central" id="projeto">

    <div class="central-intro">
        <h2>📚 Central do Projeto ENEM</h2>

        <p>
            Conheça o objetivo, as tecnologias, as funcionalidades
            e a importância deste projeto educacional.
        </p>
    </div>

    <!-- QR CODE -->
    <div class="qr-area">

        <h2>📱 Acesse pelo QR Code</h2>

        <p>
            Aponte a câmera do celular para o código
            e conheça o projeto.
        </p>

        <img id="qrCode" alt="QR Code para acessar o site">

        <p id="enderecoSite">Carregando endereço...</p>

        <button class="download" onclick="baixarQR()">
            ⬇ Baixar QR Code
        </button>

    </div>

    <!-- INFORMAÇÕES DO PROJETO -->
    <div class="central-grid">

        <div class="central-card">
            <h3>🎯 Objetivo</h3>
            <p>
                Desenvolver um site educativo para informar
                os estudantes sobre a importância do ENEM,
                suas oportunidades e formas de preparação.
            </p>
        </div>

        <div class="central-card">
            <h3>💡 Justificativa</h3>
            <p>
                Muitos estudantes têm dúvidas sobre o ENEM.
                O projeto reúne informações de forma simples,
                organizada e acessível.
            </p>
        </div>

        <div class="central-card">
            <h3>👥 Público-alvo</h3>
            <p>
                Estudantes do Ensino Médio e pessoas interessadas
                em ingressar no ensino superior.
            </p>
        </div>

        <div class="central-card">
            <h3>💻 Tecnologias</h3>
            <ul>
                <li>HTML: estrutura do site.</li>
                <li>CSS: aparência e design.</li>
                <li>JavaScript: interações e funções.</li>
                <li>GitHub Pages: publicação online.</li>
            </ul>
        </div>

        <div class="central-card">
            <h3>⚙️ Funcionalidades</h3>
            <ul>
                <li>Tela de introdução animada.</li>
                <li>Informações sobre o ENEM.</li>
                <li>Botão de download.</li>
                <li>Salvamento de conteúdo.</li>
                <li>QR Code de acesso.</li>
                <li>Link para Minha Mochila.</li>
                <li>Impressão da apresentação.</li>
            </ul>
        </div>

        <div class="central-card">
            <h3>🌎 Benefícios</h3>
            <p>
                Facilita o acesso à informação, incentiva os estudos
                e ajuda os estudantes a conhecerem oportunidades
                de ingresso no ensino superior.
            </p>
        </div>

    </div>

    <!-- PERGUNTAS DO PROFESSOR -->
    <h2 style="margin-top:55px">
        🎓 Preparação para apresentar ao professor
    </h2>

    <div class="pergunta">
        <strong>1. Qual é o objetivo do site?</strong>
        <p>
            Informar os estudantes sobre o ENEM e mostrar
            as oportunidades que ele oferece.
        </p>
    </div>

    <div class="pergunta">
        <strong>2. Por que o ENEM é importante?</strong>
        <p>
            Porque permite concorrer a vagas no ensino superior
            e participar de programas educacionais.
        </p>
    </div>

    <div class="pergunta">
        <strong>3. O que é HTML?</strong>
        <p>
            É a linguagem utilizada para estruturar
            o conteúdo de uma página.
        </p>
    </div>

    <div class="pergunta">
        <strong>4. Para que serve o CSS?</strong>
        <p>
            É utilizado para personalizar cores, tamanhos,
            layouts e animações.
        </p>
    </div>

    <div class="pergunta">
        <strong>5. Para que serve JavaScript?</strong>
        <p>
            Permite criar interações, botões e funcionalidades
            no site.
        </p>
    </div>

    <div class="pergunta">
        <strong>6. O que é GitHub Pages?</strong>
        <p>
            É um serviço que permite publicar sites
            diretamente de um repositório do GitHub.
        </p>
    </div>

    <div class="pergunta">
        <strong>7. O que é um QR Code?</strong>
        <p>
            É um código que pode ser escaneado pela câmera
            do celular para acessar um endereço ou informação.
        </p>
    </div>

    <div class="pergunta">
        <strong>8. Qual foi a maior contribuição do projeto?</strong>
        <p>
            Reunir informações importantes sobre o ENEM
            em um único lugar, facilitando o acesso dos estudantes.
        </p>
    </div>

    <div class="pergunta">
        <strong>9. Por que utilizar JavaScript no projeto?</strong>
        <p>
            Para fazer os botões funcionarem, gerar o QR Code,
            baixar arquivos e criar interações.
        </p>
    </div>

    <div class="pergunta">
        <strong>10. Como o site pode ajudar um estudante?</strong>
        <p>
            Apresentando informações, oportunidades e dicas
            de preparação para o exame.
        </p>
    </div>

    <!-- REFERÊNCIAS -->
    <h2 style="margin-top:55px">🔎 Fontes de pesquisa</h2>

    <div class="central-card">
        <h3>INEP — ENEM</h3>
        <p>Informações oficiais sobre o exame.</p>
        <a href="https://www.gov.br/inep/pt-br/areas-de-atuacao/avaliacao-e-exames-educacionais/enem" target="_blank">
            Acessar INEP
        </a>

        <h3>Ministério da Educação</h3>
        <p>Informações sobre programas de acesso ao ensino superior.</p>
        <a href="https://acessounico.mec.gov.br/" target="_blank">
            Acessar MEC
        </a>

        <h3>GitHub Pages</h3>
        <p>Documentação sobre publicação de sites.</p>
        <a href="https://pages.github.com/" target="_blank">
            Conhecer GitHub Pages
        </a>
    </div>

    <!-- CRÉDITOS -->
    <div class="creditos">

        <h2>Desenvolvido por Lucas</h2>

        <p>Projeto educacional — A importância do ENEM.</p>

        <p>Educação é uma oportunidade de transformar o futuro!</p>

        <button class="download" onclick="window.print()">
            🖨️ Imprimir apresentação
        </button>

        <button class="mochila" onclick="irMochila()">
            🎒 Minha Mochila
        </button>

    </div>

</section>

</main>

<footer>
    <p>ENEM 2026 — Educação transforma vidas.</p>
    <p>Projeto educacional desenvolvido por Lucas.</p>
    <p>Informações: INEP / Ministério da Educação.</p>
</footer>

<script>

/* ENTRAR NO SITE */
function entrarSite() {
    const intro = document.getElementById("intro");

    intro.classList.add("saindo");
    document.body.classList.add("started");

    setTimeout(() => {
        intro.remove();
    }, 1000);
}

/* MINHA MOCHILA */
function irMochila() {
    window.open(
        "https://lucas9628290-svg.github.io/lucas-gabriel-laurindo-escolate/",
        "_blank"
    );
}

/* BAIXAR O SITE */
function baixarSite() {
    const arquivo = new Blob(
        ["<!DOCTYPE html>\n" + document.documentElement.outerHTML],
        {type: "text/html;charset=utf-8"}
    );

    const url = URL.createObjectURL(arquivo);
    const link = document.createElement("a");

    link.href = url;
    link.download = "site-importancia-do-enem.html";
    link.click();

    setTimeout(() => URL.revokeObjectURL(url), 1000);
}

/* SALVAR CONTEÚDO */
function salvarConteudo() {
    const conteudo = `
IMPORTÂNCIA DO ENEM

OBJETIVO:
Informar estudantes sobre o ENEM.

OPORTUNIDADES:
- SISU
- PROUNI
- FIES
- Universidades portuguesas participantes

DICAS:
- Organizar os estudos.
- Praticar redação.
- Resolver exercícios.
- Revisar conteúdos.

TECNOLOGIAS:
- HTML
- CSS
- JavaScript
- GitHub Pages

DESENVOLVIDO POR LUCAS.
`;

    const arquivo = new Blob(
        [conteudo],
        {type: "text/plain;charset=utf-8"}
    );

    const url = URL.createObjectURL(arquivo);
    const link = document.createElement("a");

    link.href = url;
    link.download = "conteudo-sobre-o-enem.txt";
    link.click();

    setTimeout(() => URL.revokeObjectURL(url), 1000);
}

/* GERAR QR CODE */
function atualizarQR() {
    const endereco = window.location.href;

    const imagem = document.getElementById("qrCode");

    imagem.src =
        "https://api.qrserver.com/v1/create-qr-code/?size=300x300&data="
        + encodeURIComponent(endereco);

    document.getElementById("enderecoSite").textContent = endereco;
}

/* BAIXAR QR CODE */
async function baixarQR() {
    try {
        const imagem = document.getElementById("qrCode");

        const resposta = await fetch(imagem.src);

        if (!resposta.ok) {
            throw new Error("Não foi possível obter o QR Code.");
        }

        const arquivo = await resposta.blob();
        const url = URL.createObjectURL(arquivo);

        const link = document.createElement("a");
        link.href = url;
        link.download = "QR-Code-ENEM.png";
        link.click();

        setTimeout(() => URL.revokeObjectURL(url), 1000);

    } catch (erro) {
        alert("Não foi possível baixar. Verifique sua conexão e tente novamente.");
    }
}

/* INICIALIZAR */
atualizarQR();

</script>

</body>
</html>
