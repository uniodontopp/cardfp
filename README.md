<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="robots" content="noindex, nofollow">
    <title>Meu Cartão Digital</title>
    <style>
        :root {
            --bg: #0a0a0a;
            --card: #1a1a1a;
            --text: #ffffff;
            --accent: #007aff;
        }

        body { 
            background: var(--bg); 
            color: var(--text); 
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
            display: flex; justify-content: center; align-items: center; min-height: 100vh; margin: 0;
        }

        .bento-grid { 
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            grid-gap: 12px;
            max-width: 400px;
            width: 90%;
            padding: 20px;
        }

        .card { 
            background: var(--card); border-radius: 24px; padding: 25px;
            text-decoration: none; color: inherit; display: flex;
            flex-direction: column; justify-content: center; align-items: center;
            transition: 0.3s; border: 1px solid #333;
        }

        .card:hover { transform: translateY(-5px); border-color: var(--accent); }
        .full { grid-column: span 2; }
        .profile-pic { width: 70px; height: 70px; border-radius: 50%; background: #333; margin-bottom: 15px; }
        h1 { font-size: 1.4rem; margin: 5px 0; }
        p { font-size: 0.9rem; opacity: 0.6; text-align: center; }
        .icon { font-size: 1.6rem; margin-bottom: 8px; }
    </style>
</head>
<body>

    <div class="bento-grid">
        <div class="card full">
            <div class="profile-pic"></div>
            <h1>Felipe Andrigo</h1>
            <p>Designer & Marketing</p>
        </div>

        <a href="https://wa.me/5518999999999" class="card">
            <span class="icon">📱</span>
            <span style="font-weight: bold;">WhatsApp</span>
        </a>

        <a href="https://instagram.com/seuuser" class="card">
            <span class="icon">📸</span>
            <span style="font-weight: bold;">Instagram</span>
        </a>

        <a href="https://linkedin.com/in/seuuser" class="card full">
            <span class="icon">💼</span>
            <span style="font-weight: bold;">LinkedIn Profissional</span>
        </a>
    </div>

</body>
</html>
