<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Duck Dash: Chaos Spinner</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            background: #0f172a;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            touch-action: none;
        }
        #game-container {
            position: relative;
            width: 100vw;
            height: 100vh;
            cursor: none;
        }
        canvas {
            display: block;
            z-index: 1;
        }
        #duck-actor {
            position: absolute;
            width: 85px;
            height: 85px;
            pointer-events: none;
            z-index: 10;
            transform: translate(-50%, -50%);
            display: none;
            filter: drop-shadow(0 0 10px rgba(251, 191, 36, 0.5));
            object-fit: contain;
        }
        #ui-layer {
            position: absolute;
            top: 20px;
            left: 20px;
            color: white;
            pointer-events: none;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
            z-index: 20;
        }
        #menu, #settings-panel {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            background: rgba(15, 23, 42, 0.9);
            backdrop-filter: blur(12px);
            padding: 2.5rem;
            border-radius: 2rem;
            border: 2px solid rgba(251, 191, 36, 0.3);
            color: white;
            z-index: 30;
            box-shadow: 0 0 40px rgba(0,0,0,0.5);
        }
        #settings-panel {
            display: none;
            width: 320px;
        }
        .btn {
            background: #fbbf24;
            color: #0f172a;
            padding: 0.8rem 2.5rem;
            border-radius: 99px;
            font-weight: 800;
            cursor: pointer;
            transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            margin-top: 1rem;
            display: inline-block;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        .btn:hover {
            background: #f59e0b;
            transform: scale(1.1);
        }
        #settings-btn {
            position: absolute;
            top: 20px;
            right: 20px;
            z-index: 40;
            background: rgba(255,255,255,0.1);
            padding: 10px;
            border-radius: 50%;
            cursor: pointer;
            pointer-events: auto;
        }
        input[type="range"] {
            accent-color: #fbbf24;
            width: 100%;
        }
    </style>
</head>
<body>

    <div id="game-container">
        <!-- Settings Toggle -->
        <div id="settings-btn" onclick="toggleSettings()">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12.22 2h-.44a2 2 0 0 0-2 2v.18a2 2 0 0 1-1 1.73l-.43.25a2 2 0 0 1-2 0l-.15-.08a2 2 0 0 0-2.73.73l-.22.38a2 2 0 0 0 .73 2.73l.15.1a2 2 0 0 1 1 1.72v.51a2 2 0 0 1-1 1.74l-.15.09a2 2 0 0 0-.73 2.73l.22.38a2 2 0 0 0 2.73.73l.15-.08a2 2 0 0 1 2 0l.43.25a2 2 0 0 1 1 1.73V20a2 2 0 0 0 2 2h.44a2 2 0 0 0 2-2v-.18a2 2 0 0 1 1-1.73l.43-.25a2 2 0 0 1 2 0l.15.08a2 2 0 0 0 2.73-.73l.22-.39a2 2 0 0 0-.73-2.73l-.15-.08a2 2 0 0 1-1-1.74v-.5a2 2 0 0 1 1-1.74l.15-.09a2 2 0 0 0 .73-2.73l-.22-.38a2 2 0 0 0-2.73-.73l-.15.08a2 2 0 0 1-2 0l-.43-.25a2 2 0 0 1-1-1.73V4a2 2 0 0 0-2-2z"></path><circle cx="12" cy="12" r="3"></circle></svg>
        </div>

        <div id="ui-layer">
            <div class="text-3xl font-black italic tracking-tighter">SCORE: <span id="score">0</span></div>
            <div class="text-sm font-medium opacity-70">BEST: <span id="high-score">0</span></div>
        </div>

        <img id="duck-actor" src="https://media.tenor.com/IJASx_rtZLkAAAAi/spinning-duck.gif" alt="Pato">

        <!-- Main Menu -->
        <div id="menu">
            <h1 class="text-5xl font-black mb-2 text-yellow-400">DUCK DASH</h1>
            <p class="text-slate-300 mb-6 max-w-xs mx-auto">¡Recoge el oro y sobrevive al caos!</p>
            <div id="final-score-container" class="hidden mb-6">
                <p class="text-2xl font-bold">PUNTOS: <span id="final-score" class="text-yellow-400">0</span></p>
            </div>
            <div class="btn" onclick="startGame()">EMPEZAR</div>
        </div>

        <!-- Settings Panel -->
        <div id="settings-panel">
            <h2 class="text-2xl font-bold mb-4 text-yellow-400">AJUSTES</h2>
            
            <div class="mb-4 text-left">
                <label class="text-sm block mb-1">Volumen Música</label>
                <input type="range" id="music-vol" min="0" max="1" step="0.1" value="0.5">
            </div>

            <div class="mb-6 text-left">
                <label class="text-sm block mb-1">Volumen Efectos</label>
                <input type="range" id="sfx-vol" min="0" max="1" step="0.1" value="0.7">
                <button onclick="playTestSfx()" class="text-[10px] mt-1 text-yellow-400 hover:underline">PROBAR SONIDO</button>
            </div>

            <div class="mb-6">
                <label class="text-sm block mb-2 font-bold">USAR TU PROPIO GIF</label>
                <input type="file" id="gif-upload" accept="image/gif" class="text-xs text-slate-400 file:mr-4 file:py-2 file:px-4 file:rounded-full file:border-0 file:text-xs file:font-semibold file:bg-yellow-400 file:text-slate-900 hover:file:bg-yellow-500 cursor-pointer w-full">
            </div>

            <div class="btn py-2 px-6 text-sm" onclick="toggleSettings()">CERRAR</div>
        </div>

        <canvas id="gameCanvas"></canvas>
    </div>

    <!-- Audios -->
    <!-- Música de fondo 8-bit -->
    <audio id="bg-music" loop preload="auto">
        <source src="https://pixabay.com/music/download/main-title-8-bit-style-138652.mp3" type="audio/mpeg">
    </audio>
    <!-- Efecto explosión (URL más estable) -->
    <audio id="sfx-explosion" preload="auto">
        <source src="https://cdn.freesound.org/previews/235/235968_3504198-lq.mp3" type="audio/mpeg">
    </audio>

    <script>
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');
        const scoreElement = document.getElementById('score');
        const highScoreElement = document.getElementById('high-score');
        const menu = document.getElementById('menu');
        const settingsPanel = document.getElementById('settings-panel');
        const duckActor = document.getElementById('duck-actor');
        const finalScoreContainer = document.getElementById('final-score-container');
        const finalScoreText = document.getElementById('final-score');
        const bgMusic = document.getElementById('bg-music');
        const sfxExplosion = document.getElementById('sfx-explosion');

        const musicVolInput = document.getElementById('music-vol');
        const sfxVolInput = document.getElementById('sfx-vol');
        const gifUpload = document.getElementById('gif-upload');

        const duckImg = new Image();
        duckImg.src = duckActor.src;
        
        let score = 0;
        let highScore = localStorage.getItem('duckDashHighScore') || 0;
        highScoreElement.innerText = highScore;
        
        let gameActive = false;
        let isDead = false;
        let mouseX = window.innerWidth / 2;
        let mouseY = window.innerHeight / 2;

        let items = [];
        let enemies = [];
        let particles = [];
        let stars = [];
        
        const DUCK_SIZE = 85;
        let spawnTimer = 0;
        let difficultyMultiplier = 1;

        // Handler para GIF personalizado
        gifUpload.addEventListener('change', function(e) {
            const file = e.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(event) {
                    duckActor.src = event.target.result;
                    duckImg.src = event.target.result;
                };
                reader.readAsDataURL(file);
            }
        });

        function playTestSfx() {
            sfxExplosion.volume = sfxVolInput.value;
            sfxExplosion.currentTime = 0;
            sfxExplosion.play().catch(e => console.log("Audio play blocked", e));
        }

        function toggleSettings() {
            const isVisible = settingsPanel.style.display === 'block';
            settingsPanel.style.display = isVisible ? 'none' : 'block';
            if (!gameActive) menu.style.display = isVisible ? 'block' : 'none';
        }

        function initStars() {
            stars = [];
            for(let i = 0; i < 100; i++) {
                stars.push({
                    x: Math.random() * window.innerWidth,
                    y: Math.random() * window.innerHeight,
                    size: Math.random() * 2,
                    speed: Math.random() * 0.5 + 0.1
                });
            }
        }

        function resize() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
            initStars();
        }
        window.addEventListener('resize', resize);
        resize();

        const updateCoords = (x, y) => {
            if (!isDead) {
                mouseX = x;
                mouseY = y;
                duckActor.style.left = mouseX + 'px';
                duckActor.style.top = mouseY + 'px';
            }
        };

        window.addEventListener('mousemove', (e) => updateCoords(e.clientX, e.clientY));
        window.addEventListener('touchmove', (e) => {
            if (e.touches[0]) updateCoords(e.touches[0].clientX, e.touches[0].clientY);
        }, { passive: false });

        class GameObject {
            constructor(x, y, radius, color, speed) {
                this.x = x;
                this.y = y;
                this.radius = radius;
                this.color = color;
                const angle = Math.random() * Math.PI * 2;
                this.vx = Math.cos(angle) * speed;
                this.vy = Math.sin(angle) * speed;
                this.pulse = 0;
            }

            update() {
                this.x += this.vx;
                this.y += this.vy;
                this.pulse += 0.1;
                if (this.x < 0 || this.x > canvas.width) this.vx *= -1;
                if (this.y < 0 || this.y > canvas.height) this.vy *= -1;
            }

            draw() {
                ctx.save();
                ctx.beginPath();
                const currentRadius = this.radius + Math.sin(this.pulse) * 2;
                ctx.arc(this.x, this.y, currentRadius, 0, Math.PI * 2);
                ctx.shadowBlur = 15;
                ctx.shadowColor = this.color;
                ctx.fillStyle = this.color;
                ctx.fill();
                ctx.restore();
            }
        }

        function spawn() {
            if (spawnTimer <= 0) {
                if (items.length < 6) {
                    items.push(new GameObject(
                        Math.random() * canvas.width,
                        Math.random() * canvas.height,
                        8, '#fbbf24', 1.5 * difficultyMultiplier
                    ));
                }
                if (enemies.length < 4 + (difficultyMultiplier * 2)) {
                    const side = Math.floor(Math.random() * 4);
                    let x, y;
                    if(side === 0) { x = 0; y = Math.random() * canvas.height; }
                    else if(side === 1) { x = canvas.width; y = Math.random() * canvas.height; }
                    else if(side === 2) { x = Math.random() * canvas.width; y = 0; }
                    else { x = Math.random() * canvas.width; y = canvas.height; }
                    enemies.push(new GameObject(x, y, 14, '#ff4757', (2 + Math.random() * 2) * difficultyMultiplier));
                }
                spawnTimer = Math.max(20, 80 - (difficultyMultiplier * 5));
            }
            spawnTimer--;
        }

        function createTexturedExplosion(x, y, count = 40) {
            for (let i = 0; i < count; i++) {
                const sx = Math.random() * (duckImg.width - 20);
                const sy = Math.random() * (duckImg.height - 20);
                particles.push({
                    x, y,
                    vx: (Math.random() - 0.5) * 22,
                    vy: (Math.random() - 0.5) * 22,
                    rotation: Math.random() * Math.PI * 2,
                    rotationSpeed: (Math.random() - 0.5) * 0.4,
                    life: 1.0,
                    size: Math.random() * 25 + 10,
                    sx, sy,
                    sw: 24, sh: 24
                });
            }
        }

        function createSimpleExplosion(x, y, color, count = 10) {
            for (let i = 0; i < count; i++) {
                particles.push({
                    x, y,
                    vx: (Math.random() - 0.5) * 10,
                    vy: (Math.random() - 0.5) * 10,
                    life: 1.0,
                    size: Math.random() * 5 + 2,
                    color
                });
            }
        }

        function startGame() {
            // Asegurar que el audio esté listo tras el clic del usuario
            bgMusic.currentTime = 0;
            bgMusic.volume = musicVolInput.value;
            bgMusic.play().catch(() => {});

            score = 0;
            difficultyMultiplier = 1;
            items = [];
            enemies = [];
            particles = [];
            isDead = false;
            scoreElement.innerText = score;
            gameActive = true;
            menu.style.display = 'none';
            settingsPanel.style.display = 'none';
            duckActor.style.display = 'block';
            animate();
        }

        function gameOver() {
            if (isDead) return;
            isDead = true;
            duckActor.style.display = 'none';
            
            // SFX Explosion mejorado
            sfxExplosion.volume = sfxVolInput.value;
            sfxExplosion.currentTime = 0;
            sfxExplosion.play().catch(e => console.error("Error SFX:", e));

            createTexturedExplosion(mouseX, mouseY);
            
            let fadeOut = setInterval(() => {
                if(bgMusic.volume > 0.05) {
                    bgMusic.volume -= 0.05;
                } else {
                    bgMusic.pause();
                    clearInterval(fadeOut);
                }
            }, 100);

            setTimeout(() => {
                gameActive = false;
                menu.style.display = 'block';
                finalScoreContainer.classList.remove('hidden');
                finalScoreText.innerText = score;
                if (score > highScore) {
                    highScore = score;
                    localStorage.setItem('duckDashHighScore', highScore);
                    highScoreElement.innerText = highScore;
                }
            }, 1500);
        }

        function drawBackground() {
            const grad = ctx.createRadialGradient(canvas.width/2, canvas.height/2, 0, canvas.width/2, canvas.height/2, canvas.width);
            grad.addColorStop(0, '#1e293b');
            grad.addColorStop(1, '#0f172a');
            ctx.fillStyle = grad;
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            ctx.fillStyle = "white";
            stars.forEach(star => {
                star.y += star.speed;
                if(star.y > canvas.height) star.y = 0;
                ctx.globalAlpha = 0.5;
                ctx.beginPath();
                ctx.arc(star.x, star.y, star.size, 0, Math.PI * 2);
                ctx.fill();
            });
            ctx.globalAlpha = 1;
        }

        function animate() {
            if (!gameActive && particles.length === 0) return;

            drawBackground();

            for (let i = particles.length - 1; i >= 0; i--) {
                const p = particles[i];
                p.x += p.vx;
                p.y += p.vy;
                p.life -= 0.015;
                if (p.life <= 0) {
                    particles.splice(i, 1);
                    continue;
                }
                ctx.save();
                ctx.globalAlpha = p.life;
                if (p.sx !== undefined) {
                    ctx.translate(p.x, p.y);
                    ctx.rotate(p.rotation += p.rotationSpeed);
                    ctx.drawImage(duckImg, p.sx, p.sy, p.sw, p.sh, -p.size/2, -p.size/2, p.size, p.size);
                } else {
                    ctx.fillStyle = p.color;
                    ctx.beginPath();
                    ctx.arc(p.x, p.y, p.size * p.life, 0, Math.PI * 2);
                    ctx.fill();
                }
                ctx.restore();
            }

            if (!isDead) {
                for (let i = items.length - 1; i >= 0; i--) {
                    items[i].update();
                    items[i].draw();
                    const dist = Math.hypot(items[i].x - mouseX, items[i].y - mouseY);
                    if (dist < DUCK_SIZE/2.2) {
                        createSimpleExplosion(items[i].x, items[i].y, '#fbbf24', 5);
                        items.splice(i, 1);
                        score += 10;
                        scoreElement.innerText = score;
                        difficultyMultiplier += 0.03;
                    }
                }

                for (let i = enemies.length - 1; i >= 0; i--) {
                    enemies[i].update();
                    enemies[i].draw();
                    const dist = Math.hypot(enemies[i].x - mouseX, enemies[i].y - mouseY);
                    if (dist < DUCK_SIZE/3 + enemies[i].radius) {
                        gameOver();
                    }
                }
                spawn();
            }

            requestAnimationFrame(animate);
        }

        // Sincronizar volumen música en tiempo real
        musicVolInput.addEventListener('input', () => {
            if (gameActive) bgMusic.volume = musicVolInput.value;
        });

        initStars();
    </script>
</body>
</html>
