<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0"><title>Personal Life Dashboard | Sharzil Zofi</title>

<meta
    name="description"
    content="Personal Life Dashboard — a connected personal system for nutrition, finance, workouts, time tracking, daily logs and analytics."
>

<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    :root {
        --bg: #070b14;
        --bg-soft: #0d1321;
        --card: rgba(255,255,255,0.055);
        --card-hover: rgba(255,255,255,0.085);
        --border: rgba(255,255,255,0.10);
        --text: #f8fafc;
        --muted: #94a3b8;
        --blue: #38bdf8;
        --purple: #8b5cf6;
        --green: #34d399;
        --orange: #fb923c;
        --pink: #f472b6;
        --radius: 22px;
    }

    html {
        scroll-behavior: smooth;
    }

    body {
        font-family:
            Inter,
            ui-sans-serif,
            system-ui,
            -apple-system,
            BlinkMacSystemFont,
            "Segoe UI",
            sans-serif;
        background:
            radial-gradient(circle at 15% 10%, rgba(56,189,248,.12), transparent 30%),
            radial-gradient(circle at 85% 15%, rgba(139,92,246,.13), transparent 30%),
            var(--bg);
        color: var(--text);
        line-height: 1.7;
        overflow-x: hidden;
    }

    a {
        color: inherit;
        text-decoration: none;
    }

    .container {
        width: min(1120px, calc(100% - 40px));
        margin: auto;
    }

    /* ---------------- HERO ---------------- */

    .hero {
        min-height: 92vh;
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        overflow: hidden;
        text-align: center;
    }

    .hero-grid {
        position: absolute;
        inset: 0;
        opacity: .15;
        background-image:
            linear-gradient(rgba(255,255,255,.06) 1px, transparent 1px),
            linear-gradient(90deg, rgba(255,255,255,.06) 1px, transparent 1px);
        background-size: 50px 50px;
        mask-image: linear-gradient(to bottom, black, transparent);
    }

    .orb {
        position: absolute;
        border-radius: 50%;
        filter: blur(90px);
        opacity: .28;
        animation: float 8s ease-in-out infinite;
    }

    .orb.one {
        width: 300px;
        height: 300px;
        background: var(--blue);
        top: 5%;
        left: -100px;
    }

    .orb.two {
        width: 350px;
        height: 350px;
        background: var(--purple);
        right: -120px;
        top: 20%;
        animation-delay: -3s;
    }

    @keyframes float {
        0%,100% {
            transform: translateY(0) scale(1);
        }

        50% {
            transform: translateY(-35px) scale(1.08);
        }
    }

    .hero-content {
        position: relative;
        z-index: 2;
        max-width: 900px;
    }

    .badge {
        display: inline-flex;
        align-items: center;
        gap: 8px;
        padding: 8px 15px;
        border: 1px solid rgba(56,189,248,.25);
        border-radius: 999px;
        background: rgba(56,189,248,.07);
        color: var(--blue);
        font-size: .85rem;
        font-weight: 700;
        letter-spacing: .08em;
        text-transform: uppercase;
        margin-bottom: 25px;
    }

    .pulse {
        width: 8px;
        height: 8px;
        border-radius: 50%;
        background: var(--green);
        box-shadow: 0 0 0 0 rgba(52,211,153,.6);
        animation: pulse 2s infinite;
    }

    @keyframes pulse {
        70% {
            box-shadow: 0 0 0 9px rgba(52,211,153,0);
        }
    }

    .hero h1 {
        font-size: clamp(3rem, 8vw, 6.5rem);
        line-height: 1;
        letter-spacing: -0.07em;
        margin-bottom: 25px;
    }

    .gradient-text {
        background: linear-gradient(
            90deg,
            #fff,
            #38bdf8,
            #8b5cf6,
            #f472b6
        );
        background-size: 250% auto;
        -webkit-background-clip: text;
        background-clip: text;
        color: transparent;
        animation: gradientMove 6s linear infinite;
    }

    @keyframes gradientMove {
        to {
            background-position: 250% center;
        }
    }

    .hero p {
        max-width: 720px;
        margin: auto;
        color: var(--muted);
        font-size: 1.15rem;
    }

    .hero-buttons {
        display: flex;
        justify-content: center;
        gap: 12px;
        flex-wrap: wrap;
        margin-top: 35px;
    }

    .btn {
        padding: 13px 21px;
        border-radius: 12px;
        border: 1px solid var(--border);
        transition: .25s ease;
        font-weight: 700;
    }

    .btn:hover {
        transform: translateY(-3px);
    }

    .btn-primary {
        background: linear-gradient(135deg, var(--blue), var(--purple));
        border: none;
        box-shadow: 0 10px 35px rgba(56,189,248,.18);
    }

    .btn-secondary {
        background: rgba(255,255,255,.04);
    }

    /* ---------------- SECTIONS ---------------- */

    section {
        padding: 95px 0;
    }

    .section-title {
        text-align: center;
        margin-bottom: 50px;
    }

    .eyebrow {
        color: var(--blue);
        font-weight: 800;
        font-size: .8rem;
        letter-spacing: .14em;
        text-transform: uppercase;
        margin-bottom: 10px;
    }

    .section-title h2 {
        font-size: clamp(2rem, 5vw, 3.5rem);
        letter-spacing: -.045em;
        line-height: 1.1;
    }

    .section-title p {
        color: var(--muted);
        max-width: 650px;
        margin: 15px auto 0;
    }

    /* ---------------- ABOUT ---------------- */

    .about {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 25px;
    }

    .glass {
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: var(--radius);
        backdrop-filter: blur(16px);
        -webkit-backdrop-filter: blur(16px);
    }

    .about-card {
        padding: 35px;
    }

    .about-card h3 {
        font-size: 1.5rem;
        margin-bottom: 15px;
    }

    .about-card p {
        color: var(--muted);
    }

    .vision-box {
        background:
            linear-gradient(
                135deg,
                rgba(56,189,248,.09),
                rgba(139,92,246,.09)
            );
    }

    /* ---------------- MODULES ---------------- */

    .modules {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 18px;
    }

    .module {
        padding: 27px;
        transition: .3s ease;
        position: relative;
        overflow: hidden;
    }

    .module::after {
        content: "";
        position: absolute;
        width: 100px;
        height: 100px;
        background: var(--blue);
        filter: blur(65px);
        opacity: .08;
        right: -30px;
        bottom: -30px;
    }

    .module:hover {
        transform: translateY(-7px);
        background: var(--card-hover);
        border-color: rgba(56,189,248,.25);
    }

    .module-icon {
        font-size: 2rem;
        margin-bottom: 15px;
    }

    .module h3 {
        margin-bottom: 8px;
    }

    .module p {
        color: var(--muted);
        font-size: .92rem;
    }

    /* ---------------- FLOW ---------------- */

    .flow {
        display: grid;
        grid-template-columns: repeat(5, 1fr);
        gap: 10px;
        align-items: center;
    }

    .flow-item {
        text-align: center;
        padding: 25px 15px;
    }

    .flow-item .icon {
        font-size: 2rem;
        margin-bottom: 8px;
    }

    .arrow {
        color: var(--blue);
        font-size: 1.5rem;
        text-align: center;
    }

    /* ---------------- TECH ---------------- */

    .tech-grid {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 12px;
    }

    .tech {
        padding: 13px 19px;
        border: 1px solid var(--border);
        background: var(--card);
        border-radius: 12px;
        color: #dbeafe;
        font-weight: 700;
        transition: .25s;
    }

    .tech:hover {
        transform: translateY(-3px);
        border-color: var(--blue);
    }

    /* ---------------- PHASE ---------------- */

    .phase {
        display: grid;
        grid-template-columns: 110px 1fr;
        gap: 25px;
        padding: 25px;
        margin-bottom: 12px;
    }

    .phase-number {
        display: grid;
        place-items: center;
        width: 70px;
        height: 70px;
        border-radius: 18px;
        background: linear-gradient(135deg, var(--blue), var(--purple));
        font-size: 1.3rem;
        font-weight: 900;
    }

    .phase h3 {
        margin-bottom: 5px;
    }

    .phase p {
        color: var(--muted);
    }

    .status {
        display: inline-block;
        margin-top: 9px;
        font-size: .75rem;
        padding: 4px 9px;
        border-radius: 999px;
        background: rgba(52,211,153,.1);
        color: var(--green);
        font-weight: 800;
    }

    .status.pending {
        background: rgba(148,163,184,.1);
        color: var(--muted);
    }

    /* ---------------- CONTACT ---------------- */

    .contact {
        text-align: center;
        padding: 65px 30px;
        background:
            radial-gradient(circle at 20% 20%, rgba(56,189,248,.12), transparent 35%),
            radial-gradient(circle at 80% 70%, rgba(139,92,246,.13), transparent 35%),
            var(--card);
    }

    .contact h2 {
        font-size: clamp(2rem, 5vw, 3.5rem);
        letter-spacing: -.05em;
    }

    .contact p {
        max-width: 650px;
        color: var(--muted);
        margin: 15px auto 30px;
    }

    .whatsapp {
        display: inline-flex;
        align-items: center;
        gap: 10px;
        padding: 14px 22px;
        border-radius: 13px;
        background: #25D366;
        color: white;
        font-weight: 800;
        transition: .25s;
        box-shadow: 0 12px 35px rgba(37,211,102,.18);
    }

    .whatsapp:hover {
        transform: translateY(-4px);
        box-shadow: 0 18px 45px rgba(37,211,102,.28);
    }

    /* ---------------- FOOTER ---------------- */

    footer {
        padding: 35px 0;
        border-top: 1px solid var(--border);
        text-align: center;
        color: var(--muted);
    }

    footer strong {
        color: white;
    }

    /* ---------------- REVEAL ---------------- */

    .reveal {
        opacity: 0;
        transform: translateY(30px);
        transition: opacity .7s ease, transform .7s ease;
    }

    .reveal.show {
        opacity: 1;
        transform: translateY(0);
    }

    /* ---------------- RESPONSIVE ---------------- */

    @media (max-width: 850px) {

        .about {
            grid-template-columns: 1fr;
        }

        .modules {
            grid-template-columns: repeat(2, 1fr);
        }

        .flow {
            grid-template-columns: 1fr;
        }

        .arrow {
            transform: rotate(90deg);
        }

        .phase {
            grid-template-columns: 80px 1fr;
        }
    }

    @media (max-width: 600px) {

        .container {
            width: min(100% - 24px, 1120px);
        }

        section {
            padding: 65px 0;
        }

        .hero {
            min-height: 85vh;
        }

        .hero h1 {
            font-size: 3.2rem;
        }

        .hero p {
            font-size: 1rem;
        }

        .modules {
            grid-template-columns: 1fr;
        }

        .about-card {
            padding: 25px;
        }

        .phase {
            grid-template-columns: 1fr;
        }

        .phase-number {
            width: 60px;
            height: 60px;
        }
    }
</style>

</head><body><!-- ================= HERO ================= --><header class="hero"><div class="hero-grid"></div>

<div class="orb one"></div>
<div class="orb two"></div>

<div class="hero-content">

    <div class="badge">
        <span class="pulse"></span>
        Project in Development
    </div>

    <h1>
        Personal<br>
        <span class="gradient-text">Life Dashboard</span>
    </h1>

    <p>
        One connected system for managing nutrition, finance,
        workouts, time, daily life and personal analytics.
    </p>

    <div class="hero-buttons">

        <a href="#about" class="btn btn-primary">
            Explore Project ↓
        </a>

        <a href="#contact" class="btn btn-secondary">
            💬 Contact Me
        </a>

    </div>

</div>

</header><!-- ================= ABOUT ================= --><section id="about"><div class="container">

    <div class="section-title reveal">

        <div class="eyebrow">About the product</div>

        <h2>
            Your life.<br>
            One dashboard.
        </h2>

        <p>
            Personal Life Dashboard is a web application designed
            to bring important areas of everyday life into one
            connected system.
        </p>

    </div>


    <div class="about">

        <div class="glass about-card reveal">

            <h3>What is it?</h3>

            <p>
                Instead of using separate applications for food,
                money, workouts, time tracking and daily notes,
                this project brings them together into one
                personal management platform.
            </p>

            <br>

            <p>
                The system stores your information and turns it
                into useful summaries, history and analytics.
            </p>

        </div>


        <div class="glass about-card vision-box reveal">

            <h3>🎯 The Vision</h3>

            <p>
                The long-term goal is to build a personal
                operating system where your own data helps you
                understand how you spend your time, money,
                energy and effort.
            </p>

            <br>

            <strong>
                Track it → Understand it → Improve it
            </strong>

        </div>

    </div>

</div>

</section><!-- ================= MODULES ================= --><section><div class="container">

    <div class="section-title reveal">

        <div class="eyebrow">Core modules</div>

        <h2>Everything in one place.</h2>

        <p>
            Each section focuses on one part of your life while
            remaining connected to the overall dashboard.
        </p>

    </div>


    <div class="modules">

        <div class="glass module reveal">
            <div class="module-icon">🏠</div>
            <h3>Dashboard</h3>
            <p>
                A central overview of your day, statistics,
                recent activity and important information.
            </p>
        </div>


        <div class="glass module reveal">
            <div class="module-icon">🍽️</div>
            <h3>Nutrition</h3>
            <p>
                Track food, calories, protein, carbohydrates,
                fats, fiber and nutrition targets.
            </p>
        </div>


        <div class="glass module reveal">
            <div class="module-icon">💰</div>
            <h3>Finance</h3>
            <p>
                Manage accounts, income, expenses, transfers,
                balances and financial history.
            </p>
        </div>


        <div class="glass module reveal">
            <div class="module-icon">🏋️</div>
            <h3>Workout</h3>
            <p>
                Track exercises, sets, reps, weight, volume,
                workout sessions and progress.
            </p>
        </div>


        <div class="glass module reveal">
            <div class="module-icon">⏱️</div>
            <h3>Time Tracking</h3>
            <p>
                Track study, work, coding, gym, sleep,
                entertainment and free time.
            </p>
        </div>


        <div class="glass module reveal">
            <div class="module-icon">📔</div>
            <h3>Daily Log</h3>
            <p>
                Record sleep, wake time, mood, energy,
                daily rating and personal notes.
            </p>
        </div>


        <div class="glass module reveal">
            <div class="module-icon">📊</div>
            <h3>Analytics</h3>
            <p>
                Convert your stored information into charts,
                trends and useful statistics.
            </p>
        </div>


        <div class="glass module reveal">
            <div class="module-icon">🕘</div>
            <h3>History</h3>
            <p>
                Search, filter and review your previous
                records by date and category.
            </p>
        </div>


        <div class="glass module reveal">
            <div class="module-icon">⚙️</div>
            <h3>Settings</h3>
            <p>
                Manage preferences, targets, integrations
                and application data.
            </p>
        </div>

    </div>

</div>

</section><!-- ================= CONNECTION ================= --><section><div class="container">

    <div class="section-title reveal">

        <div class="eyebrow">Connected system</div>

        <h2>Everything talks to everything.</h2>

        <p>
            The modules are designed to work together instead
            of behaving like separate applications.
        </p>

    </div>


    <div class="glass flow reveal">

        <div class="flow-item">
            <div class="icon">🍽️</div>
            <strong>Nutrition</strong>
        </div>

        <div class="arrow">→</div>

        <div class="flow-item">
            <div class="icon">💰</div>
            <strong>Finance</strong>
        </div>

        <div class="arrow">→</div>

        <div class="flow-item">
            <div class="icon">🏋️</div>
            <strong>Workout</strong>
        </div>

    </div>

    <br>

    <div class="glass flow reveal">

        <div class="flow-item">
            <div class="icon">⏱️</div>
            <strong>Time</strong>
        </div>

        <div class="arrow">→</div>

        <div class="flow-item">
            <div class="icon">📔</div>
            <strong>Daily Log</strong>
        </div>

        <div class="arrow">→</div>

        <div class="flow-item">
            <div class="icon">📊</div>
            <strong>Analytics</strong>
        </div>

    </div>

</div>

</section><!-- ================= TECHNOLOGY ================= --><section><div class="container">

    <div class="section-title reveal">

        <div class="eyebrow">Technology</div>

        <h2>Built with modern tools.</h2>

        <p>
            The application is being developed using a modern
            full-stack web architecture.
        </p>

    </div>


    <div class="tech-grid reveal">

        <div class="tech">Next.js 14</div>
        <div class="tech">React</div>
        <div class="tech">TypeScript</div>
        <div class="tech">Tailwind CSS</div>
        <div class="tech">Firebase Auth</div>
        <div class="tech">Cloud Firestore</div>
        <div class="tech">Vercel</div>

    </div>

</div>

</section><!-- ================= PHASE 1 ================= --><section><div class="container">

    <div class="section-title reveal">

        <div class="eyebrow">Current development</div>

        <h2>Phase 1 — Foundation</h2>

        <p>
            The first phase establishes the core structure,
            authentication and application shell.
        </p>

    </div>


    <div class="glass phase reveal">

        <div class="phase-number">01</div>

        <div>
            <h3>Project Setup</h3>

            <p>
                Next.js 14, App Router, TypeScript and
                Tailwind CSS.
            </p>

            <span class="status">Completed</span>
        </div>

    </div>


    <div class="glass phase reveal">

        <div class="phase-number">02</div>

        <div>
            <h3>Authentication</h3>

            <p>
                Firebase email/password registration,
                login and logout.
            </p>

            <span class="status">Completed</span>
        </div>

    </div>


    <div class="glass phase reveal">

        <div class="phase-number">03</div>

        <div>
            <h3>Application Shell</h3>

            <p>
                Sidebar, header, navigation and protected
                application routes.
            </p>

            <span class="status">Completed</span>
        </div>

    </div>


    <div class="glass phase reveal">

        <div class="phase-number">04</div>

        <div>
            <h3>Firestore Foundation</h3>

            <p>
                Initial security rules and per-user
                data isolation.
            </p>

            <span class="status">Completed</span>
        </div>

    </div>

</div>

</section><!-- ================= SETUP ================= --><section><div class="container">

    <div class="section-title reveal">

        <div class="eyebrow">Getting started</div>

        <h2>Run it locally.</h2>

    </div>


    <div class="glass about-card reveal">

        <h3>1. Install dependencies</h3>

        <pre><code>npm install</code></pre>

        <br>

        <h3>2. Create Firebase project</h3>

        <p>
            Create a Firebase project, enable Email/Password
            Authentication, create Firestore and add a Web App.
        </p>

        <br>

        <h3>3. Configure environment variables</h3>

        <pre><code>cp .env.example .env.local</code></pre>

        <br>

        <h3>4. Start development server</h3>

        <pre><code>npm run dev</code></pre>

        <br>

        <p>
            Then open:
            <strong>http://localhost:3000</strong>
        </p>

    </div>

</div>

</section><!-- ================= ROADMAP ================= --><section><div class="container">

    <div class="section-title reveal">

        <div class="eyebrow">Roadmap</div>

        <h2>What's coming next?</h2>

    </div>


    <div class="modules">

        <div class="glass module reveal">
            <div class="module-icon">🔥</div>
            <h3>Phase 2</h3>
            <p>
                Firestore data layer, settings and
                user preferences.
            </p>
        </div>

        <div class="glass module reveal">
            <div class="module-icon">🍽️</div>
            <h3>Phase 3</h3>
            <p>
                Complete nutrition tracking and
                nutrition analytics.
            </p>
        </div>

        <div class="glass module reveal">
            <div class="module-icon">💰</div>
            <h3>Phase 4</h3>
            <p>
                Complete finance management and
                financial analytics.
            </p>
        </div>

        <div class="glass module reveal">
            <div class="module-icon">🏋️</div>
            <h3>Phase 5</h3>
            <p>
                Workout tracking, timers and
                progression.
            </p>
        </div>

        <div class="glass module reveal">
            <div class="module-icon">⏱️</div>
            <h3>Phase 6</h3>
            <p>
                Time tracking, timers and
                daily timeline.
            </p>
        </div>

        <div class="glass module reveal">
            <div class="module-icon">📔</div>
            <h3>Phase 7</h3>
            <p>
                Daily log, sleep, mood, energy
                and notes.
            </p>
        </div>

    </div>

</div>

</section><!-- ================= CONTACT ================= --><section id="contact"><div class="container">

    <div class="glass contact reveal">

        <div class="eyebrow">Let's build something</div>

        <h2>
            Have an app idea?
        </h2>

        <p>
            If you want to create your own personal dashboard,
            productivity system, business tool or custom web
            application, feel free to contact me.
        </p>

        <!-- Replace YOUR_WHATSAPP_NUMBER with your actual number -->
        <a
            class="whatsapp"
            href="https://wa.me/YOUR_WHATSAPP_NUMBER"
            target="_blank"
            rel="noopener noreferrer"
        >
            <span>💬</span>
            Contact Me on WhatsApp
        </a>

        <br><br>

        <strong style="font-size:1.2rem;">
            Sharzil Zofi
        </strong>

        <p style="margin-bottom:0;">
            Have an idea? Let's build it.
        </p>

    </div>

</div>

</section><!-- ================= FOOTER ================= --><footer><div class="container">

    <p>
        <strong>Personal Life Dashboard</strong>
        <br>
        Track it. Understand it. Improve it.
    </p>

    <br>

    <small>
        © <span id="year"></span> Sharzil Zofi. Built with passion.
    </small>

</div>

</footer><script>

    /* Current year */

    document.getElementById("year").textContent =
        new Date().getFullYear();


    /* Scroll reveal animation */

    const revealElements =
        document.querySelectorAll(".reveal");

    const revealObserver =
        new IntersectionObserver(
            (entries) => {

                entries.forEach((entry) => {

                    if (entry.isIntersecting) {

                        entry.target.classList.add("show");

                        revealObserver.unobserve(entry.target);

                    }

                });

            },
            {
                threshold: 0.12
            }
        );


    revealElements.forEach((element) => {

        revealObserver.observe(element);

    });

</script></body>
</html>
