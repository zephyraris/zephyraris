<div align="center">

  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:000000,100:3a3a3a&height=160&section=header&text=Zephyraris&fontSize=50&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Full%20Stack%20Developer%20%7C%20LofyGang&descSize=20&descAlignY=55"/>

  <img src="https://readme-typing-svg.herokuapp.com/?color=9f9f9f&size=24&center=true&vCenter=true&width=1000&lines=Welcome+to+my+Profile!;Building+the+future+with+code.;Always+learning+and+creating." />

  <h2 align="center">👤 About Me</h2>
  <p align="center">
    Passionate about <b>technology</b> and <b>cybersecurity</b>.<br>
    Focused on creating efficient and scalable systems.<br>
    Always exploring new tools and improving my workflow.
  </p>

  <h2 align="center">💻 Tech Stack</h2>
  <p align="center">
    <img src="https://skillicons.dev/icons?i=ts,python,nodejs,html,css,js,react&theme=dark" />
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/lua/lua-original.svg" width="48" height="48" title="Luau" />
  </p>

  <h2 align="center">📊 GitHub Analytics</h2>
  <div align="center">
    <img height="170em" src="https://github-readme-stats.vercel.app/api?username=zephyraris&show_icons=true&theme=graywhite&hide_border=true&bg_color=00000000&text_color=ffffff&title_color=cccccc&icon_color=999999" />
    <img height="170em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=zephyraris&layout=compact&theme=graywhite&hide_border=true&bg_color=00000000&text_color=ffffff&title_color=cccccc" />
  </div>

  <h2 align="center">📈 Activity Graph</h2>
  <img width="90%" src="https://github-readme-activity-graph.vercel.app/graph?username=zephyraris&bg_color=0d0d0d&color=9f9f9f&line=ffffff&point=cccccc&area=true&hide_border=true&custom_title=GitHub%20Contribution%20Graph"/>

  <h2 align="center">🎮 Snake Game</h2>
  <div align="center" style="margin: 20px 0;">
    <div style="background: rgba(0,0,0,0.8); padding: 20px; border-radius: 15px; border: 2px solid #333; display: inline-block;">
      <div style="color: #00ff00; font-size: 18px; margin-bottom: 10px;">Pontuação: <span id="snakeScore">0</span></div>
      <canvas id="snakeCanvas" width="300" height="300" style="border: 2px solid #00ff00; background: #000; border-radius: 10px;"></canvas>
      <div style="color: #ccc; font-size: 12px; margin-top: 10px;">
      </div>
    </div>
  </div>

  <h2 align="center">🌐 Contact</h2>
  <p align="center">
    <a href="mailto:zephyraris@gmail.com" target="_blank">
      <img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white">
    </a>
    <a href="https://instagram.com/zephyraris" target="_blank">
      <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white">
    </a>
    <a href="https://discord.gg/lofygang" target="_blank">
      <img src="https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white">
    </a>
    <a href="https://t.me/lofygang" target="_blank">
      <img src="https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white">
    </a>
  </p>

</div>

<style>
  #snakeCanvas {
    cursor: pointer;
  }
  
  .game-over-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,0.9);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
  }
  
  .game-over-content {
    background: #1a1a1a;
    padding: 30px;
    border-radius: 15px;
    border: 2px solid #ff0000;
    text-align: center;
    color: white;
  }
  
  .restart-btn {
    background: #00ff00;
    color: #000;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
    margin-top: 15px;
  }
  
  .restart-btn:hover {
    background: #00cc00;
  }
</style>

<script>
  const canvas = document.getElementById('snakeCanvas');
  const ctx = canvas.getContext('2d');
  const scoreElement = document.getElementById('snakeScore');

  const gridSize = 15;
  const tileCount = canvas.width / gridSize;

  let snake = [{x: 10, y: 10}];
  let food = {};
  let dx = 0;
  let dy = 0;
  let score = 0;
  let gameRunning = true;
  let gamePaused = false;

  function generateFood() {
    food = {
      x: Math.floor(Math.random() * tileCount),
      y: Math.floor(Math.random() * tileCount)
    };
    
    for (let segment of snake) {
      if (segment.x === food.x && segment.y === food.y) {
        generateFood();
        return;
      }
    }
  }

  function drawGame() {
    ctx.fillStyle = '#000';
    ctx.fillRect(0, 0, canvas.width, canvas.height);

    ctx.strokeStyle = '#333';
    ctx.lineWidth = 0.5;
    for (let i = 0; i <= tileCount; i++) {
      ctx.beginPath();
      ctx.moveTo(i * gridSize, 0);
      ctx.lineTo(i * gridSize, canvas.height);
      ctx.moveTo(0, i * gridSize);
      ctx.lineTo(canvas.width, i * gridSize);
      ctx.stroke();
    }

    ctx.fillStyle = '#00ff00';
    for (let segment of snake) {
      ctx.fillRect(segment.x * gridSize + 1, segment.y * gridSize + 1, gridSize - 2, gridSize - 2);
    }

    if (snake.length > 0) {
      ctx.fillStyle = '#00cc00';
      ctx.fillRect(snake[0].x * gridSize + 2, snake[0].y * gridSize + 2, gridSize - 4, gridSize - 4);
    }

    ctx.fillStyle = '#ff0000';
    ctx.fillRect(food.x * gridSize + 2, food.y * gridSize + 2, gridSize - 4, gridSize - 4);
  }

  function moveSnake() {
    if (!gameRunning || gamePaused) return;

    const head = {x: snake[0].x + dx, y: snake[0].y + dy};

    if (head.x < 0 || head.x >= tileCount || head.y < 0 || head.y >= tileCount) {
      gameOver();
      return;
    }

    for (let segment of snake) {
      if (head.x === segment.x && head.y === segment.y) {
        gameOver();
        return;
      }
    }

    snake.unshift(head);

    if (head.x === food.x && head.y === food.y) {
      score += 10;
      scoreElement.textContent = score;
      generateFood();
    } else {
      snake.pop();
    }
  }

  function gameOver() {
    gameRunning = false;
    showGameOver();
  }

  function showGameOver() {
    const overlay = document.createElement('div');
    overlay.className = 'game-over-overlay';
    overlay.innerHTML = `
      <div class="game-over-content">
        <h2 style="color: #ff0000; margin-bottom: 15px;">Game Over!</h2>
        <p>Sua pontuação: <span style="color: #00ff00; font-size: 18px;">${score}</span></p>
        <button class="restart-btn" onclick="restartSnakeGame()">Jogar Novamente</button>
      </div>
    `;
    document.body.appendChild(overlay);
  }

  function restartSnakeGame() {
    document.querySelector('.game-over-overlay')?.remove();
    snake = [{x: 10, y: 10}];
    dx = 0;
    dy = 0;
    score = 0;
    gameRunning = true;
    gamePaused = false;
    scoreElement.textContent = score;
    generateFood();
  }

  document.addEventListener('keydown', (e) => {
    if (!gameRunning) return;

    switch(e.key) {
      case 'ArrowUp':
        if (dy !== 1) { dx = 0; dy = -1; }
        break;
      case 'ArrowDown':
        if (dy !== -1) { dx = 0; dy = 1; }
        break;
      case 'ArrowLeft':
        if (dx !== 1) { dx = -1; dy = 0; }
        break;
      case 'ArrowRight':
        if (dx !== -1) { dx = 1; dy = 0; }
        break;
      case ' ':
        e.preventDefault();
        gamePaused = !gamePaused;
        break;
    }
  });

  function gameLoop() {
    moveSnake();
    drawGame();
    if (gameRunning) {
      setTimeout(gameLoop, 150);
    }
  }

  generateFood();
  drawGame();
  gameLoop();
</script>
