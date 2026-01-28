<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="robots" content="noindex, nofollow"> <title>Cartão Digital | Marketing & Design</title>
    <style>
        :root {
            --bg: #0a0a0a;
            --card: #1a1a1a;
            --text: #ffffff;
            --accent: #007aff; /* Azul estilo Tech */
        }

        body { 
            background: var(--bg); 
            color: var(--text); 
            font-family: 'Inter', -apple-system, sans-serif;
            display: flex; justify-content: center; align-items: center; min-height: 100vh; margin: 0;
        }

        /* TELA DE SENHA */
        #lock { text-align: center; z-index: 100; }
        input { 
            background: #222; border: 1px solid #444; color: white; 
            padding: 12px; border-radius: 12px; text-align: center; margin-top: 10px;
        }

        /* GRID BENTO */
        #bento-container { 
            display: none; /* Escondido até digitar a senha */
            grid-template-columns: repeat(2, 1fr);
            grid-gap: 12px;
            max-width: 400px;
            width: 90%;
            padding: 20px;
        }

        .card { 
            background: var(--card); border-radius: 24px; padding: 20px;
            text-decoration: none; color: inherit; display: flex;
            flex-direction: column; justify-content: center; align-items: center;
            transition: 0.3s; border: 1px solid #333;
        }

        .card:hover { transform: translateY(-5px); border-color: var(--accent); }

        /* Variações de tamanho */
        .full { grid-column: span 2; }
        .tall { grid-row: span 2; }

        .profile-pic { width: 70px; height: 70px; border-radius: 50%; background: #333; margin-bottom: 10px; }
        h1 { font-size: 1.2rem; margin: 5px 0; }
        p { font-size: 0.8rem; opacity: 0.6; text-align: center; }
        .icon { font-size: 1.5rem; margin-bottom: 8px; }
    </style>
</head>
<body>

    <div id="lock">
        <p>Acesso Restrito</p>
        <input type="password" id="pass" placeholder="Senha" oninput="check()">
    </div>

    <div id="bento-container">
        <div class="card full">
            <div class="profile-pic"></div>
            <h1>Seu Nome</h1>
            <p>Designer & Marketing</p>
        </div>

        <a href="https://wa.me/5518999999999" class="card">
            <span class="icon">📱</span>
            <span>WhatsApp</span>
        </a>

        <a href="https://instagram.com/seuuser" class="card">
            <span class="icon">📸</span>
            <span>Instagram</span>
        </a>

        <a href="https://linkedin.com/in/seuuser" class="card full">
            <span class="icon">💼</span>
            <span>LinkedIn Profissional</span>
        </a>
    </div>

    <script>
        function check() {
            const val = document.getElementById('pass').value;
            if (val === '1234') { // ALTERE SUA SENHA AQUI
                document.getElementById('lock').style.display = 'none';
                document.getElementById('bento-container').style.display = 'grid';
            }
        }
    </script>
</body>
</html>
