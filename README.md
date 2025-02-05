<div style="background-color:black; color:#00FF00; font-family:monospace; padding:20px; border-radius:5px;">
  <h1>Hi there! 👋 I'm Anila Younas.</h1>
  <p>🚀 <strong>Passionate Computer Scientist | C++ Developer | Assembly Programmer | Web Enthusiast | CyberSecurity Learner</strong></p>
  
  <p>I am a second-year CS student specializing in C++ programming and assembly language projects. I enjoy working on data structures, algorithms, and assembly programming, along with web development.</p>

  <pre id="typewriter"></pre>

  <script>
    let text = `
🔥 My Projects
🎮 Console & Game Development (C++)
♟ Chess Game (C++ CLI) – A console-based chess game with move validation and standard rules.
🎲 Snakes and Ladders (C++ CLI) – A two-player turn-based game with automated dice rolling.
🎮 Tic-Tac-Toe (C++ CLI) – A classic two-player game with an interactive console interface.
🏗 Tower of Hanoi (C++ CLI) – Stack-based Tower of Hanoi game with an interactive console UI.
🏢 Cruise Management System (C++ CLI) – A management system for handling cruise bookings and schedules.

🖥 Assembly Language & System-Level Programming
🕹 Pac-Man (Assembly Language) – A fully functional Pac-Man clone built using low-level assembly programming.

📱 Software & Web Applications
📘 Leximo – English Learning App – An interactive English learning application for vocabulary improvement.
🚗 Mercedes Webpage (HTML & CSS) – A simple and elegant Mercedes-Benz showcase website.

📜 Experience & Achievements
🌟 Millennium Fellowship – Worked on a social impact project addressing abuse in society.
👨‍🏫 Git Workshop Organizer – Conducted hands-on Git training sessions.
💡 IBA OGDC Talent Hunt Program – Selected for a prestigious talent development initiative.

📫 Connect with Me
GitHub: https://github.com/Anila-Younas
Email: anilayounas41@gmail.com
LinkedIn: https://www.linkedin.com/in/anila-younas-0483ab290/
🔹 Always learning, always improving. 🚀
💡 Open to collaborations and new challenges.
    `;

    let index = 0;
    function typeEffect() {
      if (index < text.length) {
        document.getElementById("typewriter").innerHTML += text[index];
        index++;
        setTimeout(typeEffect, Math.random() * 100); 
      }
    }

    document.addEventListener("DOMContentLoaded", typeEffect);
  </script>
</div>
