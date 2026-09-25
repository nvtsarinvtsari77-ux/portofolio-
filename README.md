<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Portofolio Dwi Novita Sari</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        :root {
            --bg: #f1f8f4;
            --card: #ffffff;
            --text: #24352b;
            --green: #78a98b;
            --dark-green: #4f8064;
            --light-green: #dceee2;
            --shadow: 0 8px 25px rgba(0,0,0,0.08);
        }

        body.dark {
            --bg: #17231c;
            --card: #223229;
            --text: #f1f8f4;
            --green: #91c5a3;
            --dark-green: #b2ddbf;
            --light-green: #30483a;
            --shadow: 0 8px 25px rgba(0,0,0,0.3);
        }

        body {
            font-family: Arial, sans-serif;
            background: var(--bg);
            color: var(--text);
            line-height: 1.6;
            transition: 0.3s;
        }

        /* NAVBAR */
        header {
            background: var(--card);
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav {
            max-width: 1100px;
            margin: auto;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 22px;
            font-weight: bold;
            color: var(--dark-green);
        }

        .nav-links {
            display: flex;
            gap: 25px;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text);
            font-weight: bold;
        }

        .nav-links a:hover {
            color: var(--green);
        }

        .menu-button {
            display: none;
            border: none;
            background: none;
            font-size: 28px;
            cursor: pointer;
            color: var(--text);
        }

        .theme-button {
            border: none;
            background: var(--light-green);
            padding: 8px 12px;
            border-radius: 20px;
            cursor: pointer;
            font-size: 16px;
        }

        /* HERO */
        .hero {
            min-height: 90vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 40px 20px;
        }

        .hero-content {
            max-width: 800px;
        }

        .profile-photo {
            width: 150px;
            height: 150px;
            object-fit: cover;
            border-radius: 50%;
            border: 5px solid var(--light-green);
            margin-bottom: 20px;
        }

        .hero h1 {
            font-size: 45px;
            margin-bottom: 10px;
        }

        .hero h1 span {
            color: var(--dark-green);
        }

        .hero p {
            font-size: 18px;
            margin-bottom: 25px;
        }

        .button {
            display: inline-block;
            padding: 12px 22px;
            background: var(--green);
            color: white;
            text-decoration: none;
            border-radius: 25px;
            border: none;
            cursor: pointer;
            font-weight: bold;
            margin: 5px;
        }

        .button:hover {
            background: var(--dark-green);
        }

        /* SECTION */
        section {
            max-width: 1100px;
            margin: auto;
            padding: 80px 20px;
        }

        .section-title {
            text-align: center;
            font-size: 32px;
            margin-bottom: 40px;
            color: var(--dark-green);
        }

        /* ABOUT */
        .about-box {
            background: var(--card);
            padding: 30px;
            border-radius: 20px;
            box-shadow: var(--shadow);
        }

        .about-box p {
            margin-bottom: 15px;
        }

        .education {
            margin-top: 25px;
        }

        .education li {
            margin: 10px 0;
            margin-left: 20px;
        }

        /* SKILLS */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .skill {
            background: var(--card);
            padding: 20px;
            border-radius: 15px;
            box-shadow: var(--shadow);
        }

        .skill-title {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-weight: bold;
        }

        .skill-bar {
            width: 100%;
            height: 10px;
            background: var(--light-green);
            border-radius: 10px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: var(--green);
            border-radius: 10px;
        }

        /* PROJECT */
        .projects {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .project-card {
            background: var(--card);
            border-radius: 20px;
            padding: 25px;
            box-shadow: var(--shadow);
            text-align: center;
            transition: 0.3s;
        }

        .project-card:hover {
            transform: translateY(-8px);
        }

        .project-icon {
            font-size: 50px;
            margin-bottom: 15px;
        }

        .project-card h3 {
            margin-bottom: 10px;
            color: var(--dark-green);
        }

        .project-card p {
            margin-bottom: 15px;
        }

        /* DEMO */
        .demo-box {
            margin-top: 50px;
            background: var(--card);
            padding: 30px;
            border-radius: 20px;
            box-shadow: var(--shadow);
        }

        .demo-box h3 {
            color: var(--dark-green);
            margin-bottom: 20px;
        }

        .calculator {
            max-width: 300px;
            margin: auto;
        }

        #calc-display {
            width: 100%;
            padding: 15px;
            font-size: 25px;
            text-align: right;
            margin-bottom: 10px;
            border: 2px solid var(--light-green);
            border-radius: 10px;
            background: var(--bg);
            color: var(--text);
        }

        .calc-buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 8px;
        }

        .calc-buttons button {
            padding: 15px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            background: var(--light-green);
            color: var(--text);
            font-size: 18px;
        }

        .calc-buttons button:hover {
            background: var(--green);
            color: white;
        }

        /* DAILY LIST */
        .todo-box {
            max-width: 500px;
            margin: auto;
        }

        .todo-input {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }

        .todo-input input {
            flex: 1;
            padding: 12px;
            border: 2px solid var(--light-green);
            border-radius: 10px;
            background: var(--bg);
            color: var(--text);
        }

        #todo-list {
            list-style: none;
        }

        #todo-list li {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: var(--light-green);
            padding: 12px;
            margin-bottom: 8px;
            border-radius: 10px;
        }

        #todo-list button {
            border: none;
            background: #d97878;
            color: white;
            padding: 5px 10px;
            border-radius: 8px;
            cursor: pointer;
        }

        /* CONTACT */
        .contact-box {
            text-align: center;
            background: var(--card);
            padding: 35px;
            border-radius: 20px;
            box-shadow: var(--shadow);
        }

        .contact-box p {
            margin: 10px;
        }

        .contact-box a {
            color: var(--dark-green);
            font-weight: bold;
            text-decoration: none;
        }

        /* FOOTER */
        footer {
            text-align: center;
            background: var(--card);
            padding: 25px;
            margin-top: 30px;
            box-shadow: var(--shadow);
        }

        /* TOP BUTTON */
        #top-button {
            position: fixed;
            right: 20px;
            bottom: 20px;
            width: 45px;
            height: 45px;
            border: none;
            border-radius: 50%;
            background: var(--green);
            color: white;
            font-size: 20px;
            cursor: pointer;
            display: none;
        }

        /* MOBILE */
        @media (max-width: 600px) {

            .nav-links {
                display: none;
                position: absolute;
                top: 65px;
                left: 0;
                width: 100%;
                background: var(--card);
                flex-direction: column;
                text-align: center;
                padding: 20px;
                box-shadow: var(--shadow);
            }

            .nav-links.active {
                display: flex;
            }

            .menu-button {
                display: block;
            }

            nav {
                position: relative;
            }

            .hero h1 {
                font-size: 32px;
            }

            .hero p {
                font-size: 16px;
            }

            .skills-container {
                grid-template-columns: 1fr;
            }

            .projects {
                grid-template-columns: 1fr;
            }

            section {
                padding: 60px 15px;
            }
        }
    </style>
</head>

<body>

    <!-- NAVBAR -->
    <header>
        <nav>
            <div class="logo">Dwi Novita Sari</div>

            <button class="menu-button" onclick="toggleMenu()">
                ☰
            </button>

            <ul class="nav-links" id="navLinks">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">Tentang</a></li>
                <li><a href="#skills">My Skills</a></li>
                <li><a href="#projects">Proyek</a></li>
                <li><a href="#contact">Kontak</a></li>
            </ul>

            <button class="theme-button" onclick="toggleTheme()">
                🌙
            </button>
        </nav>
    </header>

    <!-- HOME -->
    <main>
        <section class="hero" id="home">
            <div class="hero-content">

                <!-- Ganti foto.jpg dengan nama foto kamu -->
                <img src="https://uploads.onecompiler.io/45447qjvv/1790331070505/WhatsApp%20Image%202026-09-25%20at%2003.08.58.jpeg"
                     alt="Foto Dwi Novita Sari"
                     class="profile-photo">

                <h1>Halo, Saya <span>Dwi Novita Sari</span></h1>

                <p>
                    Pelajar PPLG yang tertarik dengan Web Development
                    dan UI/UX Design.
                </p>

                <a href="#projects" class="button">
                    Lihat Proyek
                </a>

                <a href="#contact" class="button">
                    Hubungi Saya
                </a>

            </div>
        </section>

        <!-- TENTANG -->
        <section id="about">

            <h2 class="section-title">Tentang Saya</h2>

            <div class="about-box">

                <p>
                    Halo! Saya <b>Dwi Novita Sari</b>, siswa kelas
                    <b>X RPL 3</b> di SMK Krian 1 Sidoarjo.
                    Saya sedang belajar membuat website menggunakan
                    HTML, CSS, dan JavaScript.
                </p>

                <p>
                    Saya juga tertarik dengan desain UI/UX dan ingin
                    mengembangkan kemampuan saya dalam membuat website
                    yang sederhana, menarik.
                </p>

                <div class="education">

                    <h3>🎓 Pendidikan</h3>

                    <ul>
                        <li>UPT SDN 153 GRESIK</li>
                        <li>UPT SMPN 12 GRESIK</li>
                        <li>SMK KRIAN 1 SIDOARJO - X RPL 3</li>
                    </ul>

                </div>
            </div>
        </section>

        <!-- SKILLS -->
        <section id="skills">

            <h2 class="section-title">My Skills</h2>

            <div class="skills-container">

                <div class="skill">
                    <div class="skill-title">
                        <span>HTML</span>
                        <span>85%</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width:85%"></div>
                    </div>
                </div>

                <div class="skill">
                    <div class="skill-title">
                        <span>CSS</span>
                        <span>80%</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width:80%"></div>
                    </div>
                </div>

                <div class="skill">
                    <div class="skill-title">
                        <span>JavaScript</span>
                        <span>65%</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width:65%"></div>
                    </div>
                </div>

                <div class="skill">
                    <div class="skill-title">
                        <span>UI/UX Design</span>
                        <span>75%</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width:75%"></div>
                    </div>
                </div>

                <div class="skill">
                    <div class="skill-title">
                        <span>Responsive Design</span>
                        <span>80%</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width:80%"></div>
                    </div>
                </div>

                <div class="skill">
                    <div class="skill-title">
                        <span>Problem Solving</span>
                        <span>70%</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width:70%"></div>
                    </div>
                </div>

            </div>
        </section>

        <!-- PROYEK -->
        <section id="projects">

            <h2 class="section-title">Proyek Saya</h2>

            <div class="projects">

                <article class="project-card">

                    <div class="project-icon">🧮</div>

                    <h3>Mini Kalkulator</h3>

                    <p>
                        Kalkulator sederhana menggunakan HTML,
                        CSS, dan JavaScript.
                    </p>

                    <button class="button"
                            onclick="showDemo('calculator-demo')">
                        Coba Demo
                    </button>

                </article>

                <article class="project-card">

                    <div class="project-icon">📝</div>

                    <h3>Daily List</h3>

                    <p>
                        Aplikasi sederhana untuk membuat daftar
                        kegiatan sehari-hari.
                    </p>

                    <button class="button"
                            onclick="showDemo('todo-demo')">
                        Coba Demo
                    </button>

                </article>

                <article class="project-card">

                    <div class="project-icon">💡</div>

                    <h3>Quick Notes</h3>

                    <p>
                        Aplikasi catatan sederhana untuk menulis
                        dan menyimpan catatan.
                    </p>

                    <button class="button"
                            onclick="quickNote()">
                        Coba Demo
                    </button>

                </article>

            </div>

            <!-- CALCULATOR DEMO -->
            <div class="demo-box" id="calculator-demo">

                <h3>🧮 Demo Mini Kalkulator</h3>

                <div class="calculator">

                    <input type="text"
                           id="calc-display"
                           readonly>

                    <div class="calc-buttons">

                        <button onclick="clearCalc()">C</button>
                        <button onclick="deleteCalc()">⌫</button>
                        <button onclick="addCalc('/')">÷</button>
                        <button onclick="addCalc('*')">×</button>

                        <button onclick="addCalc('7')">7</button>
                        <button onclick="addCalc('8')">8</button>
                        <button onclick="addCalc('9')">9</button>
                        <button onclick="addCalc('-')">−</button>

                        <button onclick="addCalc('4')">4</button>
                        <button onclick="addCalc('5')">5</button>
                        <button onclick="addCalc('6')">6</button>
                        <button onclick="addCalc('+')">+</button>

                        <button onclick="addCalc('1')">1</button>
                        <button onclick="addCalc('2')">2</button>
                        <button onclick="addCalc('3')">3</button>
                        <button onclick="calculate()">=</button>

                        <button onclick="addCalc('0')">0</button>
                        <button onclick="addCalc('.')">.</button>

                    </div>
                </div>
            </div>

            <!-- DAILY LIST DEMO -->
            <div class="demo-box" id="todo-demo">

                <h3>📝 Demo Daily List</h3>

                <div class="todo-box">

                    <div class="todo-input">

                        <input type="text"
                               id="todo-input"
                               placeholder="Tulis kegiatan...">

                        <button class="button"
                                onclick="addTodo()">
                            Tambah
                        </button>

                    </div>

                    <ul id="todo-list"></ul>

                </div>
            </div>

        </section>

        <!-- KONTAK -->
        <section id="contact">

            <h2 class="section-title">Kontak</h2>

            <div class="contact-box">

                <p>
                    📧 Email:
                    <a href="mailto:nsari88751@gmail.com">
                        nsari88751@gmail.com
                    </a>
                </p>

                <p>
                    📷 Instagram:
                    <b>piiistecc21</b>
                </p>

                

            </div>
        </section>

    </main>

    <!-- FOOTER -->
    <footer>
        <p>
            © 2026 Dwi Novita Sari | Mini Project Portofolio UI/UX
        </p>
    </footer>

    <!-- SCROLL TOP -->
    <button id="top-button" onclick="scrollTopPage()">
        ↑
    </button>

    <script>

        /* MENU MOBILE */
        function toggleMenu() {
            const navLinks = document.getElementById("navLinks");
            navLinks.classList.toggle("active");
        }

        /* DARK MODE */
        function toggleTheme() {
            document.body.classList.toggle("dark");

            const button = document.querySelector(".theme-button");

            if (document.body.classList.contains("dark")) {
                button.textContent = "☀️";
            } else {
                button.textContent = "🌙";
            }
        }

        /* SHOW DEMO */
        function showDemo(id) {

            const demo = document.getElementById(id);

            demo.scrollIntoView({
                behavior: "smooth"
            });
        }

        /* CALCULATOR */
        function addCalc(value) {

            const display = document.getElementById("calc-display");

            display.value += value;
        }

        function clearCalc() {

            document.getElementById("calc-display").value = "";
        }

        function deleteCalc() {

            const display = document.getElementById("calc-display");

            display.value = display.value.slice(0, -1);
        }

        function calculate() {

            const display = document.getElementById("calc-display");

            try {

                if (display.value === "") {
                    return;
                }

                display.value = Function(
                    "return " + display.value
                )();

            } catch {

                display.value = "Error";
            }
        }

        /* DAILY LIST */
        function addTodo() {

            const input = document.getElementById("todo-input");
            const list = document.getElementById("todo-list");

            const text = input.value.trim();

            if (text === "") {
                alert("Silakan tulis kegiatan terlebih dahulu!");
                return;
            }

            const li = document.createElement("li");

            li.innerHTML = `
                <span>${text}</span>
                <button onclick="this.parentElement.remove()">
                    Hapus
                </button>
            `;

            list.appendChild(li);

            input.value = "";
        }

        /* QUICK NOTES */
        function quickNote() {

            const note = prompt(
                "Tulis catatan kamu:"
            );

            if (note !== null && note.trim() !== "") {

                alert(
                    "Catatan berhasil disimpan!\n\n" +
                    note
                );

            }
        }

        /* SCROLL TOP */
        window.onscroll = function() {

            const button =
                document.getElementById("top-button");

            if (document.documentElement.scrollTop > 300) {

                button.style.display = "block";

            } else {

                button.style.display = "none";
            }
        };

        function scrollTopPage() {

            window.scrollTo({
                top: 0,
                behavior: "smooth"
            });
        }

    </script>

</body>
</html>
