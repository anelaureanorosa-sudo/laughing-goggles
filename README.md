# laughing-goggles
```javascript const listaDados = ["Cuidar da terra evita a erosão e garante que as plantas cresçam fortes."

### 1. index.html (A Estrutura)
Este arquivo monta a página e chama os outros dois.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Dicas do Agrinho</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>🌱 Dicas do Agrinho</h1>
        <p id="dica">Clique no botão para aprender algo novo!</p>
        <button id="btn-dica">Gerar Dica</button>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

### 2. style.css (O Visual)
Este arquivo dá o tom verde e organizado de sustentabilidade.

```css
body {
    background-color: #e8f5e9;
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.container {
    background: white;
    padding: 20px;
    border-radius: 15px;
    text-align: center;
    box-shadow: 0px 4px 10px rgba(0,0,0,0.1);
}

h1 { color: #2e7d32; }

button {
    background-color: #4caf50;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
}
```

### 3. script.js (A Lógica)
Este arquivo contém a lista com as suas mensagens.

```javascript
const dicas = [
    "Cuidar da terra evita a erosão e garante plantas fortes.",
    "Economizar água é essencial para um futuro sustentável.",
    "A reciclagem transforma o que era lixo em novos recursos.",
    "Plantar árvores ajuda a equilibrar o clima do nosso planeta."
];

const btn = document.getElementById('btn-dica');
const textoDica = document.getElementById('dica');

btn.addEventListener('click', function() {
    const numeroAleatorio = Math.floor(Math.random() * dicas.length);
    textoDica.innerText = dicas[numeroAleatorio];
});
```
