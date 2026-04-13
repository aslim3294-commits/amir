# amir
science<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>عالم العلوم والرياضيات | تعلم واستمتع</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Tahoma', 'Cairo', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #e9edf2 100%);
            color: #1e2a3a;
            line-height: 1.6;
        }

        nav {
            background: linear-gradient(90deg, #1e3c72, #2a5298);
            color: white;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            background: rgba(255,255,255,0.2);
            padding: 0.3rem 1rem;
            border-radius: 40px;
            cursor: pointer;
        }

        .nav-links {
            display: flex;
            gap: 1.5rem;
            flex-wrap: wrap;
        }

        .nav-links button {
            background: none;
            border: none;
            color: white;
            font-size: 1.1rem;
            cursor: pointer;
            padding: 0.5rem 1rem;
            border-radius: 30px;
            transition: all 0.3s;
            font-weight: bold;
        }

        .nav-links button:hover {
            background: rgba(255,255,255,0.25);
            transform: scale(1.05);
        }

        .container {
            max-width: 1300px;
            margin: 2rem auto;
            padding: 0 2rem;
        }

        .subjects {
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
            margin-bottom: 3rem;
        }

        .card {
            background: white;
            border-radius: 30px;
            padding: 1.5rem;
            width: 220px;
            text-align: center;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 30px rgba(0,0,0,0.15);
        }

        .card-icon {
            font-size: 4rem;
            margin-bottom: 1rem;
        }

        .card h3 {
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
        }

        .math { border-bottom: 8px solid #f39c12; }
        .physics { border-bottom: 8px solid #3498db; }
        .science { border-bottom: 8px solid #2ecc71; }

        .content-area {
            background: white;
            border-radius: 40px;
            padding: 2rem;
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
            margin-bottom: 2rem;
            min-height: 500px;
            transition: all 0.3s;
        }

        .level-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin: 1.5rem 0;
            flex-wrap: wrap;
        }

        .level-btn {
            background: #ecf0f1;
            border: none;
            padding: 0.7rem 1.8rem;
            border-radius: 50px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            transition: 0.2s;
        }

        .level-btn.active {
            background: #2a5298;
            color: white;
            box-shadow: 0 4px 10px rgba(42,82,152,0.4);
        }

        .lesson-card {
            background: #f8faff;
            border-radius: 30px;
            padding: 1.5rem;
            margin: 1rem 0;
            border-right: 10px solid #2a5298;
        }

        .fun-fact {
            background: #fff3e0;
            border-radius: 25px;
            padding: 1rem;
            margin: 1rem 0;
            display: flex;
            align-items: center;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .game-area {
            background: #eef2ff;
            border-radius: 30px;
            padding: 1.5rem;
            margin-top: 1.5rem;
            text-align: center;
        }

        button {
            background: #2a5298;
            color: white;
            border: none;
            padding: 0.6rem 1.2rem;
            border-radius: 40px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: 0.2s;
        }

        button:hover {
            background: #1e3c72;
            transform: scale(1.02);
        }

        .quiz-option {
            background: white;
            margin: 0.5rem auto;
            padding: 0.7rem;
            border-radius: 60px;
            cursor: pointer;
            border: 1px solid #ccc;
            width: 80%;
            transition: all 0.2s;
        }
        .quiz-option:hover {
            background: #d4e0ff;
            transform: scale(1.02);
        }

        .score-board {
            background: gold;
            color: #1e3c72;
            padding: 0.5rem 1rem;
            border-radius: 40px;
            display: inline-block;
            font-weight: bold;
            margin-bottom: 1rem;
        }

        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-5px); }
            75% { transform: translateX(5px); }
        }
        .shake-animation {
            animation: shake 0.3s ease-in-out;
        }
        @keyframes bounce {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
        .bounce-animation {
            animation: bounce 0.3s ease;
        }

        footer {
            text-align: center;
            padding: 2rem;
            background: #1e2a3a;
            color: white;
            margin-top: 2rem;
        }

        @media (max-width: 700px) {
            .container { padding: 0 1rem; }
            .card { width: 160px; }
            .card-icon { font-size: 2.5rem; }
            .quiz-option { width: 95%; }
        }
    </style>
</head>
<body>

<nav>
    <div class="logo" id="homeBtn">🔬🧪 عالم العلوم</div>
    <div class="nav-links">
        <button data-subject="math">📐 رياضيات</button>
        <button data-subject="physics">⚡ فيزياء</button>
        <button data-subject="science">🌿 علوم طبيعية</button>
        <button id="gameNavBtn">🎮 ألعاب ومرح</button>
    </div>
</nav>

<div class="container">
    <div class="subjects">
        <div class="card math" data-subject="math">
            <div class="card-icon">📐</div>
            <h3>رياضيات</h3>
            <p>من الجبر إلى التفاضل</p>
        </div>
        <div class="card physics" data-subject="physics">
            <div class="card-icon">⚡</div>
            <h3>فيزياء</h3>
            <p>قوانين الطبيعة</p>
        </div>
        <div class="card science" data-subject="science">
            <div class="card-icon">🧬</div>
            <h3>علوم طبيعية</h3>
            <p>الأرض والحياة</p>
        </div>
    </div>

    <div class="content-area" id="dynamicContent">
        <h2 style="text-align:center;">✨ مرحباً في رحلة العلم ✨</h2>
        <p style="text-align:center; font-size:1.2rem;">اختر مادة أو اذهب إلى الألعاب ... تعلم واستمتع!</p>
        <div style="text-align:center; margin-top:20px;">
            <button id="startGameQuick">🎲 العب مسابقة سريعة الآن</button>
        </div>
    </div>
</div>

<footer>
    <p>📚 موقع تعليمي تفاعلي | أسئلة متجددة بعد كل إجابة | مرحلة متوسطة وثانوية | للأعمار 11-22 سنة</p>
</footer>

<script>
    // البيانات: الدروس حسب المادة والمستوى
    const lessonsData = {
        math: {
            middle: [
                { title: "📌 المعادلات البسيطة", content: "حل معادلات من الدرجة الأولى: س + 5 = 12 → س = 7. مثال: 3س - 4 = 11 → 3س = 15 → س = 5." },
                { title: "📌 النسب المئوية", content: "النسبة المئوية تعني الجزء من 100. مثال: 20% من 80 = (20/100)*80 = 16." },
                { title: "🧩 الهندسة: مساحة المربع", content: "مساحة المربع = طول الضلع × نفسه. إذا كان الضلع = 4 سم، المساحة = 16 سم²." }
            ],
            high: [
                { title: "📈 الدوال الخطية", content: "الدالة الخطية: ص = أ س + ب. ميل الخط = أ. مثال: ص = 2س + 1 ميله 2." },
                { title: "🧮 التفاضل basics", content: "مشتقة الدالة: مشتقة سⁿ = ن·سⁿ⁻¹. مثال: مشتقة س² = 2س." },
                { title: "🔢 المتتاليات الحسابية", content: "حدود متتالية حسابية: حن = ح1 + (ن-1)د. مثال: 3, 7, 11, ... الأساس د=4." }
            ]
        },
        physics: {
            middle: [
                { title: "⚡ الحركة والسرعة", content: "السرعة = المسافة / الزمن. إذا قطعت 100 متر في 20 ثانية، السرعة = 5 م/ث." },
                { title: "💡 الضوء", content: "الضوء ينتقل في خطوط مستقيمة، سرعته 300 ألف كم/ث تقريباً." },
                { title: "🧲 المغناطيسية", content: "للمغناطيس قطب شمالي وجنوبي، الأقطاب المتشابهة تتنافر والمختلفة تتجاذب." }
            ],
            high: [
                { title: "🏎️ قوانين نيوتن", content: "القانون الثاني: القوة = الكتلة × التسارع (ق = ك × ت)." },
                { title: "⚛️ الكهرباء", content: "قانون أوم: الجهد = التيار × المقاومة (ج = ت × م)." },
                { title: "🌊 الموجات", content: "الطول الموجي × التردد = سرعة الموجة. الموجات الصوتية تحتاج لوسط." }
            ]
        },
        science: {
            middle: [
                { title: "🌱 الخلية النباتية", content: "تحتوي على جدار خلوي، بلاستيدات خضراء، فجوة عصارية كبيرة." },
                { title: "🦴 الجهاز الهيكلي", content: "يتكون من 206 عظمة، يحمي الأعضاء ويساعد على الحركة." },
                { title: "🌍 طبقات الأرض", content: "القشرة، الستار، اللب الخارجي، اللب الداخلي." }
            ],
            high: [
                { title: "🧬 DNA", content: "الحمض النووي يحمل الشفرة الوراثية، يتكون من قواعد A,T,C,G." },
                { title: "⚖️ التوازن البيئي", content: "السلاسل الغذائية: منتجون، مستهلكون، محللون." },
                { title: "🔬 الانقسام الميتوزي", content: "ينتج خليتين متطابقتين، يستخدم للنمو والتعويض." }
            ]
        }
    };

    const funFacts = [
        "🐙 الأخطبوط له ثلاثة قلوب!", "🌌 ملعقة صغيرة من نجم النيوترون تزن مليار طن.",
        "🧠 الدماغ البشري يولد كهرباء تكفي لتشغيل لمبة.", "🐜 النمل لا ينام أبداً!",
        "🍕 البيتزا جاءت من إيطاليا لكن المصريين القدامى صنعوا خبزاً بالجبن.",
        "🎈 الهيليوم أخف من الهواء.", "🦒 قلب الزرافة طوله 60 سم!", "🌊 المحيط يحتوي على 20 مليون طن من الذهب."
    ];

    let currentSubject = "math";
    let currentLevel = "middle";
    let userScore = 0;  // نقاط المتعة

    const dynamicDiv = document.getElementById("dynamicContent");
    const homeBtn = document.getElementById("homeBtn");
    const gameNavBtn = document.getElementById("gameNavBtn");

    // مكتبة الأسئلة الغنية (تتغير تلقائياً)
    const bigQuestionBank = {
        math_middle: [
            { q: "ما ناتج 25 × 4 ؟", options: ["80", "100", "90", "110"], correct: "100" },
            { q: "إذا كان س + 9 = 20 ، فما قيمة س؟", options: ["9", "10", "11", "12"], correct: "11" },
            { q: "مساحة مستطيل طوله 10 سم وعرضه 4 سم؟", options: ["40 سم²", "14 سم²", "44 سم²", "20 سم²"], correct: "40 سم²" },
            { q: "ما هو العدد الأولي من بين الأعداد؟", options: ["21", "33", "17", "27"], correct: "17" },
            { q: "ناتج 144 ÷ 12 ؟", options: ["10", "11", "12", "13"], correct: "12" }
        ],
        math_high: [
            { q: "مشتقة الدالة س⁴ هي ؟", options: ["4س³", "س³", "3س⁴", "4س⁵"], correct: "4س³" },
            { q: "إذا كانت د(س)= 3س+2 ، فما قيمة د(5)؟", options: ["15", "17", "20", "13"], correct: "17" },
            { q: "ما قيمة لوغاريتم 1000 للأساس 10 ؟", options: ["1", "2", "3", "4"], correct: "3" },
            { q: "حل المعادلة 2س - 5 = 9", options: ["7", "8", "6", "5"], correct: "7" },
            { q: "إذا كان الميل = 2 ونقطة (0,3) فأوجد معادلة الخط", options: ["ص=2س+3", "ص=3س+2", "ص=2س-3", "ص=س+2"], correct: "ص=2س+3" }
        ],
        physics_middle: [
            { q: "وحدة قياس السرعة هي ؟", options: ["متر", "ثانية", "متر/ثانية", "كجم"], correct: "متر/ثانية" },
            { q: "القوة التي تجذب الأجسام نحو الأرض تسمى؟", options: ["المغناطيسية", "الجاذبية", "الاحتكاك", "الشد"], correct: "الجاذبية" },
            { q: "أي من هذه مواد عازلة للكهرباء؟", options: ["نحاس", "حديد", "مطاط", "فضة"], correct: "مطاط" },
            { q: "جهاز يستخدم لقياس التيار الكهربائي؟", options: ["فولتميتر", "أميتر", "أوميتر", "بارومتر"], correct: "أميتر" }
        ],
        physics_high: [
            { q: "قانون نيوتن الثاني ينص على أن القوة = .... ؟", options: ["الكتلة × التسارع", "الكتلة / التسارع", "السرعة × الزمن", "العمل / الزمن"], correct: "الكتلة × التسارع" },
            { q: "وحدة قياس المقاومة الكهربائية؟", options: ["فولت", "أمبير", "أوم", "وات"], correct: "أوم" },
            { q: "سرعة الضوء في الفراغ تقارب؟", options: ["300,000 كم/ث", "150,000 كم/ث", "3,000 كم/ث", "30,000 كم/ث"], correct: "300,000 كم/ث" },
            { q: "طاقة الوضع تعتمد على ...", options: ["السرعة", "الارتفاع", "الكتلة فقط", "الحرارة"], correct: "الارتفاع" }
        ],
        science_middle: [
            { q: "أي عضو يقوم بضخ الدم؟", options: ["الرئة", "الكبد", "القلب", "المعدة"], correct: "القلب" },
            { q: "النباتات تصنع غذاءها بواسطة عملية؟", options: ["التنفس", "البناء الضوئي", "الهضم", "التخمر"], correct: "البناء الضوئي" },
            { q: "أكبر كوكب في المجموعة الشمسية؟", options: ["المريخ", "زحل", "المشتري", "الأرض"], correct: "المشتري" }
        ],
        science_high: [
            { q: "ما اسم الحمض النووي الذي يحمل الشفرة الوراثية؟", options: ["RNA", "DNA", "بروتين", "إنزيم"], correct: "DNA" },
            { q: "الخلايا التي تنقل السيالات العصبية تسمى؟", options: ["خلايا دهنية", "خلايا عصبية", "خلايا دم حمراء", "خلايا عضلية"], correct: "خلايا عصبية" },
            { q: "أي عضو مسؤول عن تنقية الدم في جسم الإنسان؟", options: ["القلب", "الرئتين", "الكليتين", "البنكرياس"], correct: "الكليتين" },
            { q: "الميتوكوندريا وظيفتها إنتاج ...", options: ["بروتين", "طاقة (ATP)", "DNA", "إنزيمات"], correct: "طاقة (ATP)" }
        ]
    };

    function getRandomQuestion() {
        const key = `${currentSubject}_${currentLevel}`;
        let bank = bigQuestionBank[key];
        if (!bank) bank = bigQuestionBank.math_middle;
        const randomIndex = Math.floor(Math.random() * bank.length);
        return { ...bank[randomIndex] };
    }

    let currentQuestionObj = null;

    function updateScoreUI() {
        const scoreSpan = document.getElementById("liveScore");
        if (scoreSpan) scoreSpan.innerText = userScore;
    }

    function showFunMessage(correct) {
        const messages = {
            correct: ["🎉 ممتاز! 🎉", "💪 أذكى طالب! 💪", "🧠 عبقري! 🧠", "🌟 رائع جداً! 🌟", "🏆 إجابة صحيحة! 🏆"],
            wrong: ["😅 حاول مرة أخرى!", "📚 راجع الدرس ثم عاود المحاولة", "🤔 ليس هذه المرة...下次更好", "💡 فكرة: اقرأ الدرس جيداً", "🌟 لا تيأس! السؤال القادم أسهل"]
        };
        const arr = correct ? messages.correct : messages.wrong;
        return arr[Math.floor(Math.random() * arr.length)];
    }

    function animateElement(element, animationClass) {
        if (!element) return;
        element.classList.add(animationClass);
        setTimeout(() => element.classList.remove(animationClass), 400);
    }

    function generateNewQuiz() {
        currentQuestionObj = getRandomQuestion();
        const quizContainer = document.getElementById("dynamicQuizContainer");
        if (!quizContainer) return;
        let quizHtml = `<h3>🎯 اختبر معلوماتك (تتجدد الأسئلة تلقائياً)</h3>
                        <div style="margin:15px 0;"><strong>❓ ${currentQuestionObj.q}</strong></div>`;
        currentQuestionObj.options.forEach(opt => {
            quizHtml += `<div class="quiz-option" data-answer="${opt}">🔹 ${opt}</div>`;
        });
        quizHtml += `<div id="quizFeedback" style="margin-top:10px; font-weight:bold;"></div>`;
        quizContainer.innerHTML = quizHtml;

        // إضافة حدث لكل خيار
        document.querySelectorAll('.quiz-option').forEach(optDiv => {
            optDiv.addEventListener('click', (e) => {
                const selected = optDiv.getAttribute('data-answer');
                const feedbackDiv = document.getElementById("quizFeedback");
                const isCorrect = (selected === currentQuestionObj.correct);
                
                if (isCorrect) {
                    userScore += 10;
                    feedbackDiv.innerHTML = `✅ ${showFunMessage(true)} +10 نقاط 🎊`;
                    feedbackDiv.style.color = "green";
                    animateElement(optDiv, "bounce-animation");
                    // تأثير احتفالي
                    const contentArea = document.querySelector('.content-area');
                    animateElement(contentArea, "bounce-animation");
                } else {
                    userScore = Math.max(0, userScore - 5);
                    feedbackDiv.innerHTML = `❌ ${showFunMessage(false)} الإجابة الصحيحة: ${currentQuestionObj.correct}. -5 نقاط 😊`;
                    feedbackDiv.style.color = "#c0392b";
                    animateElement(optDiv, "shake-animation");
                }
                updateScoreUI();
                // إظهار حقيقة ممتعة سريعة بعد الإجابة
                const randomFact = funFacts[Math.floor(Math.random() * funFacts.length)];
                const factDiv = document.getElementById("dynamicFactDisplay");
                if (factDiv) factDiv.innerHTML = `💡 ${randomFact}`;
                // تغيير السؤال بعد ثانية ونصف
                setTimeout(() => {
                    generateNewQuiz();
                }, 1500);
                // تعطيل النقر أثناء التحميل
                document.querySelectorAll('.quiz-option').forEach(opt => opt.style.pointerEvents = "none");
                setTimeout(() => {
                    if(document.querySelectorAll('.quiz-option')) 
                        document.querySelectorAll('.quiz-option').forEach(opt => opt.style.pointerEvents = "auto");
                }, 1400);
            });
        });
    }

    function renderSubject(subject, level) {
        currentSubject = subject;
        currentLevel = level;
        const data = lessonsData[subject];
        if (!data) return;
        const lessons = data[level];
        let html = `<div style="text-align:center;">
                        <h2>📘 ${subject === 'math' ? 'الرياضيات' : subject === 'physics' ? 'الفيزياء' : 'العلوم الطبيعية'}</h2>
                        <div class="score-board">🏆 نقاطك: <span id="liveScore">${userScore}</span> 🏆</div>
                    </div>`;
        html += `<div class="level-buttons">
                    <button class="level-btn ${level === 'middle' ? 'active' : ''}" data-level="middle">📖 المتوسط (11-15 سنة)</button>
                    <button class="level-btn ${level === 'high' ? 'active' : ''}" data-level="high">🚀 الثانوي (16-22 سنة)</button>
                 </div>`;
        html += `<div>`;
        lessons.forEach(lesson => {
            html += `<div class="lesson-card">
                        <h3>${lesson.title}</h3>
                        <p>${lesson.content}</p>
                    </div>`;
        });        
        const randomFact = funFacts[Math.floor(Math.random() * funFacts.length)];
        html += `<div class="fun-fact" id="dynamicFactDisplay">💡 <strong>هل تعلم؟</strong> ${randomFact}</div>`;
        html += `<div class="game-area" id="dynamicQuizContainer">
                    <!-- سيتم وضع السؤال المتجدد هنا -->
                </div>`;
        html += `</div>`;
        dynamicDiv.innerHTML = html;
        
        // إضافة حدث أزرار المستوى
        document.querySelectorAll('.level-btn').forEach(btn => {
            btn.addEventListener('click', (e) => {
                const newLevel = btn.getAttribute('data-level');
                renderSubject(currentSubject, newLevel);
            });
        });
        // بدء الأسئلة المتجددة
        generateNewQuiz();
        updateScoreUI();
    }

    // صفحة الألعاب الإضافية
    function showGamePage() {
        let gameHtml = `
            <h2 style="text-align:center;">🎮 ركن المرح والتحدي 🎲</h2>
            <p style="text-align:center;">ألعاب ذهنية ومسابقات لتستمتع أثناء التعلم!</p>
            <div class="score-board" style="margin-bottom:20px;">🏆 نقاطك: <span id="liveScoreGame">${userScore}</span> 🏆</div>
            <div class="game-area">
                <h3>🧠 تحدي الحساب السريع 🧠</h3>
                <div id="mathGame">
                    <p id="questionGame">اضغط "سؤال جديد" للبدء</p>
                    <input type="number" id="answerInput" placeholder="اكتب إجابتك" style="padding:10px; border-radius:40px; margin:10px; width:150px;">
                    <button id="checkAnswer">تأكيد</button>
                    <button id="newMathQuestion">➕ سؤال جديد</button>
                    <p id="gameFeedback"></p>
                </div>
            </div>
            <div class="game-area">
                <h3>🎲 لحظة مرح: حقائق عجيبة</h3>
                <p id="randomFunFactDisplay">${funFacts[Math.floor(Math.random() * funFacts.length)]}</p>
                <button id="newFactBtn">✨ حقيقة جديدة</button>
            </div>
        `;
        dynamicDiv.innerHTML = gameHtml;
        updateScoreUI();
        document.getElementById("liveScoreGame") && (document.getElementById("liveScoreGame").innerText = userScore);
        
        let currentMathQuestion = null;
        function generateMathQuestion() {
            const a = Math.floor(Math.random() * 50) + 1;
            const b = Math.floor(Math.random() * 50) + 1;
            const op = Math.random() > 0.5 ? '+' : '-';
            let answer = op === '+' ? a + b : a - b;
            if(op === '-') while(b > a) { b = Math.floor(Math.random() * 50) + 1; answer = a - b; }
            const text = `${a} ${op} ${b} = ؟`;
            return { text, answer };
        }
        function refreshMath() {
            currentMathQuestion = generateMathQuestion();
            document.getElementById("questionGame").innerHTML = `🧮 ${currentMathQuestion.text}`;
            document.getElementById("answerInput").value = '';
            document.getElementById("gameFeedback").innerHTML = '';
        }
        document.getElementById("newMathQuestion")?.addEventListener('click', refreshMath);
        document.getElementById("checkAnswer")?.addEventListener('click', () => {
            const userAns = parseInt(document.getElementById("answerInput").value);
            if (isNaN(userAns)) { document.getElementById("gameFeedback").innerHTML = "⚠️ أدخل رقماً!"; return; }
            if (userAns === currentMathQuestion.answer) {
                userScore += 5;
                document.getElementById("gameFeedback").innerHTML = "🎉 صحيح! +5 نقاط 🎉";
                document.getElementById("liveScoreGame").innerText = userScore;
                updateScoreUI();
                refreshMath();
            } else {
                userScore = Math.max(0, userScore - 2);
                document.getElementById("gameFeedback").innerHTML = `😓 خطأ! الإجابة: ${currentMathQuestion.answer} -2 نقاط.`;
                document.getElementById("liveScoreGame").innerText = userScore;
                updateScoreUI();
                refreshMath();
            }
        });
        refreshMath();
        document.getElementById("newFactBtn")?.addEventListener('click', () => {
            const newFact = funFacts[Math.floor(Math.random() * funFacts.length)];
            document.getElementById("randomFunFactDisplay").innerText = newFact;
        });
    }

    // أحداث التنقل
    document.querySelectorAll('[data-subject]').forEach(btn => {
        btn.addEventListener('click', (e) => renderSubject(btn.getAttribute('data-subject'), currentLevel));
    });
    document.querySelectorAll('.card').forEach(card => {
        card.addEventListener('click', (e) => renderSubject(card.getAttribute('data-subject'), currentLevel));
    });
    homeBtn.addEventListener('click', () => {
        dynamicDiv.innerHTML = `<h2 style="text-align:center;">✨ مرحباً مجدداً ✨</h2>
        <p style="text-align:center;">اختر مادة من الأعلى أو البطاقات.</p><div style="text-align:center;"><button id="homeGameBtn">🎮 اذهب إلى الألعاب</button></div>`;
        document.getElementById("homeGameBtn")?.addEventListener('click', showGamePage);
    });
    gameNavBtn.addEventListener('click', showGamePage);
    document.getElementById("startGameQuick")?.addEventListener('click', showGamePage);
    renderSubject("math", "middle");
</script>
</body>
</html>-education-site
