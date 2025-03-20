<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de Layout</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <aside class="menu-lateral">
            <h2>Menu</h2>
            <ul>
                <li><a href="#">conteúdo 1</a></li>
                <li><a href="#">conteúdo 2</a></li>
                <li><a href="#">conteúdo 3</a></li>
            </ul>
        </aside>
        <main class="principal">
            <div class="content-box">
                <h2>Conteúdo 1</h2>
                <button class="btn-animate" id="btn1">Clique Aqui</button>
                <div class="extra-info" id="info1" style="display:none;">
                    <p>Aqui está mais informação sobre o conteúdo 1!</p>
                </div>
            </div>
            <div class="content-box">
                <h2>Conteúdo 2</h2>
                <button class="btn-animate" id="btn2">Clique Aqui</button>
                <div class="extra-info" id="info2" style="display:none;">
                    <p>Aqui está mais informação sobre o conteúdo 2!</p>
                </div>
            </div>
            <div class="content-box">
                <h2>Conteúdo 3</h2>
                <button class="btn-animate" id="btn3">Clique Aqui</button>
                <div class="extra-info" id="info3" style="display:none;">
                    <p>Aqui está mais informação sobre o conteúdo 3!</p>
                </div>
            </div>
        </main>
    </div>

    <script>
        const buttons = document.querySelectorAll('.btn-animate');

        buttons.forEach(button => {
            button.addEventListener('click', () => {
                const buttonId = button.id;
                const contentId = `info${buttonId.charAt(buttonId.length - 1)}`;

                const content = document.getElementById(contentId);

                if (content.style.display === 'none' || content.style.display === '') {
                    content.style.display = 'block';
                } else {
                    content.style.display = 'none';
                }
            });
        });
    </script>
</body>
</html>
