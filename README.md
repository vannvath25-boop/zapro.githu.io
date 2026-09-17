<meta name='viewport' content='width=device-width, initial-scale=1'/><!DOCTYPE html>
<html lang="km">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>XAUUSD Real Gemini AI Analyzer</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <link href="https://fonts.googleapis.com/css2?family=Kantumruy+Pro:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    * {
      font-family: 'Kantumruy Pro', sans-serif;
      -webkit-tap-highlight-color: transparent;
      touch-action: manipulation;
    }
    body {
      background-color: #0b0e14;
      color: #e2e8f0;
      overflow-x: hidden;
    }
    .gold-gradient {
      background: linear-gradient(135deg, #f59e0b 0%, #d97706 100%);
    }
    .glass-card {
      background: rgba(18, 24, 38, 0.85);
      backdrop-filter: blur(12px);
      border: 1px solid rgba(255, 255, 255, 0.08);
    }
  </style>
</head>
<body class="p-2 sm:p-4 md:p-6 min-h-screen pb-12">

  <!-- Header Section with Logo & About Button -->
  <header class="max-w-4xl mx-auto mb-4">
    <div class="glass-card rounded-2xl p-4 flex flex-col sm:flex-row items-center justify-between gap-3 border-l-4 border-amber-500 shadow-xl">
      <div class="flex items-center gap-3 w-full sm:w-auto">
        <!-- Logo -->
        <div class="w-12 h-12 rounded-xl overflow-hidden border border-amber-500/40 shadow-lg shrink-0 bg-slate-900 flex items-center justify-center">
          <img src="https://i.postimg.cc/0yS7bwYD/IMG-1822.jpg" alt="Logo" class="w-full h-full object-cover">
        </div>
        <div>
          <div class="flex items-center gap-2">
            <h1 class="text-lg font-bold text-white tracking-wide">ZA PRO</h1>
            <span class="bg-amber-500/20 text-amber-400 text-xs px-2 py-0.5 rounded-full border border-amber-500/30 font-semibold">AUTO-MODEL</span>
          </div>
          <p class="text-xs text-gray-400">ប្រព័ន្ធវិភាគ Chart មាសពិតៗដោយប្រើ ZA PRO</p>
        </div>
      </div>
      
      <!-- Right Controls: About & API Key Buttons -->
      <div class="flex items-center gap-2 w-full sm:w-auto">
        <button onclick="openAboutModal()" class="flex-1 sm:flex-none px-3 py-2.5 rounded-xl bg-slate-800 hover:bg-slate-700 text-gray-200 border border-slate-700 font-semibold text-xs flex items-center justify-center gap-1.5 transition active:scale-95 shadow-md">
          <i class="fa-solid fa-circle-info text-amber-400"></i>
          <span>អំពីយើង</span>
        </button>

        <button id="toggleApiKeyBtn" onclick="openKeyModal()" class="flex-1 sm:flex-none px-3 py-2.5 rounded-xl bg-slate-800 hover:bg-slate-700 text-amber-400 border border-amber-500/30 font-semibold text-xs flex items-center justify-center gap-1.5 transition active:scale-95 shadow-md">
          <i class="fa-solid fa-key"></i>
          <span id="keyStatusText">API Key</span>
        </button>
      </div>
    </div>
  </header>

  <!-- Main Container -->
  <main class="max-w-4xl mx-auto space-y-4">

    <!-- Upload & Action Box -->
    <section class="glass-card rounded-2xl p-4 shadow-xl">
      <h2 class="text-sm font-bold text-gray-300 mb-3 flex items-center gap-2">
        <i class="fa-solid fa-cloud-arrow-up text-amber-400"></i> ១. ជ្រើសរើសរូបភាព Chart XAUUSD
      </h2>

      <!-- Upload Zone -->
      <div id="dropZone" onclick="triggerFileInput()" class="border-2 border-dashed border-slate-700 hover:border-amber-500/50 bg-slate-900/60 rounded-xl p-4 text-center cursor-pointer transition relative min-h-[160px] flex flex-col items-center justify-center">
        <input type="file" id="chartInput" accept="image/*" class="hidden" onchange="handleFileSelect(event)">
        
        <div id="uploadPrompt" class="space-y-2">
          <i class="fa-solid fa-file-image text-3xl text-amber-400 mb-1"></i>
          <p class="text-xs text-gray-300 font-semibold">ចុចទីនេះ ដើម្បី Upload រូបភាព Chart</p>
          <p class="text-[10px] text-gray-500">(អាចទាញទម្លាក់រូបភាព ឬ Capture ពី TradingView)</p>
        </div>

        <div id="previewContainer" class="hidden w-full relative">
          <img id="chartPreview" class="max-h-60 mx-auto rounded-lg border border-slate-700 shadow-md object-contain" alt="Chart Preview">
          <button onclick="removeImage(event)" class="absolute top-1 right-1 bg-red-600/80 hover:bg-red-600 text-white w-7 h-7 rounded-full text-xs flex items-center justify-center shadow-md">
            <i class="fa-solid fa-xmark"></i>
          </button>
        </div>
      </div>

      <!-- Quick Controls -->
      <div class="grid grid-cols-1 sm:grid-cols-2 gap-2 mt-3">
        <button id="sampleBtn" onclick="loadSampleChart()" class="py-3 px-4 rounded-xl bg-slate-800 hover:bg-slate-700 text-xs font-semibold text-gray-200 border border-slate-700 flex items-center justify-center gap-2 active:scale-95 transition">
          <i class="fa-solid fa-wand-magic-sparkles text-amber-400"></i> ប្រើ Chart គំរូ (មិនទានដំណើកា)
        </button>

        <button id="analyzeBtn" onclick="analyzeChartWithAI()" class="py-3 px-4 rounded-xl gold-gradient text-black font-bold text-xs shadow-lg flex items-center justify-center gap-2 active:scale-95 transition">
          <i class="fa-solid fa-bolt"></i> Analysis
        </button>
      </div>
    </section>

    <!-- Signal Output Card -->
    <section class="glass-card rounded-2xl p-4 shadow-xl border-t-2 border-amber-500/40">
      <div class="flex items-center justify-between mb-3 border-b border-slate-800 pb-2">
        <h2 class="text-sm font-bold text-gray-200 flex items-center gap-2">
          <i class="fa-solid fa-square-poll-vertical text-amber-400"></i> ZA PRO AI Signal Analysis
        </h2>
        <span id="winRateBadge" class="bg-slate-800 text-amber-400 text-[11px] px-2.5 py-0.5 rounded-full border border-amber-500/20 font-bold">
          Win Rate: --%
        </span>
      </div>

      <!-- Signal Main Grid -->
      <div class="grid grid-cols-2 sm:grid-cols-4 gap-2 text-center mb-4">
        <div class="bg-slate-900/80 p-3 rounded-xl border border-slate-800 col-span-2 sm:col-span-1 flex flex-col justify-center">
          <span class="text-[10px] text-gray-400 block mb-1">SIGNAL ACTION</span>
          <span id="signalText" class="text-xl font-extrabold text-gray-500">WAITING</span>
        </div>

        <div class="bg-slate-900/80 p-3 rounded-xl border border-slate-800">
          <span class="text-[10px] text-gray-400 block mb-1">ENTRY PRICE</span>
          <span id="entryPrice" class="text-base font-bold text-amber-400">--.--</span>
        </div>

        <div class="bg-slate-900/80 p-3 rounded-xl border border-slate-800">
          <span class="text-[10px] text-red-400 block mb-1">STOP LOSS (SL)</span>
          <span id="slPrice" class="text-base font-bold text-red-400">--.--</span>
        </div>

        <div class="bg-slate-900/80 p-3 rounded-xl border border-slate-800">
          <span class="text-[10px] text-emerald-400 block mb-1">TAKE PROFIT (TP1)</span>
          <span id="tpPrice" class="text-base font-bold text-emerald-400">--.--</span>
        </div>
      </div>

      <!-- Detail Analysis Text -->
      <div class="bg-slate-900/90 rounded-xl p-3 border border-slate-800">
        <h3 class="text-xs font-bold text-gray-300 mb-1 flex items-center gap-1.5">
          <i class="fa-solid fa-align-left text-amber-400"></i> ការបកស្រាយបច្ចេកទេស (AI Reason)
        </h3>
        <p id="analysisReason" class="text-xs text-gray-400 leading-relaxed min-h-[60px]">
          សូម Upload រូបភាព Chart XAUUSD រួចចុចប៊ូតុង "វិភាគ Chart ដោយ AI" ដើម្បីទទួលបានការវិភាគបច្ចេកទេសលម្អិត។
        </p>
      </div>
    </section>

    <!-- Chat Assistant Section -->
    <section class="glass-card rounded-2xl p-4 shadow-xl">
      <h2 class="text-sm font-bold text-gray-300 mb-3 flex items-center gap-2">
        <i class="fa-solid fa-comments text-amber-400"></i> AI Trading Assistant (សួរនាំបន្ថែម)
      </h2>

      <div id="chatBox" class="bg-slate-900/90 rounded-xl p-3 h-48 overflow-y-auto space-y-2 border border-slate-800 mb-3 text-xs">
        <div class="bg-slate-800/80 p-2.5 rounded-lg max-w-[85%] text-gray-300">
          សួស្តី! ខ្ញុំជា AI ជំនួយការវិភាគ XAUUSD។ អ្នកអាចសួរសំណួរផ្សេងៗអំពីទីផ្សារមាសបាន!
        </div>
      </div>

      <div class="flex gap-2">
        <input type="text" id="chatInput" placeholder="សួរសំណួរអំពី XAUUSD..." onkeypress="if(event.key==='Enter') sendChatMessage()" class="flex-1 bg-slate-900 border border-slate-700 rounded-xl px-3 py-2 text-xs text-white focus:outline-none focus:border-amber-500">
        <button onclick="sendChatMessage()" class="px-4 py-2 bg-amber-500 hover:bg-amber-600 text-black font-bold rounded-xl text-xs flex items-center justify-center active:scale-95 transition">
          <i class="fa-solid fa-paper-plane"></i>
        </button>
      </div>
    </section>

  </main>

  <!-- ABOUT MODAL (Updated with Profile & Custom Description) -->
  <div id="aboutModal" class="fixed inset-0 bg-black/80 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
    <div class="glass-card rounded-2xl p-5 max-w-md w-full shadow-2xl border border-amber-500/35 text-center">
      <div class="flex justify-between items-center mb-2">
        <h3 class="text-sm font-bold text-amber-400 flex items-center gap-2">
          <i class="fa-solid fa-circle-info"></i> អំពីអ្នកបង្កើតវេបសាយ
        </h3>
        <button onclick="closeAboutModal()" class="text-gray-400 hover:text-white"><i class="fa-solid fa-xmark"></i></button>
      </div>

      <!-- Profile Image -->
      <div class="flex justify-center my-3">
        <div class="w-24 h-24 rounded-full overflow-hidden border-2 border-amber-500 shadow-xl bg-slate-900">
          <img src="https://i.postimg.cc/RVS6W3D7/IMG-0978.jpg" alt="VATH Profile" class="w-full h-full object-cover">
        </div>
      </div>

      <!-- Description Text -->
      <div class="space-y-3 text-xs text-gray-300 leading-relaxed text-left bg-slate-900/80 p-3.5 rounded-xl border border-slate-800">
        <p>
          វេបសាយនេះបង្កើតឡើងដោយ <strong class="text-amber-400">VATH</strong> ក្នុងការបង្កើតវេបសាយនេះមកគឺជួយដល់ការវិភាគទៅលើ XAUUSD អោយបានខ្លាំង ព្រោះវាមាន AI ខ្លាំងៗក្នុងនោះដូចជា GPT, Gemini, Claude ក្នុងការធ្វើការចូលគ្នាដើម្បីបោះ Signal នឹងមានបង្ហាញ ENTRY PRICE នឹង TAKE PROFIT នឹង STOP LOSS (SL) បានល្អ នឹងមានមុខងារចាំឆ្លើយសំណួរក្នុងនោះទៀតផង។
        </p>
      </div>

      <button onclick="closeAboutModal()" class="w-full mt-4 py-2.5 gold-gradient text-black font-bold text-xs rounded-xl shadow-md active:scale-95 transition">
        យល់ព្រម / បិទ
      </button>
    </div>
  </div>

  <!-- API KEY MODAL -->
  <div id="keyModal" class="fixed inset-0 bg-black/80 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
    <div class="glass-card rounded-2xl p-5 max-w-md w-full shadow-2xl border border-amber-500/30">
      <div class="flex justify-between items-center mb-3">
        <h3 class="text-sm font-bold text-amber-400 flex items-center gap-2">
          <i class="fa-solid fa-key"></i> កែប្រែ Gemini API Key
        </h3>
        <button onclick="closeKeyModal()" class="text-gray-400 hover:text-white"><i class="fa-solid fa-xmark"></i></button>
      </div>

      <p class="text-xs text-gray-300 mb-3 leading-relaxed">
        បញ្ចូល API Key ថ្មីរបស់អ្នកនៅទីនេះ៖
      </p>

      <input type="text" id="apiKeyInput" placeholder="Paste API Key ថ្មីនៅទីនេះ (AIzaSy...)" class="w-full bg-slate-900 border border-slate-700 rounded-xl px-3 py-2.5 text-xs text-white mb-3 focus:outline-none focus:border-amber-500">

      <div class="flex flex-col gap-2">
        <button onclick="saveApiKey()" class="w-full py-2.5 gold-gradient text-black font-bold text-xs rounded-xl shadow-md active:scale-95 transition">
          រក្សាទុក Key ថ្មី
        </button>
        <button onclick="clearStoredKey()" class="w-full py-2 bg-red-900/60 hover:bg-red-800 text-red-200 border border-red-700/50 font-bold text-xs rounded-xl transition">
          លុប Key ចាស់ចោល (Clear Cache)
        </button>
      </div>
    </div>
  </div>

  <script>
    let currentBase64Image = null;

    window.addEventListener('DOMContentLoaded', () => {
      const savedKey = localStorage.getItem('gemini_api_key');
      if (savedKey) {
        document.getElementById('apiKeyInput').value = savedKey;
        document.getElementById('keyStatusText').innerText = 'បានរក្សាទុក';
      }
    });

    function openAboutModal() {
      document.getElementById('aboutModal').classList.remove('hidden');
    }

    function closeAboutModal() {
      document.getElementById('aboutModal').classList.add('hidden');
    }

    function openKeyModal() {
      document.getElementById('keyModal').classList.remove('hidden');
    }

    function closeKeyModal() {
      document.getElementById('keyModal').classList.add('hidden');
    }

    function saveApiKey() {
      const key = document.getElementById('apiKeyInput').value.trim();
      if (!key) {
        alert('សូមបញ្ចូល API Key ត្រឹមត្រូវ!');
        return;
      }
      localStorage.setItem('gemini_api_key', key);
      document.getElementById('keyStatusText').innerText = 'បានរក្សាទុក';
      closeKeyModal();
      alert('រក្សាទុក API Key ថ្មីជោគជ័យ!');
    }

    function clearStoredKey() {
      localStorage.removeItem('gemini_api_key');
      document.getElementById('apiKeyInput').value = '';
      document.getElementById('keyStatusText').innerText = 'API Key';
      alert('បានលុប API Key ចាស់ចេញពី Web រួចរាល់!');
    }

    function triggerFileInput() {
      document.getElementById('chartInput').click();
    }

    function handleFileSelect(e) {
      const file = e.target.files[0];
      if (file) {
        processFile(file);
      }
    }

    function processFile(file) {
      const reader = new FileReader();
      reader.onload = function(e) {
        currentBase64Image = e.target.result;
        document.getElementById('chartPreview').src = currentBase64Image;
        document.getElementById('uploadPrompt').classList.add('hidden');
        document.getElementById('previewContainer').classList.remove('hidden');
      };
      reader.readAsDataURL(file);
    }

    function removeImage(e) {
      e.stopPropagation();
      currentBase64Image = null;
      document.getElementById('chartInput').value = '';
      document.getElementById('previewContainer').classList.add('hidden');
      document.getElementById('uploadPrompt').classList.remove('hidden');
    }

    function loadSampleChart() {
      const sampleSvg = `data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="600" height="300" viewBox="0 0 600 300" style="background:%230f172a;"><path d="M 50 220 L 120 180 L 200 210 L 280 130 L 360 160 L 450 90 L 550 110" stroke="%23eab308" stroke-width="4" fill="none"/><circle cx="550" cy="110" r="6" fill="%2322c55e"/><text x="50" y="50" fill="%23ffffff" font-size="18" font-family="sans-serif">XAUUSD H1 Chart Sample</text></svg>`;
      
      currentBase64Image = sampleSvg;
      document.getElementById('chartPreview').src = currentBase64Image;
      document.getElementById('uploadPrompt').classList.add('hidden');
      document.getElementById('previewContainer').classList.remove('hidden');
    }

    async function callGeminiStableAPI(apiKey, bodyData) {
      const activeModels = [
        'gemini-2.5-flash',
        'gemini-2.5-pro',
        'gemini-3.6-flash',
        'gemini-3.7-flash'
      ];

      let lastErr = null;

      for (const model of activeModels) {
        try {
          const res = await fetch(`https://generativelanguage.googleapis.com/v1beta/models/${model}:generateContent?key=${apiKey}`, {
            method: 'POST',
            headers: { 'Content-Type': 'application/json' },
            body: JSON.stringify(bodyData)
          });
          const data = await res.json();
          if (!data.error) {
            return data;
          }
          lastErr = data.error.message;
        } catch (err) {
          lastErr = err.message;
        }
      }
      throw new Error(lastErr || "API Request Failed");
    }

    async function analyzeChartWithAI() {
      const apiKey = localStorage.getItem('gemini_api_key');
      if (!apiKey) {
        alert('សូមបញ្ចូល Gemini API Key របស់អ្នកជាមុនសិន!');
        openKeyModal();
        return;
      }

      if (!currentBase64Image) {
        alert('សូម Upload រូបភាព Chart ឬចុចប៊ូតុង "ប្រើ Chart គំរូ" ជាមុនសិន!');
        return;
      }

      const analyzeBtn = document.getElementById('analyzeBtn');
      analyzeBtn.disabled = true;
      analyzeBtn.innerHTML = `<i class="fa-solid fa-spinner fa-spin"></i> កំពុងវិភាគដោយ AI...`;

      try {
        const base64Data = currentBase64Image.split(',')[1];
        const prompt = `Analyze this XAUUSD Gold chart image as a professional trader.
Return STRICT JSON format ONLY like this:
{
  "action": "BUY" or "SELL" or "HOLD",
  "win_rate": 85,
  "entry": "2650.50",
  "sl": "2642.00",
  "tp1": "2665.00",
  "reason": "Write concise technical analysis explanation in Khmer language describing market structure, support/resistance, or trend line setup."
}`;

        const requestBody = {
          contents: [{
            parts: [
              { text: prompt },
              { inline_data: { mime_type: "image/png", data: base64Data } }
            ]
          }]
        };

        const data = await callGeminiStableAPI(apiKey, requestBody);

        const rawText = data.candidates[0].content.parts[0].text;
        const jsonMatch = rawText.match(/\{[\s\S]*\}/);
        
        if (!jsonMatch) {
          throw new Error("AI មិនបានបោះទិន្នន័យជា JSON ត្រឹមត្រូវ");
        }

        const result = JSON.parse(jsonMatch[0]);

        const signalText = document.getElementById('signalText');
        signalText.innerText = result.action;
        signalText.className = `text-xl font-extrabold ${result.action === 'BUY' ? 'text-emerald-400' : result.action === 'SELL' ? 'text-red-400' : 'text-amber-400'}`;

        document.getElementById('winRateBadge').innerText = `Win Rate: ${result.win_rate}%`;
        document.getElementById('entryPrice').innerText = result.entry;
        document.getElementById('slPrice').innerText = result.sl;
        document.getElementById('tpPrice').innerText = result.tp1;
        document.getElementById('analysisReason').innerText = result.reason;

      } catch (err) {
        alert('ការវិភាគមានបញ្ហា៖ ' + err.message);
      } finally {
        analyzeBtn.disabled = false;
        analyzeBtn.innerHTML = `<i class="fa-solid fa-bolt"></i> ⚡ វិភាគ Chart ដោយ AI ពិតប្រាកដ`;
      }
    }

    async function sendChatMessage() {
      const apiKey = localStorage.getItem('gemini_api_key');
      const input = document.getElementById('chatInput');
      const msg = input.value.trim();

      if (!msg) return;
      if (!apiKey) {
        alert('សូមបញ្ចូល API Key ជាមុនសិន!');
        openKeyModal();
        return;
      }

      const chatBox = document.getElementById('chatBox');
      
      chatBox.innerHTML += `
        <div class="bg-amber-500/20 text-amber-300 p-2.5 rounded-lg max-w-[85%] ml-auto text-right font-medium">
          ${msg}
        </div>
      `;
      input.value = '';
      chatBox.scrollTop = chatBox.scrollHeight;

      try {
        const requestBody = {
          contents: [{ parts: [{ text: `You are an expert XAUUSD Gold Trading Assistant. Answer in Khmer: ${msg}` }] }]
        };

        const data = await callGeminiStableAPI(apiKey, requestBody);
        const reply = data.candidates[0].content.parts[0].text;

        chatBox.innerHTML += `
          <div class="bg-slate-800/80 p-2.5 rounded-lg max-w-[85%] text-gray-300">
            ${reply}
          </div>
        `;
        chatBox.scrollTop = chatBox.scrollHeight;
      } catch (err) {
        chatBox.innerHTML += `
          <div class="bg-red-900/40 text-red-400 p-2.5 rounded-lg max-w-[85%]">
            Error: ${err.message}
          </div>
        `;
      }
    }
  </script>
</body>
</html>
