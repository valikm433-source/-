<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FrostLynx Studio | Создание игр</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #0f172a;
            --secondary: #1e293b;
            --accent: #3b82f6;
            --text: #f8fafc;
            --glow: rgba(59, 130, 246, 0.5);
        }

        body {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: var(--text);
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* Анимированный фон */
        .bg-animation {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.1;
        }

        /* Шапка */
        header {
            padding: 1rem 2rem;
            background: rgba(15, 23, 42, 0.9);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid var(--accent);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--text);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text);
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        /* Главный экран */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 0 2rem;
            margin-top: 80px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, var(--accent), #8b5cf6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .cta-button {
            display: inline-block;
            padding: 12px 30px;
            background: var(--accent);
            color: var(--text);
            text-decoration: none;
            border-radius: 5px;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px var(--glow);
        }

        /* Разделы */
        .section {
            padding: 100px 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--accent);
        }

        /* О нас */
        .about-content {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
            font-size: 1.2rem;
            line-height: 1.6;
        }

        /* Проекты */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .project-card {
            background: rgba(30, 41, 59, 0.6);
            border-radius: 15px;
            padding: 2rem;
            border: 1px solid rgba(59, 130, 246, 0.3);
            transition: transform 0.3s;
            text-align: center;
        }

        .project-card:hover {
            transform: translateY(-5px);
        }

        .project-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        /* Контакты */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .contact-info {
            background: rgba(30, 41, 59, 0.6);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid rgba(59, 130, 246, 0.3);
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .contact-icon {
            color: var(--accent);
            font-size: 1.5rem;
        }

        /* Хостинг информация */
        .hosting-info {
            background: rgba(30, 41, 59, 0.6);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid rgba(59, 130, 246, 0.3);
            margin-top: 2rem;
            text-align: center;
        }

        /* Подвал */
        footer {
            background: rgba(15, 23, 42, 0.9);
            padding: 2rem;
            text-align: center;
            border-top: 1px solid var(--accent);
            margin-top: 100px;
        }
    </style>
</head>
<body>
    <div class="bg-animation" id="bgAnimation"></div>

    <header>
        <div class="nav-container">
            <a href="#" class="logo">
                <span>⚡</span>
                FrostLynx Studio
            </a>
            <nav>
                <ul class="nav-links">
                    <li><a href="#home">Главная</a></li>
                    <li><a href="#about">О нас</a></li>
                    <li><a href="#projects">Проекты</a></li>
                    <li><a href="#hosting">Хостинг</a></li>
                    <li><a href="#contact">Контакты</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="hero-content">
            <h1>FrostLynx Studio</h1>
            <p>Создаём игры будущего с собственным хостингом</p>
            <a href="#projects" class="cta-button">Наши проекты</a>
        </div>
    </section>

    <section class="section" id="about">
        <h2 class="section-title">О нас</h2>
        <div class="about-content">
            <p>FrostLynx Studio - молодая и амбициозная команда разработчиков, создающая уникальные игровые проекты. Мы специализируемся на разработке игр различных жанров и предоставляем собственный хостинг для наших проектов.</p>
            <p style="margin-top: 1rem;">Наша миссия - создавать игры, которые вдохновляют и захватывают игроков по всему миру.</p>
        </div>
    </section>

    <section class="section" id="projects">
        <h2 class="section-title">Наши проекты</h2>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-icon">🐺</div>
                <h3>WOLF</h3>
                <p>Приключенческая игра в мире дикой природы. Исследуй леса, развивай своего волка и становись вожаком стаи.</p>
            </div>
            <div class="project-card">
                <div class="project-icon">🔲</div>
                <h3>PIXEL</h3>
                <p>Креативная пиксель-арт игра с уникальным геймплеем. Создавай, исследуй и открывай новые возможности.</p>
            </div>
            <div class="project-card">
                <div class="project-icon">🌌</div>
                <h3>CYBER DASH</h3>
                <p>Динамичный раннер в киберпанк-стиле с продвинутой графикой и захватывающим геймплеем.</p>
            </div>
        </div>
    </section>

    <section class="section" id="hosting">
        <h2 class="section-title">Наш хостинг</h2>
        <div class="hosting-info">
            <h3>🚀 FrostLynx Hosting</h3>
            <p>Мы предоставляем собственный надежный хостинг для всех наших проектов</p>
            <div style="margin-top: 1rem;">
                <p>✔️ Высокая производительность</p>
                <p>✔️ Защита от DDoS-атак</p>
                <p>✔️ Автоматическое резервное копирование</p>
                <p>✔️ Круглосуточная техническая поддержка</p>
            </div>
        </div>
    </section>

    <section class="section" id="contact">
        <h2 class="section-title">Контакты</h2>
        <div class="contact-grid">
            <div class="contact-info">
                <div class="contact-item">
                    <span class="contact-icon">📧</span>
                    <span>valikm433@gmail.com</span>
                </div>
                <div class="contact-item">
                    <span class="contact-icon">📱</span>
                    <span>Telegram: @frostLynxu</span>
                </div>
                <div class="contact-item">
                    <span class="contact-icon">🎮</span>
                    <span>Разработка игр и приложений</span>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 FrostLynx Studio. Все права защищены.</p>
    </footer>

    <script>
        // Создание частиц для фона
        function createParticles() {
            const container = document.getElementById('bgAnimation');
            for (let i = 0; i < 20; i++) {
                const particle = document.createElement('div');
                particle.style.cssText = `
                    position: absolute;
                    width: ${Math.random() * 5 + 1}px;
                    height: ${Math.random() * 5 + 1}px;
                    background: rgba(59, 130, 246, ${Math.random() * 0.3});
                    border-radius: 50%;
                    left: ${Math.random() * 100}%;
                    top: ${Math.random() * 100}%;
                    animation: float ${Math.random() * 10 + 5}s ease-in-out infinite;
                `;
                container.appendChild(particle);
            }
        }

        // Плавная прокрутка
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });

        // Добавление стилей для анимации
        const style = document.createElement('style');
        style.textContent = `
            @keyframes float {
                0%, 100% { transform: translateY(0px) rotate(0deg); }
                50% { transform: translateY(-20px) rotate(180deg); }
            }
        `;
        document.head.appendChild(style);

        // Инициализация
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            document.querySelector('footer p').textContent = `© ${new Date().getFullYear()} FrostLynx Studio. Все права защищены.`;
        });
    </script>
</body>
</html>
