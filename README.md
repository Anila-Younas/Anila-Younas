<!DOCTYPE html>
<html>
<head>
    <style>
        body {
            background-color: black;
            color: #00FF00;
            font-family: 'Courier New', monospace;
            line-height: 1.6;
            white-space: pre-wrap;
        }
        .cursor {
            animation: blink 0.7s infinite;
        }
        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }
    </style>
</head>
<body>
<div id="content"></div>
<span class="cursor">|</span>

<script>
    const sections = [
        '# Hi there! 👋 I\'m Anila Younas\n\n',
        '🚀 **Passionate Computer Scientist | C++ Developer | Assembly Programmer | Web Enthusiast | CyberSecurity Learner**\n\n',
        'I am a second-year CS student specializing in C++ programming and assembly language projects. I enjoy working on data structures, algorithms, and assembly programming, along with web development. I also explore **machine learning, cybersecurity, and computer vision**.\n\n',
        '## 🔥 My Projects\n\n',
        '### 🎮 Console & Game Development (C++)\n',
        '♟ Chess Game (C++ CLI) – A console-based chess game with move validation and standard rules.\n',
        '🎲 Snakes and Ladders (C++ CLI) – A two-player turn-based game with automated dice rolling.\n',
        '🎮 Tic-Tac-Toe (C++ CLI) – A classic two-player game with an interactive console interface.\n',
        '🏗 Tower of Hanoi (C++ CLI) – Stack-based Tower of Hanoi game with an interactive console UI.\n',
        '🏢 Cruise Management System (C++ CLI) – A management system for handling cruise bookings and schedules.\n\n',
        '### 🖥 Assembly Language & System-Level Programming\n',
        '🕹 Pac-Man (Assembly Language) – A fully functional Pac-Man clone built using low-level assembly programming.\n\n',
        '### 📱 Software & Web Applications\n',
        '📘 Leximo – English Learning App – An interactive English learning application for vocabulary improvement.\n',
        '🚗 Mercedes Webpage (HTML & CSS) – A simple and elegant Mercedes-Benz showcase website.\n\n',
        '## 🛠 Tech Stack\n\n',
        'Programming Languages:\n',
        'C++\n',
        'Assembly Language\n',
        'JavaScript\n',
        'HTML\n',
        'CSS\n',
        'Java\n',
        'Kotlin\n',
        'Python\n\n',
        'Tools & Technologies:\n',
        'VS Code\n',
        'CodeBlocks\n',
        'Visual Studio\n',
        'Intellij IDEA\n',
        'PyCharm\n',
        'GCC\n',
        'Git\n',
        'GitHub\n\n',
        'Expertise Areas:\n',
        'Game Development (Pac-Man, Chess, Snakes & Ladders)\n',
        'Assembly Programming\n',
        'Data Structures & Algorithms\n',
        'Web Development\n',
        'Cybersecurity & Ethical Hacking\n\n',
        '## 📜 Experience & Achievements\n',
        '🌟 Millennium Fellowship – Worked on a social impact project addressing abuse in society.\n',
        '👨‍🏫 Git Workshop Organizer – Conducted hands-on Git training sessions.\n',
        '💡 IBA OGDC Talent Hunt Program – Selected for a prestigious talent development initiative.\n\n',
        '## 📫 Connect with Me\n',
        'GitHub: https://github.com/Anila-Younas\n',
        'Email: anilayounas41@gmail.com\n',
        'LinkedIn: https://www.linkedin.com/in/anila-younas-0483ab290/\n\n',
        '🔹 Always learning, always improving. 🚀\n',
        '💡 Open to collaborations and new challenges.\n'
    ];

    const contentDiv = document.getElementById('content');
    const cursor = document.querySelector('.cursor');
    let sectionIndex = 0;
    let charIndex = 0;
    let displayedSections = [];

    function typeWriter() {
        if (sectionIndex < sections.length) {
            const currentSection = sections[sectionIndex];
            
            if (charIndex < currentSection.length) {
                const newContent = displayedSections.join('') + currentSection.slice(0, charIndex + 1);
                contentDiv.innerHTML = newContent;
                charIndex++;
            } else {
                displayedSections.push(currentSection);
                sectionIndex++;
                charIndex = 0;
            }
            
            setTimeout(typeWriter, Math.random() * 20 + 10);
        } else {
            cursor.style.display = 'none';
        }
    }

    typeWriter();
</script>
</body>
</html>
