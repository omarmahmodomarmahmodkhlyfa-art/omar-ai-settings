# omar-ai-settings
OMAR AI - Settings static site (index.html) 
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>عمر AI - شركة عمر البغدادي للتصميم والعلوم البرمجية</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Google Fonts & Material Symbols -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;800;900&family=Space+Grotesk:wght@500;700&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200" />
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          colors: {
            brand: {
              gold: '#D4AF37',
              sand: '#d4b996',
              dark: '#121315',
              card: '#1b1c1e',
              border: '#2a2c30',
              accent: '#06b6d4'
            }
          },
          fontFamily: {
            cairo: ['Cairo', 'sans-serif'],
            mono: ['"JetBrains Mono"', 'monospace'],
            grotesk: ['"Space Grotesk"', 'sans-serif']
          }
        }
      }
    }
  </script>
  <style>
    body {
      font-family: 'Cairo', sans-serif;
      background-color: #0d0e10;
      color: #f3f4f6;
      -webkit-tap-highlight-color: transparent;
    }
    .custom-scroll::-webkit-scrollbar {
      width: 4px;
    }
    .custom-scroll::-webkit-scrollbar-thumb {
      background: #2a2c30;
      border-radius: 4px;
    }
    .pulse-glow {
      box-shadow: 0 0 15px rgba(212, 175, 55, 0.25);
    }
  </style>
</head>
<body class="flex flex-col h-screen max-w-md mx-auto border-x border-[#2a2c30] shadow-2xl relative bg-[#121315] select-none">

  <!-- TOP HEADER -->
  <header class="sticky top-0 z-40 bg-[#121315]/90 backdrop-blur-md border-b border-[#2a2c30] px-4 py-3 flex items-center justify-between">
    <div class="flex items-center gap-3">
      <div class="w-9 h-9 rounded-xl bg-gradient-to-tr from-[#D4AF37] to-amber-200 p-0.5 shadow-md flex items-center justify-center">
        <div class="w-full h-full bg-[#121315] rounded-[10px] flex items-center justify-center text-[#D4AF37] font-extrabold text-lg">
          ع
        </div>
      </div>
      <div>
        <div class="flex items-center gap-1.5">
          <span class="font-extrabold text-base tracking-wide text-white">عمر AI</span>
          <span class="w-2 h-2 rounded-full bg-emerald-400 animate-pulse"></span>
          <span class="text-[10px] bg-emerald-950/80 text-emerald-400 px-1.5 py-0.5 rounded border border-emerald-800/50 font-mono">v4.8 LIVE</span>
        </div>
        <p class="text-[10px] text-zinc-400 font-medium">شركة عمر البغدادي للتصميم والبرمجة</p>
      </div>
    </div>
    
    <div class="flex items-center gap-2">
      <button onclick="toggleTheme()" class="w-8 h-8 rounded-lg bg-zinc-800/80 hover:bg-zinc-700 flex items-center justify-center text-zinc-300 transition">
        <span class="material-symbols-outlined text-[18px]">palette</span>
      </button>
      <button onclick="showInfoModal()" class="w-8 h-8 rounded-lg bg-zinc-800/80 hover:bg-zinc-700 flex items-center justify-center text-zinc-300 transition">
        <span class="material-symbols-outlined text-[18px]">info</span>
      </button>
    </div>
  </header>

  <!-- MAIN SCROLLABLE CONTENT VIEWPORTS -->
  <main id="mainContainer" class="flex-1 overflow-y-auto custom-scroll p-4 space-y-4 pb-24">
    
    <!-- TAB 1: CHAT VIEW (DEFAULT) -->
    <section id="viewChat" class="space-y-4">
      <!-- Status pill banner -->
      <div class="bg-gradient-to-r from-amber-950/30 via-zinc-900 to-zinc-900 border border-amber-600/30 rounded-2xl p-3.5 flex items-center justify-between">
        <div class="flex items-center gap-2.5">
          <span class="material-symbols-outlined text-[#D4AF37]">neurology</span>
          <div>
            <h4 class="text-xs font-bold text-amber-200">النموذج الرافديني المعرفي</h4>
            <p class="text-[10px] text-zinc-400">توليد واجهات، تحليل شيفرات، تصميم هويات بصرية</p>
          </div>
        </div>
        <span class="text-[11px] font-mono text-[#D4AF37] bg-black/40 px-2 py-1 rounded-md border border-[#D4AF37]/20">0.38s</span>
      </div>

      <!-- Chat Messages Container -->
      <div id="chatMessages" class="space-y-3 pt-1">
        <!-- AI Message 1 -->
        <div class="flex items-start gap-2.5">
          <div class="w-7 h-7 rounded-lg bg-[#D4AF37]/20 border border-[#D4AF37]/40 flex items-center justify-center shrink-0 text-[#D4AF37]">
            <span class="material-symbols-outlined text-[16px]">smart_toy</span>
          </div>
          <div class="bg-[#1b1c1e] border border-[#2a2c30] rounded-2xl rounded-tr-sm p-3.5 max-w-[85%] text-xs text-zinc-200 leading-relaxed shadow-sm">
            مرحباً بك يا أستاذ عمر! أنا المساعد الذكي الخاص بشركة **عمر البغدادي للتصميم والعلوم البرمجية**. المنظومة جاهزة للعمل التفاعلي الحقيقي. يمكنك طلبي لتوليد تصاميم، فحص كود، أو بناء هوية بصرية فورية.
          </div>
        </div>

        <!-- AI Message 2 with code snippet -->
        <div class="flex items-start gap-2.5">
          <div class="w-7 h-7 rounded-lg bg-[#D4AF37]/20 border border-[#D4AF37]/40 flex items-center justify-center shrink-0 text-[#D4AF37]">
            <span class="material-symbols-outlined text-[16px]">terminal</span>
          </div>
          <div class="bg-[#1b1c1e] border border-[#2a2c30] rounded-2xl rounded-tr-sm p-3 max-w-[88%] text-xs text-zinc-200 shadow-sm space-y-2">
            <div class="flex items-center justify-between border-b border-zinc-800 pb-1.5 text-[10px] text-zinc-400 font-mono">
              <span>OmarBaghdadiEngine.ts</span>
              <span class="text-emerald-400">Compiled 100%</span>
            </div>
            <pre class="bg-black/60 p-2.5 rounded-lg font-mono text-[11px] text-amber-200 overflow-x-auto text-left" dir="ltr">const engine = new OmarAIEngine({
  client: "Baghdad Studio v4.8",
  status: "ACTIVE_LIVE"
});</pre>
            <div class="flex gap-2 pt-1">
              <button onclick="quickAction('توليد شعار رافديني')" class="text-[10px] bg-zinc-800 hover:bg-zinc-700 text-amber-300 px-2.5 py-1 rounded-full border border-zinc-700 transition">✨ توليد شعار</button>
              <button onclick="quickAction('فحص جاهزية النظام')" class="text-[10px] bg-zinc-800 hover:bg-zinc-700 text-cyan-300 px-2.5 py-1 rounded-full border border-zinc-700 transition">⚡ فحص النظام</button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- TAB 2: CANVAS & IMAGE STUDIO -->
    <section id="viewCanvas" class="hidden space-y-4">
      <div class="flex items-center justify-between">
        <h3 class="text-sm font-bold flex items-center gap-2">
          <span class="material-symbols-outlined text-[#D4AF37] text-base">brush</span>
          استوديو توليد الصور والكانفاس
        </h3>
        <span class="text-[10px] text-zinc-400 font-mono">4K Vector Ready</span>
      </div>

      <div class="relative bg-zinc-900 border border-zinc-800 rounded-2xl overflow-hidden aspect-video flex flex-col items-center justify-center p-4 text-center group">
        <div id="artPreview" class="w-24 h-24 rounded-full border-2 border-dashed border-[#D4AF37]/60 flex items-center justify-center bg-black/40 mb-2 transition-transform duration-500 group-hover:scale-105">
          <span class="material-symbols-outlined text-4xl text-[#D4AF37] animate-spin" style="animation-duration: 15s;">token</span>
        </div>
        <p id="artTitle" class="text-xs font-bold text-zinc-200">ختم بابل الهندسي - الجيل الرابع</p>
        <p class="text-[10px] text-zinc-500 font-mono mt-0.5">Vector Mesh • Seed: 884029</p>

        <div class="absolute bottom-2 flex gap-1.5">
          <button onclick="generateNewArt()" class="bg-[#D4AF37] hover:bg-amber-500 text-black font-bold text-[10px] px-3 py-1.5 rounded-lg flex items-center gap-1 shadow-md">
            <span class="material-symbols-outlined text-[13px]">refresh</span>
            توليد نموذج جديد
          </button>
          <button onclick="copyFeedback('تم نسخ صيغة الـ SVG بنجاح')" class="bg-zinc-800/90 hover:bg-zinc-700 text-zinc-300 text-[10px] px-3 py-1.5 rounded-lg flex items-center gap-1">
            <span class="material-symbols-outlined text-[13px]">download</span>
            تصدير SVG
          </button>
        </div>
      </div>

      <!-- Presets Grid -->
      <div class="grid grid-cols-2 gap-2">
        <div onclick="selectPreset('زخارف سومرية ذهبية')" class="bg-[#1b1c1e] hover:border-amber-500/50 border border-[#2a2c30] p-3 rounded-xl cursor-pointer transition">
          <span class="material-symbols-outlined text-amber-400 text-lg">auto_awesome</span>
          <h5 class="text-xs font-bold mt-1">زخرفة سومرية</h5>
          <p class="text-[9px] text-zinc-400">فيكتور هندسي دقيق</p>
        </div>
        <div onclick="selectPreset('مخطط معماري عصري')" class="bg-[#1b1c1e] hover:border-cyan-500/50 border border-[#2a2c30] p-3 rounded-xl cursor-pointer transition">
          <span class="material-symbols-outlined text-cyan-400 text-lg">architecture</span>
          <h5 class="text-xs font-bold mt-1">هندسة معمارية</h5>
          <p class="text-[9px] text-zinc-400">تصاميم واجهات حديثة</p>
        </div>
      </div>
    </section>

    <!-- TAB 3: VIDEO & MOTION STUDIO -->
    <section id="viewVideo" class="hidden space-y-4">
      <div class="flex items-center justify-between">
        <h3 class="text-sm font-bold flex items-center gap-2">
          <span class="material-symbols-outlined text-purple-400 text-base">movie_creation</span>
          استوديو توليد الفيديو الحركي
        </h3>
        <span class="text-[10px] text-emerald-400 bg-emerald-950/60 px-2 py-0.5 rounded border border-emerald-800/40 font-mono">GPU Active</span>
      </div>

      <div class="bg-[#1b1c1e] border border-[#2a2c30] rounded-2xl p-4 space-y-3">
        <div class="flex justify-between items-center text-xs">
          <span class="font-bold text-zinc-300">رندرة مشهد بغداد 2050 (360°)</span>
          <span id="renderPercent" class="text-purple-400 font-mono font-bold">78%</span>
        </div>
        <!-- Progress bar -->
        <div class="w-full bg-black/60 rounded-full h-2.5 overflow-hidden p-0.5 border border-zinc-800">
          <div id="renderBar" class="bg-gradient-to-r from-purple-500 to-amber-400 h-full rounded-full transition-all duration-300" style="width: 78%"></div>
        </div>
        <div class="flex justify-between text-[10px] text-zinc-400 font-mono">
          <span>الجودة: ProRes 4K 60fps</span>
          <span>الوقت المتبقي: 4 ثوانٍ</span>
        </div>
        <div class="flex gap-2 pt-2">
          <button onclick="simulateVideoRender()" class="flex-1 bg-purple-600 hover:bg-purple-500 text-white font-bold py-2 rounded-xl text-xs flex items-center justify-center gap-1.5">
            <span class="material-symbols-outlined text-sm">play_arrow</span>
            بدء رندرة تجريبية
          </button>
        </div>
      </div>
    </section>

    <!-- TAB 4: SETTINGS & DEPLOY -->
    <section id="viewSettings" class="hidden space-y-4">
      <div class="flex items-center justify-between">
        <h3 class="text-sm font-bold flex items-center gap-2">
          <span class="material-symbols-outlined text-[#D4AF37] text-base">settings</span>
          إعدادات النظام والتشغيل السحابي
        </h3>
      </div>

      <div class="bg-[#1b1c1e] border border-[#2a2c30] rounded-2xl p-4 space-y-3">
        <h4 class="text-xs font-bold text-amber-200">ربط النطاق والاستضافة</h4>
        <div class="bg-black/50 p-2.5 rounded-xl border border-zinc-800 text-[11px] font-mono text-zinc-300 flex items-center justify-between">
          <span class="truncate">https://app.omar-ai.com</span>
          <button onclick="copyFeedback('تم نسخ الرابط')" class="text-xs text-[#D4AF37] hover:underline font-bold shrink-0 mr-2">نسخ</button>
        </div>
        <p class="text-[10px] text-zinc-400">
          لتشغيل هذا الرابط فعلياً على الإنترنت، يمكنك رفع هذا الملف إلى أي استضافة مجانية مثل Vercel أو Cloudflare Pages أو GitHub Pages وتوجيه نطاقك إليه.
        </p>
      </div>

      <div class="bg-[#1b1c1e] border border-[#2a2c30] rounded-2xl p-4 space-y-2">
        <h4 class="text-xs font-bold text-zinc-200">الشركة المالكة</h4>
        <p class="text-xs text-zinc-400 font-semibold">شركة عمر البغدادي لتصميم الجرافيك والعلوم البرمجية</p>
        <p class="text-[10px] text-zinc-500 font-mono">الترخيص: برمجيات خاصة مؤسسية v4.8</p>
      </div>
    </section>

  </main>

  <!-- FLOATING INPUT BAR (ACTIVE IN CHAT VIEW) -->
  <div id="floatingInputArea" class="absolute bottom-16 left-0 right-0 p-3 bg-gradient-to-t from-[#121315] via-[#121315]/95 to-transparent z-30">
    <div class="bg-[#1b1c1e] border border-[#2a2c30] focus-within:border-[#D4AF37] rounded-2xl p-1.5 flex items-center gap-2 shadow-xl transition">
      <button onclick="quickAction('إرفاق ملف أو صورة')" class="w-8 h-8 rounded-xl text-zinc-400 hover:text-white flex items-center justify-center transition">
        <span class="material-symbols-outlined text-[20px]">attach_file</span>
      </button>
      <input id="userQueryInput" type="text" placeholder="اطلب أي فكرة تصميم، فحص كود، أو توليد مشهد..." 
        class="flex-1 bg-transparent text-xs text-white placeholder-zinc-500 focus:outline-none py-1.5 px-1 font-medium"
        onkeydown="if(event.key === 'Enter') handleSend();"
      >
      <button onclick="handleSend()" class="w-8 h-8 rounded-xl bg-gradient-to-tr from-[#D4AF37] to-amber-200 text-black font-bold flex items-center justify-center shadow-md hover:scale-105 active:scale-95 transition">
        <span class="material-symbols-outlined text-[18px]">arrow_upward</span>
      </button>
    </div>
  </div>

  <!-- BOTTOM NAVIGATION BAR -->
  <nav class="fixed bottom-0 max-w-md w-full bg-[#0d0e10]/95 backdrop-blur-xl border-t border-[#2a2c30] z-40 px-3 py-2 flex justify-around items-center">
    <button onclick="switchTab('chat')" id="navChat" class="flex flex-col items-center gap-0.5 text-[#D4AF37]">
      <span class="material-symbols-outlined text-[22px]">chat</span>
      <span class="text-[10px] font-bold">المحادثة</span>
    </button>

    <button onclick="switchTab('canvas')" id="navCanvas" class="flex flex-col items-center gap-0.5 text-zinc-400 hover:text-zinc-200">
      <span class="material-symbols-outlined text-[22px]">palette</span>
      <span class="text-[10px] font-medium">الكانفاس</span>
    </button>

    <button onclick="switchTab('video')" id="navVideo" class="flex flex-col items-center gap-0.5 text-zinc-400 hover:text-zinc-200">
      <span class="material-symbols-outlined text-[22px]">movie</span>
      <span class="text-[10px] font-medium">الفيديو</span>
    </button>

    <button onclick="switchTab('settings')" id="navSettings" class="flex flex-col items-center gap-0.5 text-zinc-400 hover:text-zinc-200">
      <span class="material-symbols-outlined text-[22px]">tune</span>
      <span class="text-[10px] font-medium">الإعدادات</span>
    </button>
  </nav>

  <!-- POPUP NOTIFICATION TOAST -->
  <div id="toast" class="fixed top-14 left-1/2 -translate-x-1/2 bg-zinc-900 border border-[#D4AF37] text-amber-200 text-xs px-4 py-2 rounded-xl shadow-2xl opacity-0 pointer-events-none transition-all duration-300 z-50 flex items-center gap-2">
    <span class="material-symbols-outlined text-sm">check_circle</span>
    <span id="toastText">تم بنجاح</span>
  </div>

  <script>
    // Tab Switching Logic
    function switchTab(tab) {
      const views = ['Chat', 'Canvas', 'Video', 'Settings'];
      views.forEach(v => {
        document.getElementById('view' + v).classList.add('hidden');
        document.getElementById('nav' + v).className = 'flex flex-col items-center gap-0.5 text-zinc-400 hover:text-zinc-200';
      });

      const selectedView = document.getElementById('view' + tab.charAt(0).toUpperCase() + tab.slice(1));
      const selectedNav = document.getElementById('nav' + tab.charAt(0).toUpperCase() + tab.slice(1));
      
      if (selectedView) selectedView.classList.remove('hidden');
      if (selectedNav) {
        selectedNav.className = 'flex flex-col items-center gap-0.5 text-[#D4AF37] font-bold';
      }

      const inputArea = document.getElementById('floatingInputArea');
      if (tab === 'chat') {
        inputArea.classList.remove('hidden');
      } else {
        inputArea.classList.add('hidden');
      }
    }

    // Interactive Sending
    function handleSend() {
      const input = document.getElementById('userQueryInput');
      const val = input.value.trim();
      if (!val) return;

      const chatContainer = document.getElementById('chatMessages');

      // Add user message
      const userDiv = document.createElement('div');
      userDiv.className = 'flex items-start justify-end gap-2';
      userDiv.innerHTML = `
        <div class="bg-amber-500/20 border border-amber-500/40 rounded-2xl rounded-tl-sm p-3 max-w-[85%] text-xs text-amber-100 shadow-sm leading-relaxed">
          ${val}
        </div>
      `;
      chatContainer.appendChild(userDiv);
      input.value = '';

      // Scroll to bottom
      const main = document.getElementById('mainContainer');
      main.scrollTop = main.scrollHeight;

      // Simulate AI Answer
      setTimeout(() => {
        const aiDiv = document.createElement('div');
        aiDiv.className = 'flex items-start gap-2.5';
        aiDiv.innerHTML = `
          <div class="w-7 h-7 rounded-lg bg-[#D4AF37]/20 border border-[#D4AF37]/40 flex items-center justify-center shrink-0 text-[#D4AF37]">
            <span class="material-symbols-outlined text-[16px]">smart_toy</span>
          </div>
          <div class="bg-[#1b1c1e] border border-[#2a2c30] rounded-2xl rounded-tr-sm p-3.5 max-w-[85%] text-xs text-zinc-200 leading-relaxed shadow-sm">
            تم استلام أمرك بنجاح من قبل محرك <strong>شركة عمر البغدادي AI</strong>! جاري المعالجة الفورية وتطبيق متطلباتك بدقة فائقة.
          </div>
        `;
        chatContainer.appendChild(aiDiv);
        main.scrollTop = main.scrollHeight;
      }, 600);
    }

    function quickAction(text) {
      document.getElementById('userQueryInput').value = text;
      handleSend();
    }

    function copyFeedback(msg) {
      showToast(msg);
    }

    function showToast(msg) {
      const toast = document.getElementById('toast');
      document.getElementById('toastText').innerText = msg;
      toast.classList.remove('opacity-0', 'pointer-events-none');
      setTimeout(() => {
        toast.classList.add('opacity-0', 'pointer-events-none');
      }, 2500);
    }

    // Art generation simulation
    const artPresets = [
      { title: "ختم بابل الهندسي - الجيل الرابع", icon: "token" },
      { title: "بوابة عشتار المستقبلية - سايبربانك", icon: "temple_hindu" },
      { title: "شعار عمر AI التفاعلي - المتجهات الذهبية", icon: "auto_awesome" },
      { title: "شريحة الرافدين المعرفية النيورونية", icon: "memory" }
    ];
    let artIndex = 0;
    function generateNewArt() {
      artIndex = (artIndex + 1) % artPresets.length;
      document.getElementById('artTitle').innerText = artPresets[artIndex].title;
      document.getElementById('artPreview').querySelector('span').innerText = artPresets[artIndex].icon;
      showToast('تم توليد تصميم جديد');
    }

    function selectPreset(name) {
      switchTab('canvas');
      document.getElementById('artTitle').innerText = name;
      showToast('تم اختيار النموذج: ' + name);
    }

    // Video render simulation
    function simulateVideoRender() {
      let p = 10;
      const bar = document.getElementById('renderBar');
      const text = document.getElementById('renderPercent');
      showToast('بدأت الرندرة الفورية...');
      const interval = setInterval(() => {
        p += 15;
        if (p >= 100) {
          p = 100;
          clearInterval(interval);
          showToast('اكتمل توليد الفيديو بنجاح بدقة 4K!');
        }
        bar.style.width = p + '%';
        text.innerText = p + '%';
      }, 300);
    }

    function toggleTheme() {
      showToast('نمط الرؤية: الوضع الليلي الفاخر (Obsidian Gold)');
    }

    function showInfoModal() {
      showToast('تطبيق عمر AI • شركة عمر البغدادي للتصميم والبرمجة');
    }
  </script>
</body>
</html>

