<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Site Oculto Interativo</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #121212;
      color: #fff;
      display: flex;
      justify-content: center;
      padding: 2rem;
    }

    .container {
      max-width: 600px;
      width: 100%;
      background: #1e1e1e;
      border-radius: 10px;
      padding: 2rem;
    }

    header {
      text-align: center;
      margin-bottom: 1rem;
    }

    header h1 {
      font-size: 1.5rem;
      color: #b983ff;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
    }

    .tabs input[type="radio"] {
      display: none;
    }

    .tabs label {
      background-color: #b983ff;
      padding: 0.6rem 1.2rem;
      margin: 0.2rem;
      border-radius: 5px;
      cursor: pointer;
      font-weight: bold;
      display: inline-block;
      color: #000;
      transition: background 0.2s;
    }

    .tabs label:hover {
      background-color: #d0a8ff;
    }

    .tabs input:checked + label {
      background-color: #7a37c0;
      color: #fff;
    }

    .section {
      display: none;
      margin-top: 1.5rem;
      background: #2c2c2c;
      padding: 1rem;
      border-radius: 5px;
    }

    /* Mostrar seções de acordo com o botão selecionado */
    #sec1:checked ~ .content #content1 {
      display: block;
    }

    #sec2:checked ~ .content #content2 {
      display: block;
    }

    #sec3:checked ~ .content #content3 {
      display: block;
    }

    .success-message {
      display: none;
      margin-top: 1rem;
      background: #015c4b;
      color: #c2f4e9;
      padding: 1rem;
      border-radius: 5px;
      font-weight: bold;
    }

    /* Mostrar a mensagem final apenas na Seção 3 */
    #sec3:checked ~ .content #success {
      display: block;
    }

    form {
      display: none;
      margin-top: 2rem;
      background: #2c2c2c;
      padding: 1.5rem;
      border-radius: 8px;
    }

    /* Mostrar o formulário só na seção 3 */
    #sec3:checked ~ .content form {
      display: block;
    }

    form h2 {
      margin-bottom: 1rem;
      color: #ffb3ec;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    form input, form textarea {
      width: 100%;
      padding: 0.75rem;
      margin: 0.5rem 0;
      border: none;
      border-radius: 5px;
      background: #1e1e1e;
      color: #fff;
      resize: vertical;
    }

    form button {
      background: #b983ff;
      color: #000;
      font-weight: bold;
      border: none;
      padding: 0.75rem 1.5rem;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.2s;
      width: 100%;
    }

    form button:hover {
      background: #d0a8ff;
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>🌑 Site Interativo - Tema Escuro</h1>
    </header>

    <div class="tabs">
      <input type="radio" name="tab" id="sec1" checked>
      <label for="sec1">🔍 Seção 1</label>

      <input type="radio" name="tab" id="sec2">
      <label for="sec2">📱 Seção 2</label>

      <input type="radio" name="tab" id="sec3">
      <label for="sec3">🔒 Seção 3</label>
    </div>

    <div class="content">
      <div id="content1" class="section">
        <p><strong>Seção 1:</strong> Bem-vindo(a)! Você descobriu a primeira parte da Seção.</p>
      </div>
      <div id="content2" class="section">
        <p><strong>Seção 2:</strong> Ótimo! Continue clicando para desbloquear tudo.</p>
      </div>
      <div id="content3" class="section">
        <p><strong>Seção 3:</strong> Quase lá! Prepare-se para a revelação final.</p>
      </div>

      <div id="success" class="success-message">
        🎉 Parabéns! Você desbloqueou todo o conteúdo!
      </div>

      <form>
        <h2>📨 Formulário de Contato</h2>
        <input type="text" placeholder="Seu nome" required>
        <input type="email" placeholder="Seu e-mail" required>
        <textarea rows="4" placeholder="Sua mensagem" required></textarea>
        <button type="submit">Enviar</button>
      </form>
    </div>
  </div>
</body>
</html>
