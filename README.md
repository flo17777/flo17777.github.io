
[tv_display.html](https://github.com/user-attachments/files/24055181/tv_display.html)
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SILITECH AG</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #0a1628 0%, #1a365d 50%, #0a1628 100%);
            min-height: 100vh;
            font-family: 'Segoe UI', system-ui, sans-serif;
            overflow: hidden;
            color: white;
        }

        .slide {
            position: absolute;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 1.5s ease-in-out;
            padding: 60px;
        }

        .slide.active {
            opacity: 1;
        }

        .slide img {
            max-width: 70%;
            max-height: 50vh;
            object-fit: contain;
            filter: drop-shadow(0 20px 40px rgba(0,0,0,0.3));
        }

        .slide h1 {
            font-size: 4rem;
            font-weight: 300;
            margin-top: 40px;
            text-align: center;
            letter-spacing: 2px;
        }

        .slide h2 {
            font-size: 2rem;
            font-weight: 300;
            margin-top: 20px;
            opacity: 0.8;
            text-align: center;
        }

        .slide.hero {
            background: linear-gradient(135deg, #0052a3 0%, #003366 100%);
        }

        .slide.hero h1 {
            font-size: 5rem;
            font-weight: 200;
            letter-spacing: 8px;
        }

        .slide.hero h2 {
            font-size: 1.8rem;
            letter-spacing: 4px;
            margin-top: 30px;
        }

        .partners-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 60px;
            margin-top: 40px;
        }

        .partners-grid img {
            max-width: 250px;
            max-height: 120px;
            filter: brightness(0) invert(1) drop-shadow(0 10px 20px rgba(0,0,0,0.2));
            opacity: 0.9;
        }

        .tagline {
            position: fixed;
            bottom: 40px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 1.2rem;
            opacity: 0.6;
            letter-spacing: 3px;
            text-transform: uppercase;
        }

        .corner-logo {
            position: fixed;
            top: 30px;
            right: 40px;
            width: 150px;
            opacity: 0.7;
            filter: brightness(0) invert(1);
        }

        /* Subtle animated background */
        .bg-glow {
            position: fixed;
            width: 800px;
            height: 800px;
            border-radius: 50%;
            background: radial-gradient(circle, rgba(0,82,147,0.3) 0%, transparent 70%);
            animation: float 20s ease-in-out infinite;
            pointer-events: none;
        }

        .bg-glow:nth-child(1) { top: -400px; left: -200px; }
        .bg-glow:nth-child(2) { bottom: -400px; right: -200px; animation-delay: -10s; }

        @keyframes float {
            0%, 100% { transform: translate(0, 0) scale(1); }
            50% { transform: translate(50px, 30px) scale(1.1); }
        }

        .progress {
            position: fixed;
            bottom: 0;
            left: 0;
            height: 4px;
            background: rgba(255,255,255,0.8);
            animation: progress 6s linear infinite;
        }

        @keyframes progress {
            0% { width: 0%; }
            100% { width: 100%; }
        }
    </style>
</head>
<body>
    <div class="bg-glow"></div>
    <div class="bg-glow"></div>

    <img src="01_LOGOS_PARTNER/16 zu 9, transparent/SILISIL_logo_tp.png" class="corner-logo" alt="">

    <!-- Slide 1: Hero -->
    <div class="slide hero active">
        <h1>SILITECH AG</h1>
        <h2>Silikon- & Klebstoffsysteme</h2>
    </div>

    <!-- Slide 2: SILISIL -->
    <div class="slide">
        <img src="01_LOGOS_PARTNER/16 zu 9, transparent/SILISIL_logo_tp.png" alt="SILISIL">
        <h1>SILISIL</h1>
        <h2>Hochleistungs-Silikone</h2>
    </div>

    <!-- Slide 3: RTV Produkt -->
    <div class="slide">
        <img src="01_LOGOS_PARTNER/16 zu 9, transparent/SILISIL RTV CT-Body 10.png" alt="RTV">
        <h2>RTV-2 Silikonsysteme</h2>
    </div>

    <!-- Slide 4: Partners -->
    <div class="slide">
        <h1 style="margin-bottom: 60px; margin-top: 0;">Unsere Partner</h1>
        <div class="partners-grid">
            <img src="01_LOGOS_PARTNER/16 zu 9, transparent/Permabond_Logo_tp.png" alt="Permabond">
            <img src="01_LOGOS_PARTNER/16 zu 9, transparent/Loctite_Logo_tp.png" alt="Loctite">
            <img src="01_LOGOS_PARTNER/16 zu 9, transparent/Henkel_Logo_tp.png" alt="Henkel">
        </div>
    </div>

    <!-- Slide 5: CAF -->
    <div class="slide">
        <img src="Nach Hersteller/Elkem/CAF/Silitech_Elkem_CAF_33_Black_1.JPG" alt="CAF 33" style="max-height: 60vh; border-radius: 10px;">
        <h2>CAF Dichtmassen</h2>
    </div>

    <!-- Slide 6: Loctite -->
    <div class="slide">
        <img src="01_LOGOS_PARTNER/16 zu 9, transparent/Loctite_Logo_tp.png" alt="Loctite">
        <h1>Loctite</h1>
        <h2>Strukturklebstoffe & Schraubensicherung</h2>
    </div>

    <!-- Slide 7: Permabond -->
    <div class="slide">
        <img src="01_LOGOS_PARTNER/16 zu 9, transparent/Permabond_Logo_tp.png" alt="Permabond">
        <h1>Permabond</h1>
        <h2>Anaerobe Klebstoffe</h2>
    </div>

    <!-- Slide 8: Zhermack/Flex -->
    <div class="slide">
        <img src="01_LOGOS_PARTNER/16 zu 9, transparent/SILISIL RTV CT-Flex 25.png" alt="Flex">
        <h2>Entwicklungspartner für Speziallösungen</h2>
    </div>

    <div class="progress"></div>
    <div class="tagline">Ihr Partner in der Schweiz</div>

    <script>
        const slides = document.querySelectorAll('.slide');
        let current = 0;
        const duration = 6000; // 6 Sekunden pro Slide

        function nextSlide() {
            slides[current].classList.remove('active');
            current = (current + 1) % slides.length;
            slides[current].classList.add('active');

            // Reset progress bar
            const progress = document.querySelector('.progress');
            progress.style.animation = 'none';
            progress.offsetHeight; // Trigger reflow
            progress.style.animation = `progress ${duration/1000}s linear infinite`;
        }

        setInterval(nextSlide, duration);
    </script>
</body>
</html>
