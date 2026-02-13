<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>💕 Surat Cinta Valentine 💕</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #ffd6e8 0%, #c7ceea 25%, #b5ead7 50%, #ffd6e8 75%, #e0bbe4 100%);
            background-size: 400% 400%;
            animation: gradientShift 15s ease infinite;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Comic Sans MS', 'Arial Rounded MT Bold', cursive;
            padding: 20px;
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .main-container {
            width: 100%;
            max-width: 700px;
        }

        /* ENVELOPE STYLING */
        .envelope-container {
            position: relative;
            width: 100%;
            perspective: 1000px;
            filter: drop-shadow(0 20px 60px rgba(255, 182, 193, 0.4));
            margin-bottom: 40px;
        }

        /* ENVELOPE BODY */
        .envelope-body {
            width: 100%;
            height: 450px;
            background: linear-gradient(135deg, #fff5f9 0%, #ffe4f0 100%);
            border: 5px solid #ffb6d9;
            border-radius: 15px 15px 8px 8px;
            position: relative;
            box-shadow: 0 30px 80px rgba(255, 105, 180, 0.3), inset 0 1px 0 rgba(255, 255, 255, 0.8);
            overflow: hidden;
        }

        .envelope-body::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 40px;
            background: linear-gradient(to bottom, rgba(255, 182, 193, 0.1), transparent);
            pointer-events: none;
        }

        .envelope-body::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            height: 100%;
            background-image: 
                radial-gradient(circle at 20% 30%, rgba(255, 218, 224, 0.4) 0%, transparent 50%),
                radial-gradient(circle at 80% 70%, rgba(200, 230, 201, 0.3) 0%, transparent 50%);
            pointer-events: none;
        }

        /* ENVELOPE FLAP */
        .envelope-flap {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            width: 100%;
            height: 50%;
            background: linear-gradient(135deg, #ffb6d9 0%, #ff9cd5 50%, #ff85c9 100%);
            border: 5px solid #ffb6d9;
            border-bottom: none;
            border-radius: 15px 15px 0 0;
            clip-path: polygon(0 0, 100% 0, 100% 60%, 50% 100%, 0 60%);
            transform-origin: top center;
            transition: transform 0.8s cubic-bezier(0.68, -0.55, 0.265, 1.55);
            z-index: 20;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 4em;
            box-shadow: 0 15px 40px rgba(255, 105, 180, 0.35), inset 0 -5px 15px rgba(255, 255, 255, 0.3);
            position: relative;
        }

        .envelope-flap::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 100%;
            background: linear-gradient(180deg, rgba(255, 255, 255, 0.3) 0%, transparent 70%);
            border-radius: 15px 15px 0 0;
            pointer-events: none;
        }

        .envelope-flap:hover {
            filter: brightness(1.15);
        }

        .envelope-flap.open {
            transform: rotateX(120deg);
        }

        /* ENVELOPE BOTTOM PART */
        .envelope-bottom {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            width: 100%;
            height: 8px;
            background: linear-gradient(to right, #ffb6d9 0%, #ff85c9 50%, #ffb6d9 100%);
            border-bottom: 5px solid #ffb6d9;
            box-shadow: inset 0 2px 4px rgba(255, 105, 180, 0.3), 0 3px 8px rgba(255, 105, 180, 0.2);
            border-radius: 0 0 8px 8px;
        }

        /* ENVELOPE FRONT CONTENT */
        .envelope-front {
            position: absolute;
            top: 50px;
            left: 0;
            right: 0;
            width: 100%;
            height: 380px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 10;
            text-align: center;
            transition: opacity 0.6s ease;
            padding: 20px;
        }

        .envelope-front.hide {
            opacity: 0;
            pointer-events: none;
        }

        .stamp {
            position: absolute;
            top: 30px;
            right: 30px;
            width: 70px;
            height: 90px;
            background: linear-gradient(45deg, #ffd6e8 0%, #ffb3d9 25%, #ff9cd5 50%, #ffd6e8 75%, #ffb3d9 100%);
            background-size: 200% 200%;
            animation: stampRotate 3s ease-in-out infinite;
            border: 3px dashed #ff9cd5;
            border-radius: 6px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 2.2em;
            box-shadow: 0 6px 16px rgba(255, 105, 180, 0.3);
            transform: rotate(-20deg);
            flex-direction: column;
        }

        .stamp::before {
            content: '';
            position: absolute;
            inset: 3px;
            border: 2px dashed rgba(255, 182, 193, 0.5);
            border-radius: 4px;
            pointer-events: none;
        }

        @keyframes stampRotate {
            0%, 100% { transform: rotate(-20deg) scale(1); }
            50% { transform: rotate(-20deg) scale(1.08); }
        }

        .envelope-label {
            font-size: 1.9em;
            color: #ff69b4;
            margin-bottom: 15px;
            font-weight: bold;
            letter-spacing: 2px;
            text-shadow: 3px 3px 6px rgba(255, 105, 180, 0.15);
        }

        .hearts-decoration {
            display: flex;
            justify-content: center;
            gap: 25px;
            font-size: 2.8em;
            margin-bottom: 20px;
            filter: drop-shadow(0 3px 6px rgba(255, 105, 180, 0.2));
        }

        .heart-icon {
            animation: heartBeat 0.6s ease-in-out infinite;
        }

        .heart-icon:nth-child(1) { animation-delay: 0s; }
        .heart-icon:nth-child(2) { animation-delay: 0.2s; }
        .heart-icon:nth-child(3) { animation-delay: 0.4s; }

        @keyframes heartBeat {
            0%, 100% { transform: scale(1); }
            25% { transform: scale(1.5); }
            50% { transform: scale(1); }
        }

        .click-hint {
            color: #ff69b4;
            font-size: 1.05em;
            animation: bounce-text 2s ease-in-out infinite;
            margin-top: 20px;
            font-style: italic;
            font-weight: bold;
            text-shadow: 2px 2px 4px rgba(255, 105, 180, 0.1);
        }

        @keyframes bounce-text {
            0%, 100% { transform: translateY(0); opacity: 0.7; }
            50% { transform: translateY(-10px); opacity: 1; }
        }

        /* LETTER CONTENT */
        .letter-page {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 450px;
            background: linear-gradient(135deg, #fffbfc 0%, #fff8fa 50%, #ffe4f0 100%);
            border: 5px solid #ffb6d9;
            border-radius: 15px;
            padding: 35px 35px;
            overflow-y: auto;
            box-shadow: 0 30px 80px rgba(255, 105, 180, 0.3), inset 0 0 40px rgba(255, 182, 193, 0.1);
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.6s ease 0.3s;
            z-index: 15;
        }

        .letter-page.show {
            opacity: 1;
            pointer-events: auto;
        }

        .letter-page::-webkit-scrollbar {
            width: 8px;
        }

        .letter-page::-webkit-scrollbar-track {
            background: rgba(255, 182, 193, 0.1);
            border-radius: 10px;
        }

        .letter-page::-webkit-scrollbar-thumb {
            background: linear-gradient(180deg, #ffb6d9, #ff9cd5);
            border-radius: 10px;
        }

        .letter-paper {
            position: relative;
        }

        .letter-paper::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: repeating-linear-gradient(
                90deg,
                #ffb6d9,
                #ffb6d9 25px,
                transparent 25px,
                transparent 30px
            );
            opacity: 0.4;
        }

        .letter-header {
            text-align: center;
            margin-bottom: 15px;
            padding-bottom: 12px;
            border-bottom: 3px dashed #ffb6d9;
        }

        .letter-decoration-top {
            font-size: 1.6em;
            margin-bottom: 8px;
            letter-spacing: 10px;
            filter: drop-shadow(0 2px 4px rgba(255, 105, 180, 0.15));
        }

        .letter-title {
            font-size: 1.6em;
            color: #ff1493;
            margin: 8px 0;
            font-weight: bold;
            text-shadow: 3px 3px 6px rgba(255, 105, 180, 0.15);
            letter-spacing: 1px;
        }

        .letter-subtitle {
            font-size: 0.95em;
            color: #ff69b4;
            font-style: italic;
            margin-bottom: 6px;
            font-weight: bold;
        }

        .letter-content {
            font-size: 0.95em;
            color: #d1466a;
            line-height: 1.75;
            text-align: justify;
            font-weight: 500;
        }

        .letter-content p {
            margin-bottom: 10px;
            position: relative;
            padding-left: 18px;
        }

        .letter-content p::before {
            content: '💕';
            position: absolute;
            left: 0;
            top: 0px;
            font-size: 0.85em;
            opacity: 0.7;
            animation: sparkleIcon 2s ease-in-out infinite;
        }

        @keyframes sparkleIcon {
            0%, 100% { opacity: 0.7; transform: scale(1); }
            50% { opacity: 1; transform: scale(1.15); }
        }

        .dancing-emojis {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 15px 0;
            font-size: 1.6em;
            filter: drop-shadow(0 3px 6px rgba(255, 105, 180, 0.2));
        }

        .emoji-dance {
            animation: dance 1s ease-in-out infinite;
        }

        .emoji-dance:nth-child(1) { animation-delay: 0s; }
        .emoji-dance:nth-child(2) { animation-delay: 0.2s; }
        .emoji-dance:nth-child(3) { animation-delay: 0.4s; }
        .emoji-dance:nth-child(4) { animation-delay: 0.2s; }

        @keyframes dance {
            0%, 100% { transform: rotate(0deg) translateY(0); }
            25% { transform: rotate(-18deg) translateY(-12px); }
            50% { transform: rotate(18deg) translateY(0); }
            75% { transform: rotate(-18deg) translateY(-12px); }
        }

        .letter-signature {
            text-align: right;
            margin-top: 15px;
            padding-top: 10px;
            border-top: 3px dashed #ffb6d9;
            font-size: 1em;
            color: #ff1493;
            font-weight: bold;
            font-style: italic;
            text-shadow: 2px 2px 4px rgba(255, 105, 180, 0.1);
        }

        .letter-footer {
            text-align: center;
            margin-top: 10px;
            font-size: 1.2em;
            letter-spacing: 6px;
            color: #ffb6d9;
            filter: drop-shadow(0 2px 4px rgba(255, 105, 180, 0.15));
        }

        /* BUTTON CONTAINER - INSIDE LETTER */
        .button-container {
            display: flex;
            gap: 12px;
            justify-content: center;
            margin-top: 15px;
            flex-wrap: wrap;
        }

        .btn {
            padding: 11px 24px;
            font-size: 0.93em;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 6px 16px rgba(255, 105, 180, 0.3);
            font-family: 'Comic Sans MS', cursive;
            letter-spacing: 0.3px;
            line-height: 1.3;
        }

        .btn-yes {
            background: linear-gradient(135deg, #ff6bb6, #ff1493, #ff6bb6);
            background-size: 200% 200%;
            color: white;
            animation: gradientShift2 3s ease infinite;
        }

        @keyframes gradientShift2 {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .btn-yes:hover:not(.enlarge) {
            transform: scale(1.12);
            box-shadow: 0 10px 24px rgba(255, 20, 147, 0.5);
        }

        .btn-yes.enlarge {
            animation: enlargeYes 0.5s ease-out forwards;
        }

        @keyframes enlargeYes {
            0% { transform: scale(1); }
            100% { transform: scale(1.4); box-shadow: 0 15px 40px rgba(255, 20, 147, 0.6); }
        }

        .btn-no {
            background: linear-gradient(135deg, #ffd6e8, #ffb6d9);
            color: #ff69b4;
            box-shadow: 0 6px 16px rgba(255, 182, 193, 0.4);
            font-weight: bold;
        }

        .btn-no:hover:not(:disabled) {
            transform: translateX(40px);
            background: linear-gradient(135deg, #ffb6d9, #ff9cd5);
            box-shadow: 0 8px 20px rgba(255, 182, 193, 0.5);
        }

        .btn-no:disabled {
            opacity: 0.3;
            cursor: not-allowed;
        }

        .floating-hearts {
            position: fixed;
            pointer-events: none;
            bottom: -50px;
            font-size: 2.8em;
            animation: float-up 5s ease-in-out infinite;
            filter: drop-shadow(0 3px 8px rgba(255, 105, 180, 0.25));
        }

        @keyframes float-up {
            0% { transform: translateY(0) translateX(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-750px) translateX(180px) rotate(360deg); opacity: 0; }
        }

        .floating-hearts:nth-child(1) { left: 5%; animation-delay: 0s; }
        .floating-hearts:nth-child(2) { left: 50%; animation-delay: 1.5s; }
        .floating-hearts:nth-child(3) { left: 85%; animation-delay: 3s; }

        @media (max-width: 750px) {
            .main-container {
                max-width: 95%;
            }

            .envelope-body {
                height: 400px;
            }

            .letter-page {
                height: 400px;
                padding: 30px 25px;
            }

            .envelope-label {
                font-size: 1.6em;
            }

            .hearts-decoration {
                gap: 18px;
                font-size: 2.3em;
            }

            .letter-title {
                font-size: 1.5em;
            }

            .letter-content {
                font-size: 0.9em;
                line-height: 1.7;
            }

            .letter-content p {
                padding-left: 16px;
                margin-bottom: 8px;
            }

            .letter-content p::before {
                font-size: 0.8em;
            }

            .stamp {
                width: 60px;
                height: 80px;
                font-size: 1.8em;
                top: 20px;
                right: 20px;
            }

            .btn {
                padding: 10px 18px;
                font-size: 0.88em;
            }
        }
    </style>
</head>
<body>
    <!-- Floating hearts background -->
    <div class="floating-hearts">💕</div>
    <div class="floating-hearts">💖</div>
    <div class="floating-hearts">💗</div>

    <!-- Main Container -->
    <div class="main-container">
        <!-- ENVELOPE -->
        <div class="envelope-container">
            <!-- Envelope Body -->
            <div class="envelope-body">
                <!-- Envelope Flap -->
                <div class="envelope-flap" id="envelopeFlap" onclick="openEnvelope()">
                    <span>💌</span>
                </div>

                <!-- Stamp -->
                <div class="stamp">💕</div>

                <!-- Front Content -->
                <div class="envelope-front" id="envelopeFront">
                    <div class="envelope-label">To: Sayangg ❤️</div>
                    
                    <div class="hearts-decoration">
                        <span class="heart-icon">💖</span>
                        <span class="heart-icon">💕</span>
                        <span class="heart-icon">💗</span>
                    </div>
                    
                    <div class="click-hint">
                        ✨ Klik amplop untuk membuka surat istimewa... ✨
                    </div>
                </div>

                <!-- Letter Inside -->
                <div class="letter-page" id="letterPage">
                    <div class="letter-paper">
                        <div class="letter-header">
                            <div class="letter-decoration-top">✨ 💕 ✨</div>
                            <div class="letter-title">Untuk Sayangg Ku</div>
                            <div class="letter-subtitle">~ Selamatt Hari Valentine 🤍 ~</div>
                        </div>

                        <div class="letter-content">
                            <p>Sayanggg,</p>
                            
                            <p>Selamatt harii valentine yaaa 🤍 Makasiii banyakk udahh jadii bagian paling maniss di hari hari abanggg.</p>
                            
                            <p>Hadirr dedeee bikin abanggg ngerasaa lebihh tenangg, lebihh semangatt, dan lebihh mauu jadii versi terbaik dari diri abanggg. Abanggg senengg bangettt bisaa ketawaa, ceritaaa, dan lewatin banyakk hal barengg dedeee.</p>
                            
                            <p>Semogaa harii inii jadii pengingatt kalauu dedeee itu disayanggg, dihargaii, dan berartii. Abanggg doainn dedeee selaluu sehatt, ceriaa, dan dikelilingii hal hal baikk.</p>
                            
                            <p>Kitaa jalaninn hubungann inii pelann pelann, salingg jagaa, salingg ngertiin, dan salingg nguatiinn yaa. Terimakasii udahh tetappt milihh buat bertahan dan berusaha barengg.</p>
                            
                            <p>Abanggg sayanggg dedeee harii inii dan seterusnyaa 🤍</p>
                        </div>

                        <div class="dancing-emojis">
                            <span class="emoji-dance">🎉</span>
                            <span class="emoji-dance">🤍</span>
                            <span class="emoji-dance">💕</span>
                            <span class="emoji-dance">🎉</span>
                        </div>

                        <div class="letter-signature">
                            Dengan sepenuh hati,<br>
                            Abanggg 💕
                        </div>

                        <div class="letter-footer">
                            ✨ 💕 ✨
                        </div>

                        <!-- BUTTONS INSIDE LETTER -->
                        <div class="button-container">
                            <button class="btn btn-yes" id="yesBtn" onclick="handleYes()">❤️ Iyaaaaaaaaa<br>akuuuuuu mauuuu<br>bebeeeee!</button>
                            <button class="btn btn-no" id="noBtn" onclick="handleNo()">🤍 Maafff gaaa<br>duluuuu<br>bebeeeee!</button>
                        </div>
                    </div>
                </div>

                <!-- Envelope Bottom -->
                <div class="envelope-bottom"></div>
            </div>
        </div>
    </div>

    <script>
        const envelopeFlap = document.getElementById('envelopeFlap');
        const envelopeFront = document.getElementById('envelopeFront');
        const letterPage = document.getElementById('letterPage');
        const yesBtn = document.getElementById('yesBtn');
        const noBtn = document.getElementById('noBtn');

        function openEnvelope() {
            envelopeFlap.classList.add('open');
            envelopeFront.classList.add('hide');
            letterPage.classList.add('show');
        }

        function handleYes() {
            createConfetti(['💖', '💕', '🤍', '🎉', '✨', '💐', '🌹', '🎊', '💗', '💌', '😍', '🥰'], 80);

            setTimeout(() => {
                alert('🎉 IYAAAAAAAA!!!\n\nAbanggg sayanggg dedeee selamanyaaa!!! 💕✨🤍\n\nKitaa bakal indah2 aja bareng dedeee 💕');
            }, 500);
        }

        function handleNo() {
            yesBtn.classList.add('enlarge');
            createConfetti(['💋', '😘', '🤍', '💕', '✨', '🥺', '😘'], 60);

            setTimeout(() => {
                alert('🤭 Abanggg ngerti kok!\n\nTapi tombol YES-nya jadi lebih gede & lebih menarik.. nah gimana? 😘💕\n\nPasti dedeee bakal pilih YES kan? 🥺💕');
            }, 300);

            noBtn.disabled = true;
        }

        function createConfetti(colors, count) {
            for (let i = 0; i < count; i++) {
                const confetti = document.createElement('div');
                confetti.textContent = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.position = 'fixed';
                confetti.style.left = Math.random() * 100 + '%';
                confetti.style.top = '-30px';
                confetti.style.fontSize = Math.random() * 0.6 + 1.1 + 'em';
                confetti.style.pointerEvents = 'none';
                confetti.style.opacity = '1';
                confetti.style.animation = `fall ${2.5 + Math.random() * 2}s linear forwards`;
                document.body.appendChild(confetti);

                setTimeout(() => confetti.remove(), 4500);
            }
        }

        // Add fall animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes fall {
                to {
                    transform: translateY(120vh) rotate(720deg);
                    opacity: 0;
                }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
