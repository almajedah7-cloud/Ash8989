<!DOCTYPE html>
<html lang="ar" dir="rtl" class="h-full"<!DOCTYPE html>
<html lang="ar" dir="rtl" class="h-full">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>خطة نجمات الانضباط - رمضان</title>
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <script src="/_sdk/data_sdk.js"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;800&display=swap" rel="stylesheet">
  <style>
    * { font-family: 'Tajawal', sans-serif; }
    .star-icon { transition: all 0.3s ease; }
    .star-icon:hover { transform: scale(1.2); }
    .card-hover { transition: all 0.3s ease; }
    .card-hover:hover { transform: translateY(-2px); box-shadow: 0 8px 25px rgba(0,0,0,0.15); }
    @keyframes sparkle {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.7; transform: scale(1.1); }
    }
    .sparkle { animation: sparkle 2s infinite; }
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
    .float { animation: float 3s ease-in-out infinite; }
    .gradient-bg {
      background: linear-gradient(135deg, #0c3b66 0%, #1565a0 50%, #0c3b66 100%);
    }
    .sky-gradient {
      background: linear-gradient(135deg, #00a8e8 0%, #00d4ff 50%, #00a8e8 100%);
    }
    .pattern-overlay {
      background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.05'%3E%3Cpath d='M30 30l15-15v30l-15-15zM30 30L15 15v30l15-15z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    }
  </style>
</head>
<body class="h-full gradient-bg pattern-overlay text-white overflow-auto">
  <div class="min-h-full p-4 md:p-6">
    <!-- Header Section -->
    <header class="text-center mb-6">
      <div class="inline-block mb-4">
        <div class="text-6xl float">🌙</div>
      </div>
      <h1 id="school-title" class="text-xl md:text-2xl font-bold text-cyan-300 mb-2">الابتدائية الثالثة وثمانون للطفولة المبكرة والروضة الملحقة بها</h1>
      <div class="sky-gradient text-gray-900 py-3 px-6 rounded-full inline-block shadow-lg">
        <h2 id="program-title" class="text-xl md:text-2xl font-extrabold">✨ نجمات الانضباط ✨</h2>
      </div>
      <p class="text-cyan-200 mt-3 text-lg">خطة الانضباط المدرسي في شهر رمضان المبارك</p>
      <div class="flex justify-center gap-4 mt-3 text-sm flex-wrap">
        <span class="bg-white/10 px-4 py-2 rounded-full">📅 المدة: 12 يوم</span>
        <span class="bg-white/10 px-4 py-2 rounded-full">⭐ الهدف: 12 نجمة</span>
      </div>
    </header>

    <!-- Goals & Values Section -->
    <div class="grid md:grid-cols-2 gap-4 mb-6 max-w-5xl mx-auto">
      <!-- Goals Card -->
      <div class="bg-white/10 backdrop-blur rounded-2xl p-5 card-hover border border-cyan-400/30">
        <div class="flex items-center justify-between gap-3 mb-4">
          <div class="flex items-center gap-3">
            <div class="w-12 h-12 bg-cyan-400 rounded-full flex items-center justify-center text-2xl">🎯</div>
            <h3 class="text-xl font-bold text-cyan-300">أهداف البرنامج</h3>
          </div>
          <button onclick="toggleGoalsEdit()" class="text-cyan-300 hover:text-cyan-100 text-2xl transition">✏️</button>
        </div>
        <ul id="goals-display" class="space-y-3 text-white/90">
          <!-- Goals will be displayed here -->
        </ul>
        <div id="goals-edit" class="hidden space-y-2 mt-3">
          <input type="text" id="goal-1" placeholder="الهدف الأول" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-cyan-400">
          <input type="text" id="goal-2" placeholder="الهدف الثاني" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-cyan-400">
          <input type="text" id="goal-3" placeholder="الهدف الثالث" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-cyan-400">
          <input type="text" id="goal-4" placeholder="الهدف الرابع" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-cyan-400">
          <button onclick="saveGoals()" class="w-full bg-cyan-500 hover:bg-cyan-600 text-white font-bold py-2 rounded-lg transition">حفظ</button>
        </div>
      </div>

      <!-- Values Card -->
      <div class="bg-white/10 backdrop-blur rounded-2xl p-5 card-hover border border-blue-400/30">
        <div class="flex items-center justify-between gap-3 mb-4">
          <div class="flex items-center gap-3">
            <div class="w-12 h-12 bg-blue-400 rounded-full flex items-center justify-center text-2xl">💎</div>
            <h3 class="text-xl font-bold text-blue-300">قيم رمضان</h3>
          </div>
          <button onclick="toggleValuesEdit()" class="text-blue-300 hover:text-blue-100 text-2xl transition">✏️</button>
        </div>
        <div id="values-display" class="grid grid-cols-2 gap-3">
          <!-- Values will be displayed here -->
        </div>
        <div id="values-edit" class="hidden space-y-2 mt-3">
          <input type="text" id="value-1" placeholder="القيمة الأولى" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-blue-400">
          <input type="text" id="value-2" placeholder="القيمة الثانية" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-blue-400">
          <input type="text" id="value-3" placeholder="القيمة الثالثة" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-blue-400">
          <input type="text" id="value-4" placeholder="القيمة الرابعة" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-blue-400">
          <button onclick="saveValues()" class="w-full bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 rounded-lg transition">حفظ</button>
        </div>
      </div>
    </div>

    <!-- Implementation Mechanism -->
    <div class="bg-white/10 backdrop-blur rounded-2xl p-5 mb-6 max-w-5xl mx-auto card-hover border border-cyan-400/20">
      <div class="flex items-center gap-3 mb-4">
        <div class="w-12 h-12 bg-blue-500 rounded-full flex items-center justify-center text-2xl">⚙️</div>
        <h3 class="text-xl font-bold text-blue-200">آلية التنفيذ</h3>
      </div>
      <div class="grid md:grid-cols-3 gap-4">
        <div class="bg-gradient-to-br from-cyan-500/30 to-blue-500/30 rounded-xl p-4 text-center">
          <div class="text-3xl mb-2">📋</div>
          <p class="font-bold mb-1">لوحة النجمات</p>
          <p class="text-sm text-white/80">لكل طالبة بطاقة باسمها وتتبع تطورها</p>
        </div>
        <div class="bg-gradient-to-br from-blue-500/30 to-cyan-500/30 rounded-xl p-4 text-center">
          <div class="text-3xl mb-2">⭐</div>
          <p class="font-bold mb-1">جمع النجمات</p>
          <p class="text-sm text-white/80">نجمة يومية عند تحقيق السلوك الحسن</p>
        </div>
        <div class="bg-gradient-to-br from-cyan-400/30 to-blue-400/30 rounded-xl p-4 text-center">
          <div class="text-3xl mb-2">🎁</div>
          <p class="font-bold mb-1">الجائزة والتكريم</p>
          <p class="text-sm text-white/80">شهادة تقدير عند جمع 12 نجمة</p>
        </div>
      </div>
    </div>

    <!-- Rewards Section -->
    <div class="bg-white/10 backdrop-blur rounded-2xl p-5 mb-6 max-w-5xl mx-auto card-hover border border-cyan-400/20">
      <div class="flex items-center gap-3 mb-4">
        <div class="w-12 h-12 bg-cyan-500 rounded-full flex items-center justify-center text-2xl">🎁</div>
        <h3 class="text-xl font-bold text-cyan-300">أمثلة الجوائز والحوافز</h3>
      </div>
      <div class="flex flex-wrap gap-3 justify-center">
        <span class="bg-gradient-to-r from-cyan-500/40 to-blue-500/40 px-4 py-2 rounded-full text-sm">📖 قصة قصيرة مشهورة</span>
        <span class="bg-gradient-to-r from-blue-500/40 to-cyan-500/40 px-4 py-2 rounded-full text-sm">👑 تاج نجمة رمضان</span>
        <span class="bg-gradient-to-r from-cyan-400/40 to-blue-400/40 px-4 py-2 rounded-full text-sm">📜 شهادة تقدير مختومة</span>
        <span class="bg-gradient-to-r from-blue-600/40 to-cyan-600/40 px-4 py-2 rounded-full text-sm">🌟 ملصقات ذهبية مميزة</span>
        <span class="bg-gradient-to-r from-cyan-600/40 to-blue-600/40 px-4 py-2 rounded-full text-sm">🍫 حلويات رمضانية فاخرة</span>
      </div>
    </div>

    <!-- Add Student Section -->
    <div class="bg-white/10 backdrop-blur rounded-2xl p-5 mb-6 max-w-5xl mx-auto border border-cyan-400/20">
      <div class="flex items-center gap-3 mb-4">
        <div class="w-12 h-12 bg-blue-500 rounded-full flex items-center justify-center text-2xl">➕</div>
        <h3 class="text-xl font-bold text-blue-300">إضافة طالبة جديدة</h3>
      </div>
      <form id="add-student-form" class="flex flex-col sm:flex-row gap-3">
        <input 
          type="text" 
          id="student-name" 
          placeholder="اسم الطالبة..." 
          class="flex-1 bg-white/20 border border-white/30 rounded-xl px-4 py-3 text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-cyan-400"
          required
        >
        <button 
          type="submit" 
          id="add-btn"
          class="bg-gradient-to-r from-cyan-400 to-blue-500 hover:from-cyan-500 hover:to-blue-600 text-white font-bold px-6 py-3 rounded-xl transition-all duration-300 flex items-center justify-center gap-2"
        >
          <span>إضافة</span>
          <span>✨</span>
        </button>
      </form>
      <p id="limit-warning" class="hidden text-red-300 text-sm mt-2 text-center">⚠️ تم الوصول للحد الأقصى (999 طالبة)</p>
    </div>

    <!-- Students Table -->
    <div class="bg-white/10 backdrop-blur rounded-2xl p-5 max-w-5xl mx-auto border border-cyan-400/20">
      <div class="flex items-center justify-between mb-4">
        <div class="flex items-center gap-3">
          <div class="w-12 h-12 bg-cyan-500 rounded-full flex items-center justify-center text-2xl">📊</div>
          <h3 class="text-xl font-bold text-cyan-300">جدول الطالبات والنجمات</h3>
        </div>
        <div id="student-count" class="bg-white/20 px-4 py-2 rounded-full text-sm">
          العدد: <span id="count-num">0</span>
        </div>
      </div>
      
      <div class="overflow-x-auto">
        <table class="w-full">
          <thead>
            <tr class="border-b border-cyan-400/30">
              <th class="text-right py-3 px-4 text-cyan-300">الاسم</th>
              <th class="text-center py-3 px-4 text-cyan-300">النجمات (12)</th>
              <th class="text-center py-3 px-4 text-cyan-300">إضافة نجمة</th>
              <th class="text-center py-3 px-4 text-cyan-300">شهادة</th>
              <th class="text-center py-3 px-4 text-cyan-300">حذف</th>
            </tr>
          </thead>
          <tbody id="students-table">
            <!-- Students will be added here -->
          </tbody>
        </table>
      </div>
      
      <div id="empty-state" class="text-center py-10 text-white/60">
        <div class="text-5xl mb-3">🌙</div>
        <p>لا توجد طالبات مسجلة حالياً</p>
        <p class="text-sm">أضيفي أسماء الطالبات لبدء البرنامج</p>
      </div>
    </div>

    <!-- Certificate Modal -->
    <div id="certificate-modal" class="fixed inset-0 bg-black/70 flex items-center justify-center p-4 z-50 hidden">
      <div class="bg-gradient-to-br from-cyan-50 to-blue-50 rounded-3xl p-8 max-w-lg w-full text-gray-800 relative shadow-2xl">
        <button onclick="closeCertificate()" class="absolute top-4 left-4 text-gray-500 hover:text-gray-700 text-2xl">&times;</button>
        <div class="text-center">
          <div class="text-6xl mb-4">🏆</div>
          <h2 class="text-2xl font-bold text-blue-700 mb-2">شهادة تقدير</h2>
          <div class="w-24 h-1 bg-gradient-to-r from-cyan-400 to-blue-500 mx-auto mb-4 rounded-full"></div>
          <p class="text-lg mb-2 text-gray-700">تُمنح هذه الشهادة للطالبة المتميزة</p>
          <p id="cert-name" class="text-3xl font-extrabold text-blue-600 mb-4">اسم الطالبة</p>
          <p class="text-gray-600 mb-4 leading-relaxed">لتحقيقها الانضباط المثالي والالتزام بقيم رمضان الكريمة وجمعها 12 نجمة في برنامج نجمات الانضباط</p>
          <div class="flex justify-center gap-2 text-4xl mb-4">
            <span>⭐</span><span>🌙</span><span>⭐</span>
          </div>
          <p class="text-sm text-gray-500 border-t border-gray-300 pt-3 mt-3">الابتدائية الثالثة وثمانون للطفولة المبكرة</p>
        </div>
      </div>
    </div>

    <!-- Footer -->
    <footer class="text-center mt-8 text-white/60 text-sm">
      <p>🌙 رمضان كريم 🌙</p>
      <p>نسأل الله أن يجعل طالباتنا من المتفوقات المنضبطات الملتزمات</p>
    </footer>
  </div>

  <script>
    // Default configuration
    const defaultConfig = {
      school_name: 'الابتدائية الثالثة وثمانون للطفولة المبكرة والروضة الملحقة بها',
      program_name: 'نجمات الانضباط',
      goal_1: 'تعزيز الانضباط الذاتي والتركيز والاهتمام داخل الصف الدراسي',
      goal_2: 'تشجيع السلوكيات الإيجابية والالتزام بالقيم الإسلامية النبيلة',
      goal_3: 'غرس قيم رمضان الكريمة من الصيام والعبادة والتسامح والعفو',
      goal_4: 'تقليل الفوضى والتأخر والحرص على احترام الوقت والنظام',
      value_1: 'الصمت والهدوء - الاستماع الفعال وعدم المقاطعة',
      value_2: 'احترام المعلم والزملاء والتعامل برقة وأدب وتهذيب',
      value_3: 'التعاون والتكافل - العمل بروح الفريق الواحد والترابط',
      value_4: 'الاستقامة والصدق - الالتزام بالوعود والمسؤولية والأمانة'
    };

    let config = { ...defaultConfig };
    let studentsData = [];
    let currentRecordCount = 0;
    let isGoalsEditOpen = false;
    let isValuesEditOpen = false;

    // Data Handler for Data SDK
    const dataHandler = {
      onDataChanged(data) {
        studentsData = data;
        currentRecordCount = data.length;
        renderStudentsTable();
      }
    };

    // Initialize Element SDK
    window.elementSdk.init({
      defaultConfig,
      onConfigChange: async (configData) => {
        config = { ...config, ...configData };
        const schoolTitle = document.getElementById('school-title');
        const programTitle = document.getElementById('program-title');
        
        if (schoolTitle) {
          schoolTitle.textContent = config.school_name || defaultConfig.school_name;
        }
        if (programTitle) {
          programTitle.textContent = `✨ ${config.program_name || defaultConfig.program_name} ✨`;
        }
        
        renderGoals();
        renderValues();
      },
      mapToCapabilities: (configData) => ({
        recolorables: [],
        borderables: [],
        fontEditable: undefined,
        fontSizeable: undefined
      }),
      mapToEditPanelValues: (configData) => new Map([
        ['school_name', configData.school_name || defaultConfig.school_name],
        ['program_name', configData.program_name || defaultConfig.program_name],
        ['goal_1', configData.goal_1 || defaultConfig.goal_1],
        ['goal_2', configData.goal_2 || defaultConfig.goal_2],
        ['goal_3', configData.goal_3 || defaultConfig.goal_3],
        ['goal_4', configData.goal_4 || defaultConfig.goal_4],
        ['value_1', configData.value_1 || defaultConfig.value_1],
        ['value_2', configData.value_2 || defaultConfig.value_2],
        ['value_3', configData.value_3 || defaultConfig.value_3],
        ['value_4', configData.value_4 || defaultConfig.value_4]
      ])
    });

    // Initialize Data SDK
    async function initApp() {
      const result = await window.dataSdk.init(dataHandler);
      if (!result.isOk) {
        console.error('Failed to initialize Data SDK');
      }
      renderGoals();
      renderValues();
    }

    // Render goals
    function renderGoals() {
      const display = document.getElementById('goals-display');
      display.innerHTML = '';
      
      for (let i = 1; i <= 4; i++) {
        const goalText = config[`goal_${i}`] || defaultConfig[`goal_${i}`];
        const li = document.createElement('li');
        li.className = 'flex items-start gap-3 bg-white/5 p-3 rounded-lg';
        li.innerHTML = `<span class="text-cyan-400 text-xl flex-shrink-0 mt-1">◆</span><span>${escapeHtml(goalText)}</span>`;
        display.appendChild(li);
      }
    }

    // Render values
    function renderValues() {
      const display = document.getElementById('values-display');
      display.innerHTML = '';
      
      const icons = ['🤫', '🤝', '👥', '✋'];
      for (let i = 1; i <= 4; i++) {
        const valueText = config[`value_${i}`] || defaultConfig[`value_${i}`];
        const div = document.createElement('div');
        div.className = 'bg-white/10 rounded-xl p-3 text-center hover:bg-white/15 transition';
        div.innerHTML = `
          <div class="text-2xl mb-2">${icons[i-1]}</div>
          <span class="text-sm line-clamp-3">${escapeHtml(valueText)}</span>
        `;
        display.appendChild(div);
      }
    }

    // Toggle goals edit
    function toggleGoalsEdit() {
      isGoalsEditOpen = !isGoalsEditOpen;
      document.getElementById('goals-display').classList.toggle('hidden');
      document.getElementById('goals-edit').classList.toggle('hidden');
      
      if (isGoalsEditOpen) {
        for (let i = 1; i <= 4; i++) {
          document.getElementById(`goal-${i}`).value = config[`goal_${i}`] || defaultConfig[`goal_${i}`];
        }
      }
    }

    // Toggle values edit
    function toggleValuesEdit() {
      isValuesEditOpen = !isValuesEditOpen;
      document.getElementById('values-display').classList.toggle('hidden');
      document.getElementById('values-edit').classList.toggle('hidden');
      
      if (isValuesEditOpen) {
        for (let i = 1; i <= 4; i++) {
          document.getElementById(`value-${i}`).value = config[`value_${i}`] || defaultConfig[`value_${i}`];
        }
      }
    }

    // Save goals
    async function saveGoals() {
      const newConfig = {};
      for (let i = 1; i <= 4; i++) {
        newConfig[`goal_${i}`] = document.getElementById(`goal-${i}`).value || defaultConfig[`goal_${i}`];
      }
      
      config = { ...config, ...newConfig };
      await window.elementSdk.setConfig(newConfig);
      renderGoals();
      toggleGoalsEdit();
    }

    // Save values
    async function saveValues() {
      const newConfig = {};
      for (let i = 1; i <= 4; i++) {
        newConfig[`value_${i}`] = document.getElementById(`value-${i}`).value || defaultConfig[`value_${i}`];
      }
      
      config = { ...config, ...newConfig };
      await window.elementSdk.setConfig(newConfig);
      renderValues();
      toggleValuesEdit();
    }

    // Render students table
    function renderStudentsTable() {
      const tableBody = document.getElementById('students-table');
      const emptyState = document.getElementById('empty-state');
      const countNum = document.getElementById('count-num');
      
      countNum.textContent = studentsData.length;
      
      if (studentsData.length === 0) {
        tableBody.innerHTML = '';
        emptyState.classList.remove('hidden');
        return;
      }
      
      emptyState.classList.add('hidden');
      
      const existingRows = new Map();
      [...tableBody.children].forEach(row => {
        existingRows.set(row.dataset.studentId, row);
      });
      
      const processedIds = new Set();
      
      studentsData.forEach(student => {
        processedIds.add(student.__backendId);
        
        if (existingRows.has(student.__backendId)) {
          const row = existingRows.get(student.__backendId);
          updateRowContent(row, student);
        } else {
          const row = createStudentRow(student);
          tableBody.appendChild(row);
        }
      });
      
      existingRows.forEach((row, id) => {
        if (!processedIds.has(id)) {
          row.remove();
        }
      });
    }

    function createStudentRow(student) {
      const row = document.createElement('tr');
      row.className = 'border-b border-cyan-400/20 hover:bg-white/5 transition';
      row.dataset.studentId = student.__backendId;
      updateRowContent(row, student);
      return row;
    }

    function updateRowContent(row, student) {
      const stars = student.stars || 0;
      const maxStars = 12;
      
      row.innerHTML = `
        <td class="py-3 px-4 font-bold">${escapeHtml(student.name)}</td>
        <td class="py-3 px-4">
          <div class="flex items-center justify-center gap-1 flex-wrap">
            ${generateStars(stars, maxStars, student.__backendId)}
          </div>
          <div class="text-center text-xs text-white/60 mt-1">${stars}/${maxStars}</div>
        </td>
        <td class="py-3 px-4 text-center">
          <button 
            onclick="addStar('${student.__backendId}')" 
            class="bg-gradient-to-r from-cyan-400 to-blue-500 hover:from-cyan-500 hover:to-blue-600 text-white px-3 py-1 rounded-lg text-sm transition-all ${stars >= maxStars ? 'opacity-50 cursor-not-allowed' : ''}"
            ${stars >= maxStars ? 'disabled' : ''}
          >
            +⭐
          </button>
        </td>
        <td class="py-3 px-4 text-center">
          ${stars >= maxStars ? 
            `<button onclick="showCertificate('${escapeHtml(student.name)}')" class="bg-gradient-to-r from-cyan-400 to-blue-500 hover:from-cyan-500 hover:to-blue-600 text-white px-3 py-1 rounded-lg text-sm font-bold transition-all sparkle">
              🏆 شهادة
            </button>` : 
            `<span class="text-white/40 text-sm">تحتاج ${maxStars - stars}</span>`
          }
        </td>
        <td class="py-3 px-4 text-center">
          <button 
            onclick="confirmDelete('${student.__backendId}')" 
            class="bg-red-500/30 hover:bg-red-500/50 text-red-300 px-3 py-1 rounded-lg text-sm transition-all"
            data-delete-btn="${student.__backendId}"
          >
            🗑️
          </button>
        </td>
      `;
    }

    function generateStars(count, max, studentId) {
      let html = '';
      for (let i = 0; i < max; i++) {
        if (i < count) {
          html += `<span class="star-icon text-xl cursor-pointer" onclick="removeStar('${studentId}', ${count})" title="انقر لإزالة نجمة">⭐</span>`;
        } else {
          html += `<span class="text-xl text-white/20">☆</span>`;
        }
      }
      return html;
    }

    function escapeHtml(text) {
      const div = document.createElement('div');
      div.textContent = text;
      return div.innerHTML;
    }

    // Add new student
    document.getElementById('add-student-form').addEventListener('submit', async (e) => {
      e.preventDefault();
      
      if (currentRecordCount >= 999) {
        document.getElementById('limit-warning').classList.remove('hidden');
        return;
      }
      
      const nameInput = document.getElementById('student-name');
      const addBtn = document.getElementById('add-btn');
      const name = nameInput.value.trim();
      
      if (!name) return;
      
      addBtn.disabled = true;
      addBtn.innerHTML = '<span>جاري الإضافة...</span>';
      
      const result = await window.dataSdk.create({
        id: Date.now().toString(),
        name: name,
        stars: 0,
        hasCertificate: false,
        createdAt: new Date().toISOString()
      });
      
      addBtn.disabled = false;
      addBtn.innerHTML = '<span>إضافة</span><span>✨</span>';
      
      if (result.isOk) {
        nameInput.value = '';
      }
    });

    // Add star to student
    async function addStar(studentId) {
      const student = studentsData.find(s => s.__backendId === studentId);
      if (!student || student.stars >= 12) return;
      
      const updatedStudent = { ...student, stars: student.stars + 1 };
      if (updatedStudent.stars >= 12) {
        updatedStudent.hasCertificate = true;
      }
      
      await window.dataSdk.update(updatedStudent);
    }

    // Remove star from student
    async function removeStar(studentId, currentStars) {
      const student = studentsData.find(s => s.__backendId === studentId);
      if (!student || currentStars <= 0) return;
      
      const updatedStudent = { ...student, stars: student.stars - 1 };
      await window.dataSdk.update(updatedStudent);
    }

    // Confirm delete with inline UI
    function confirmDelete(studentId) {
      const btn = document.querySelector(`[data-delete-btn="${studentId}"]`);
      if (!btn) return;
      
      btn.innerHTML = 'تأكيد؟';
      btn.className = 'bg-red-600 hover:bg-red-700 text-white px-3 py-1 rounded-lg text-sm transition-all';
      btn.onclick = () => deleteStudent(studentId);
      
      setTimeout(() => {
        if (btn) {
          btn.innerHTML = '🗑️';
          btn.className = 'bg-red-500/30 hover:bg-red-500/50 text-red-300 px-3 py-1 rounded-lg text-sm transition-all';
          btn.onclick = () => confirmDelete(studentId);
        }
      }, 3000);
    }

    // Delete student
    async function deleteStudent(studentId) {
      const student = studentsData.find(s => s.__backendId === studentId);
      if (!student) return;
      
      const btn = document.querySelector(`[data-delete-btn="${studentId}"]`);
      if (btn) {
        btn.innerHTML = 'جاري...';
        btn.disabled = true;
      }
      
      await window.dataSdk.delete(student);
    }

    // Show certificate modal
    function showCertificate(name) {
      document.getElementById('cert-name').textContent = name;
      document.getElementById('certificate-modal').classList.remove('hidden');
    }

    // Close certificate modal
    function closeCertificate() {
      document.getElementById('certificate-modal').classList.add('hidden');
    }

    // Close modal on outside click
    document.getElementById('certificate-modal').addEventListener('click', (e) => {
      if (e.target.id === 'certificate-modal') {
        closeCertificate();
      }
    });

    // Initialize app
    initApp();
  </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9cfbeaefe7822cf4',t:'MTc3MTQwMDg2MC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>خطة نجمات الانضباط - رمضان</title>
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <script src="/_sdk/data_sdk.js"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;800&display=swap" rel="stylesheet">
  <style>
    * { font-family: 'Tajawal', sans-serif; }
    .star-icon { transition: all 0.3s ease; }
    .star-icon:hover { transform: scale(1.2); }
    .card-hover { transition: all 0.3s ease; }
    .card-hover:hover { transform: translateY(-2px); box-shadow: 0 8px 25px rgba(0,0,0,0.15); }
    @keyframes sparkle {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.7; transform: scale(1.1); }
    }
    .sparkle { animation: sparkle 2s infinite; }
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
    .float { animation: float 3s ease-in-out infinite; }
    .gradient-bg {
      background: linear-gradient(135deg, #0c3b66 0%, #1565a0 50%, #0c3b66 100%);
    }
    .sky-gradient {
      background: linear-gradient(135deg, #00a8e8 0%, #00d4ff 50%, #00a8e8 100%);
    }
    .pattern-overlay {
      background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.05'%3E%3Cpath d='M30 30l15-15v30l-15-15zM30 30L15 15v30l15-15z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    }
  </style>
</head>
<body class="h-full gradient-bg pattern-overlay text-white overflow-auto">
  <div class="min-h-full p-4 md:p-6">
    <!-- Header Section -->
    <header class="text-center mb-6">
      <div class="inline-block mb-4">
        <div class="text-6xl float">🌙</div>
      </div>
      <h1 id="school-title" class="text-xl md:text-2xl font-bold text-cyan-300 mb-2">الابتدائية الثالثة وثمانون للطفولة المبكرة والروضة الملحقة بها</h1>
      <div class="sky-gradient text-gray-900 py-3 px-6 rounded-full inline-block shadow-lg">
        <h2 id="program-title" class="text-xl md:text-2xl font-extrabold">✨ نجمات الانضباط ✨</h2>
      </div>
      <p class="text-cyan-200 mt-3 text-lg">خطة الانضباط المدرسي في شهر رمضان المبارك</p>
      <div class="flex justify-center gap-4 mt-3 text-sm flex-wrap">
        <span class="bg-white/10 px-4 py-2 rounded-full">📅 المدة: 12 يوم</span>
        <span class="bg-white/10 px-4 py-2 rounded-full">⭐ الهدف: 12 نجمة</span>
      </div>
    </header>

    <!-- Goals & Values Section -->
    <div class="grid md:grid-cols-2 gap-4 mb-6 max-w-5xl mx-auto">
      <!-- Goals Card -->
      <div class="bg-white/10 backdrop-blur rounded-2xl p-5 card-hover border border-cyan-400/30">
        <div class="flex items-center justify-between gap-3 mb-4">
          <div class="flex items-center gap-3">
            <div class="w-12 h-12 bg-cyan-400 rounded-full flex items-center justify-center text-2xl">🎯</div>
            <h3 class="text-xl font-bold text-cyan-300">أهداف البرنامج</h3>
          </div>
          <button onclick="toggleGoalsEdit()" class="text-cyan-300 hover:text-cyan-100 text-2xl transition">✏️</button>
        </div>
        <ul id="goals-display" class="space-y-3 text-white/90">
          <!-- Goals will be displayed here -->
        </ul>
        <div id="goals-edit" class="hidden space-y-2 mt-3">
          <input type="text" id="goal-1" placeholder="الهدف الأول" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-cyan-400">
          <input type="text" id="goal-2" placeholder="الهدف الثاني" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-cyan-400">
          <input type="text" id="goal-3" placeholder="الهدف الثالث" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-cyan-400">
          <input type="text" id="goal-4" placeholder="الهدف الرابع" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-cyan-400">
          <button onclick="saveGoals()" class="w-full bg-cyan-500 hover:bg-cyan-600 text-white font-bold py-2 rounded-lg transition">حفظ</button>
        </div>
      </div>

      <!-- Values Card -->
      <div class="bg-white/10 backdrop-blur rounded-2xl p-5 card-hover border border-blue-400/30">
        <div class="flex items-center justify-between gap-3 mb-4">
          <div class="flex items-center gap-3">
            <div class="w-12 h-12 bg-blue-400 rounded-full flex items-center justify-center text-2xl">💎</div>
            <h3 class="text-xl font-bold text-blue-300">قيم رمضان</h3>
          </div>
          <button onclick="toggleValuesEdit()" class="text-blue-300 hover:text-blue-100 text-2xl transition">✏️</button>
        </div>
        <div id="values-display" class="grid grid-cols-2 gap-3">
          <!-- Values will be displayed here -->
        </div>
        <div id="values-edit" class="hidden space-y-2 mt-3">
          <input type="text" id="value-1" placeholder="القيمة الأولى" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-blue-400">
          <input type="text" id="value-2" placeholder="القيمة الثانية" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-blue-400">
          <input type="text" id="value-3" placeholder="القيمة الثالثة" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-blue-400">
          <input type="text" id="value-4" placeholder="القيمة الرابعة" class="w-full bg-white/10 border border-white/20 rounded-lg px-3 py-2 text-sm text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-blue-400">
          <button onclick="saveValues()" class="w-full bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 rounded-lg transition">حفظ</button>
        </div>
      </div>
    </div>

    <!-- Implementation Mechanism -->
    <div class="bg-white/10 backdrop-blur rounded-2xl p-5 mb-6 max-w-5xl mx-auto card-hover border border-cyan-400/20">
      <div class="flex items-center gap-3 mb-4">
        <div class="w-12 h-12 bg-blue-500 rounded-full flex items-center justify-center text-2xl">⚙️</div>
        <h3 class="text-xl font-bold text-blue-200">آلية التنفيذ</h3>
      </div>
      <div class="grid md:grid-cols-3 gap-4">
        <div class="bg-gradient-to-br from-cyan-500/30 to-blue-500/30 rounded-xl p-4 text-center">
          <div class="text-3xl mb-2">📋</div>
          <p class="font-bold mb-1">لوحة النجمات</p>
          <p class="text-sm text-white/80">لكل طالبة بطاقة باسمها وتتبع تطورها</p>
        </div>
        <div class="bg-gradient-to-br from-blue-500/30 to-cyan-500/30 rounded-xl p-4 text-center">
          <div class="text-3xl mb-2">⭐</div>
          <p class="font-bold mb-1">جمع النجمات</p>
          <p class="text-sm text-white/80">نجمة يومية عند تحقيق السلوك الحسن</p>
        </div>
        <div class="bg-gradient-to-br from-cyan-400/30 to-blue-400/30 rounded-xl p-4 text-center">
          <div class="text-3xl mb-2">🎁</div>
          <p class="font-bold mb-1">الجائزة والتكريم</p>
          <p class="text-sm text-white/80">شهادة تقدير عند جمع 12 نجمة</p>
        </div>
      </div>
    </div>

    <!-- Rewards Section -->
    <div class="bg-white/10 backdrop-blur rounded-2xl p-5 mb-6 max-w-5xl mx-auto card-hover border border-cyan-400/20">
      <div class="flex items-center gap-3 mb-4">
        <div class="w-12 h-12 bg-cyan-500 rounded-full flex items-center justify-center text-2xl">🎁</div>
        <h3 class="text-xl font-bold text-cyan-300">أمثلة الجوائز والحوافز</h3>
      </div>
      <div class="flex flex-wrap gap-3 justify-center">
        <span class="bg-gradient-to-r from-cyan-500/40 to-blue-500/40 px-4 py-2 rounded-full text-sm">📖 قصة قصيرة مشهورة</span>
        <span class="bg-gradient-to-r from-blue-500/40 to-cyan-500/40 px-4 py-2 rounded-full text-sm">👑 تاج نجمة رمضان</span>
        <span class="bg-gradient-to-r from-cyan-400/40 to-blue-400/40 px-4 py-2 rounded-full text-sm">📜 شهادة تقدير مختومة</span>
        <span class="bg-gradient-to-r from-blue-600/40 to-cyan-600/40 px-4 py-2 rounded-full text-sm">🌟 ملصقات ذهبية مميزة</span>
        <span class="bg-gradient-to-r from-cyan-600/40 to-blue-600/40 px-4 py-2 rounded-full text-sm">🍫 حلويات رمضانية فاخرة</span>
      </div>
    </div>

    <!-- Add Student Section -->
    <div class="bg-white/10 backdrop-blur rounded-2xl p-5 mb-6 max-w-5xl mx-auto border border-cyan-400/20">
      <div class="flex items-center gap-3 mb-4">
        <div class="w-12 h-12 bg-blue-500 rounded-full flex items-center justify-center text-2xl">➕</div>
        <h3 class="text-xl font-bold text-blue-300">إضافة طالبة جديدة</h3>
      </div>
      <form id="add-student-form" class="flex flex-col sm:flex-row gap-3">
        <input 
          type="text" 
          id="student-name" 
          placeholder="اسم الطالبة..." 
          class="flex-1 bg-white/20 border border-white/30 rounded-xl px-4 py-3 text-white placeholder-white/50 focus:outline-none focus:ring-2 focus:ring-cyan-400"
          required
        >
        <button 
          type="submit" 
          id="add-btn"
          class="bg-gradient-to-r from-cyan-400 to-blue-500 hover:from-cyan-500 hover:to-blue-600 text-white font-bold px-6 py-3 rounded-xl transition-all duration-300 flex items-center justify-center gap-2"
        >
          <span>إضافة</span>
          <span>✨</span>
        </button>
      </form>
      <p id="limit-warning" class="hidden text-red-300 text-sm mt-2 text-center">⚠️ تم الوصول للحد الأقصى (999 طالبة)</p>
    </div>

    <!-- Students Table -->
    <div class="bg-white/10 backdrop-blur rounded-2xl p-5 max-w-5xl mx-auto border border-cyan-400/20">
      <div class="flex items-center justify-between mb-4">
        <div class="flex items-center gap-3">
          <div class="w-12 h-12 bg-cyan-500 rounded-full flex items-center justify-center text-2xl">📊</div>
          <h3 class="text-xl font-bold text-cyan-300">جدول الطالبات والنجمات</h3>
        </div>
        <div id="student-count" class="bg-white/20 px-4 py-2 rounded-full text-sm">
          العدد: <span id="count-num">0</span>
        </div>
      </div>
      
      <div class="overflow-x-auto">
        <table class="w-full">
          <thead>
            <tr class="border-b border-cyan-400/30">
              <th class="text-right py-3 px-4 text-cyan-300">الاسم</th>
              <th class="text-center py-3 px-4 text-cyan-300">النجمات (12)</th>
              <th class="text-center py-3 px-4 text-cyan-300">إضافة نجمة</th>
              <th class="text-center py-3 px-4 text-cyan-300">شهادة</th>
              <th class="text-center py-3 px-4 text-cyan-300">حذف</th>
            </tr>
          </thead>
          <tbody id="students-table">
            <!-- Students will be added here -->
          </tbody>
        </table>
      </div>
      
      <div id="empty-state" class="text-center py-10 text-white/60">
        <div class="text-5xl mb-3">🌙</div>
        <p>لا توجد طالبات مسجلة حالياً</p>
        <p class="text-sm">أضيفي أسماء الطالبات لبدء البرنامج</p>
      </div>
    </div>

    <!-- Certificate Modal -->
    <div id="certificate-modal" class="fixed inset-0 bg-black/70 flex items-center justify-center p-4 z-50 hidden">
      <div class="bg-gradient-to-br from-cyan-50 to-blue-50 rounded-3xl p-8 max-w-lg w-full text-gray-800 relative shadow-2xl">
        <button onclick="closeCertificate()" class="absolute top-4 left-4 text-gray-500 hover:text-gray-700 text-2xl">&times;</button>
        <div class="text-center">
          <div class="text-6xl mb-4">🏆</div>
          <h2 class="text-2xl font-bold text-blue-700 mb-2">شهادة تقدير</h2>
          <div class="w-24 h-1 bg-gradient-to-r from-cyan-400 to-blue-500 mx-auto mb-4 rounded-full"></div>
          <p class="text-lg mb-2 text-gray-700">تُمنح هذه الشهادة للطالبة المتميزة</p>
          <p id="cert-name" class="text-3xl font-extrabold text-blue-600 mb-4">اسم الطالبة</p>
          <p class="text-gray-600 mb-4 leading-relaxed">لتحقيقها الانضباط المثالي والالتزام بقيم رمضان الكريمة وجمعها 12 نجمة في برنامج نجمات الانضباط</p>
          <div class="flex justify-center gap-2 text-4xl mb-4">
            <span>⭐</span><span>🌙</span><span>⭐</span>
          </div>
          <p class="text-sm text-gray-500 border-t border-gray-300 pt-3 mt-3">الابتدائية الثالثة وثمانون للطفولة المبكرة</p>
        </div>
      </div>
    </div>

    <!-- Footer -->
    <footer class="text-center mt-8 text-white/60 text-sm">
      <p>🌙 رمضان كريم 🌙</p>
      <p>نسأل الله أن يجعل طالباتنا من المتفوقات المنضبطات الملتزمات</p>
    </footer>
  </div>

  <script>
    // Default configuration
    const defaultConfig = {
      school_name: 'الابتدائية الثالثة وثمانون للطفولة المبكرة والروضة الملحقة بها',
      program_name: 'نجمات الانضباط',
      goal_1: 'تعزيز الانضباط الذاتي والتركيز والاهتمام داخل الصف الدراسي',
      goal_2: 'تشجيع السلوكيات الإيجابية والالتزام بالقيم الإسلامية النبيلة',
      goal_3: 'غرس قيم رمضان الكريمة من الصيام والعبادة والتسامح والعفو',
      goal_4: 'تقليل الفوضى والتأخر والحرص على احترام الوقت والنظام',
      value_1: 'الصمت والهدوء - الاستماع الفعال وعدم المقاطعة',
      value_2: 'احترام المعلم والزملاء والتعامل برقة وأدب وتهذيب',
      value_3: 'التعاون والتكافل - العمل بروح الفريق الواحد والترابط',
      value_4: 'الاستقامة والصدق - الالتزام بالوعود والمسؤولية والأمانة'
    };

    let config = { ...defaultConfig };
    let studentsData = [];
    let currentRecordCount = 0;
    let isGoalsEditOpen = false;
    let isValuesEditOpen = false;

    // Data Handler for Data SDK
    const dataHandler = {
      onDataChanged(data) {
        studentsData = data;
        currentRecordCount = data.length;
        renderStudentsTable();
      }
    };

    // Initialize Element SDK
    window.elementSdk.init({
      defaultConfig,
      onConfigChange: async (configData) => {
        config = { ...config, ...configData };
        const schoolTitle = document.getElementById('school-title');
        const programTitle = document.getElementById('program-title');
        
        if (schoolTitle) {
          schoolTitle.textContent = config.school_name || defaultConfig.school_name;
        }
        if (programTitle) {
          programTitle.textContent = `✨ ${config.program_name || defaultConfig.program_name} ✨`;
        }
        
        renderGoals();
        renderValues();
      },
      mapToCapabilities: (configData) => ({
        recolorables: [],
        borderables: [],
        fontEditable: undefined,
        fontSizeable: undefined
      }),
      mapToEditPanelValues: (configData) => new Map([
        ['school_name', configData.school_name || defaultConfig.school_name],
        ['program_name', configData.program_name || defaultConfig.program_name],
        ['goal_1', configData.goal_1 || defaultConfig.goal_1],
        ['goal_2', configData.goal_2 || defaultConfig.goal_2],
        ['goal_3', configData.goal_3 || defaultConfig.goal_3],
        ['goal_4', configData.goal_4 || defaultConfig.goal_4],
        ['value_1', configData.value_1 || defaultConfig.value_1],
        ['value_2', configData.value_2 || defaultConfig.value_2],
        ['value_3', configData.value_3 || defaultConfig.value_3],
        ['value_4', configData.value_4 || defaultConfig.value_4]
      ])
    });

    // Initialize Data SDK
    async function initApp() {
      const result = await window.dataSdk.init(dataHandler);
      if (!result.isOk) {
        console.error('Failed to initialize Data SDK');
      }
      renderGoals();
      renderValues();
    }

    // Render goals
    function renderGoals() {
      const display = document.getElementById('goals-display');
      display.innerHTML = '';
      
      for (let i = 1; i <= 4; i++) {
        const goalText = config[`goal_${i}`] || defaultConfig[`goal_${i}`];
        const li = document.createElement('li');
        li.className = 'flex items-start gap-3 bg-white/5 p-3 rounded-lg';
        li.innerHTML = `<span class="text-cyan-400 text-xl flex-shrink-0 mt-1">◆</span><span>${escapeHtml(goalText)}</span>`;
        display.appendChild(li);
      }
    }

    // Render values
    function renderValues() {
      const display = document.getElementById('values-display');
      display.innerHTML = '';
      
      const icons = ['🤫', '🤝', '👥', '✋'];
      for (let i = 1; i <= 4; i++) {
        const valueText = config[`value_${i}`] || defaultConfig[`value_${i}`];
        const div = document.createElement('div');
        div.className = 'bg-white/10 rounded-xl p-3 text-center hover:bg-white/15 transition';
        div.innerHTML = `
          <div class="text-2xl mb-2">${icons[i-1]}</div>
          <span class="text-sm line-clamp-3">${escapeHtml(valueText)}</span>
        `;
        display.appendChild(div);
      }
    }

    // Toggle goals edit
    function toggleGoalsEdit() {
      isGoalsEditOpen = !isGoalsEditOpen;
      document.getElementById('goals-display').classList.toggle('hidden');
      document.getElementById('goals-edit').classList.toggle('hidden');
      
      if (isGoalsEditOpen) {
        for (let i = 1; i <= 4; i++) {
          document.getElementById(`goal-${i}`).value = config[`goal_${i}`] || defaultConfig[`goal_${i}`];
        }
      }
    }

    // Toggle values edit
    function toggleValuesEdit() {
      isValuesEditOpen = !isValuesEditOpen;
      document.getElementById('values-display').classList.toggle('hidden');
      document.getElementById('values-edit').classList.toggle('hidden');
      
      if (isValuesEditOpen) {
        for (let i = 1; i <= 4; i++) {
          document.getElementById(`value-${i}`).value = config[`value_${i}`] || defaultConfig[`value_${i}`];
        }
      }
    }

    // Save goals
    async function saveGoals() {
      const newConfig = {};
      for (let i = 1; i <= 4; i++) {
        newConfig[`goal_${i}`] = document.getElementById(`goal-${i}`).value || defaultConfig[`goal_${i}`];
      }
      
      config = { ...config, ...newConfig };
      await window.elementSdk.setConfig(newConfig);
      renderGoals();
      toggleGoalsEdit();
    }

    // Save values
    async function saveValues() {
      const newConfig = {};
      for (let i = 1; i <= 4; i++) {
        newConfig[`value_${i}`] = document.getElementById(`value-${i}`).value || defaultConfig[`value_${i}`];
      }
      
      config = { ...config, ...newConfig };
      await window.elementSdk.setConfig(newConfig);
      renderValues();
      toggleValuesEdit();
    }

    // Render students table
    function renderStudentsTable() {
      const tableBody = document.getElementById('students-table');
      const emptyState = document.getElementById('empty-state');
      const countNum = document.getElementById('count-num');
      
      countNum.textContent = studentsData.length;
      
      if (studentsData.length === 0) {
        tableBody.innerHTML = '';
        emptyState.classList.remove('hidden');
        return;
      }
      
      emptyState.classList.add('hidden');
      
      const existingRows = new Map();
      [...tableBody.children].forEach(row => {
        existingRows.set(row.dataset.studentId, row);
      });
      
      const processedIds = new Set();
      
      studentsData.forEach(student => {
        processedIds.add(student.__backendId);
        
        if (existingRows.has(student.__backendId)) {
          const row = existingRows.get(student.__backendId);
          updateRowContent(row, student);
        } else {
          const row = createStudentRow(student);
          tableBody.appendChild(row);
        }
      });
      
      existingRows.forEach((row, id) => {
        if (!processedIds.has(id)) {
          row.remove();
        }
      });
    }

    function createStudentRow(student) {
      const row = document.createElement('tr');
      row.className = 'border-b border-cyan-400/20 hover:bg-white/5 transition';
      row.dataset.studentId = student.__backendId;
      updateRowContent(row, student);
      return row;
    }

    function updateRowContent(row, student) {
      const stars = student.stars || 0;
      const maxStars = 12;
      
      row.innerHTML = `
        <td class="py-3 px-4 font-bold">${escapeHtml(student.name)}</td>
        <td class="py-3 px-4">
          <div class="flex items-center justify-center gap-1 flex-wrap">
            ${generateStars(stars, maxStars, student.__backendId)}
          </div>
          <div class="text-center text-xs text-white/60 mt-1">${stars}/${maxStars}</div>
        </td>
        <td class="py-3 px-4 text-center">
          <button 
            onclick="addStar('${student.__backendId}')" 
            class="bg-gradient-to-r from-cyan-400 to-blue-500 hover:from-cyan-500 hover:to-blue-600 text-white px-3 py-1 rounded-lg text-sm transition-all ${stars >= maxStars ? 'opacity-50 cursor-not-allowed' : ''}"
            ${stars >= maxStars ? 'disabled' : ''}
          >
            +⭐
          </button>
        </td>
        <td class="py-3 px-4 text-center">
          ${stars >= maxStars ? 
            `<button onclick="showCertificate('${escapeHtml(student.name)}')" class="bg-gradient-to-r from-cyan-400 to-blue-500 hover:from-cyan-500 hover:to-blue-600 text-white px-3 py-1 rounded-lg text-sm font-bold transition-all sparkle">
              🏆 شهادة
            </button>` : 
            `<span class="text-white/40 text-sm">تحتاج ${maxStars - stars}</span>`
          }
        </td>
        <td class="py-3 px-4 text-center">
          <button 
            onclick="confirmDelete('${student.__backendId}')" 
            class="bg-red-500/30 hover:bg-red-500/50 text-red-300 px-3 py-1 rounded-lg text-sm transition-all"
            data-delete-btn="${student.__backendId}"
          >
            🗑️
          </button>
        </td>
      `;
    }

    function generateStars(count, max, studentId) {
      let html = '';
      for (let i = 0; i < max; i++) {
        if (i < count) {
          html += `<span class="star-icon text-xl cursor-pointer" onclick="removeStar('${studentId}', ${count})" title="انقر لإزالة نجمة">⭐</span>`;
        } else {
          html += `<span class="text-xl text-white/20">☆</span>`;
        }
      }
      return html;
    }

    function escapeHtml(text) {
      const div = document.createElement('div');
      div.textContent = text;
      return div.innerHTML;
    }

    // Add new student
    document.getElementById('add-student-form').addEventListener('submit', async (e) => {
      e.preventDefault();
      
      if (currentRecordCount >= 999) {
        document.getElementById('limit-warning').classList.remove('hidden');
        return;
      }
      
      const nameInput = document.getElementById('student-name');
      const addBtn = document.getElementById('add-btn');
      const name = nameInput.value.trim();
      
      if (!name) return;
      
      addBtn.disabled = true;
      addBtn.innerHTML = '<span>جاري الإضافة...</span>';
      
      const result = await window.dataSdk.create({
        id: Date.now().toString(),
        name: name,
        stars: 0,
        hasCertificate: false,
        createdAt: new Date().toISOString()
      });
      
      addBtn.disabled = false;
      addBtn.innerHTML = '<span>إضافة</span><span>✨</span>';
      
      if (result.isOk) {
        nameInput.value = '';
      }
    });

    // Add star to student
    async function addStar(studentId) {
      const student = studentsData.find(s => s.__backendId === studentId);
      if (!student || student.stars >= 12) return;
      
      const updatedStudent = { ...student, stars: student.stars + 1 };
      if (updatedStudent.stars >= 12) {
        updatedStudent.hasCertificate = true;
      }
      
      await window.dataSdk.update(updatedStudent);
    }

    // Remove star from student
    async function removeStar(studentId, currentStars) {
      const student = studentsData.find(s => s.__backendId === studentId);
      if (!student || currentStars <= 0) return;
      
      const updatedStudent = { ...student, stars: student.stars - 1 };
      await window.dataSdk.update(updatedStudent);
    }

    // Confirm delete with inline UI
    function confirmDelete(studentId) {
      const btn = document.querySelector(`[data-delete-btn="${studentId}"]`);
      if (!btn) return;
      
      btn.innerHTML = 'تأكيد؟';
      btn.className = 'bg-red-600 hover:bg-red-700 text-white px-3 py-1 rounded-lg text-sm transition-all';
      btn.onclick = () => deleteStudent(studentId);
      
      setTimeout(() => {
        if (btn) {
          btn.innerHTML = '🗑️';
          btn.className = 'bg-red-500/30 hover:bg-red-500/50 text-red-300 px-3 py-1 rounded-lg text-sm transition-all';
          btn.onclick = () => confirmDelete(studentId);
        }
      }, 3000);
    }

    // Delete student
    async function deleteStudent(studentId) {
      const student = studentsData.find(s => s.__backendId === studentId);
      if (!student) return;
      
      const btn = document.querySelector(`[data-delete-btn="${studentId}"]`);
      if (btn) {
        btn.innerHTML = 'جاري...';
        btn.disabled = true;
      }
      
      await window.dataSdk.delete(student);
    }

    // Show certificate modal
    function showCertificate(name) {
      document.getElementById('cert-name').textContent = name;
      document.getElementById('certificate-modal').classList.remove('hidden');
    }

    // Close certificate modal
    function closeCertificate() {
      document.getElementById('certificate-modal').classList.add('hidden');
    }

    // Close modal on outside click
    document.getElementById('certificate-modal').addEventListener('click', (e) => {
      if (e.target.id === 'certificate-modal') {
        closeCertificate();
      }
    });

    // Initialize app
    initApp();
  </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9cfbeaefe7822cf4',t:'MTc3MTQwMDg2MC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
