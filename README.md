```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surat Cinta Untuk Dhiya Kinanti ❤️</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600;700&family=Poppins:wght@300;400;500;600;700&family=Sacramento&display=swap" rel="stylesheet">
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Canvas Confetti Library -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        rosepink: '#ff8fa3',
                        softpink: '#fff0f3',
                        deeprose: '#c9184a',
                        blush: '#ffb3c1',
                        gold: '#ffb703',
                    },
                    fontFamily: {
                        dancing: ['"Dancing Script"', 'cursive'],
                        sacramento: ['Sacramento', 'cursive'],
                        poppins: ['Poppins', 'sans-serif'],
                    }
                }
            }
        }
    </script>

    <style>
        /* Floating Heart Background Animation */
        @keyframes floatUp {
            0% { transform: translateY(0) rotate(0deg); opacity: 0.8; }
            50% { transform: translateY(-30px) rotate(15deg); opacity: 0.5; }
            100% { transform: translateY(-60px) rotate(-15deg); opacity: 0; }
        }

        @keyframes pulseGlow {
            0%, 100% { box-shadow: 0 0 15px rgba(201, 24, 74, 0.4); transform: scale(1); }
            50% { box-shadow: 0 0 25px rgba(201, 24, 74, 0.7); transform: scale(1.03); }
        }

        .floating-heart {
            position: absolute;
            animation: floatUp 4s ease-in-out infinite;
            pointer-events: none;
        }

        .pulse-btn {
            animation: pulseGlow 2s infinite;
        }

        .glass-card {
            background: rgba(255, 255, 255, 0.88);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 182, 193, 0.5);
        }

        /* Responsive Envelope CSS */
        .envelope-wrapper {
            perspective: 1000px;
        }

        .envelope {
            position: relative;
            width: 280px;
            height: 180px;
            background: #ffb3c1;
            border-bottom-left-radius: 12px;
            border-bottom-right-radius: 12px;
            box-shadow: 0 12px 28px rgba(201, 24, 74, 0.2);
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        @media (min-width: 640px) {
            .envelope {
                width: 320px;
                height: 200px;
            }
        }

        .envelope:hover {
            transform: translateY(-5px) scale(1.02);
        }

        .envelope-flap {
            position: absolute;
            top: 0;
            left: 0;
            width: 0;
            height: 0;
            border-left: 140px solid transparent;
            border-right: 140px solid transparent;
            border-top: 110px solid #ff8fa3;
            transform-origin: top;
            transition: transform 0.5s ease;
            z-index: 3;
        }

        @media (min-width: 640px) {
            .envelope-flap {
                border-left-width: 160px;
                border-right-width: 160px;
                border-top-width: 120px;
            }
        }

        .envelope.open .envelope-flap {
            transform: rotateX(180deg);
            z-index: 1;
        }

        .envelope-pocket {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 0;
            border-left: 140px solid #ffccd5;
            border-right: 140px solid #ffccd5;
            border-bottom: 100px solid #ffb3c1;
            border-bottom-left-radius: 12px;
            border-bottom-right-radius: 12px;
            z-index: 2;
        }

        @media (min-width: 640px) {
            .envelope-pocket {
                border-left-width: 160px;
                border-right-width: 160px;
                border-bottom-width: 110px;
            }
        }

        .letter-preview {
            position: absolute;
            bottom: 10px;
            left: 50%;
            transform: translateX(-50%);
            width: 85%;
            height: 80%;
            background: white;
            border-radius: 8px;
            padding: 10px;
            z-index: 2;
            transition: transform 0.5s ease;
            box-shadow: 0 -2px 10px rgba(0,0,0,0.05);
        }

        .envelope.open .letter-preview {
            transform: translateX(-50%) translateY(-60px);
        }

        .modal-transition {
            transition: all 0.35s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
    </style>
</head>
<body class="bg-gradient-to-br from-softpink via-pink-100 to-rose-200 min-h-screen font-poppins flex flex-col justify-between items-center relative overflow-x-hidden selection:bg-rosepink selection:text-white">

    <!-- Floating Background Decor -->
    <div id="floating-bg" class="fixed inset-0 pointer-events-none z-0"></div>

    <!-- Header Banner -->
    <header class="w-full text-center pt-8 pb-4 z-10 px-4">
        <span class="px-4 py-1.5 bg-rose-200/60 text-deeprose text-xs sm:text-sm rounded-full font-medium tracking-wide uppercase shadow-sm border border-rose-300/50 inline-flex items-center gap-1.5">
            <i class="fa-solid fa-heart text-xs text-deeprose"></i> Surat Spesial & Exclusive
        </span>
        <h1 class="font-dancing text-4xl sm:text-6xl text-deeprose font-bold mt-2 drop-shadow-sm">
            Untuk Dhiya Kinanti ❤️
        </h1>
        <p class="text-xs sm:text-sm text-gray-600 mt-1 font-light max-w-md mx-auto">
            Buka lembar demi lembar surat ini untuk menemukan pesan manis di setiap langkahnya...
        </p>
    </header>

    <!-- Main Content Area -->
    <main class="w-full max-w-lg px-4 my-auto flex flex-col items-center z-10">

        <!-- Progress Counter Display -->
        <div class="mb-6 text-center glass-card px-6 py-3 rounded-2xl shadow-md w-full border border-rose-200">
            <div class="flex justify-between items-center text-xs text-gray-500 mb-1 font-medium">
                <span>Perjalanan Surat Cinta</span>
                <span id="counter-text" class="text-deeprose font-bold text-sm">0 / 15 Surat</span>
            </div>
            <!-- Progress Bar -->
            <div class="w-full bg-rose-100 h-3 rounded-full overflow-hidden p-0.5 border border-rose-200">
                <div id="progress-bar" class="bg-gradient-to-r from-rosepink to-deeprose h-full rounded-full transition-all duration-500 ease-out" style="width: 0%"></div>
            </div>
            <p id="hint-text" class="text-xs text-rose-500 mt-2 italic font-dancing text-base sm:text-lg">
                "Klik amplop di bawah ini untuk mulai membuka surat..."
            </p>
        </div>

        <!-- Envelope Interactive Component -->
        <div class="envelope-wrapper my-4">
            <div id="envelope" class="envelope flex items-center justify-center">
                <div class="envelope-flap"></div>
                <div class="letter-preview flex flex-col justify-center items-center text-center p-2">
                    <i class="fa-solid fa-heart text-deeprose text-2xl mb-1 animate-bounce"></i>
                    <p id="letter-preview-title" class="font-dancing text-lg text-deeprose font-bold">Surat Ke-1</p>
                    <p class="text-[10px] text-gray-400">Klik untuk membuka</p>
                </div>
                <div class="envelope-pocket"></div>
                <!-- Wax Seal -->
                <div id="wax-seal" class="absolute z-10 w-12 h-12 bg-deeprose rounded-full flex items-center justify-center shadow-lg border-2 border-rose-300">
                    <i class="fa-solid fa-envelope-open text-gold text-xl"></i>
                </div>
            </div>
        </div>

        <!-- Action Button -->
        <button id="open-btn" onclick="openCurrentLetter()" class="mt-6 px-8 py-3.5 bg-gradient-to-r from-deeprose to-rosepink text-white font-semibold rounded-full shadow-lg hover:shadow-xl hover:scale-105 transition-all duration-300 pulse-btn flex items-center gap-2">
            <i class="fa-solid fa-envelope-open-text"></i>
            <span id="btn-label">Buka Surat Ke-1</span>
        </button>

    </main>

    <!-- Footer -->
    <footer class="w-full text-center py-4 text-xs text-gray-500 z-10">
        Dibuat khusus dengan <i class="fa-solid fa-heart text-deeprose"></i> hanya untuk Dhiya Kinanti
    </footer>

    <!-- POPUP MODAL FOR LETTERS -->
    <div id="letter-modal" class="fixed inset-0 bg-black/60 backdrop-blur-sm z-50 flex items-center justify-center p-4 hidden opacity-0 transition-opacity duration-300">
        <div id="modal-card" class="glass-card bg-white w-full max-w-md rounded-3xl p-6 sm:p-8 text-center shadow-2xl relative border-2 border-rose-200 modal-transition transform scale-90">
            
            <!-- Close Button (Visible for steps 1-14) -->
            <button id="close-modal-btn" onclick="closeLetterModal()" class="absolute top-4 right-4 w-9 h-9 bg-rose-100 hover:bg-rose-200 text-deeprose rounded-full flex items-center justify-center transition-colors">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>

            <!-- Heart Badge Header -->
            <div class="w-16 h-16 bg-rose-100 text-deeprose rounded-full flex items-center justify-center mx-auto mb-3 shadow-inner">
                <i id="modal-icon" class="fa-solid fa-heart-pulse text-3xl"></i>
            </div>

            <span id="modal-badge" class="px-3.5 py-1 bg-rose-100 text-deeprose text-xs font-semibold rounded-full uppercase tracking-wider">Surat Ke-1</span>
            
            <h2 id="modal-title" class="font-dancing text-3xl text-deeprose font-bold my-2">Pesan Spesial</h2>
            
            <!-- Message Content -->
            <div class="max-h-60 overflow-y-auto my-4 px-2 text-gray-700 leading-relaxed font-normal text-sm sm:text-base" id="modal-body">
                <!-- Injected via JavaScript -->
            </div>

            <!-- Interactivity Area for Step 15 (Do You Love Me Question) -->
            <div id="interactive-question-area" class="hidden mt-4 pt-4 border-t border-rose-100 relative">
                <p id="love-question" class="font-dancing text-3xl text-deeprose font-bold mb-5">Do you love me? ❤️</p>
                <div class="flex flex-row justify-center items-center gap-4 min-h-[70px] relative w-full" id="button-container">
                    <!-- YES Button -->
                    <button id="yes-btn" onclick="handleYesClick()" class="px-8 py-3 bg-gradient-to-r from-emerald-500 to-green-600 hover:from-emerald-600 hover:to-green-700 text-white font-bold rounded-full shadow-lg hover:scale-110 transition-all duration-300 z-20 flex items-center gap-2">
                        <i class="fa-solid fa-heart"></i> Yes! I Do ❤️
                    </button>
                    <!-- NO Button (Escapes on hover/touch) -->
                    <button id="no-btn" onmouseover="moveNoButton()" onclick="moveNoButton()" ontouchstart="moveNoButton()" class="px-6 py-3 bg-gray-400 hover:bg-gray-500 text-white font-bold rounded-full shadow transition-all duration-200 z-10 absolute sm:relative">
                        No 😜
                    </button>
                </div>
            </div>

            <!-- Continue Button for standard steps -->
            <button id="modal-next-btn" onclick="closeLetterModal()" class="w-full mt-3 py-3 bg-deeprose hover:bg-rose-700 text-white font-medium rounded-xl shadow-md transition-all duration-200">
                Lanjutkan Perjalanan <i class="fa-solid fa-arrow-right ml-1"></i>
            </button>
        </div>
    </div>

    <!-- FINAL CELEBRATION MODAL -->
    <div id="celebration-modal" class="fixed inset-0 bg-rose-950/80 backdrop-blur-md z-50 flex items-center justify-center p-4 hidden opacity-0 transition-opacity duration-500">
        <div class="bg-white/95 w-full max-w-lg rounded-3xl p-6 sm:p-10 text-center shadow-2xl relative border-4 border-rose-300 overflow-hidden">
            
            <div class="inline-block p-4 bg-rose-100 rounded-full text-deeprose mb-4 animate-bounce">
                <i class="fa-solid fa-crown text-4xl"></i>
            </div>

            <h1 class="font-dancing text-4xl sm:text-5xl text-deeprose font-extrabold mb-2">I love you sayang ❤️</h1>
            <p class="text-rose-500 font-semibold text-sm sm:text-base mb-6">Makasih banyak ya sudah selalu membuka hatimu untukku!</p>

            <div class="bg-rose-50/90 p-5 rounded-2xl border border-rose-200 text-left space-y-3 mb-6 text-xs sm:text-sm text-gray-700 leading-relaxed shadow-inner">
                <p><strong>Dearest Dhiya Kinanti,</strong></p>
                <p>Terima kasih sudah sabar membuka surat demi surat dari ke-1 hingga ke-15 ini. Kamu adalah kebahagiaan terindah dan alasan terbaik di balik senyumku setiap hari.</p>
                <p>Aku berjanji akan selalu ada untukmu, mencintaimu dengan tulus, dan membuat setiap harimu dipenuhi kehangatan.</p>
                <p class="font-sacramento text-2xl text-deeprose text-right font-bold pt-2">- Cintamu Selamanya -</p>
            </div>

            <button onclick="restartJourney()" class="px-8 py-3 bg-gradient-to-r from-deeprose to-rosepink hover:from-rose-700 hover:to-rose-500 text-white font-bold rounded-full shadow-lg hover:scale-105 transition-all duration-300">
                <i class="fa-solid fa-rotate-right mr-2"></i> Baca Lagi Dari Awal
            </button>
        </div>
    </div>

    <!-- JavaScript Application Logic -->
    <script>
        // Array of 15 Letters tailored specifically for Dhiya Kinanti
        const romanticLetters = [
            {
                step: 1,
                badge: "Surat Ke-1",
                title: "Awal Dari Cerita",
                body: "Halo Dhiya Kinanti manis... Selamat datang di surat interaktif kecil yang sengaja kubuat khusus untukmu. Ada 15 lembar ungkapan rasa di sini. Buka satu per satu ya sayang..."
            },
            {
                step: 2,
                badge: "Surat Ke-2",
                title: "Senyumanmu",
                body: "Tahu gak? Setiap kali aku teringat senyumanmu, hariku yang rasanya biasa saja langsung berubah jadi penuh warna dan ceria."
            },
            {
                step: 3,
                badge: "Surat Ke-3",
                title: "Sosok Istimewa",
                body: "Dhiya Kinanti itu sosok yang sangat luar biasa. Kebaikanmu, tawamu, dan caramu memperlakukanku selalu bikin aku kagum."
            },
            {
                step: 4,
                badge: "Surat Ke-4",
                title: "Rasa Syukur",
                body: "Aku selalu bersyukur bisa mengenal kamu dalam hidup ini. Kehadiranmu membawa ketenangan yang gak pernah kurasakan sebelumnya."
            },
            {
                step: 5,
                badge: "Surat Ke-5 🌟",
                title: "Pesan Khusus!",
                body: "<div class='p-3 bg-rose-50 border border-rose-200 rounded-xl mb-3'><span class='text-deeprose font-bold block text-center text-base sm:text-lg'>Semangat ya, sedikit lagi... Buka terus sampai akhir ya manis! ✨</span></div>Kamu hebat udah sampai di surat ke-5! Perjalanan kita masih berlanjut, terus klik ya sayang..."
            },
            {
                step: 6,
                badge: "Surat Ke-6",
                title: "Kenangan Manis",
                body: "Setiap momen bersamamu selalu tersimpan rapi di hatiku. Rasanya waktu berputar terlalu cepat kalau aku lagi sama kamu."
            },
            {
                step: 7,
                badge: "Surat Ke-7",
                title: "Rumah Untuk Hati",
                body: "Di dunia yang begitu ramai ini, menemukan kamu rasanya seperti akhirnya menemukan tempat pulang yang paling tenang dan hangat."
            },
            {
                step: 8,
                badge: "Surat Ke-8",
                title: "Selalu Mengagumimu",
                body: "Setiap hari aku selalu menemukan alasan baru untuk makin menyayangi Dhiya Kinanti. Gak ada habisnya hal manis di dalam dirimu."
            },
            {
                step: 9,
                badge: "Surat Ke-9",
                title: "Penyemangat Hariku",
                body: "Saat hariku terasa lelah atau berat, cukup dengan melihat senyummu atau mendengar kabarmu, semua rasa lelahku langsung hilang."
            },
            {
                step: 10,
                badge: "Surat Ke-10 💖",
                title: "Pesan Khusus!",
                body: "<div class='p-3 bg-rose-50 border border-rose-200 rounded-xl mb-3'><span class='text-deeprose font-bold block text-center text-base sm:text-lg'>Dikit lagi nih sayang, tahan bentar lagi ya... 🌸</span></div>Wah, udah surat ke-10! Sebentar lagi kamu akan sampai di puncak kejutan ini. Lanjut klik lagi yuk!"
            },
            {
                step: 11,
                badge: "Surat Ke-11",
                title: "Masa Depan",
                body: "Aku selalu berharap bisa terus ada di setiap langkahmu. Menemanimu tumbuh, tertawa bersama, dan saling melengkapi."
            },
            {
                step: 12,
                badge: "Surat Ke-12",
                title: "Ketulusan Cinta",
                body: "Cinta yang kurasakan untukmu itu murni dan tulus. Kamu adalah bagian terindah di dalam hidupku, Dhiya."
            },
            {
                step: 13,
                badge: "Surat Ke-13",
                title: "Hampir Sampai",
                body: "Hampir sampai di surat terakhir! Terima kasih ya sudah dengan sabar membuka lembar demi lembar ungkapan hatiku ini."
            },
            {
                step: 14,
                badge: "Surat Ke-14",
                title: "Satu Langkah Lagi",
                body: "Ini surat ke-14, tepat sebelum pertanyaan yang paling penting. Siapkan hatimu ya cantik..."
            },
            {
                step: 15,
                badge: "Surat Ke-15 ❤️",
                title: "Pertanyaan Dari Hatiku",
                body: "Untuk Dhiya Kinanti tersayang...\n\nKita sudah membaca 14 lembar surat ini. Dan sekarang, di lembar ke-15 yang terakhir ini, aku ingin bertanya satu hal yang paling tulus dari lubuk hatiku..."
            }
        ];

        // State variables
        let currentStep = 0;
        const totalSteps = 15;
        let noBtnEscapeCount = 0;

        // DOM elements
        const envelope = document.getElementById('envelope');
        const counterText = document.getElementById('counter-text');
        const progressBar = document.getElementById('progress-bar');
        const hintText = document.getElementById('hint-text');
        const btnLabel = document.getElementById('btn-label');
        const letterPreviewTitle = document.getElementById('letter-preview-title');
        
        // Modal elements
        const letterModal = document.getElementById('letter-modal');
        const modalCard = document.getElementById('modal-card');
        const modalBadge = document.getElementById('modal-badge');
        const modalTitle = document.getElementById('modal-title');
        const modalBody = document.getElementById('modal-body');
        const modalNextBtn = document.getElementById('modal-next-btn');
        const closeModalBtn = document.getElementById('close-modal-btn');
        const interactiveQuestionArea = document.getElementById('interactive-question-area');
        const noBtn = document.getElementById('no-btn');
        const yesBtn = document.getElementById('yes-btn');
        const celebrationModal = document.getElementById('celebration-modal');

        // Floating Hearts Setup
        function createFloatingHearts() {
            const container = document.getElementById('floating-bg');
            const heartIcons = ['fa-heart', 'fa-heart-pulse', 'fa-sparkles', 'fa-heart text-pink-300'];
            
            for (let i = 0; i < 18; i++) {
                const heart = document.createElement('i');
                const randomIcon = heartIcons[Math.floor(Math.random() * heartIcons.length)];
                heart.className = `fa-solid ${randomIcon} floating-heart text-rosepink/40 text-sm sm:text-xl`;
                heart.style.left = `${Math.random() * 100}%`;
                heart.style.top = `${Math.random() * 100}%`;
                heart.style.animationDelay = `${Math.random() * 4}s`;
                heart.style.animationDuration = `${3 + Math.random() * 4}s`;
                container.appendChild(heart);
            }
        }

        // Open Current Letter Action
        function openCurrentLetter() {
            if (currentStep < totalSteps) {
                currentStep++;
            }

            envelope.classList.add('open');

            setTimeout(() => {
                showLetterModal(currentStep);
            }, 350);
        }

        // Display Modal with Content based on step
        function showLetterModal(stepIndex) {
            const letterData = romanticLetters[stepIndex - 1];

            modalBadge.innerText = letterData.badge;
            modalTitle.innerText = letterData.title;
            modalBody.innerHTML = letterData.body.replace(/\n/g, '<br>');

            // Step 15 Specific Logic (Do You Love Me Question)
            if (stepIndex === 15) {
                interactiveQuestionArea.classList.remove('hidden');
                modalNextBtn.classList.add('hidden');
                closeModalBtn.classList.add('hidden'); // Force user to choose Yes
                
                // Reset No Button position
                noBtn.style.position = 'relative';
                noBtn.style.left = '0px';
                noBtn.style.top = '0px';
                noBtn.style.transform = 'scale(1)';
                noBtnEscapeCount = 0;
            } else {
                interactiveQuestionArea.classList.add('hidden');
                modalNextBtn.classList.remove('hidden');
                closeModalBtn.classList.remove('hidden');
            }

            // Animate Modal Show
            letterModal.classList.remove('hidden');
            setTimeout(() => {
                letterModal.classList.remove('opacity-0');
                modalCard.classList.remove('scale-90');
                modalCard.classList.add('scale-100');
            }, 10);

            updateUI();
        }

        // Close Modal
        function closeLetterModal() {
            letterModal.classList.add('opacity-0');
            modalCard.classList.remove('scale-100');
            modalCard.classList.add('scale-90');

            setTimeout(() => {
                letterModal.classList.add('hidden');
                envelope.classList.remove('open');
            }, 300);
        }

        // Update UI Counter and Hints
        function updateUI() {
            counterText.innerText = `${currentStep} / ${totalSteps} Surat`;
            const percentage = (currentStep / totalSteps) * 100;
            progressBar.style.width = `${percentage}%`;

            if (currentStep < totalSteps) {
                const nextStep = currentStep + 1;
                btnLabel.innerText = `Buka Surat Ke-${nextStep}`;
                letterPreviewTitle.innerText = `Surat Ke-${nextStep}`;
            } else {
                btnLabel.innerText = `Lihat Surat Ke-15 ❤️`;
                letterPreviewTitle.innerText = `Surat Ke-15 ❤️`;
            }

            // Hints
            if (currentStep === 0) {
                hintText.innerText = `"Klik tombol atau amplop untuk mulai..."`;
            } else if (currentStep < 5) {
                hintText.innerText = `"Terus buka ya manis, masih banyak kejutan di dalam..."`;
            } else if (currentStep >= 5 && currentStep < 10) {
                hintText.innerText = `"Semangat ya, sedikit lagi... Buka terus sampai akhir ya manis!"`;
            } else if (currentStep >= 10 && currentStep < 15) {
                hintText.innerText = `"Dikit lagi nih sayang, tahan bentar lagi ya..."`;
            } else if (currentStep === 15) {
                hintText.innerText = `"Ini surat terakhir! Temukan pertanyaan dari hatiku..."`;
            }
        }

        // Playful NO Button Escape Logic
        function moveNoButton() {
            noBtnEscapeCount++;

            // Shrink button slightly on each escape
            const currentScale = Math.max(0.35, 1 - (noBtnEscapeCount * 0.12));
            
            const container = document.getElementById('button-container');
            const containerRect = container.getBoundingClientRect();
            
            // Random offset values away from original location
            const x = (Math.random() - 0.5) * (containerRect.width * 1.4);
            const y = (Math.random() - 0.5) * 120;

            noBtn.style.position = 'absolute';
            noBtn.style.transition = 'all 0.2s cubic-bezier(0.1, 0.8, 0.3, 1)';
            noBtn.style.left = `${x}px`;
            noBtn.style.top = `${y}px`;
            noBtn.style.transform = `scale(${currentScale})`;

            if (noBtnEscapeCount > 10) {
                noBtn.style.display = 'none'; // Disappear if tried too many times
            }
        }

        // YES Button Click Handler
        function handleYesClick() {
            closeLetterModal();
            triggerConfetti();

            setTimeout(() => {
                celebrationModal.classList.remove('hidden');
                setTimeout(() => {
                    celebrationModal.classList.remove('opacity-0');
                }, 10);
            }, 350);
        }

        // Confetti Celebration Effects
        function triggerConfetti() {
            const count = 200;
            const defaults = { origin: { y: 0.7 } };

            function fire(particleRatio, opts) {
                confetti(Object.assign({}, defaults, opts, {
                    particleCount: Math.floor(count * particleRatio)
                }));
            }

            fire(0.25, { spread: 26, startVelocity: 55, colors: ['#ff8fa3', '#c9184a', '#ffb3c1'] });
            fire(0.2, { spread: 60, colors: ['#ffffff', '#ffb703', '#ff8fa3'] });
            fire(0.35, { spread: 100, decay: 0.91, scalar: 0.8 });
            fire(0.1, { spread: 120, startVelocity: 25, decay: 0.92, colors: ['#e63946', '#ffb3c1'] });
            fire(0.1, { spread: 120, startVelocity: 45 });
        }

        // Reset journey
        function restartJourney() {
            celebrationModal.classList.add('opacity-0');
            setTimeout(() => {
                celebrationModal.classList.add('hidden');
                currentStep = 0;
                noBtn.style.display = 'inline-block';
                noBtn.style.opacity = '1';
                updateUI();
            }, 300);
        }

        // Click on envelope triggers opening
        envelope.addEventListener('click', () => {
            openCurrentLetter();
        });

        // Initialize on load
        window.onload = function() {
            createFloatingHearts();
            updateUI();
        };
    </script>
</body>
</html>
```
