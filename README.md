<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Biblioteca da Alicia</title>
<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
:root{
--bg:#ffffff;
--text:#111111;
--menu:#f0f0f0;
--card:#f9f9f9;
--border:#e0e0e0;
--shadow:rgba(0,0,0,0.1);
}
.offwhite{
--bg:#f4efe6;
--text:#2a2a2a;
--menu:#e0d8cc;
--card:#e9e1d5;
--border:#d4c9ba;
--shadow:rgba(0,0,0,0.15);
}
.black{
--bg:#111111;
--text:#ffffff;
--menu:#1a1a1a;
--card:#2a2a2a;
--border:#3a3a3a;
--shadow:rgba(255,255,255,0.1);
}
body{
margin:0;
background:var(--bg);
color:var(--text);
font-family:'Georgia', serif;
transition:0.3s;
min-height:100vh;
}
/* MENU */
.menu{
display:flex;
justify-content:space-between;
align-items:center;
padding:15px 40px;
background:var(--menu);
box-shadow:0 2px 10px var(--shadow);
position:sticky;
top:0;
z-index:100;
}
.logo {
font-size:24px;
font-weight:bold;
letter-spacing:2px;
}
.menu ul{
display:flex;
gap:30px;
list-style:none;
margin:0;
padding:0;
}
.menu a{
text-decoration:none;
color:var(--text);
font-weight:bold;
font-size:18px;
transition:0.3s;
position:relative;
}
.menu a:hover {
color:#B55690;
}
.menu a::after {
content:'';
position:absolute;
bottom:-5px;
left:0;
width:0;
height:2px;
background:#B55690;
transition:0.3s;
}
.menu a:hover::after {
width:100%;
}
.tema{
font-size:24px;
border:none;
background:none;
cursor:pointer;
color:var(--text);
transition:0.3s;
}
.tema:hover {
transform:scale(1.2);
color:#B55690;
}
/* Conteudo principal */
main {
padding:40px;
max-width:1200px;
margin:0 auto;
}
h1 {
text-align:center;
margin:40px 0;
font-size:48px;
font-weight:normal;
letter-spacing:3px;
position:relative;
}
h1::after {
content:'';
display:block;
width:100px;
height:2px;
background:#B55690;
margin:20px auto;
}
/* BIBLIOTECA */
.biblioteca {
display:grid;
grid-template-columns:repeat(auto-fit, minmax(300px, 1fr));
gap:40px;
padding:20px;
justify-items:center;
}
.livro{
text-decoration:none;
color:var(--text);
width:300px;
transition:0.3s;
cursor:pointer;
position:relative;
background:var(--card);
border-radius:15px;
padding:20px;
box-shadow:0 4px 15px var(--shadow);
}
.livro:hover {
transform:translateY(-10px);
box-shadow:0 10px 30px var(--shadow);
}
.livro img{
width:100%;
height:400px;
object-fit:cover;
border-radius:10px;
box-shadow:0 4px 10px var(--shadow);
transition:0.3s;
}
.livro h3{
margin:20px 0 10px;
text-align:center;
font-size:24px;
color:#B55690;
}
.sinopse {
font-size:14px;
line-height:1.6;
text-align:justify;
margin-bottom:15px;
padding:0 10px;
font-style:italic;
}
.leia-mais {
display:inline-block;
color:#B55690;
font-weight:bold;
margin-top:10px;
text-align:center;
width:100%;
}
/* SEÇÃO DE COMENTÁRIOS */
.comentarios-section {
max-width:800px;
margin:60px auto;
padding:30px;
background:var(--card);
border-radius:20px;
box-shadow:0 4px 20px var(--shadow);
}
.comentarios-section h2 {
font-size:28px;
margin-bottom:20px;
text-align:center;
color:#B55690;
}
.comentarios-lista {
margin-bottom:30px;
max-height:500px;
overflow-y:auto;
padding:10px;
}
.comentario {
padding:20px;
margin-bottom:15px;
background:var(--bg);
border-radius:15px;
border-left:4px solid #B55690;
box-shadow:0 2px 10px var(--shadow);
}
.comentario-header {
display:flex;
justify-content:space-between;
align-items:center;
margin-bottom:10px;
}
.comentario-nome {
font-weight:bold;
color:#B55690;
font-size:18px;
}
.comentario-data {
font-size:12px;
color:var(--text);
opacity:0.7;
}
.comentario-texto {
font-size:16px;
line-height:1.6;
margin-bottom:10px;
}
.comentario-respostas {
margin-left:30px;
padding-left:20px;
border-left:2px solid var(--border);
margin-top:15px;
}
.resposta {
padding:15px;
margin-bottom:10px;
background:var(--card);
border-radius:10px;
}
/* FORMULÁRIO DE COMENTÁRIOS */
.comentario-form {
background:var(--bg);
padding:25px;
border-radius:15px;
}
.comentario-form h3 {
margin-bottom:20px;
font-size:22px;
color:#B55690;
}
.form-grupo {
margin-bottom:20px;
}
.form-grupo label {
display:block;
margin-bottom:5px;
font-weight:bold;
font-size:14px;
}
.form-grupo input,
.form-grupo textarea,
.form-grupo select {
width:100%;
padding:12px;
border:2px solid var(--border);
border-radius:8px;
background:var(--bg);
color:var(--text);
font-family:Georgia, serif;
font-size:16px;
transition:0.3s;
}
.form-grupo input:focus,
.form-grupo textarea:focus,
.form-grupo select:focus {
outline:none;
border-color:#B55690;
}
textarea {
min-height:120px;
resize:vertical;
}
.btn {
background:#B55690;
color:white;
border:none;
padding:12px 30px;
border-radius:8px;
font-size:16px;
font-weight:bold;
cursor:pointer;
transition:0.3s;
font-family:Georgia, serif;
}
.btn:hover {
background:#9e7008;
transform:scale(1.02);
}
.btn-pequeno {
padding:8px 15px;
font-size:14px;
background:var(--border);
color:var(--text);
margin-left:10px;
}
/* MODAL */
.modal {
display:none;
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,0.9);
z-index:1000;
justify-content:center;
align-items:center;
}
.modal-conteudo {
background:var(--bg);
max-width:800px;
width:90%;
max-height:90vh;
overflow-y:auto;
border-radius:20px;
padding:40px;
position:relative;
box-shadow:0 10px 40px rgba(0,0,0,0.3);
}
.modal-fechar {
position:absolute;
top:20px;
right:20px;
font-size:40px;
cursor:pointer;
color:var(--text);
transition:0.3s;
z-index:2;
}
.modal-fechar:hover {
color:#B55690;
transform:scale(1.2) rotate(90deg);
}
.modal img {
width:100%;
max-height:400px;
object-fit:cover;
border-radius:10px;
margin:20px 0;
box-shadow:0 4px 15px var(--shadow);
}
.modal h2 {
font-size:36px;
margin:20px 0;
color:#B55690;
text-align:center;
}
.modal .sinopse-completa {
font-size:18px;
line-height:1.8;
margin:30px 0;
white-space:pre-line;
font-style:italic;
padding:20px;
background:var(--card);
border-radius:10px;
}
.modal p {
font-size:18px;
line-height:1.8;
margin-bottom:30px;
}
footer {
background:var(--menu);
padding:30px;
text-align:center;
margin-top:60px;
border-top:2px solid var(--border);
}
.footer-links {
display:flex;
justify-content:center;
gap:30px;
margin:20px 0;
flex-wrap:wrap;
}
.footer-links a {
color:var(--text);
text-decoration:none;
transition:0.3s;
}
.footer-links a:hover {
color:#B55690;
}
/* RESPONSIVIDADE */
@media (max-width:768px) {
.menu {
flex-direction:column;
gap:15px;
padding:15px;
}
    .menu ul {
gap:20px;
}
    h1 {
font-size:32px;
}
    .biblioteca {
grid-template-columns:1fr;
}
    main {
padding:20px;
}
    .comentarios-section {
padding:20px;
margin:30px 20px;
}
    .comentario-respostas {
margin-left:15px;
padding-left:10px;
}
    .modal-conteudo {
padding:20px;
}
}
/* ANIMAÇÕES */
@keyframes fadeIn {
from {
opacity:0;
transform:translateY(20px);
}
to {
opacity:1;
transform:translateY(0);
}
}
.comentario, .livro {
animation:fadeIn 0.5s ease-out;
}
/* CITAÇÕES */
.citacao {
text-align:center;
font-size:20px;
font-style:italic;
margin:40px 0;
padding:20px;
color:#B55690;
border-left:4px solid #B55690;
background:var(--card);
}
/* SEÇÃO DE CAPÍTULOS (NOVO) */
.capitulos-container {
max-width:900px;
margin:40px auto;
}
.capitulo-item {
background:var(--card);
border-radius:15px;
padding:25px;
margin-bottom:20px;
box-shadow:0 4px 15px var(--shadow);
border-left:4px solid #B55690;
}
.capitulo-header {
display:flex;
justify-content:space-between;
align-items:center;
margin-bottom:15px;
flex-wrap:wrap;
gap:10px;
}
.capitulo-titulo {
font-size:24px;
color:#B55690;
}
.capitulo-numero {
font-size:18px;
color:var(--text);
opacity:0.7;
}
.capitulo-data {
font-size:14px;
color:var(--text);
opacity:0.6;
}
.capitulo-conteudo {
font-size:16px;
line-height:1.8;
margin:20px 0;
white-space:pre-line;
}
.form-capitulo {
background:var(--card);
border-radius:20px;
padding:30px;
margin:40px auto;
max-width:800px;
}
.form-capitulo h2 {
color:#B55690;
margin-bottom:20px;
text-align:center;
}
.btn-editar {
background:#4a6fa5;
}
.btn-editar:hover {
background:#3d5f8a;
}
.btn-excluir {
background:#a54a4a;
}
.btn-excluir:hover {
background:#8f3e3e;
}
.btn-voltar {
background:var(--border);
color:var(--text);
margin-right:10px;
}
</style>
</head>
<body>

<nav class="menu">
<div class="logo">📚 Biblioteca da Alicia</div>
<ul>
<li><a href="#" onclick="mostrarHome()">Home</a></li>
<li><a href="#" onclick="mostrarHistorias()">Histórias</a></li>
<li><a href="#" onclick="mostrarSobre()">Sobre</a></li>
</ul>
<button class="tema" onclick="trocarTema()">🌙</button>
</nav>

<main id="conteudo-principal">
<!-- Conteúdo será carregado aqui -->
</main>

<!-- Modal para ler história -->
<div class="modal" id="modal-leitura">
<div class="modal-conteudo">
<span class="modal-fechar" onclick="fecharModal()">&times;</span>
<div id="conteudo-historia"></div>
</div>
</div>

<footer>
<p>&copy; 2026 Biblioteca da Alicia - Todos os direitos reservados</p>
<div class="footer-links">
<a href="#" onclick="mostrarHome()">Home</a>
<a href="#" onclick="mostrarHistorias()">Histórias</a>
<a href="#" onclick="mostrarSobre()">Sobre</a>
<a href="#" onclick="mostrarPrivacidade()">Política de Privacidade</a>
</div>
</footer>

<script>
// ===== SISTEMA PARA TODOS VEREM OS CAPÍTULOS =====
// Aqui você vai colocar SEUS capítulos (só você edita)

const capitulosParaTodos = [
    {
        id: 1,
        livroId: 1,
        numero: 1,
        titulo: "O Primeiro Silêncio",
        conteudo: `O som do relógio na parede era o único que ousava romper o silêncio da biblioteca municipal. Agatha observava as estantes como se elas pudessem confessar um crime.

O assistente entregou a ela um livro envolto em plástico. A Megera Domada. Abriu na página marcada e leu a dedicatória escrita à mão: "De seu filho querido, para minha mãe amada. - G. A."

O terceiro crime. O terceiro livro. E ainda nenhuma pista sólida.`,
        data: "2024-03-08"
    },
    {
        id: 2,
        livroId: 1,
        numero: 2,
        titulo: "Vozes na Estante",
        conteudo: `A biblioteca fechava às oito. Agatha entrou às sete e se escondeu entre as estantes do fundo.

Quando o último funcionário saiu, as luzes se apagaram. Mas não completamente. Uma luz azulada vinha da seção de livros raros.

Agatha se aproximou em silêncio e viu uma figura encapuzada folheando um livro. Era o mesmo livro. A Megera Domada.`,
        data: "2024-03-08"
    }
];

// Modificar a função de carregar capítulos

// Sistema de temas
let tema = 0;

function trocarTema() {
    document.body.classList.remove("offwhite","black");
    tema++;
    
    if(tema === 1){
        document.body.classList.add("offwhite");
    } else if(tema === 2){
        document.body.classList.add("black");
    } else {
        tema = 0;
    }
}

// Banco de dados de livros com suas sinopses
const livros = [
    {
        id: 1,
        titulo: "Assassino da Biblioteca",
        sinopse: `O silêncio não é sempre reconfortante, ele pode te corroer por dentro, as vezes, até por fora. 
Nem toda voz está viva. E nem toda voz é clara.

Agatha é uma investigadora que não vai parar enquanto não achar o criminoso. De mãos atadas, praticamente sem nenhuma prova, ela terá que fazer o possível e o impossível para achá-lo.

Peatle, a única vítima que sobreviveu, pode ser uma peça chave para a investigação.
Peatle, a única vítima que sobreviveu.

O apelido "Assassino da Biblioteca" não é à toa. Todos os ataques até agora ocorreram em bibliotecas. A única coisa que marca seus crimes é um livro: A Megera Domada, de William Shakespeare. Dentro dele, uma dedicatória:
"De seu filho querido, para minha mãe amada. - G. A."

Existem coisas que nem a pessoa mais inteligente poderia prever, nem mesmo Agatha.
Coisas que não deveriam ser possíveis no mundo real.
Pelo menos, era o que achávamos.`,
        imagem: "https://img.wattpad.com/cover/388186412-256-k897628.jpg"
    },
    {
        id: 2,
        titulo: "Casa de Dois Andares",
        sinopse: `Aurora lia Rosa como ninguém jamais poderia fazer.

Aprenderam a se proteger desde muito cedo, ajudando contra os valentões do orfanato, contra as pessoas malvadas do mundo. Elas nunca receberam o amor que mereciam, mas o amor que tinham uma pela outra ultrapassava todas as barreiras, que o tempo, espaço e a vida tentava impor.

Em 1950, no interior de Minas Gerais. Aurora era uma amante da leitura, escrevia de maneira brilhante, o contrário de sua amiga Rosa, ela nunca aprendeu a ler, mesmo tentando de tudo.

Após a maioridade, seguiram caminhos diferentes. Aurora estudou, se formou e até se casou. Por medo, Rosa abandonou quem mais amava, achando que estava lhe fazendo um favor.

Mas o reencontro anos depois revela o que Aurora tentava esconder: estava exausta. Com um bebê nos braços e um marido violento ao lado, ela já não conseguia fingir que a vida estava bem.

Foi então que Rosa voltou a fazer o que sempre fez: proteger.`,
        imagem: "https://img.wattpad.com/cover/398767553-144-k798846.jpg"
    }
];

// Banco de dados de comentários
let comentarios = [
    
];

// ===== SISTEMA DE CAPÍTULOS (SALVO AUTOMATICAMENTE) =====

// Carregar capítulos salvos ou começar vazio
// Seus capítulos que TODOS vão ver
let capitulos = [
    {
        id: 1,
        livroId: 1,
        numero: 1,
        titulo: "O Primeiro Silêncio",
        conteudo: `O som do relógio na parede era o único que ousava romper o silêncio da biblioteca municipal. Agatha observava as estantes como se elas pudessem confessar um crime.

O assistente entregou a ela um livro envolto em plástico. A Megera Domada. Abriu na página marcada e leu a dedicatória escrita à mão: "De seu filho querido, para minha mãe amada. - G. A."

O terceiro crime. O terceiro livro. E ainda nenhuma pista sólida.`,
        data: "2024-03-08"
    },
    {
        id: 2,
        livroId: 1,
        numero: 2,
        titulo: "Vozes na Estante",
        conteudo: `A biblioteca fechava às oito. Agatha entrou às sete e se escondeu entre as estantes do fundo.

Quando o último funcionário saiu, as luzes se apagaram. Mas não completamente. Uma luz azulada vinha da seção de livros raros.

Agatha se aproximou em silêncio e viu uma figura encapuzada folheando um livro. Era o mesmo livro. A Megera Domada.`,
        data: "2024-03-08"
    }
];

// Função para salvar capítulos no navegador
function salvarCapitulos() {
    localStorage.setItem('capitulos', JSON.stringify(capitulos));
}

// Função para mostrar a página de histórias (com os livros)
function mostrarHistorias() {
    const principal = document.getElementById('conteudo-principal');
    principal.innerHTML = `
        <h1>Minhas Histórias</h1>
        
        <div class="biblioteca" id="biblioteca-historias">
            ${livros.map(livro => `
                <div class="livro" onclick="mostrarCapitulosLivro(${livro.id})">
                    <img src="${livro.imagem}" alt="${livro.titulo}">
                    <h3>${livro.titulo}</h3>
                    <div class="sinopse">Clique para ver os capítulos</div>
                    <span class="leia-mais">📖 Ver capítulos</span>
                </div>
            `).join('')}
        </div>
    `;
}

// Função para mostrar os capítulos de um livro específico
function mostrarCapitulosLivro(livroId) {
    const livro = livros.find(l => l.id === livroId);
    const capitulosDoLivro = capitulos.filter(c => c.livroId === livroId);
    
    // Ordenar capítulos por número
    capitulosDoLivro.sort((a, b) => a.numero - b.numero);
    
    const principal = document.getElementById('conteudo-principal');
    principal.innerHTML = `
        <button class="btn btn-voltar" onclick="mostrarHistorias()">← Voltar para Histórias</button>
        
        <h1>${livro.titulo}</h1>
        
        <div style="text-align: center; margin: 30px;">
            <button class="btn" onclick="mostrarFormCapitulo(${livroId})">✍️ Escrever novo capítulo</button>
        </div>
        
        <div class="capitulos-container" id="lista-capitulos">
            ${capitulosDoLivro.length === 0 ? `
                <div style="text-align:center; padding:50px; background:var(--card); border-radius:15px;">
                    <p style="font-size:18px; margin-bottom:20px;">📝 Nenhum capítulo publicado ainda</p>
                    <p>Seja a primeira voz a ecoar nesta história!</p>
                </div>
            ` : capitulosDoLivro.map(cap => `
                <div class="capitulo-item" id="capitulo-${cap.id}">
                    <div class="capitulo-header">
                        <div>
                            <span class="capitulo-numero">Capítulo ${cap.numero}</span>
                            <h3 class="capitulo-titulo">${cap.titulo}</h3>
                        </div>
                        <span class="capitulo-data">${new Date(cap.data).toLocaleDateString('pt-BR')}</span>
                    </div>
                    
                    <div class="capitulo-conteudo" id="conteudo-${cap.id}">
                        ${cap.conteudo.substring(0, 300)}...
                    </div>
                    
                    <div style="margin: 20px 0;">
                        <button class="btn btn-pequeno" onclick="lerCapituloCompleto(${cap.id})">📖 Ler completo</button>
                        <button class="btn btn-pequeno btn-editar" onclick="editarCapitulo(${cap.id})">✏️ Editar</button>
                        <button class="btn btn-pequeno btn-excluir" onclick="excluirCapitulo(${cap.id})">🗑️ Excluir</button>
                    </div>
                    
                    <!-- Comentários do capítulo (escondidos inicialmente) -->
                    <div id="comentarios-cap-${cap.id}" style="display:none; margin-top:20px;">
                        <!-- Aqui vão os comentários -->
                    </div>
                </div>
            `).join('')}
        </div>
    `;
}

// Função para mostrar formulário de novo capítulo
function mostrarFormCapitulo(livroId) {
    const livro = livros.find(l => l.id === livroId);
    const proximoNumero = capitulos.filter(c => c.livroId === livroId).length + 1;
    
    const principal = document.getElementById('conteudo-principal');
    principal.innerHTML = `
        <button class="btn btn-voltar" onclick="mostrarCapitulosLivro(${livroId})">← Voltar para capítulos</button>
        
        <div class="form-capitulo">
            <h2>✍️ Escrevendo: ${livro.titulo}</h2>
            
            <form onsubmit="salvarCapitulo(event, ${livroId})">
                <div class="form-grupo">
                    <label>Número do capítulo:</label>
                    <input type="number" id="cap-numero" value="${proximoNumero}" readonly style="background:var(--border);">
                </div>
                
                <div class="form-grupo">
                    <label>Título do capítulo:</label>
                    <input type="text" id="cap-titulo" required placeholder="Ex: O Primeiro Encontro">
                </div>
                
                <div class="form-grupo">
                    <label>Conteúdo:</label>
                    <textarea id="cap-conteudo" required placeholder="Escreva seu capítulo aqui..."></textarea>
                </div>
                
                <button type="submit" class="btn">Publicar capítulo</button>
            </form>
        </div>
    `;
}

// Função para salvar capítulo
function salvarCapitulo(event, livroId) {
    event.preventDefault();
    
    const novoCapitulo = {
        id: Date.now(), // ID único baseado no horário
        livroId: livroId,
        numero: parseInt(document.getElementById('cap-numero').value),
        titulo: document.getElementById('cap-titulo').value,
        conteudo: document.getElementById('cap-conteudo').value,
        data: new Date().toISOString().split('T')[0],
        comentarios: []
    };
    
    capitulos.push(novoCapitulo);
    salvarCapitulos(); // Salva no navegador
    
    alert('Capítulo publicado com sucesso! 📚');
    mostrarCapitulosLivro(livroId);
}

// Função para ler capítulo completo
function lerCapituloCompleto(capituloId) {
    const cap = capitulos.find(c => c.id === capituloId);
    if (!cap) return;
    
    const livro = livros.find(l => l.id === cap.livroId);
    
    const modal = document.getElementById('modal-leitura');
    const conteudo = document.getElementById('conteudo-historia');
    
    conteudo.innerHTML = `
        <h2>${livro.titulo}</h2>
        <h3 style="color: var(--text); margin: 10px 0 30px;">Capítulo ${cap.numero}: ${cap.titulo}</h3>
        <div style="font-size:18px; line-height:1.8; white-space:pre-line;">${cap.conteudo}</div>
        
        <div style="margin-top:40px;">
            <button class="btn" onclick="comentarCapitulo(${cap.id})">💬 Comentar este capítulo</button>
        </div>
    `;
    
    modal.style.display = 'flex';
}

// Função para editar capítulo
function editarCapitulo(capituloId) {
    const cap = capitulos.find(c => c.id === capituloId);
    if (!cap) return;
    
    const principal = document.getElementById('conteudo-principal');
    principal.innerHTML = `
        <button class="btn btn-voltar" onclick="mostrarCapitulosLivro(${cap.livroId})">← Voltar</button>
        
        <div class="form-capitulo">
            <h2>✏️ Editando Capítulo ${cap.numero}</h2>
            
            <form onsubmit="atualizarCapitulo(event, ${cap.id})">
                <div class="form-grupo">
                    <label>Título:</label>
                    <input type="text" id="edit-titulo" value="${cap.titulo}" required>
                </div>
                
                <div class="form-grupo">
                    <label>Conteúdo:</label>
                    <textarea id="edit-conteudo" required>${cap.conteudo}</textarea>
                </div>
                
                <button type="submit" class="btn">Salvar alterações</button>
            </form>
        </div>
    `;
}

// Função para atualizar capítulo
function atualizarCapitulo(event, capituloId) {
    event.preventDefault();
    
    const cap = capitulos.find(c => c.id === capituloId);
    if (cap) {
        cap.titulo = document.getElementById('edit-titulo').value;
        cap.conteudo = document.getElementById('edit-conteudo').value;
        
        salvarCapitulos();
        alert('Capítulo atualizado! ✨');
        mostrarCapitulosLivro(cap.livroId);
    }
}

// Função para excluir capítulo
function excluirCapitulo(capituloId) {
    if (confirm('Tem certeza que quer excluir este capítulo? Essa ação não pode ser desfeita.')) {
        const cap = capitulos.find(c => c.id === capituloId);
        if (cap) {
            capitulos = capitulos.filter(c => c.id !== capituloId);
            salvarCapitulos();
            mostrarCapitulosLivro(cap.livroId);
        }
    }
}

// Funções de navegação
function mostrarHome() {
    document.querySelector('h1')?.remove();
    
    const principal = document.getElementById('conteudo-principal');
    principal.innerHTML = `
        <h1>Biblioteca da Alicia</h1>
        
        <div class="citacao">
            "O silêncio não é sempre reconfortante,<br>
            ele pode te corroer por dentro,<br>
            as vezes, até por fora."
        </div>
        
        <div class="biblioteca" id="biblioteca">
            ${livros.map(livro => `
                <div class="livro" onclick="abrirHistoria(${livro.id})">
                    <img src="${livro.imagem}" alt="${livro.titulo}">
                    <h3>${livro.titulo}</h3>
                    <div class="sinopse">${livro.sinopse.substring(0, 150)}...</div>
                    <span class="leia-mais">Clique para ler a sinopse completa</span>
                </div>
            `).join('')}
        </div>
        
        <div class="comentarios-section">
            <h2>💬 Vozes que encontraram eco</h2>
            <div class="comentarios-lista" id="lista-comentarios"></div>
            
            <div class="comentario-form">
                <h3>Deixe sua voz</h3>
                <form onsubmit="adicionarComentario(event)">
                    <div class="form-grupo">
                        <label>Seu nome:</label>
                        <input type="text" id="nome" required placeholder="Como prefere ser chamado?">
                    </div>
                    <div class="form-grupo">
                        <label>Seu comentário:</label>
                        <textarea id="texto" required placeholder="O que ecoou em você?"></textarea>
                    </div>
                    <div class="form-grupo">
                        <label>Sua avaliação:</label>
                        <select id="avaliacao">
                            <option value="5">⭐⭐⭐⭐⭐ - Ecoou profundamente</option>
                            <option value="4">⭐⭐⭐⭐ - Tocou</option>
                            <option value="3">⭐⭐⭐ - Interessante</option>
                            <option value="2">⭐⭐ - Poderia ecoar mais</option>
                            <option value="1">⭐ - Não ecoou</option>
                        </select>
                    </div>
                    <button type="submit" class="btn">Compartilhar</button>
                </form>
            </div>
        </div>
    `;
    
    carregarComentarios();
}

function mostrarSobre() {
    const principal = document.getElementById('conteudo-principal');
    principal.innerHTML = `
        <h1>Sobre a Autora</h1>
        <div style="max-width:800px; margin:0 auto; padding:20px;">
            <img src="https://picsum.photos/300/300?random=3" alt="Alicia" style="width:200px; height:200px; border-radius:50%; margin:20px auto; display:block; border:4px solid #B55690;">
            <h2 style="text-align:center; color:#B55690; margin:20px 0;">Alicia</h2>
            <p style="font-size:18px; line-height:1.8; margin:30px 0; font-style:italic;">
                "Escrevo sobre o silêncio que grita, sobre vozes que não se calam, 
                sobre amores que transcendem o tempo e o espaço."
            </p>
            <p style="font-size:16px; line-height:1.8; margin:30px 0;">
                Alicia começou a escrever aos 15 anos, descobrindo que as palavras têm o poder 
                de dar voz ao que o silêncio tenta calar. Suas histórias exploram os mistérios 
                da alma humana, os laços que nos unem e os segredos que nos consomem.
            </p>
            <p style="font-size:16px; line-height:1.8; margin:30px 0;">
                Inspirada pelas bibliotecas silenciosas e pelos corredores cheios de histórias 
                não contadas, ela cria narrativas onde o sobrenatural e o real se encontram, 
                onde o amor e o mistério caminham lado a lado.
            </p>
            <div style="display:flex; justify-content:center; gap:20px; margin:40px 0;">
                <a href="#" style="color:var(--text); text-decoration:none;">📧 Email</a>
                <a href="#" style="color:var(--text); text-decoration:none;">📷 Instagram</a>
                <a href="#" style="color:var(--text); text-decoration:none;">📘 Facebook</a>
            </div>
        </div>
    `;
}

function mostrarPrivacidade() {
    const principal = document.getElementById('conteudo-principal');
    principal.innerHTML = `
        <h1>Vozes em Confiança</h1>
        <div style="max-width:800px; margin:0 auto; padding:20px;">
            <p style="font-size:18px; line-height:1.8; margin:30px 0; font-style:italic;">
                "Nem toda voz está viva. E nem toda voz é clara. 
                Mas aqui, todas as vozes são respeitadas."
            </p>
            
            <h2 style="margin:40px 0 20px;">1. O que guardamos</h2>
            <p style="line-height:1.8;">Guardamos apenas seu nome e as palavras que escolhe compartilhar conosco - seus comentários, suas histórias, suas impressões.</p>
            
            <h2 style="margin:40px 0 20px;">2. O que fazemos com elas</h2>
            <p style="line-height:1.8;">Suas palavras vivem aqui, como parte das histórias que contamos. Elas inspiram, ecoam e criam conexões entre leitores e autora.</p>
            
            <h2 style="margin:40px 0 20px;">3. Suas pegadas digitais</h2>
            <p style="line-height:1.8;">Um pequeno arquivo guarda sua preferência entre a luz e a escuridão (nosso tema claro/escuro). Nada mais.</p>
            
            <h2 style="margin:40px 0 20px;">4. Se quiser falar conosco</h2>
            <p style="line-height:1.8;">Para questões sobre privacidade ou para pedir que suas palavras sejam silenciadas (removidas), escreva para: vozes@bibliotecadaalicia.com</p>
        </div>
    `;
}

// Função para abrir história no modal
function abrirHistoria(id) {
    const livro = livros.find(l => l.id === id);
    if (livro) {
        const modal = document.getElementById('modal-leitura');
        const conteudo = document.getElementById('conteudo-historia');
        conteudo.innerHTML = `
            <h2>${livro.titulo}</h2>
            <img src="${livro.imagem}" alt="${livro.titulo}">
            <div class="sinopse-completa">${livro.sinopse}</div>
            <button class="btn" onclick="comentarHistoria(${id})">Compartilhar o que ecoou em você</button>
        `;
        modal.style.display = 'flex';
    }
}

function fecharModal() {
    document.getElementById('modal-leitura').style.display = 'none';
}

// Sistema de comentários
function carregarComentarios() {
    const lista = document.getElementById('lista-comentarios');
    if (lista) {
        lista.innerHTML = comentarios.map(comentario => `
            <div class="comentario">
                <div class="comentario-header">
                    <span class="comentario-nome">${comentario.nome}</span>
                    <span class="comentario-data">${new Date(comentario.data).toLocaleDateString('pt-BR')}</span>
                </div>
                <div style="margin-bottom:10px;">${'⭐'.repeat(comentario.avaliacao)}</div>
                <div class="comentario-texto">${comentario.texto}</div>
                <button class="btn btn-pequeno" onclick="responderComentario(${comentario.id})">Responder</button>
                <div class="comentario-respostas" id="respostas-${comentario.id}">
                    ${comentario.respostas.map(resposta => `
                        <div class="resposta">
                            <div class="comentario-header">
                                <span class="comentario-nome">↳ ${resposta.nome}</span>
                                <span class="comentario-data">${new Date(resposta.data).toLocaleDateString('pt-BR')}</span>
                            </div>
                            <div>${resposta.texto}</div>
                        </div>
                    `).join('')}
                </div>
            </div>
        `).join('');
    }
}

function adicionarComentario(event) {
    event.preventDefault();
    
    const nome = document.getElementById('nome').value;
    const texto = document.getElementById('texto').value;
    const avaliacao = document.getElementById('avaliacao').value;
    
    const novoComentario = {
        id: comentarios.length + 1,
        nome: nome,
        texto: texto,
        data: new Date().toISOString().split('T')[0],
        avaliacao: parseInt(avaliacao),
        respostas: []
    };
    
    comentarios.push(novoComentario);
    carregarComentarios();
    event.target.reset();
    
    alert('Sua voz foi ouvida. Obrigada por compartilhar!');
}

function responderComentario(id) {
    const nome = prompt('Seu nome:');
    const texto = prompt('Sua resposta:');
    
    if (nome && texto) {
        const comentario = comentarios.find(c => c.id === id);
        if (comentario) {
            comentario.respostas.push({
                nome: nome,
                texto: texto,
                data: new Date().toISOString().split('T')[0]
            });
            carregarComentarios();
        }
    }
}

function comentarHistoria(id) {
    const livro = livros.find(l => l.id === id);
    if (livro) {
        fecharModal();
        setTimeout(() => {
            document.getElementById('nome').value = '';
            document.getElementById('texto').value = `Sobre "${livro.titulo}": `;
            document.getElementById('texto').focus();
        }, 300);
    }
}

// Fechar modal com clique fora
window.onclick = function(event) {
    const modal = document.getElementById('modal-leitura');
    if (event.target === modal) {
        fecharModal();
    }
}

// Inicializar página
mostrarHome();
</script>

</body>
</html>