<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>App de Animes e Mangás</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>App de Animes e Mangás</h1>
    </header>
    <main>
        <section id="form-section">
            <h2>Adicionar Anime ou Mangá</h2>
            <form id="item-form">
                <input type="text" id="item-name" placeholder="Nome do Anime ou Mangá" required>
                <button type="submit">Adicionar</button>
            </form>
        </section>
        <section id="list-section">
            <h2>Lista de Animes e Mangás</h2>
            <ul id="item-list"></ul>
        </section>
    </main>
    <footer>
        <p>Para mais informações, envie um e-mail para <a href="mailto:contato@animeemanga.com">contato@animeemanga.com</a>.</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f6f8fa;
    color: #24292e;
}

header {
    background-color: #24292e;
    color: #fff;
    padding: 1rem 0;
    text-align: center;
}

main {
    padding: 2rem;
    max-width: 800px;
    margin: 0 auto;
}

section {
    margin-bottom: 2rem;
}

h2 {
    border-bottom: 1px solid #e1e4e8;
    padding-bottom: 0.5rem;
}

form {
    display: flex;
    gap: 1rem;
}

input {
    flex: 1;
    padding: 0.5rem;
    border: 1px solid #e1e4e8;
    border-radius: 6px;
}

button {
    padding: 0.5rem 1rem;
    background-color: #2ea44f;
    color: #fff;
    border: none;
    border-radius: 6px;
    cursor: pointer;
}

button:hover {
    background-color: #2c974b;
}

ul {
    list-style: none;
    padding: 0;
}

li {
    background-color: #fff;
    margin-bottom: 0.5rem;
    padding: 0.5rem;
    border: 1px solid #e1e4e8;
    border-radius: 6px;
}
document.addEventListener('DOMContentLoaded', () => {
    const form = document.getElementById('item-form');
    const itemList = document.getElementById('item-list');

    form.addEventListener('submit', (e) => {
        e.preventDefault();
        const itemName = document.getElementById('item-name').value;
        if (itemName) {
            const listItem = document.createElement('li');
            listItem.textContent = itemName;
            itemList.appendChild(listItem);
            form.reset();
        }
    });
});
