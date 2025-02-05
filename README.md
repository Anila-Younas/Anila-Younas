import curses
import time
import random

def typing_effect(stdscr, text, delay=0.05):
    curses.start_color()
    curses.init_pair(1, curses.COLOR_GREEN, curses.COLOR_BLACK)
    stdscr.clear()
    stdscr.attron(curses.color_pair(1))
    
    y, x = 2, 2  # Start position
    stdscr.addstr(y, x, "$")  # Initial prompt
    x += 2
    
    for char in text:
        stdscr.addstr(y, x, char)
        stdscr.refresh()
        x += 1
        time.sleep(delay + random.uniform(0, 0.05))  # Randomized delay for effect
    
    stdscr.attroff(curses.color_pair(1))
    stdscr.addstr(y+2, 2, "Press any key to exit...")
    stdscr.refresh()
    stdscr.getch()

if __name__ == "__main__":
    readme_text = """
    Hi there! 👋 I'm Anila Younas.
    
    🚀 Passionate Computer Scientist | C++ Developer | Assembly Programmer | Web Enthusiast | CyberSecurity Learner
    
    I am a second-year CS student specializing in C++ programming and assembly language projects. I enjoy working on data structures, algorithms, and assembly programming, along with web development. I also explore machine learning, cybersecurity, and computer vision.
    
    🔥 My Projects
    - ⚖ Chess Game (C++ CLI) – Console-based chess game with move validation and standard rules.
    - 🎮 Tic-Tac-Toe (C++ CLI) – Classic two-player game with an interactive console UI.
    - 🛠 Assembly: Pac-Man – A Pac-Man clone built using assembly language.
    - 🛠 Cruise Management System – Manages cruise bookings and schedules.
    
    🛠 Tech Stack
    - C++, Assembly, JavaScript, Python
    - VS Code, Git, GCC, PyCharm
    - Web Development, Ethical Hacking
    
    💌 Connect with Me:
    GitHub: github.com/Anila-Younas
    LinkedIn: linkedin.com/in/anila-younas-0483ab290/
    Email: anilayounas41@gmail.com
    
    """
    curses.wrapper(typing_effect, readme_text)
