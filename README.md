<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>امتحان البيئة النباتية - تصحيح فوري</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(145deg, #eef5e6 0%, #d9e3c6 100%);
            font-family: 'Segoe UI', 'Tahoma', 'Traditional Arabic', 'Arial', sans-serif;
            padding: 30px 20px;
            color: #1e3a2f;
        }

        .exam-container {
            max-width: 1100px;
            margin: 0 auto;
            background: #fefcf0;
            border-radius: 48px;
            box-shadow: 0 20px 40px rgba(0, 20, 0, 0.2);
            overflow: hidden;
            padding: 25px 30px 40px;
            border: 1px solid #c0d6b3;
        }

        h1 {
            font-size: 2.3rem;
            text-align: center;
            color: #2c5e2a;
            margin-bottom: 10px;
            border-bottom: 3px solid #9bc48f;
            display: inline-block;
            width: auto;
            padding-bottom: 8px;
        }

        .header-sub {
            text-align: center;
            font-weight: bold;
            color: #4a6741;
            margin-bottom: 30px;
            font-size: 1.1rem;
            background: #e9f3e3;
            display: inline-block;
            width: 100%;
            padding: 10px;
            border-radius: 60px;
        }

        .score-board {
            background: #2c5e2a;
            color: white;
            border-radius: 40px;
            padding: 12px 20px;
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            flex-wrap: wrap;
            margin-bottom: 30px;
            font-weight: bold;
            gap: 15px;
        }

        .score-item {
            background: #f9b81b;
            color: #1e3a2f;
            padding: 6px 18px;
            border-radius: 50px;
            font-size: 1.2rem;
        }

        .question-section {
            margin-bottom: 45px;
            background: #ffffffd9;
            border-radius: 40px;
            padding: 20px 25px;
            box-shadow: 0 5px 12px rgba(0, 0, 0, 0.05);
            transition: 0.2s;
        }

        .section-title {
            font-size: 1.8rem;
            font-weight: bold;
            background: #e0f0da;
            display: inline-block;
            padding: 5px 25px;
            border-radius: 40px;
            margin-bottom: 20px;
            color: #1e5620;
            border-right: 6px solid #5b8c50;
        }

        .question-card {
            background: #fffef7;
            margin-bottom: 22px;
            border-radius: 28px;
            padding: 16px 22px;
            border: 1px solid #e2efda;
            transition: 0.1s;
        }

        .question-text {
            font-size: 1.15rem;
            font-weight: 600;
            margin-bottom: 14px;
            color: #1e4620;
            display: flex;
            align-items: baseline;
            gap: 12px;
            flex-wrap: wrap;
        }

        .q-num {
            background: #6f9e5c;
            color: white;
            width: 30px;
            height: 30px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            font-size: 0.9rem;
            font-weight: bold;
        }

        .options {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin: 12px 0 8px;
            padding-right: 20px;
        }

        .option {
            display: flex;
            align-items: center;
            gap: 8px;
            background: #f8fbf4;
            padding: 6px 16px;
            border-radius: 40px;
            border: 1px solid #cddfc2;
            cursor: pointer;
            transition: 0.1s;
        }

        .option:hover {
            background: #e7f3e0;
        }

        input[type="radio"] {
            width: 18px;
            height: 18px;
            cursor: pointer;
            accent-color: #437c3a;
        }

        .feedback {
            margin-top: 12px;
            font-size: 0.9rem;
            padding: 8px 16px;
            border-radius: 30px;
            display: inline-block;
            font-weight: 500;
        }

        .correct-feedback {
            background: #d4edc9;
            color: #1f5a1a;
            border-right: 5px solid #3b8c2e;
        }

        .wrong-feedback {
            background: #ffe1de;
            color: #b13e3e;
            border-right: 5px solid #d9534f;
        }

        .truefalse-group {
            display: flex;
            gap: 25px;
            align-items: center;
        }

        hr {
            margin: 15px 0;
            border: 0;
            height: 1px;
            background: #d4e2ca;
        }

        .essay-box {
            background: #fef6e0;
            border-radius: 24px;
            padding: 15px;
            margin-top: 12px;
        }

        .essay-question {
            font-weight: bold;
            margin-bottom: 12px;
        }

        textarea {
            width: 100%;
            border-radius: 24px;
            border: 1px solid #c6ddb5;
            padding: 12px;
            font-family: inherit;
            background: white;
            resize: vertical;
        }

        .model-answer-btn {
            background: #6c8f5c;
            color: white;
            border: none;
            padding: 6px 15px;
            border-radius: 30px;
            margin-top: 10px;
            cursor: pointer;
            font-size: 0.8rem;
            transition: 0.2s;
        }

        .model-answer {
            margin-top: 12px;
            background: #eef3e9;
            padding: 12px;
            border-radius: 20px;
            display: none;
            border-right: 4px solid #2e7d32;
        }

        button {
            background: #508c42;
            border: none;
            color: white;
            font-weight: bold;
            padding: 8px 20px;
            border-radius: 34px;
            cursor: pointer;
            font-size: 1rem;
            transition: 0.2s;
        }

        button:hover {
            background: #2c6e2a;
            transform: scale(0.98);
        }

        .reset-btn {
            background: #b87c4f;
            margin-right: 15px;
        }

        footer {
            text-align: center;
            margin-top: 30px;
            color: #527a45;
        }

        @media (max-width: 700px) {
            .exam-container {
                padding: 15px;
            }
            .options {
                gap: 12px;
            }
            .question-card {
                padding: 12px;
            }
        }
    </style>
</head>
<body>
<div class="exam-container">
    <div style="text-align: center;">
        <h1>🌿 امتحان البيئة النباتية 🌱</h1>
        <div class="header-sub">التصحيح الفوري بعد اختيار الإجابة | الأسئلة الموضوعية تُصحح أوتوماتيكياً</div>
    </div>

    <div class="score-board">
        <span>📊 مجموع درجاتك (الموضوعي فقط):</span>
        <span class="score-item" id="totalScoreDisplay">0 / 45</span>
        <button id="resetExamBtn" class="reset-btn">🔄 إعادة المحاولة</button>
    </div>

    <!-- ========================= السؤال الأول (اختيار من متعدد) ========================= -->
    <div class="question-section">
        <div class="section-title">⦿ السؤال الأول: اختر الإجابة الصحيحة (10 أسئلة × 3 درجات = 30)</div>
        <div id="mcq-questions"></div>
    </div>

    <!-- ========================= السؤال الثاني (صح/خطأ) ========================= -->
    <div class="question-section">
        <div class="section-title">⦿ السؤال الثاني: ضع علامة (صح) أو (خطأ) (15 عبارة × 1 درجة = 15)</div>
        <div id="tf-questions"></div>
    </div>

    <!-- ========================= السؤال الثالث (مقالي) ========================= -->
    <div class="question-section">
        <div class="section-title">✍️ السؤال الثالث: اكتب ما تعرفه (أسئلة مقالية - تقييم ذاتي)</div>
        <div style="margin-bottom: 10px; background: #fef1ce; border-radius: 24px; padding: 12px;">
            <p>📌 <strong>تنبيه:</strong> الأسئلة المقالية تعرض للإجابة الحرة. يمكنك الاطلاع على نموذج إجابة مبسط بعد كتابة إجابتك. لا يتم تصحيحها آلياً، بل هي مراجعة ذاتية.</p>
        </div>
        <div id="essay-questions"></div>
    </div>
    <footer>✔️ عند اختيار أي إجابة في الأسئلة الموضوعية، تظهر علامة (صحيح/خطأ) ويتم تحديث الدرجة تلقائياً.</footer>
</div>

<script>
    // --------------------------------------------------------------
    // بيانات السؤال الأول: اختيار من متعدد
    // --------------------------------------------------------------
    const mcqData = [
        { text: "يؤثر قوام التربة على صفاتها الأخرى مثل:", options: ["أ- السعة المائية", "ب- النفاذية", "ج- (أ – ب) معا"], correct: "ج- (أ – ب) معا", score: 3 },
        { text: "تقسم الأراضي التي تحتوي على نسبة عالية من الأملاح وزيادة الصوديوم إلى:", options: ["أ- أراضي ملحية قلوية", "ب- أراضي غير ملحية قلوية", "ج- (أ – ب) معا"], correct: "أ- أراضي ملحية قلوية", score: 3 },
        { text: "جميع ما يأتي يعتبر من العوامل غير الحية ماعدا:", options: ["أ- الأشجار", "ب- درجة الحرارة", "ج- الرقم الهيدروجيني"], correct: "أ- الأشجار", score: 3 },
        { text: "تعرف مجموعة الأفراد من نفس النوع الذين يعيشون في نفس المنطقة باسم:", options: ["أ- الأنواع", "ب- الجماعات", "ج- المجتمع"], correct: "ب- الجماعات", score: 3 },
        { text: "التأثيرات البيولوجية على الكائنات الحية داخل النظام البيئي تسمى:", options: ["أ- العوامل الحية", "ب- العوامل غير الحية", "ج- الموارد غير المتجددة"], correct: "أ- العوامل الحية", score: 3 },
        { text: "...... هي مجموعة من النظم البيئية التي لها نفس المناخ والتضاريس وخصائص التربة", options: ["أ- المحيط الحيوي", "ب- المنطقة الإحيائية", "ج- الموطن"], correct: "ب- المنطقة الإحيائية", score: 3 },
        { text: "أي مما يلي يشتمل على العوامل غير الحية المهمة لأي نظام بيئي ؟", options: ["أ- درجة الحرارة", "ب- الرياح", "ج- جميع ما سبق"], correct: "ج- جميع ما سبق", score: 3 },
        { text: "في النظام البيئي (اليابس) يكون المستوى الغذائي الذي يحتوي على أكبر كتلة حيوية هو:", options: ["أ- الكائنات المنتجة", "ب- الكائنات المستهلكة الأولية", "ج- الكائنات المحللة"], correct: "أ- الكائنات المنتجة", score: 3 },
        { text: "أي مما يلي قد يكون من العوامل الحية في النظام البيئي؟", options: ["أ- البكتيريا", "ب- التربة", "ج- درجة الحرارة"], correct: "أ- البكتيريا", score: 3 },
        { text: "نظام الذروة البيئي هو:", options: ["أ- مجتمع نباتي مستقر", "ب- مجتمع نباتي مضطرب", "ج- (أ – ب) معا"], correct: "أ- مجتمع نباتي مستقر", score: 3 }
    ];

    // بيانات السؤال الثاني: صح/خطأ (15 عبارة) (true = صح, false = خطأ)
    const tfData = [
        { text: "أن أهم ما يميز النظام البيئي هو التوازن الدقيق القائم بين مكوناته مع المرونة والحركة وبالتالي فإن الاتزان الذي تحظى به الأنظمة البيئية هو من النوع الديناميكي", correct: true, score: 1 },
        { text: "الدرجات الحدية وهي الدرجات التي تحدث عندها تغيرات حساسة في حيوية النباتات وفي نموه وفي طاقته الإنتاجية", correct: true, score: 1 },
        { text: "السعة الحقلية عبارة عن المحتوى المائي للتربة بعد عملية الري أو سقوط الأمطار مباشرة", correct: false, score: 1 },
        { text: "تعد المصبات أنظمة مائية يختلط فيها الماء العذب القادم من اليابسة مع ماء البحر ويحدث له تخفيف في نسبة الملوحة لذا فهي انتقالية بين المياه العذبة والمياه المالحة", correct: true, score: 1 },
        { text: "يطلق على ظاهرة اختلاف استجابة النباتات للطول النسبي لكل من الليل والنهار بظاهرة التآقت الضوئي", correct: true, score: 1 },
        { text: "التعاقد البيئي هي سلسلة من المجتمعات الحيوية التي تحل محل بعضها البعض مما يؤدي إلى تغيير المجتمع", correct: true, score: 1 },
        { text: "يطلق على مجمل التأثيرات المتبادلة بين الكائنات الحية المختلفة اسم العوامل الأحيائية", correct: true, score: 1 },
        { text: "المادة العضوية ليس لها دور في تحسين الخواص الفيزيائية والكيميائية للتربة", correct: false, score: 1 },
        { text: "تنتقل التربة إلى مستوى السعة الحقلية بعد 24 ساعة من الري أو هطول الأمطار", correct: true, score: 1 },
        { text: "توضح الدورات البيوجيوميكيائية حركة العناصر الغذائية في الأنظمة البيئية", correct: true, score: 1 },
        { text: "دورة الفسفور دورة مهمة بسبب أهمية الفسفور في تركيب المادة الحية البروتوبالزما ، وكذلك في تركيب الأحماض النووية وفي نمو العظام وغير ذلك", correct: true, score: 1 },
        { text: "تعرف حدود النظام البيئي على أنها مجموعة من الظروف الفيزيائية والكيميائية التي تشكل نهايتها أو التدرج البيئي", correct: true, score: 1 },
        { text: "التحلل المائي هو اتحاد الماء مع جزيئات الصخور ويعمل على تفكيك الصخور فيزيائيا", correct: false, score: 1 },
        { text: "وفقاً لنوع الصخور، تتكون المواد الأم للتربة من البركانية والرسوبية والمتحولة", correct: true, score: 1 },
        { text: "الماء المقيد (الهيجروسكوب) الجزء المتبقي من الماء في الفراغات البيئية لحبيبات التربة بفعل التوتر السطحي وقوى التلاصق بين الماء وحبيبات التربة", correct: true, score: 1 }
    ];

    // بيانات المقالي (5 مواضيع)
    const essayTopics = [
        { title: "1- التعاقب المائي", model: "هو سلسلة من التغيرات في المجتمعات النباتية داخل بيئة مائية (بحيرات، مستنقعات) حيث تتحول تدريجياً إلى أرض يابسة عبر مراحل من النباتات الغاطسة فالطافية فالقصبية فأشجار، وينتهي بغابة أو نظام أرضي." },
        { title: "2- دورة ثاني أكسيد الكربون في الطبيعة", model: "ثاني أكسيد الكربون ينتج عن التنفس والتحلل والاحتراق، وتمتصه النباتات في البناء الضوئي لتصنع مواد عضوية، ثم يعود للجو عن طريق التنفس والتحلل، وكذلك حرق الوقود، دورة حيوية جيوكيميائية." },
        { title: "3- المحتوى المائي للتربة", model: "كمية الماء الموجودة في التربة وتتوزع على: الماء الجاذلي (يتحرك بسرعة)، والماء الشعري (الاحتفاظ به في المسام)، والماء Hygroscopic (الماء المقيد بشدة)، ومنه السعة الحقلية ونقطة الذبول." },
        { title: "4- الرياح كمثال للعوامل المناخية", model: "الرياح تؤثر على النباتات من خلال: زيادة النتح، تشتيت الأبواغ والبذور، التلقيح، التعرية، تشويه نمو الأشجار، وتأثير ميكانيكي، كما تنقل الحرارة والرطوبة." },
        { title: "5- أضرار ارتفاع درجة الحرارة على العمليات الحيوية للنبات", model: "ارتفاع الحرارة يسبب: زيادة النتح والجفاف، توقف البناء الضوئي، تلف البروتوبلازم، إنزيمات معطلة، حرق الأنسجة، موت الخلايا، إجهاض الأزهار، وانخفاض الإنتاجية." }
    ];

    // تخزين إجابات المستخدم للأسئلة الموضوعية
    let mcqAnswers = new Array(mcqData.length).fill(null);
    let tfAnswers = new Array(tfData.length).fill(null);

    // حساب الدرجة الحالية
    function calculateTotalScore() {
        let total = 0;
        // mcq scores
        for (let i = 0; i < mcqData.length; i++) {
            if (mcqAnswers[i] !== null && mcqAnswers[i] === mcqData[i].correct) {
                total += mcqData[i].score;
            }
        }
        // tf scores
        for (let i = 0; i < tfData.length; i++) {
            if (tfAnswers[i] !== null && tfAnswers[i] === tfData[i].correct) {
                total += tfData[i].score;
            }
        }
        return total;
    }

    function updateTotalDisplay() {
        const total = calculateTotalScore();
        document.getElementById("totalScoreDisplay").innerText = `${total} / 45`;
    }

    // عرض رسالة التغذية الراجعة للإجابة
    function renderMcqFeedback(qIndex, selectedValue) {
        const feedbackDiv = document.getElementById(`mcq-fb-${qIndex}`);
        if (!feedbackDiv) return;
        const isCorrect = (selectedValue === mcqData[qIndex].correct);
        if (selectedValue) {
            if (isCorrect) {
                feedbackDiv.innerHTML = `<span class="feedback correct-feedback">✅ صحيح! إجابتك (${selectedValue}) صحيحة. (+${mcqData[qIndex].score} درجة)</span>`;
            } else {
                feedbackDiv.innerHTML = `<span class="feedback wrong-feedback">❌ خطأ! الإجابة الصحيحة هي: ${mcqData[qIndex].correct}. (0 درجة)</span>`;
            }
        } else {
            feedbackDiv.innerHTML = '';
        }
    }

    function renderTfFeedback(qIndex, selectedBool) {
        const feedbackDiv = document.getElementById(`tf-fb-${qIndex}`);
        if (!feedbackDiv) return;
        const isCorrect = (selectedBool === tfData[qIndex].correct);
        const correctAnswerText = tfData[qIndex].correct ? "صحيح (✓)" : "خطأ (✗)";
        if (selectedBool !== null) {
            if (isCorrect) {
                feedbackDiv.innerHTML = `<span class="feedback correct-feedback">✅ صحيح! الإجابة ${selectedBool ? 'صحيحة' : 'خاطئة'} مطابقة. (+${tfData[qIndex].score} درجة)</span>`;
            } else {
                feedbackDiv.innerHTML = `<span class="feedback wrong-feedback">❌ خطأ! الإجابة الصحيحة هي ${correctAnswerText}. (0 درجة)</span>`;
            }
        } else {
            feedbackDiv.innerHTML = '';
        }
    }

    // بناء السؤال الأول (اختيار من متعدد)
    function buildMcqSection() {
        const container = document.getElementById("mcq-questions");
        container.innerHTML = "";
        mcqData.forEach((q, idx) => {
            const card = document.createElement("div");
            card.className = "question-card";
            const qNumber = idx + 1;
            card.innerHTML = `
                <div class="question-text">
                    <span class="q-num">${qNumber}</span>
                    <span>${q.text}</span>
                </div>
                <div class="options" id="mcq-options-${idx}"></div>
                <div id="mcq-fb-${idx}" class="feedback-area"></div>
            `;
            container.appendChild(card);

            const optionsDiv = document.getElementById(`mcq-options-${idx}`);
            q.options.forEach(opt => {
                const label = document.createElement("label");
                label.className = "option";
                const radio = document.createElement("input");
                radio.type = "radio";
                radio.name = `mcq-${idx}`;
                radio.value = opt;
                radio.addEventListener("change", (e) => {
                    const selectedVal = e.target.value;
                    mcqAnswers[idx] = selectedVal;
                    renderMcqFeedback(idx, selectedVal);
                    updateTotalDisplay();
                });
                const span = document.createElement("span");
                span.innerText = opt;
                label.appendChild(radio);
                label.appendChild(span);
                optionsDiv.appendChild(label);
            });
            // إذا كان هناك إجابة مخزنة مسبقاً (عند إعادة تعيين) نعيد تعيينها ولكن reset سيعيد بناء الكل
        });
    }

    // بناء السؤال الثاني (صح/خطأ)
    function buildTfSection() {
        const container = document.getElementById("tf-questions");
        container.innerHTML = "";
        tfData.forEach((item, idx) => {
            const card = document.createElement("div");
            card.className = "question-card";
            const qNumber = idx + 1;
            card.innerHTML = `
                <div class="question-text">
                    <span class="q-num">${qNumber}</span>
                    <span>${item.text}</span>
                </div>
                <div class="truefalse-group" id="tf-group-${idx}">
                    <label class="option"><input type="radio" name="tf-${idx}" value="true"> ✔️ صح</label>
                    <label class="option"><input type="radio" name="tf-${idx}" value="false"> ❌ خطأ</label>
                </div>
                <div id="tf-fb-${idx}" class="feedback-area"></div>
            `;
            container.appendChild(card);
            // الأحداث
            const radioTrue = document.querySelector(`input[name="tf-${idx}"][value="true"]`);
            const radioFalse = document.querySelector(`input[name="tf-${idx}"][value="false"]`);
            const handleTfChange = (e) => {
                const selectedVal = e.target.value;
                const boolVal = selectedVal === "true";
                tfAnswers[idx] = boolVal;
                renderTfFeedback(idx, boolVal);
                updateTotalDisplay();
            };
            if (radioTrue) radioTrue.addEventListener("change", handleTfChange);
            if (radioFalse) radioFalse.addEventListener("change", handleTfChange);
        });
    }

    // بناء الأسئلة المقالية (غير تصحيح آلي ولكن مع نموذج إجابة)
    function buildEssaySection() {
        const container = document.getElementById("essay-questions");
        container.innerHTML = "";
        essayTopics.forEach((topic, idx) => {
            const essayDiv = document.createElement("div");
            essayDiv.className = "essay-box";
            essayDiv.style.marginBottom = "20px";
            essayDiv.innerHTML = `
                <div class="essay-question">📝 ${topic.title}</div>
                <textarea rows="3" placeholder="اكتب إجابتك هنا ..." id="essay-input-${idx}"></textarea>
                <button class="model-answer-btn" data-idx="${idx}">📖 عرض نموذج الإجابة</button>
                <div id="model-answer-${idx}" class="model-answer"></div>
            `;
            container.appendChild(essayDiv);
        });
        // إضافة فعالية الأزرار
        document.querySelectorAll('.model-answer-btn').forEach(btn => {
            btn.addEventListener('click', (e) => {
                const idx = btn.getAttribute('data-idx');
                const modelDiv = document.getElementById(`model-answer-${idx}`);
                if (modelDiv) {
                    if (modelDiv.style.display === 'none' || !modelDiv.style.display) {
                        modelDiv.innerHTML = `<strong>📘 نموذج إجابة مختصرة:</strong><br>${essayTopics[idx].model}`;
                        modelDiv.style.display = 'block';
                    } else {
                        modelDiv.style.display = 'none';
                    }
                }
            });
        });
    }

    // إعادة تعيين كل شيء
    function resetExam() {
        // إعادة تهيئة المصفوفات
        mcqAnswers.fill(null);
        tfAnswers.fill(null);
        // إعادة بناء واجهة الأسئلة لإلغاء التحديدات
        buildMcqSection();
        buildTfSection();
        // المقالي لا نحتاج لإعادة بنائها لأنها نصية فقط، لكن نزيل أي نموذج إجابة مفتوح ونفرغ الحقول
        for (let i = 0; i < essayTopics.length; i++) {
            const textarea = document.getElementById(`essay-input-${i}`);
            if (textarea) textarea.value = '';
            const modelDiv = document.getElementById(`model-answer-${i}`);
            if (modelDiv) {
                modelDiv.style.display = 'none';
                modelDiv.innerHTML = '';
            }
        }
        // إعادة تحديث العرض الكلي
        updateTotalDisplay();
        // إزالة أي رسائل تغذية راجعة مرئية (المحتوى تم بناؤه جديد)
    }

    // إعداد زر إعادة المحاولة
    function setupResetButton() {
        const resetBtn = document.getElementById("resetExamBtn");
        resetBtn.addEventListener("click", () => {
            resetExam();
        });
    }

    // تهيئة الصفحة
    function init() {
        buildMcqSection();
        buildTfSection();
        buildEssaySection();
        setupResetButton();
        updateTotalDisplay();
    }

    init();
</script>
</body>
</html>
