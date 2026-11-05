

<!DOCTYPE html>
<html lang="km">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VATH Trading | AI Market Analysis</title>
    <link href="https://fonts.googleapis.com/css2?family=Kantumruy+Pro:wght@300;400;500;600;700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-base: #0b0e14;
            --bg-panel: rgba(21, 26, 36, 0.8);
            --bg-input: #0f131a;
            --border-color: #1f2937;
            --text-main: #e2e8f0;
            --text-muted: #94a3b8;
            --bullish: #00e676;
            --bullish-bg: rgba(0, 230, 118, 0.1);
            --bearish: #ff5252;
            --gold: #fbbf24;
            --gold-glow: rgba(251, 191, 36, 0.3);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: "Kantumruy Pro", "Inter", sans-serif;
            background-color: var(--bg-base);
            color: var(--text-main);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            overflow-x: hidden;
            background-image: 
                radial-gradient(circle at 15% 50%, rgba(0, 230, 118, 0.03) 0%, transparent 50%),
                radial-gradient(circle at 85% 30%, rgba(251, 191, 36, 0.03) 0%, transparent 50%);
        }

        /* ================= Top Header & Settings ================= */
        .top-nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 16px 24px;
            border-bottom: 1px solid var(--border-color);
            background: rgba(13, 17, 23, 0.8);
            backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .logo {
            font-family: "Inter", sans-serif;
            font-size: 24px;
            font-weight: 800;
            color: #fff;
            letter-spacing: -0.5px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .logo span { color: var(--gold); text-shadow: 0 0 15px var(--gold-glow); }
        
        .logo-badge {
            font-family: "Kantumruy Pro", sans-serif;
            font-size: 10px;
            background: var(--bullish-bg);
            color: var(--bullish);
            padding: 3px 8px;
            border-radius: 12px;
            border: 1px solid rgba(0, 230, 118, 0.3);
            font-weight: 600;
        }

        .settings-btn {
            background: transparent;
            border: 1px solid var(--border-color);
            color: var(--text-main);
            width: 42px;
            height: 42px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        .settings-btn:hover {
            background: rgba(255,255,255,0.05);
            border-color: var(--gold);
            color: var(--gold);
            transform: rotate(90deg);
        }
        .settings-btn svg { width: 22px; height: 22px; }

        /* ================= Ticker Bar ================= */
        .ticker-wrap {
            width: 100%;
            background: #0d1117;
            border-bottom: 1px solid var(--border-color);
            overflow: hidden;
            height: 40px;
            display: flex;
            align-items: center;
        }
        .ticker {
            display: flex;
            white-space: nowrap;
            animation: ticker 25s linear infinite;
        }
        .ticker:hover { animation-play-state: paused; }
        .ticker-item {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 0 24px;
            font-family: "Inter", sans-serif;
            font-size: 13px;
            font-weight: 600;
            border-right: 1px solid var(--border-color);
        }
        .ticker-item span.symbol { color: var(--text-muted); }
        .ticker-item span.price.buy { color: var(--bullish); }
        .ticker-item span.price.sell { color: var(--bearish); }

        @keyframes ticker {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        /* ================= Main Layout ================= */
        .main-wrapper {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 24px;
            max-width: 1100px;
            margin: 0 auto;
            padding: 30px 24px 60px;
            width: 100%;
            flex: 1;
        }

        /* ================= Panel Design ================= */
        .panel {
            background: var(--bg-panel);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 24px;
            backdrop-filter: blur(16px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .panel-header {
            font-size: 14px;
            font-weight: 700;
            color: #fff;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .panel-header svg { width: 18px; height: 18px; color: var(--gold); }

        /* ================= Upload Area ================= */
        .upload-zone {
            border: 2px dashed rgba(255,255,255,0.1);
            border-radius: 12px;
            padding: 50px 20px;
            text-align: center;
            cursor: pointer;
            background: rgba(0,0,0,0.2);
            transition: all 0.3s ease;
        }
        .upload-zone:hover, .upload-zone.dragover {
            border-color: var(--bullish);
            background: var(--bullish-bg);
        }
        .upload-icon { font-size: 40px; margin-bottom: 16px; display: block; color: var(--text-muted); }
        .upload-zone:hover .upload-icon { color: var(--bullish); }
        .upload-text { font-size: 14px; color: var(--text-muted); line-height: 1.8; }
        .upload-text strong { color: #fff; }

        .preview-img {
            max-width: 100%;
            max-height: 250px;
            border-radius: 8px;
            display: block;
            margin: 0 auto;
            box-shadow: 0 4px 20px rgba(0,0,0,0.6);
            border: 1px solid var(--border-color);
            cursor: pointer;
        }
        .file-input { display: none; }

        /* ================= Analyze Button ================= */
        .analyze-btn {
            width: 100%;
            padding: 18px;
            font-size: 16px;
            background: linear-gradient(135deg, var(--bullish), #00b359);
            color: #000;
            border: none;
            border-radius: 10px;
            font-weight: 700;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(0, 230, 118, 0.2);
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.2s;
        }
        .analyze-btn:hover:not(:disabled) {
            background: linear-gradient(135deg, #00ff84, #00e676);
            box-shadow: 0 6px 20px rgba(0, 230, 118, 0.4);
            transform: translateY(-2px);
        }
        .analyze-btn:disabled { opacity: 0.4; cursor: not-allowed; }

        /* ================= Result Area ================= */
        .result-container {
            display: none;
            flex-direction: column;
            flex: 1;
            background: var(--bg-input);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            overflow: hidden;
            position: relative;
        }
        .result-container.show { display: flex; }
        .result-container::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--bullish), var(--gold), var(--bearish));
        }

        .result-header {
            padding: 14px 20px;
            background: rgba(0,0,0,0.3);
            border-bottom: 1px solid var(--border-color);
            font-size: 13px;
            font-weight: 600;
            color: var(--text-muted);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .status-dot {
            display: inline-block;
            width: 8px; height: 8px;
            border-radius: 50%;
            background: var(--bullish);
            box-shadow: 0 0 8px var(--bullish);
            margin-right: 8px;
        }

        .result-content {
            padding: 24px;
            font-size: 14.5px;
            line-height: 1.9;
            color: #cbd5e1;
            overflow-y: auto;
            max-height: 550px;
        }
        .result-content::-webkit-scrollbar { width: 6px; }
        .result-content::-webkit-scrollbar-thumb { background: #334155; border-radius: 4px; }
        
        /* ការរចនាពិសេសសម្រាប់ប្រអប់ TP/SL/Entry */
        .trade-box {
            background: rgba(0,0,0,0.4);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            padding: 16px;
            margin: 16px 0;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
        }
        .trade-item {
            display: flex;
            flex-direction: column;
            gap: 4px;
        }
        .trade-label { font-size: 12px; color: var(--text-muted); text-transform: uppercase; letter-spacing: 0.5px; }
        .trade-value { font-family: "Inter", monospace; font-size: 16px; font-weight: 700; }
        .trade-value.entry { color: #fff; }
        .trade-value.tp { color: var(--bullish); }
        .trade-value.sl { color: var(--bearish); }
        
        /* ការរចនាសម្រាប់ចំណងជើងផ្នែក */
        .section-title {
            font-size: 14px;
            font-weight: 700;
            color: var(--gold);
            margin-top: 20px;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 6px;
        }
        .section-title::before {
            content: '';
            display: inline-block;
            width: 4px; height: 14px;
            background: var(--gold);
            border-radius: 2px;
        }

        .empty-state {
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            height: 100%; min-height: 400px; color: var(--text-muted); text-align: center;
        }

        /* ================= Loading & Error ================= */
        .loading-state {
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            padding: 50px 0; gap: 20px;
        }
        .loader {
            width: 40px; height: 40px;
            border: 3px solid rgba(0, 230, 118, 0.1);
            border-top-color: var(--bullish);
            border-radius: 50%;
            animation: spin 0.8s linear infinite;
        }
        .loading-text { font-size: 14px; color: var(--bullish); font-weight: 500; animation: pulse 1.5s ease-in-out infinite; }
        
        .error-state { text-align: center; padding: 30px; color: var(--bearish); }
        .retry-btn {
            margin-top: 20px; background: transparent; color: var(--text-main);
            border: 1px solid var(--bearish); padding: 8px 20px; font-size: 13px;
            border-radius: 6px; cursor: pointer; transition: 0.2s;
        }
        .retry-btn:hover { background: rgba(255, 82, 82, 0.1); }

        @keyframes spin { to { transform: rotate(360deg); } }
        @keyframes pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.5; } }

        /* ================= Settings Modal ================= */
        .modal-overlay {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.75); backdrop-filter: blur(8px);
            display: none; align-items: center; justify-content: center; z-index: 1000;
        }
        .modal-overlay.active { display: flex; }
        
        .modal-box {
            background: var(--bg-panel);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 28px;
            width: 100%;
            max-width: 420px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.6);
            animation: slideUp 0.3s ease;
        }
        @keyframes slideUp { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }

        .modal-header {
            display: flex; justify-content: space-between; align-items: center;
            margin-bottom: 24px; padding-bottom: 16px; border-bottom: 1px solid var(--border-color);
        }
        .modal-header h2 { font-size: 18px; font-weight: 700; color: #fff; }
        .close-btn { 
            background: rgba(255,255,255,0.05); border: 1px solid var(--border-color); 
            color: var(--text-muted); font-size: 20px; cursor: pointer; 
            width: 32px; height: 32px; border-radius: 50%; display: flex; 
            align-items: center; justify-content: center; transition: 0.2s;
        }
        .close-btn:hover { background: var(--bearish); color: #fff; border-color: var(--bearish); }

        .setting-group { margin-bottom: 24px; }
        .setting-label { font-size: 13px; color: var(--text-muted); margin-bottom: 10px; display: block; font-weight: 500; }
        
        .lang-switch { display: flex; gap: 10px; background: var(--bg-input); padding: 5px; border-radius: 10px; border: 1px solid var(--border-color); }
        .lang-btn {
            flex: 1; padding: 10px; background: transparent; border: none;
            color: var(--text-muted); border-radius: 8px; cursor: pointer; 
            font-weight: 600; transition: all 0.2s; font-family: "Inter", "Kantumruy Pro", sans-serif;
        }
        .lang-btn:hover { color: #fff; }
        .lang-btn.active { background: var(--bullish-bg); color: var(--bullish); box-shadow: 0 2px 10px rgba(0, 230, 118, 0.1); }

        .key-input-group { display: flex; gap: 10px; }
        .key-input {
            flex: 1; padding: 12px 16px; background: var(--bg-input); border: 1px solid var(--border-color);
            border-radius: 10px; color: #fff; outline: none; font-family: monospace; font-size: 14px;
            transition: border-color 0.2s;
        }
        .key-input:focus { border-color: var(--gold); }
        .save-btn {
            padding: 12px 20px; background: var(--gold); color: #000; border: none;
            border-radius: 10px; font-weight: 700; cursor: pointer; transition: all 0.2s;
        }
        .save-btn:hover { background: #fcd34d; }

        .status-msg { font-size: 13px; margin-top: 12px; display: none; padding: 10px 14px; border-radius: 8px; font-weight: 500; }
        .status-msg.success { display: block; background: var(--bullish-bg); color: var(--bullish); border: 1px solid rgba(0,230,118,0.2); }
        .status-msg.error { display: block; background: rgba(255, 82, 82, 0.1); color: var(--bearish); border: 1px solid rgba(255,82,82,0.2); }

        /* Footer */
        footer { text-align: center; padding: 24px; font-size: 12px; color: var(--text-muted); border-top: 1px solid var(--border-color); }

        /* Responsive */
        @media (max-width: 900px) {
            .main-wrapper { grid-template-columns: 1fr; padding: 20px 16px; }
            .ticker { animation-duration: 15s; }
        }
    </style>
</head>
<body>

    <!-- Top Navigation -->
    <div class="top-nav">
        <div class="logo">
            VATH <span>Trading</span>
            <div class="logo-badge" data-i18n="badge">AI ANALYZER</div>
        </div>
        <!-- Settings Button -->
        <button class="settings-btn" id="openSettingsBtn" title="Settings">
            <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"></path>
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
            </svg>
        </button>
    </div>

    <!-- Ticker Bar -->
    <div class="ticker-wrap">
        <div class="ticker">
            <div class="ticker-item"><span class="symbol">XAUUSD</span><span class="price buy">▲ 2,385.50</span></div>
            <div class="ticker-item"><span class="symbol">BTCUSDT</span><span class="price buy">▲ 67,432.00</span></div>
            <div class="ticker-item"><span class="symbol">EURUSD</span><span class="price sell">▼ 1.0842</span></div>
            <div class="ticker-item"><span class="symbol">GBPUSD</span><span class="price sell">▼ 1.2631</span></div>
            <div class="ticker-item"><span class="symbol">USDJPY</span><span class="price buy">▲ 151.42</span></div>
            <!-- Duplicate for smooth loop -->
            <div class="ticker-item"><span class="symbol">XAUUSD</span><span class="price buy">▲ 2,385.50</span></div>
            <div class="ticker-item"><span class="symbol">BTCUSDT</span><span class="price buy">▲ 67,432.00</span></div>
            <div class="ticker-item"><span class="symbol">EURUSD</span><span class="price sell">▼ 1.0842</span></div>
            <div class="ticker-item"><span class="symbol">GBPUSD</span><span class="price sell">▼ 1.2631</span></div>
            <div class="ticker-item"><span class="symbol">USDJPY</span><span class="price buy">▲ 151.42</span></div>
        </div>
    </div>

    <!-- Main Content -->
    <div class="main-wrapper">
        
        <!-- Left Column (Upload) -->
        <div class="panel">
            <div class="panel-header">
                <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z"></path></svg>
                <span data-i18n="upload_header">ទិន្នន័យតារាង XAUUSD</span>
            </div>
            
            <div class="upload-zone" id="uploadArea">
                <input type="file" class="file-input" id="fileInput" accept="image/png,image/jpeg,image/webp">
                <span class="upload-icon">📊</span>
                <div class="upload-text" data-i18n="upload_text">
                    <strong>អូស ឬចុច</strong> ដើម្បីផ្ទុករូបភាពតារាង<br>
                    <small>PNG, JPG (អតិបរមា 7MB)</small>
                </div>
            </div>
            <img id="previewImg" class="preview-img" style="display:none;">

            <button class="analyze-btn" id="analyzeBtn" disabled data-i18n="analyze_btn">
                ចាប់ផ្តើមវិភាគទីផ្សារ
            </button>
        </div>

        <!-- Right Column (Result) -->
        <div class="panel" style="padding: 0; background: transparent; border: none; box-shadow: none;">
            
            <div class="result-container" id="resultPanel">
                <div class="result-header">
                    <div><span class="status-dot"></span> <span data-i18n="result_header">របាយការណ៍វិភាគ AI</span></div>
                    <div style="font-family: monospace;">XAUUSD</div>
                </div>
                <div class="result-content" id="resultArea"></div>
            </div>
            
            <div class="empty-state" id="emptyState">
                <svg style="width:64px; height:64px; margin-bottom:20px; opacity:0.2;" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"></path></svg>
                <p style="font-size:15px;" data-i18n="empty_title">មិនទាន់មានទិន្នន័យវិភាគនៅឡើយទេ</p>
                <p style="font-size:13px; margin-top:8px; opacity:0.7;" data-i18n="empty_sub">សូមផ្ទុករូបភាពតារាង ហើយចុច "ចាប់ផ្តើមវិភាគ"</p>
            </div>
        </div>

    </div>

    <!-- ================= Settings Modal ================= -->
    <div class="modal-overlay" id="settingsModal">
        <div class="modal-box">
            <div class="modal-header">
                <h2 data-i18n="settings_title">ការកំណត់</h2>
                <button class="close-btn" id="closeSettingsBtn">&times;</button>
            </div>

            <!-- Language Setting -->
            <div class="setting-group">
                <label class="setting-label" data-i18n="lang_label">ភាសា / Language</label>
                <div class="lang-switch">
                    <button class="lang-btn active" id="btnKm" onclick="setLanguage('km')">ខ្មែរ</button>
                    <button class="lang-btn" id="btnEn" onclick="setLanguage('en')">English</button>
                </div>
            </div>

            <!-- API Key Setting -->
            <div class="setting-group">
                <label class="setting-label" data-i18n="api_label">Gemini API Key</label>
                <div class="key-input-group">
                    <input type="password" class="key-input" id="apiKeyInput" placeholder="AIzaSy...">
                    <button class="save-btn" id="saveKeyBtn" data-i18n="save_btn">រក្សាទុក</button>
                </div>
                <div class="status-msg" id="statusMsg"></div>
            </div>
        </div>
    </div>

    <footer>
        &copy; 2026 VATH Trading. All rights reserved.
    </footer>

    <!-- ================= Main JavaScript ================= -->
    <script>
        // 1. Translation Dictionary
        const translations = {
            km: {
                badge: "AI ANALYZER",
                upload_header: "ទិន្នន័យតារាង XAUUSD",
                upload_text: "<strong>អូស ឬចុច</strong> ដើម្បីផ្ទុករូបភាពតារាង<br><small>PNG, JPG (អតិបរមា 7MB)</small>",
                analyze_btn: "ចាប់ផ្តើមវិភាគទីផ្សារ",
                result_header: "របាយការណ៍វិភាគ AI",
                empty_title: "មិនទាន់មានទិន្នន័យវិភាគនៅឡើយទេ",
                empty_sub: "សូមផ្ទុករូបភាពតារាង ហើយចុច \"ចាប់ផ្តើមវិភាគ\"",
                settings_title: "ការកំណត់",
                lang_label: "ភាសា / Language",
                api_label: "Gemini API Key",
                save_btn: "រក្សាទុក",
                saved_msg: "✅ បានរក្សាទុកដោយជោគជ័យ",
                key_removed: "🗑️ បានលុប Key ចេញ",
                retry: "ព្យាយាមម្តងទៀត",
                loading: "AI កំពុងវិភាគទិន្នន័យតារាង...",
                wait_retry: "ទីផ្សារកំពុងរវល់ កំពុងព្យាយាមឡើងវិញ",
                error_title: "មានបញ្ហាកើតឡើង",
                analyzing: "កំពុងវិភាគ..."
            },
            en: {
                badge: "AI ANALYZER",
                upload_header: "XAUUSD Chart Data",
                upload_text: "<strong>Drag or Click</strong> to upload chart<br><small>PNG, JPG (Max 7MB)</small>",
                analyze_btn: "Start Market Analysis",
                result_header: "AI Analysis Report",
                empty_title: "No analysis data yet",
                empty_sub: "Please upload a chart and click \"Start Analysis\"",
                settings_title: "Settings",
                lang_label: "Language",
                api_label: "Gemini API Key",
                save_btn: "Save",
                saved_msg: "✅ Saved successfully",
                key_removed: "🗑️ Key removed",
                retry: "Retry",
                loading: "AI is analyzing the chart...",
                wait_retry: "Market busy, retrying",
                error_title: "An error occurred",
                analyzing: "Analyzing..."
            }
        };

        let currentLang = localStorage.getItem('vath_lang') || 'km';

        // 2. Set Language Function
        function setLanguage(lang) {
            currentLang = lang;
            localStorage.setItem('vath_lang', lang);
            
            // Update buttons active state
            document.getElementById('btnKm').classList.toggle('active', lang === 'km');
            document.getElementById('btnEn').classList.toggle('active', lang === 'en');

            // Translate all elements with data-i18n
            document.querySelectorAll('[data-i18n]').forEach(el => {
                const key = el.getAttribute('data-i18n');
                if (translations[lang][key]) {
                    el.innerHTML = translations[lang][key];
                }
            });

            // Update upload text if no image is selected
            if (currentImageBase64 === null) {
                document.querySelector('.upload-text').innerHTML = translations[lang].upload_text;
            }
        }

        // 3. Modal Logic
        const modal = document.getElementById('settingsModal');
        const openBtn = document.getElementById('openSettingsBtn');
        const closeBtn = document.getElementById('closeSettingsBtn');

        openBtn.addEventListener('click', () => modal.classList.add('active'));
        closeBtn.addEventListener('click', () => modal.classList.remove('active'));
        modal.addEventListener('click', (e) => {
            if (e.target === modal) modal.classList.remove('active');
        });

        // 4. API Key Logic
        const apiKeyInput = document.getElementById('apiKeyInput');
        const saveKeyBtn = document.getElementById('saveKeyBtn');
        const statusMsg = document.getElementById('statusMsg');
        
        const savedKey = localStorage.getItem('vath_gemini_api_key');
        if (savedKey) apiKeyInput.value = savedKey;

        saveKeyBtn.addEventListener('click', () => {
            const key = apiKeyInput.value.trim();
            if (key) {
                localStorage.setItem('vath_gemini_api_key', key);
                statusMsg.textContent = translations[currentLang].saved_msg;
                statusMsg.className = 'status-msg success';
                updateAnalyzeBtn();
                setTimeout(() => { statusMsg.className = 'status-msg'; }, 2500);
            } else {
                localStorage.removeItem('vath_gemini_api_key');
                statusMsg.textContent = translations[currentLang].key_removed;
                statusMsg.className = 'status-msg error';
                updateAnalyzeBtn();
            }
        });

        // 5. App Variables
        let currentImageBase64 = null;
        let currentImageMime = null;

        const uploadArea = document.getElementById('uploadArea');
        const fileInput = document.getElementById('fileInput');
        const previewImg = document.getElementById('previewImg');
        const analyzeBtn = document.getElementById('analyzeBtn');
        const resultPanel = document.getElementById('resultPanel');
        const resultArea = document.getElementById('resultArea');
        const emptyState = document.getElementById('emptyState');

        // 6. File Upload Logic
        uploadArea.addEventListener('click', () => fileInput.click());
        uploadArea.addEventListener('dragover', (e) => { e.preventDefault(); uploadArea.classList.add('dragover'); });
        uploadArea.addEventListener('dragleave', () => uploadArea.classList.remove('dragover'));
        uploadArea.addEventListener('drop', (e) => {
            e.preventDefault();
            uploadArea.classList.remove('dragover');
            if (e.dataTransfer.files[0]) handleFile(e.dataTransfer.files[0]);
        });
        fileInput.addEventListener('change', (e) => {
            if (e.target.files[0]) handleFile(e.target.files[0]);
        });

        function handleFile(file) {
            if (!['image/png', 'image/jpeg', 'image/webp'].includes(file.type)) {
                alert(currentLang === 'km' ? 'សូមផ្ទុករូបភាព PNG, JPG ឬ WebP ប៉ុណ្ណោះ' : 'Please upload PNG, JPG or WebP only');
                return;
            }
            if (file.size > 7 * 1024 * 1024) {
                alert(currentLang === 'km' ? 'រូបភាពធំពេក (ក្រោម 7MB)' : 'Image too large (Under 7MB)');
                return;
            }
            const reader = new FileReader();
            reader.onload = (e) => {
                const dataUrl = e.target.result;
                currentImageBase64 = dataUrl.split(',')[1];
                currentImageMime = file.type;
                previewImg.src = dataUrl;
                previewImg.style.display = 'block';
                uploadArea.style.display = 'none';
                updateAnalyzeBtn();
            };
            reader.readAsDataURL(file);
        }

        // Allow clicking preview to change image
        previewImg.addEventListener('click', () => {
            uploadArea.style.display = 'block';
            previewImg.style.display = 'none';
            currentImageBase64 = null;
            fileInput.value = '';
            updateAnalyzeBtn();
        });

        function updateAnalyzeBtn() {
            const hasKey = apiKeyInput.value.trim().length > 0 || localStorage.getItem('vath_gemini_api_key');
            const hasImage = currentImageBase64 !== null;
            analyzeBtn.disabled = !(hasKey && hasImage);
        }
        apiKeyInput.addEventListener('input', updateAnalyzeBtn);

        // 7. Fetch with Retry (For 503 High Demand errors)
        async function fetchWithRetry(url, options, maxRetries = 3) {
            for (let i = 0; i < maxRetries; i++) {
                const response = await fetch(url, options);
                const data = await response.json();
                
                if (response.ok || (data.error && data.error.code !== 503 && !data.error.message.includes("high demand"))) {
                    return { response, data };
                }
                
                if (i < maxRetries - 1) {
                    resultArea.innerHTML = `
                        <div class="loading-state">
                            <div class="loader"></div>
                            <span class="loading-text">${translations[currentLang].wait_retry} (${i+1}/${maxRetries})...</span>
                        </div>`;
                    await new Promise(resolve => setTimeout(resolve, 3000));
                } else {
                    return { response, data };
                }
            }
        }

        // 8. Analyze Logic
        analyzeBtn.addEventListener('click', async () => {
            let apiKey = apiKeyInput.value.trim();
            if (!apiKey) apiKey = localStorage.getItem('vath_gemini_api_key');
            if (!apiKey || !currentImageBase64) return;

            // Save key if typed directly
            if (apiKeyInput.value.trim()) {
                localStorage.setItem('vath_gemini_api_key', apiKey);
            }

            analyzeBtn.disabled = true;
            analyzeBtn.innerHTML = `<div class="loader" style="width:16px;height:16px;border-width:2px;margin-right:8px;display:inline-block;vertical-align:middle;"></div> ${translations[currentLang].analyzing}`;
            
            emptyState.style.display = 'none';
            resultPanel.classList.add('show');
            resultArea.innerHTML = `
                <div class="loading-state">
                    <div class="loader"></div>
                    <span class="loading-text">${translations[currentLang].loading}</span>
                </div>`;

            try {
                // Prompt ត្រូវបានកែឱ្យផ្តល់ Entry, TP, SL និងហេតុផលឱ្យបានច្បាស់លាស់
                const prompt = `អ្នកគឺជាអ្នកវិភាគបច្ចេកទេស XAUUSD អាជីពរបស់ VATH Trading។ សូមវិភាគរូបភាពតារាង XAUUSD ខាងក្រោម ហើយផ្តល់លទ្ធផលជាភាសាខ្មែរតែមួយគត់។

សូមរៀបចំចម្លើយតាមទម្រង់ដូចខាងក្រោមយ៉ាងច្បាស់លាស់ (សូមប្រើប្រាស់សញ្ញា ** ដើម្បីធ្វើឱ្យអក្សរដិត)៖

**1. ទិសដៅនិន្នាការ (Trend):**
(បញ្ជាក់ថាឡើង/ចុះ/រាបស្មើ)

**2. តម្លៃសំខាន់ៗសម្រាប់ការជួញដូរ (Trade Setup):**
* **Entry (តម្លៃចូល):** (ដាក់តម្លៃជាលេខ ឧទាហរណ៍ 2340.50)
* **TP (Take Profit - យកចំណេញ):** (ដាក់តម្លៃជាលេខ)
* **SL (Stop Loss - កាត់ខាត):** (ដាក់តម្លៃជាលេខ)

**3. មូលហេតុ (Reasoning):**
* ហេតុអ្វីបានជាជ្រើសរើស Entry នេះ? (ឧ. ជួបកម្រិត Support/Resistance, មានសញ្ញា Reversal...)
* ហេតុអ្វីបានជាដាក់ TP និង SL នេះ? (ឧ. SL នៅក្រោមតួទៀនមុន, TP ជួបកម្រិត Resistance បន្ទាប់...)

**4. ការរំលឹកហានិភ័យ (Risk Warning):**
(ចំណុចដែលត្រូវយកចិត្តទុកដាក់)

សូមវិភាគតាមអ្វីដែលអ្នកឃើញពីតារាងដោយផ្ទាល់។ សូមឆ្លើយតបជាភាសាខ្មែរតែមួយគត់។`;

                const url = `https://generativelanguage.googleapis.com/v1beta/models/gemini-3.6-flash:generateContent?key=${apiKey}`;
                const options = {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({
                        contents: [{
                            parts: [
                                { text: prompt },
                                { inline_data: { mime_type: currentImageMime, data: currentImageBase64 } }
                            ]
                        }]
                    })
                };

                const { response, data } = await fetchWithRetry(url, options);

                if (!response.ok) {
                    const errMsg = data.error?.message || `Error ${response.status}`;
                    
                    if (errMsg.includes("high demand") || response.status === 503) {
                        resultArea.innerHTML = `
                            <div class="error-state">
                                ⏳ <strong>${translations[currentLang].wait_retry}</strong><br><br>
                                <span style="font-size:13px;opacity:0.8;">Please try again.</span><br><br>
                                <button class="retry-btn" onclick="document.getElementById('analyzeBtn').click()">${translations[currentLang].retry}</button>
                            </div>`;
                    } else {
                        throw new Error(errMsg);
                    }
                    return;
                }

                let text = data.candidates?.[0]?.content?.parts?.[0]?.text;
                if (!text) throw new Error('AI empty response');
                
                // បំប្លែងទម្រង់អក្សរឱ្យស្អាត (Markdown ទៅ HTML)
                text = text
                    .replace(/\*\*(.*?)\*\*/g, '<strong>$1</strong>')
                    .replace(/\*(.*?)\*/g, '<em>$1</em>')
                    .replace(/\n/g, '<br>');

                // បន្ថែមការរចនាពិសេសសម្រាប់ប្រអប់ Entry/TP/SL
                // យើងប្រើ Regex ដើម្បីស្វែងរកតម្លៃ ហើយដាក់វាក្នុង Box
                text = text.replace(
                    /(\* \*\*Entry.*?<\/strong>.*?)(?:\n|<br>)+(\* \*\*TP.*?<\/strong>.*?)(?:\n|<br>)+(\* \*\*SL.*?<\/strong>.*?)(?:\n|<br>)+/gi,
                    `<div class="trade-box">
                        <div class="trade-item"><span class="trade-label">Entry</span><span class="trade-value entry">$1</span></div>
                        <div class="trade-item"><span class="trade-label">Take Profit</span><span class="trade-value tp">$2</span></div>
                        <div class="trade-item"><span class="trade-label">Stop Loss</span><span class="trade-value sl">$3</span></div>
                    </div>`
                );
                
                // សម្អាតពាក្យ Entry/TP/SL ដែលនៅសល់ចេញពី Box
                text = text.replace(/\* \*\*(Entry|TP|SL).*?<\/strong>/gi, '');

                resultArea.innerHTML = text;

            } catch (err) {
                resultArea.innerHTML = `
                    <div class="error-state">
                        ❌ <strong>${translations[currentLang].error_title}</strong><br><br>
                        <span style="font-size:13px;opacity:0.8;">${err.message}</span>
                    </div>`;
            } finally {
                analyzeBtn.disabled = false;
                analyzeBtn.innerHTML = translations[currentLang].analyze_btn;
                updateAnalyzeBtn();
            }
        });

        // 9. Initialize App
        setLanguage(currentLang);
        updateAnalyzeBtn();
    </script>
</body>
</html>
