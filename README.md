<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>نَمِّ فكرتك | من بذرة إلى مشروع</title>

<style>
:root {
  --bg: #080d1b;
  --panel: #111a30;
  --panel2: #17223d;
  --purple: #a78bfa;
  --blue: #68a9ff;
  --silver: #e1e8f5;
  --muted: #aab7d0;
  --green: #79e0b1;
}

* {
  box-sizing: border-box;
  scroll-behavior: smooth;
}

body {
  margin: 0;
  background:
    radial-gradient(ellipse at top right, #25204b 0, transparent 38%),
    radial-gradient(ellipse at bottom left, #102c4c 0, transparent 35%),
    var(--bg);
  color: var(--silver);
  font-family: Tahoma, Arial, sans-serif;
  line-height: 1.8;
}

button, input, textarea, select {
  font: inherit;
}

button {
  cursor: pointer;
}

header {
  padding: 17px 6%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 15px;
  flex-wrap: wrap;
  border-bottom: 1px solid #ffffff14;
  background: #080d1bd9;
  position: sticky;
  top: 0;
  z-index: 10;
  backdrop-filter: blur(12px);
}

.logo {
  color: white;
  font-weight: bold;
  font-size: 22px;
}

.logo span {
  color: var(--green);
}

nav {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

nav a {
  color: var(--muted);
  text-decoration: none;
  padding: 6px 10px;
  border-radius: 9px;
  font-size: 13px;
}

nav a:hover {
  background: #ffffff12;
  color: white;
}

.hero {
  padding: 75px 7% 60px;
  text-align: center;
  max-width: 1000px;
  margin: auto;
}

.badge {
  display: inline-block;
  color: var(--green);
  border: 1px solid #79e0b144;
  border-radius: 30px;
  padding: 5px 16px;
  font-size: 13px;
}

h1 {
  font-size: clamp(34px, 7vw, 65px);
  line-height: 1.35;
  margin: 20px 0;
}

.gradient {
  background: linear-gradient(90deg, var(--blue), var(--purple), var(--green));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.hero p {
  color: var(--muted);
  max-width: 650px;
  margin: 0 auto 25px;
}

.actions {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 25px;
}

.btn {
  border: 0;
  border-radius: 12px;
  padding: 12px 20px;
  font-weight: bold;
  background: linear-gradient(110deg, var(--blue), var(--purple));
  color: #080d1b;
  text-decoration: none;
  display: inline-block;
}

.btn:hover {
  filter: brightness(1.12);
  transform: translateY(-1px);
}

.btn.secondary {
  color: var(--silver);
  background: #ffffff0b;
  border: 1px solid #ffffff22;
}

.stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-top: 45px;
}

.stat, .card, .box {
  background: linear-gradient(145deg, #182440d9, #10182bd9);
  border: 1px solid #ffffff12;
  border-radius: 18px;
  padding: 20px;
}

.stat strong {
  display: block;
  font-size: 24px;
  color: var(--green);
}

.stat span {
  font-size: 13px;
  color: var(--muted);
}

section {
  padding: 48px 6%;
  max-width: 1250px;
  margin: auto;
  scroll-margin-top: 95px;
}

.section-title {
  margin-bottom: 25px;
}

.section-title h2 {
  font-size: clamp(25px, 4vw, 36px);
  margin: 0 0 8px;
}

.section-title p {
  color: var(--muted);
  margin: 0;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(min(100%, 240px), 1fr));
  gap: 16px;
}

.card {
  transition: .2s;
}

.card:hover {
  border-color: #a78bfa66;
  transform: translateY(-3px);
}

.icon {
  font-size: 30px;
}

.card h3 {
  margin: 8px 0;
}

.card p {
  color: var(--muted);
  font-size: 14px;
}

input, textarea, select {
  width: 100%;
  color: var(--silver);
  background: #080f20;
  border: 1px solid #ffffff24;
  border-radius: 11px;
  padding: 12px;
  outline: none;
  margin: 7px 0 15px;
}

input:focus, textarea:focus, select:focus {
  border-color: var(--purple);
}

textarea {
  min-height: 95px;
  resize: vertical;
}

label {
  display: block;
  font-weight: bold;
  font-size: 14px;
}

.field {
  margin-bottom: 10px;
}

.field small {
  color: var(--muted);
}

.progress-wrap {
  background: #ffffff12;
  border-radius: 20px;
  height: 8px;
  margin: 15px 0 25px;
  overflow: hidden;
}

#progress {
  height: 100%;
  width: 0;
  background: linear-gradient(90deg, var(--blue), var(--green));
  transition: .3s;
}

.step {
  display: none;
}

.step.active {
  display: block;
}

.step-number {
  color: var(--green);
  font-size: 13px;
}

.result {
  display: none;
  white-space: pre-wrap;
  line-height: 2;
  padding: 20px;
  background: #080f20;
  border: 1px solid #79e0b144;
  border-radius: 14px;
  margin-top: 20px;
}

.quiz-option {
  display: block;
  width: 100%;
  margin: 10px 0;
  padding: 12px;
  text-align: right;
  background: #ffffff08;
  border: 1px solid #ffffff20;
  color: var(--silver);
  border-radius: 10px;
}

.quiz-option:hover {
  border-color: var(--purple);
  background: #a78bfa14;
}

#quizFeedback {
  margin-top: 12px;
  font-weight: bold;
}

.notice {
  border-right: 3px solid var(--green);
  background: #79e0b10b;
  padding: 12px 15px;
  border-radius: 8px;
  color: var(--muted);
  font-size: 13px;
}

footer {
  text-align: center;
  border-top: 1px solid #ffffff14;
  padding: 30px 15px;
  color: var(--muted);
  font-size: 13px;
}

@media (max-width: 600px) {
  header {
    position: static;
  }
  nav {
    width: 100%;
  }
  nav a {
    padding: 5px 7px;
  }
  .hero {
    padding-top: 45px;
  }
  section {
    padding: 35px 5%;
  }
}
</style>
</head>

<body>

<header>
  <div class="logo">🌱 نَمِّ <span>فكرتك</span></div>
  <nav>
    <a href="#home">الرئيسية</a>
    <a href="#workshop">طوّر فكرتك</a>
    <a href="#awareness">التوعية</a>
    <a href="#games">الألعاب</a>
    <a href="#resources">المصادر</a>
  </nav>
</header>

<main>

<div class="hero" id="home">
  <span class="badge">من بذرة صغيرة إلى فكرة تنمو</span>
  <h1>كل مشروع عظيم<br>بدأ <span class="gradient">بفكرة</span></h1>
  <p>
    لديك فكرة ولا تعرف كيف تبدأ؟ أو تبحث عن شيء جديد تتعلمه؟
    نَمِّ فكرتك مساحة تجمع تطوير الأفكار والتعلم والتوعية
    والتفكير الإبداعي في مكان واحد.
  </p>

  <div class="actions">
    <a class="btn" href="#workshop">🌱 لدي فكرة</a>
    <a class="btn secondary" href="#games">🧠 أريد أن أتعلم</a>
  </div>

  <div class="stats">
    <div class="stat"><strong>01</strong><span>ابدأ بفكرتك</span></div>
    <div class="stat"><strong>02</strong><span>اكتشف المشكلة</span></div>
    <div class="stat"><strong>03</strong><span>خطط للحل</span></div>
    <div class="stat"><strong>04</strong><span>ابدأ بالتجربة</span></div>
  </div>
</div>

<section id="workshop">
  <div class="section-title">
    <h2>🌱 ورشة نمو الفكرة</h2>
    <p>أجب عن الأسئلة بالترتيب لبناء تصور أولي لمشروعك.</p>
  </div>

  <div class="box">
    <div class="progress-wrap"><div id="progress"></div></div>

    <div class="step active">
      <span class="step-number">الخطوة ١ من ٥</span>
      <h3>ما بذرة فكرتك؟</h3>
      <div class="field">
        <label for="ideaName">اسم الفكرة</label>
        <input id="ideaName" placeholder="مثال: منصة لتبادل الكتب">
      </div>
      <div class="field">
        <label for="ideaField">مجال الفكرة</label>
        <select id="ideaField">
          <option value="">اختر المجال</option>
          <option>التقنية والابتكار</option>
          <option>الصحة</option>
          <option>البيئة</option>
          <option>التعليم</option>
          <option>الوعي المالي</option>
          <option>خدمة المجتمع</option>
          <option>مجال آخر</option>
        </select>
      </div>
      <div class="field">
        <label for="ideaDesc">اشرح فكرتك بطريقتك</label>
        <textarea id="ideaDesc" placeholder="ما الشيء الذي تفكر في صنعه أو تطويره؟"></textarea>
      </div>
      <button class="btn" onclick="nextStep(1)">الخطوة التالية ←</button>
    </div>

    <div class="step">
      <span class="step-number">الخطوة ٢ من ٥</span>
      <h3>ما المشكلة التي تريد حلها؟</h3>
      <div class="field">
        <label for="problem">ما المشكلة التي لاحظتها؟</label>
        <textarea id="problem" placeholder="صف المشكلة التي تريد أن تعالجها فكرتك."></textarea>
      </div>
      <div class="field">
        <label for="audience">من الأشخاص الذين قد يستفيدون؟</label>
        <input id="audience" placeholder="مثال: الطلاب، الأسر، أصحاب المشاريع">
      </div>
      <button class="btn secondary" onclick="nextStep(-1)">→ السابقة</button>
      <button class="btn" onclick="nextStep(1)">التالية ←</button>
    </div>

    <div class="step">
      <span class="step-number">الخطوة ٣ من ٥</span>
      <h3>كيف يمكن أن تعمل فكرتك؟</h3>
      <div class="field">
        <label for="solution">ما الحل الذي تقترحه؟</label>
        <textarea id="solution" placeholder="كيف ستساعد فكرتك في حل المشكلة؟"></textarea>
      </div>
      <div class="field">
        <label for="difference">ما الذي يميز فكرتك؟</label>
        <textarea id="difference" placeholder="ما الإضافة التي تتمنى أن تقدمها؟"></textarea>
      </div>
      <button class="btn secondary" onclick="nextStep(-1)">→ السابقة</button>
      <button class="btn" onclick="nextStep(1)">التالية ←</button>
    </div>

    <div class="step">
      <span class="step-number">الخطوة ٤ من ٥</span>
      <h3>ما الذي تحتاج إليه؟</h3>
      <div class="field">
        <label for="tools">الأدوات والموارد المتاحة</label>
        <textarea id="tools" placeholder="ما الأدوات أو المهارات أو المصادر التي تحتاجها؟"></textarea>
      </div>
      <div class="field">
        <label for="cost">التكلفة المتوقعة إن وجدت</label>
        <input id="cost" placeholder="مثال: لا أعرف بعد، أو تقدير مبدئي">
        <small>هذا تقدير تكتبه بنفسك، وليس حسابًا ماليًا موثقًا.</small>
      </div>
      <button class="btn secondary" onclick="nextStep(-1)">→ السابقة</button>
      <button class="btn" onclick="nextStep(1)">التالية ←</button>
    </div>

    <div class="step">
      <span class="step-number">الخطوة ٥ من ٥</span>
      <h3>خطوتك الأولى نحو التنفيذ</h3>
      <div class="field">
        <label for="firstStep">ما أول خطوة تستطيع تنفيذها؟</label>
        <textarea id="firstStep" placeholder="مثال: البحث عن حلول مشابهة أو سؤال المستفيدين."></textarea>
      </div>
      <div class="field">
        <label for="testPlan">كيف ستختبر فكرتك مبدئيًا؟</label>
        <textarea id="testPlan" placeholder="كيف تعرف أن الحل مفيد فعلًا؟"></textarea>
      </div>
      <button class="btn secondary" onclick="nextStep(-1)">→ السابقة</button>
      <button class="btn" onclick="makeSummary()">إنشاء ملخص الفكرة ✨</button>
    </div>

    <div class="result" id="summary"></div>
    <div class="actions" id="summaryActions" style="display:none">
      <button class="btn" onclick="copySummary()">نسخ الملخص</button>
      <button class="btn secondary" onclick="downloadSummary()">حفظ الملخص نصيًا</button>
      <button class="btn secondary" onclick="saveDraft()">حفظ المسودة في هذا المتصفح</button>
    </div>
    <p class="notice">المعلومات التي تدخلها تبقى في هذه الصفحة ما لم تستخدم خاصية الحفظ المحلي. لا تدخِل بيانات شخصية أو سرية.</p>
  </div>
</section>

<section id="awareness">
  <div class="section-title">
    <h2>🌍 مساحة التوعية</h2>
    <p>معرفة صغيرة قد تصنع فرقًا كبيرًا.</p>
  </div>

  <div class="grid">
    <article class="card">
      <div class="icon">🌿</div>
      <h3>البيئة المستدامة</h3>
      <p>ابدأ بعادة بسيطة: قلل الهدر، وأعد استخدام ما تستطيع، وافصل النفايات حيث تتوفر خدمة الفرز.</p>
    </article>
    <article class="card">
      <div class="icon">💚</div>
      <h3>الصحة والعافية</h3>
      <p>النوم الكافي، والحركة المنتظمة، والغذاء المتوازن عادات تساعد على دعم الصحة العامة.</p>
    </article>
    <article class="card">
      <div class="icon">🔐</div>
      <h3>الوعي الرقمي</h3>
      <p>لا تشارك كلمات المرور أو رموز التحقق، وتأكد من مصدر الرسائل قبل فتح الروابط.</p>
    </article>
    <article class="card">
      <div class="icon">💰</div>
      <h3>الوعي المالي</h3>
      <p>دوّن مصروفاتك وميّز بين الحاجة والرغبة، وقارن الأسعار قبل اتخاذ قرار الشراء.</p>
    </article>
    <article class="card">
      <div class="icon">🧠</div>
      <h3>التفكير الناقد</h3>
      <p>اسأل: ما مصدر المعلومة؟ ما الدليل؟ وهل توجد تفسيرات أخرى؟</p>
    </article>
    <article class="card">
      <div class="icon">💡</div>
      <h3>الإبداع والابتكار</h3>
      <p>جرّب النظر إلى المشكلة من زوايا مختلفة، واجمع بين أفكار متباعدة لصناعة حلول جديدة.</p>
    </article>
  </div>
</section>

<section id="games">
  <div class="section-title">
    <h2>🎮 تحديات العقل</h2>
    <p>اختبر معرفتك، وفكّر قبل أن تختار.</p>
  </div>

  <div class="grid">
    <article class="card">
      <div class="icon">🔎</div>
      <h3>تحدي التفكير الناقد</h3>
      <p>هل تستطيع التمييز بين الادعاء والدليل؟</p>
      <button class="btn" onclick="startQuiz('critical')">ابدأ التحدي</button>
    </article>
    <article class="card">
      <div class="icon">✨</div>
      <h3>تحدي التفكير الإبداعي</h3>
      <p>ابحث عن أكثر من حل للمشكلة.</p>
      <button class="btn" onclick="startQuiz('creative')">ابدأ التحدي</button>
    </article>
    <article class="card">
      <div class="icon">🌎</div>
      <h3>تحدي الوعي العام</h3>
      <p>اختبر معرفتك بالبيئة والمجتمع والتقنية.</p>
      <button class="btn" onclick="startQuiz('awareness')">ابدأ التحدي</button>
    </article>
  </div>

  <div class="box" id="quizBox" style="display:none;margin-top:20px">
    <div id="quizCategory" class="step-number"></div>
    <h3 id="quizQuestion"></h3>
    <div id="quizOptions"></div>
    <div id="quizFeedback" aria-live="polite"></div>
    <p id="quizScore"></p>
    <button class="btn secondary" id="nextQuestion" onclick="nextQuestion()" style="display:none">السؤال التالي</button>
    <button class="btn" onclick="closeQuiz()">إغلاق اللعبة</button>
  </div>
</section>

<section id="resources">
  <div class="section-title">
    <h2>📚 أدوات ومصادر للانطلاق</h2>
    <p>استخدم مصادر موثوقة، وابحث عن الأدلة قبل اعتماد أي معلومة.</p>
  </div>

  <div class="grid">
    <article class="card">
      <div class="icon">🔬</div>
      <h3>البحث العلمي</h3>
      <p>ابحث عن الدراسات والأبحاث المنشورة.</p>
      <a class="btn" href="https://scholar.google.com/" target="_blank" rel="noopener">Google Scholar</a>
    </article>
    <article class="card">
      <div class="icon">🌐</div>
      <h3>المعرفة العامة</h3>
      <p>استكشف موضوعات متنوعة، ثم تحقق من المصادر الأصلية.</p>
      <a class="btn" href="https://www.britannica.com/" target="_blank" rel="noopener">Britannica</a>
    </article>
    <article class="card">
      <div class="icon">💻</div>
      <h3>تعلم التقنية</h3>
      <p>تعرف على أساسيات بناء صفحات الويب.</p>
      <a class="btn" href="https://developer.mozilla.org/" target="_blank" rel="noopener">MDN Web Docs</a>
    </article>
    <article class="card">
      <div class="icon">🇸🇦</div>
      <h3>معلومات رسمية سعودية</h3>
      <p>ارجع إلى الجهات الرسمية عند البحث عن معلومات محلية.</p>
      <a class="btn" href="https://www.my.gov.sa/" target="_blank" rel="noopener">البوابة الوطنية</a>
    </article>
  </div>
</section>

<section id="reflection">
  <div class="section-title">
    <h2>🪞 مساحة التفكير</h2>
    <p>اكتب إجابتك بنفسك لتتدرب على التحليل وصناعة الحلول.</p>
  </div>
  <div class="box">
    <label for="reflectionQuestion">لو استطعت حل مشكلة واحدة حولك، فما هي؟ ولماذا؟</label>
    <textarea id="reflectionQuestion" placeholder="اكتب فكرتك هنا..."></textarea>
    <button class="btn" onclick="saveReflection()">حفظ إجابتي محليًا</button>
    <button class="btn secondary" onclick="loadReflection()">عرض إجابتي المحفوظة</button>
    <p id="reflectionMessage" aria-live="polite"></p>
    <p class="notice">الحفظ هنا داخل متصفحك فقط، وليس في قاعدة بيانات أو حساب سحابي.</p>
  </div>
</section>

</main>

<footer>
  <div class="logo">🌱 نَمِّ فكرتك</div>
  <p>مساحة تجمع التعلم والتطوير والإبداع.</p>
  <p>نسخة تجريبية قابلة للتطوير والتحسين.</p>
</footer>

<script>
/* ورشة تطوير الفكرة */
let currentStep = 0;
const steps = document.querySelectorAll(".step");

function showStep() {
  steps.forEach((step, index) => {
    step.classList.toggle("active", index === currentStep);
  });

  document.getElementById("progress").style.width =
    ((currentStep / 4) * 100) + "%";
}

function nextStep(direction) {
  const next = currentStep + direction;

  if (next < 0 || next >= steps.length) return;

  if (direction > 0 && currentStep === 0) {
    if (!document.getElementById("ideaName").value.trim()) {
      alert("اكتب اسم فكرتك أولًا.");
      return;
    }
    if (!document.getElementById("ideaDesc").value.trim()) {
      alert("اكتب وصفًا مختصرًا لفكرتك أولًا.");
      return;
    }
  }

  currentStep = next;
  showStep();
}

function getValue(id) {
  return document.getElementById(id).value.trim() || "لم تتم الإجابة بعد";
}

function makeSummary() {
  const text =
`ملخص فكرة مشروع — نَمِّ فكرتك

اسم الفكرة:
${getValue("ideaName")}

المجال:
${getValue("ideaField")}

وصف الفكرة:
${getValue("ideaDesc")}

المشكلة:
${getValue("problem")}

الفئة المستفيدة:
${getValue("audience")}

الحل المقترح:
${getValue("solution")}

ما يميز الفكرة:
${getValue("difference")}

الأدوات والموارد:
${getValue("tools")}

التكلفة التقديرية:
${getValue("cost")}

الخطوة الأولى:
${getValue("firstStep")}

طريقة اختبار الفكرة:
${getValue("testPlan")}

ملاحظة:
هذا ملخص أولي مبني على إجابات المستخدم، وليس إثباتًا للجدوى أو الأصالة أو النجاح.`;

  const summary = document.getElementById("summary");
  summary.textContent = text;
  summary.style.display = "block";
  document.getElementById("summaryActions").style.display = "flex";
  document.getElementById("progress").style.width = "100%";
  summary.scrollIntoView({behavior: "smooth", block: "start"});
}

function copySummary() {
  const text = document.getElementById("summary").textContent;

  if (navigator.clipboard && window.isSecureContext) {
    navigator.clipboard.writeText(text)
      .then(() => alert("تم نسخ الملخص."))
      .catch(() => fallbackCopy(text));
  } else {
    fallbackCopy(text);
  }
}

function fallbackCopy(text) {
  const area = document.createElement("textarea");
  area.value = text;
  document.body.appendChild(area);
  area.select();
  try {
    document.execCommand("copy");
    alert("تم النسخ إن سمح المتصفح بذلك.");
  } catch (error) {
    alert("تعذر النسخ تلقائيًا. حددي النص وانسخيه يدويًا.");
  }
  area.remove();
}

function downloadSummary() {
  const text = document.getElementById("summary").textContent;
  const blob = new Blob(["\uFEFF" + text], {type: "text/plain;charset=utf-8"});
  const url = URL.createObjectURL(blob);
  const a = document.createElement("a");
  a.href = url;
  a.download = "ملخص-فكرتي.txt";
  a.click();
  URL.revokeObjectURL(url);
}

function saveDraft() {
  const ids = [
    "ideaName", "ideaField", "ideaDesc", "problem", "audience",
    "solution", "difference", "tools", "cost", "firstStep", "testPlan"
  ];
  const data = {};
  ids.forEach(id => data[id] = document.getElementById(id).value);

  try {
    localStorage.setItem("namiIdeaDraft", JSON.stringify(data));
    alert("حُفظت المسودة في هذا المتصفح.");
  } catch (error) {
    alert("لم يتم الحفظ. قد لا يدعم المتصفح التخزين في هذه الصفحة.");
  }
}

function loadDraft() {
  try {
    const data = JSON.parse(localStorage.getItem("namiIdeaDraft") || "{}");
    Object.keys(data).forEach(id => {
      const element = document.getElementById(id);
      if (element) element.value = data[id];
    });
  } catch (error) {
    console.log("لا توجد مسودة قابلة للقراءة.");
  }
}

loadDraft();

/* الألعاب التعليمية */
const quizzes = {
  critical: {
    name: "التفكير الناقد",
    questions: [
      {
        q: "قرأ شخص منشورًا يقول إن منتجًا ما يحل كل المشكلات. ما التصرف الأنسب؟",
        options: [
          "تصديقه فورًا",
          "البحث عن أدلة ومصادر مستقلة",
          "نشره دون قراءة"
        ],
        answer: 1,
        why: "التحقق من الأدلة والمصادر يساعد على تقييم الادعاء."
      },
      {
        q: "وجدت معلومتين متعارضتين على الإنترنت. ماذا تفعل؟",
        options: [
          "أختار الأقصر
