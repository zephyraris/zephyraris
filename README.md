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
      <div style="color: #00ff00; font-size: 18px; margin-bottom: 10px;">🐍 Jogo da Cobra Interativo</div>
      
      <!-- Snake Game usando HTML/CSS puro -->
      <div style="width: 300px; height: 300px; border: 2px solid #00ff00; background: #000; border-radius: 10px; position: relative; overflow: hidden;">
        
        <!-- Cobra animada com movimento em loop -->
        <div style="position: absolute; width: 18px; height: 18px; background: linear-gradient(45deg, #00ff00, #00cc00); border-radius: 3px; top: 40px; left: 40px; animation: snakeMove 4s infinite linear; box-shadow: 0 0 8px rgba(0,255,0,0.6);"></div>
        <div style="position: absolute; width: 18px; height: 18px; background: linear-gradient(45deg, #00cc00, #00aa00); border-radius: 3px; top: 40px; left: 20px; animation: snakeMove 4s infinite linear 0.3s; box-shadow: 0 0 6px rgba(0,204,0,0.5);"></div>
        <div style="position: absolute; width: 18px; height: 18px; background: linear-gradient(45deg, #00aa00, #008800); border-radius: 3px; top: 40px; left: 0px; animation: snakeMove 4s infinite linear 0.6s; box-shadow: 0 0 4px rgba(0,170,0,0.4);"></div>
        
        <!-- Comida animada com efeitos -->
        <div style="position: absolute; width: 16px; height: 16px; background: radial-gradient(circle, #ff0000, #cc0000); border-radius: 50%; top: 80px; left: 180px; animation: foodPulse 1.5s infinite alternate; box-shadow: 0 0 12px rgba(255,0,0,0.8);"></div>
        <div style="position: absolute; width: 16px; height: 16px; background: radial-gradient(circle, #ff0000, #cc0000); border-radius: 50%; top: 180px; left: 120px; animation: foodPulse 1.5s infinite alternate 0.7s; box-shadow: 0 0 12px rgba(255,0,0,0.8);"></div>
        <div style="position: absolute; width: 16px; height: 16px; background: radial-gradient(circle, #ff0000, #cc0000); border-radius: 50%; top: 120px; left: 240px; animation: foodPulse 1.5s infinite alternate 1.4s; box-shadow: 0 0 12px rgba(255,0,0,0.8);"></div>
        
        <!-- Grid pattern sutil -->
        <div style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; background-image: 
          linear-gradient(to right, rgba(0,255,0,0.1) 1px, transparent 1px),
          linear-gradient(to bottom, rgba(0,255,0,0.1) 1px, transparent 1px);
          background-size: 20px 20px;"></div>
        
        <!-- Pontuação com efeito neon -->
        <div style="position: absolute; top: 8px; left: 8px; color: #00ff00; font-size: 14px; font-weight: bold; animation: scoreBlink 3s infinite; text-shadow: 0 0 5px #00ff00;">
          🐍 Score: 150
        </div>
        
        <!-- Efeito de partículas -->
        <div style="position: absolute; top: 60px; left: 100px; width: 4px; height: 4px; background: #00ff00; border-radius: 50%; animation: particleFloat 2s infinite linear;"></div>
        <div style="position: absolute; top: 140px; left: 80px; width: 3px; height: 3px; background: #00ff00; border-radius: 50%; animation: particleFloat 2s infinite linear 0.5s;"></div>
        <div style="position: absolute; top: 220px; left: 160px; width: 4px; height: 4px; background: #00ff00; border-radius: 50%; animation: particleFloat 2s infinite linear 1s;"></div>
        
        <!-- Game Over overlay com timing -->
        <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); 
             background: rgba(0,0,0,0.95); color: #ff0000; padding: 15px; border-radius: 8px; 
             text-align: center; font-weight: bold; animation: gameOverFlash 8s infinite; border: 1px solid #ff0000;">
          <div style="font-size: 16px;">💀 GAME OVER!</div>
          <div style="font-size: 10px; color: #ccc; margin-top: 3px;">🎮 Demonstração do Jogo</div>
        </div>
      </div>
      
      <div style="color: #ccc; font-size: 12px; margin-top: 10px;">
        🎮 Demonstração do Jogo da Cobra | Animações CSS
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
  /* Animações do Jogo da Cobra */
  @keyframes snakeMove {
    0% { transform: translateX(0) translateY(0); }
    25% { transform: translateX(200px) translateY(0); }
    50% { transform: translateX(200px) translateY(200px); }
    75% { transform: translateX(0) translateY(200px); }
    100% { transform: translateX(0) translateY(0); }
  }
  
  @keyframes foodPulse {
    0% { transform: scale(1); opacity: 1; }
    100% { transform: scale(1.2); opacity: 0.7; }
  }
  
  @keyframes scoreBlink {
    0%, 50% { opacity: 1; }
    51%, 100% { opacity: 0.5; }
  }
  
  @keyframes gameOverFlash {
    0%, 80% { opacity: 0; }
    85%, 95% { opacity: 1; }
    100% { opacity: 0; }
  }
  
  @keyframes particleFloat {
    0% { transform: translateY(0) translateX(0); opacity: 1; }
    50% { transform: translateY(-20px) translateX(10px); opacity: 0.7; }
    100% { transform: translateY(0) translateX(20px); opacity: 0; }
  }
  
  /* Efeitos visuais adicionais */
  .snake-segment {
    box-shadow: 0 0 10px rgba(0, 255, 0, 0.5);
  }
  
  .food-item {
    box-shadow: 0 0 15px rgba(255, 0, 0, 0.8);
  }
</style>

<!-- Jogo da Cobra para GitHub - Versão HTML/CSS pura -->
