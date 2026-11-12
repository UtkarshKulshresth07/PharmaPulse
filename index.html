<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
<!-- This site is hosted on Netlify. Anyone can build and deploy a site
     like this one for free: https://netlify.new/?utm_campaign=loops&utm_source=ai-legible&utm_medium=owned&utm_content=comment&utm_id=f9aea178-60d2-4e33-8f6c-a81d305f569f
     Netlify hosting facts for this site: static/SSR served via Netlify Edge. -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>PharmaPulse - Manager Dashboard</title>
    <meta name="description" content="Product launch strategy, sales analytics and MR visit tracking.">
    <meta name="theme-color" content="#0b1120">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-title" content="PharmaPulse">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <link rel="manifest" href="/manifest.webmanifest">
    <link rel="icon" href="/icons/icon.svg" type="image/svg+xml">
    <link rel="apple-touch-icon" href="/icons/apple-touch-icon.png">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=Noto+Sans+Devanagari:wght@400;500;600;700&display=swap" rel="stylesheet">
    <script>
        // Apply saved theme + language before first paint to avoid a flash.
        (function () {
            try {
                var t = localStorage.getItem('ppTheme');
                if (t === 'light' || t === 'dark') document.documentElement.setAttribute('data-theme', t);
                var l = localStorage.getItem('ppLang');
                if (l === 'hi' || l === 'en') document.documentElement.setAttribute('lang', l);
            } catch (e) {}
        })();
    </script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        /* ---------- Theme tokens ---------- */
        :root {
            --bg: #0b1120; --bg-glow-1: rgba(56,189,248,0.14); --bg-glow-2: rgba(16,185,129,0.10);
            --surface: rgba(30,41,59,0.72); --surface-solid: #1e293b; --surface-2: #273449; --inset: #0f172a;
            --border: rgba(148,163,184,0.16); --input-border: #3b4a63;
            --text: #e2e8f0; --text-strong: #f8fafc; --text-nav: #cbd5e1; --muted: #94a3b8;
            --accent: #0284c7; --accent-2: #06b6d4; --accent-hover: #0369a1; --brand: #38bdf8;
            --success: #10b981; --warning: #f59e0b; --danger: #ef4444;
            --input-text: #ffffff; --nav-hover-text: #ffffff; --shadow: 0 10px 30px rgba(0,0,0,0.30);
            --grad: linear-gradient(135deg, #0284c7 0%, #06b6d4 100%);
            color-scheme: dark;
        }
        [data-theme="light"] {
            --bg: #eef3f9; --bg-glow-1: rgba(14,165,233,0.14); --bg-glow-2: rgba(16,185,129,0.10);
            --surface: rgba(255,255,255,0.85); --surface-solid: #ffffff; --surface-2: #e8eef6; --inset: #f5f8fc;
            --border: rgba(15,23,42,0.10); --input-border: #c3cedc;
            --text: #1e293b; --text-strong: #0f172a; --text-nav: #334155; --muted: #526077;
            --accent: #0369a1; --accent-2: #0891b2; --accent-hover: #075985; --brand: #0369a1;
            --success: #047857; --warning: #b45309; --danger: #dc2626;
            --input-text: #0f172a; --nav-hover-text: #0f172a; --shadow: 0 10px 30px rgba(15,23,42,0.08);
            --grad: linear-gradient(135deg, #0369a1 0%, #0891b2 100%);
            color-scheme: light;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { -webkit-text-size-adjust: 100%; text-size-adjust: 100%; }
        html, button, input, select { font-family: 'Plus Jakarta Sans', 'Noto Sans Devanagari', 'Segoe UI', 'Nirmala UI', Tahoma, sans-serif; }
        html[lang="hi"], html[lang="hi"] button, html[lang="hi"] input, html[lang="hi"] select { font-family: 'Noto Sans Devanagari', 'Plus Jakarta Sans', 'Nirmala UI', 'Mangal', sans-serif; }
        body {
            display: flex; height: 100vh; overflow: hidden; font-size: 16px; line-height: 1.55; color: var(--text);
            background:
                radial-gradient(900px 500px at 100% -10%, var(--bg-glow-1), transparent 60%),
                radial-gradient(700px 500px at 0% 110%, var(--bg-glow-2), transparent 60%),
                var(--bg);
            transition: background-color 0.3s, color 0.3s;
        }

        img, video, iframe, embed, object, svg, canvas { max-width: 100%; }
        img, video { height: auto; }

        /* ---------- Sidebar ---------- */
        .sidebar { width: 250px; flex-shrink: 0; background: var(--surface); backdrop-filter: blur(12px); -webkit-backdrop-filter: blur(12px); padding: 20px; display: flex; flex-direction: column; gap: 15px; border-right: 1px solid var(--border); }
        .sidebar-header, .sidebar-nav { display: contents; }
        .brand { display: flex; align-items: center; gap: 12px; margin-bottom: 20px; }
        .brand-logo { width: 44px; height: 44px; border-radius: 12px; background: var(--grad); display: grid; place-items: center; font-size: 22px; box-shadow: 0 6px 18px rgba(2,132,199,0.35); flex-shrink: 0; }
        .brand-name { font-size: 20px; font-weight: 800; color: var(--text-strong); letter-spacing: -0.02em; line-height: 1.2; }
        .brand-name span { color: var(--brand); }
        .brand-tag { font-size: 13px; color: var(--muted); font-weight: 500; }
        .nav-label { font-size: 12px; text-transform: uppercase; letter-spacing: 0.08em; color: var(--muted); font-weight: 700; margin: 0 4px -6px; }
        .menu-toggle { display: none; }
        .nav-btn { position: relative; display: flex; align-items: center; gap: 12px; padding: 12px 14px; min-height: 48px; background: transparent; color: var(--text-nav); border: 1px solid transparent; text-align: left; font-size: 16px; font-weight: 600; cursor: pointer; border-radius: 12px; transition: 0.2s; margin: 0; }
        .nav-btn .ico { width: 30px; height: 30px; border-radius: 9px; display: grid; place-items: center; background: var(--surface-2); font-size: 16px; flex-shrink: 0; transition: 0.2s; }
        .nav-btn:hover { background: var(--surface-2); color: var(--nav-hover-text); }
        .nav-btn.active { background: var(--grad); color: #fff; box-shadow: 0 8px 20px rgba(2,132,199,0.30); }
        .nav-btn.active .ico { background: rgba(255,255,255,0.2); }
        button:focus-visible, select:focus-visible, input:focus-visible { outline: 2px solid var(--brand); outline-offset: 2px; }

        .app-actions { margin-top: auto; display: flex; flex-direction: column; gap: 8px; padding-top: 15px; border-top: 1px solid var(--border); }
        .app-actions > button { margin: 0; min-height: 44px; display: flex; align-items: center; gap: 10px; background: transparent; color: var(--text-nav); border: 1px solid var(--border); font-weight: 600; font-size: 16px; text-align: left; box-shadow: none; }
        .app-actions > button:hover { background: var(--surface-2); color: var(--nav-hover-text); transform: none; }

        /* Language segmented control */
        .lang-switch { display: grid; grid-template-columns: 1fr 1fr; padding: 4px; gap: 4px; background: var(--inset); border: 1px solid var(--border); border-radius: 12px; }
        .lang-switch button { margin: 0; min-height: 40px; padding: 6px 8px; background: transparent; color: var(--muted); font-size: 16px; font-weight: 700; border-radius: 9px; box-shadow: none; }
        .lang-switch button:hover { background: var(--surface-2); color: var(--text-strong); transform: none; }
        .lang-switch button[aria-pressed="true"] { background: var(--grad); color: #fff; }
        .lang-switch button[lang="hi"] { font-family: 'Noto Sans Devanagari', 'Nirmala UI', sans-serif; }

        .toast { position: fixed; left: 50%; bottom: calc(20px + env(safe-area-inset-bottom)); transform: translate(-50%, 20px); background: var(--text-strong); color: var(--bg); padding: 12px 18px; border-radius: 12px; font-size: 16px; font-weight: 600; max-width: calc(100vw - 32px); opacity: 0; pointer-events: none; transition: 0.25s; z-index: 100; box-shadow: 0 10px 30px rgba(0,0,0,0.3); }
        .toast.show { opacity: 1; transform: translate(-50%, 0); }

        /* ---------- Main ---------- */
        .main-content { flex: 1; padding: 40px; overflow-y: auto; min-width: 0; }
        .section { display: none; max-width: 760px; }
        .active-section { display: block; animation: fadeUp 0.35s ease; }
        @keyframes fadeUp { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; transform: none; } }
        @media (prefers-reduced-motion: reduce) { .active-section { animation: none; } * { transition: none !important; } }

        .page-head { margin-bottom: 24px; }
        .eyebrow { display: inline-flex; align-items: center; gap: 6px; font-size: 13px; font-weight: 700; letter-spacing: 0.06em; text-transform: uppercase; color: var(--brand); background: color-mix(in srgb, var(--brand) 12%, transparent); padding: 4px 10px; border-radius: 999px; margin-bottom: 10px; }
        h1 { color: var(--text-strong); font-size: 30px; font-weight: 800; letter-spacing: -0.02em; line-height: 1.25; overflow-wrap: anywhere; }
        .subtitle { color: var(--muted); margin-top: 6px; max-width: 60ch; }

        .card { background: var(--surface); backdrop-filter: blur(12px); -webkit-backdrop-filter: blur(12px); padding: 26px; border-radius: 18px; border: 1px solid var(--border); box-shadow: var(--shadow); max-width: 700px; }
        .card + .card { margin-top: 18px; }
        label { display: block; margin-top: 16px; color: var(--muted); margin-bottom: 6px; font-weight: 600; font-size: 15px; }
        label:first-child { margin-top: 0; }
        label .opt { font-weight: 500; opacity: 0.8; }
        .field-row { display: grid; grid-template-columns: 1fr 1fr; gap: 0 16px; }
        .field-row > div { min-width: 0; }
        select, input[type="number"], input[type="text"] { width: 100%; min-height: 48px; padding: 12px 14px; background: var(--inset); color: var(--input-text); border: 1px solid var(--input-border); border-radius: 12px; font-size: 16px; outline: none; transition: border-color 0.2s, box-shadow 0.2s; }
        select:focus, input:focus { border-color: var(--brand); box-shadow: 0 0 0 4px color-mix(in srgb, var(--brand) 18%, transparent); }
        input.invalid { border-color: var(--danger); box-shadow: 0 0 0 4px color-mix(in srgb, var(--danger) 18%, transparent); }
        button { padding: 12px 22px; min-height: 48px; font-size: 16px; background: var(--grad); color: white; cursor: pointer; font-weight: 700; border: none; border-radius: 12px; margin-top: 20px; transition: transform 0.15s, box-shadow 0.2s, background 0.2s; touch-action: manipulation; box-shadow: 0 8px 20px rgba(2,132,199,0.28); }
        button:hover { transform: translateY(-1px); box-shadow: 0 10px 24px rgba(2,132,199,0.35); }
        button:active { transform: translateY(0); }
        .hidden { display: none !important; }

        /* Strategy result */
        .result-box { margin-top: 22px; padding: 18px; background: var(--inset); border: 1px solid var(--border); border-left: 5px solid var(--success); border-radius: 12px; }
        .result-box.average { border-left-color: var(--warning); }
        .result-head { display: flex; align-items: center; justify-content: space-between; gap: 10px; flex-wrap: wrap; margin-bottom: 8px; }
        .result-head h3 { font-size: 18px; color: var(--text-strong); }
        .badge { font-size: 14px; font-weight: 700; padding: 4px 12px; border-radius: 999px; background: color-mix(in srgb, var(--success) 18%, transparent); color: var(--success); }
        .average .badge { background: color-mix(in srgb, var(--warning) 18%, transparent); color: var(--warning); }
        .meter { margin-top: 14px; }
        .meter-top { display: flex; justify-content: space-between; font-size: 15px; color: var(--muted); font-weight: 600; margin-bottom: 6px; }
        .meter-top strong { color: var(--text-strong); }
        .meter-bar { height: 10px; background: var(--surface-2); border-radius: 999px; overflow: hidden; }
        .meter-fill { height: 100%; width: 0; background: linear-gradient(90deg, var(--success), #34d399); border-radius: 999px; transition: width 0.6s ease; }

        /* Analytics */
        .stats { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; margin-bottom: 20px; }
        .stat { background: var(--inset); border: 1px solid var(--border); border-radius: 14px; padding: 14px; min-width: 0; }
        .stat-label { font-size: 14px; color: var(--muted); font-weight: 600; }
        .stat-value { font-size: 22px; font-weight: 800; color: var(--text-strong); margin-top: 2px; overflow-wrap: anywhere; }
        .stat-value.up { color: var(--success); } .stat-value.down { color: var(--danger); }
        .quarter-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 12px; }
        .quarter-grid > div { min-width: 0; }
        .quarter-grid label { margin-top: 0; }
        .chart-container { margin-top: 24px; background: var(--inset); border: 1px solid var(--border); padding: 16px; border-radius: 14px; position: relative; height: 300px; }

        /* MR tracker */
        .visit-form .actions { display: flex; justify-content: flex-end; }
        .list-head { display: flex; align-items: center; justify-content: space-between; gap: 10px; margin-bottom: 14px; }
        .list-head h3 { font-size: 18px; color: var(--text-strong); }
        .count-pill { font-size: 14px; font-weight: 700; color: var(--brand); background: color-mix(in srgb, var(--brand) 12%, transparent); padding: 4px 12px; border-radius: 999px; white-space: nowrap; }
        ul#doctorList { list-style-type: none; display: flex; flex-direction: column; gap: 10px; }
        ul#doctorList li { padding: 12px 14px; background: var(--inset); border: 1px solid var(--border); border-radius: 14px; display: flex; align-items: center; gap: 12px; }
        .avatar { width: 44px; height: 44px; border-radius: 50%; background: var(--grad); color: #fff; font-weight: 800; display: grid; place-items: center; flex-shrink: 0; font-size: 16px; }
        .visit-info { flex: 1; min-width: 0; }
        .visit-name { font-weight: 700; color: var(--text-strong); overflow-wrap: anywhere; }
        .visit-meta { font-size: 14px; color: var(--muted); display: flex; flex-wrap: wrap; gap: 4px 12px; margin-top: 2px; }
        .visit-meta span { overflow-wrap: anywhere; }
        .del-btn { background: transparent; color: var(--danger); border: 1px solid color-mix(in srgb, var(--danger) 45%, transparent); padding: 8px 14px; margin: 0; font-size: 15px; min-width: 44px; min-height: 44px; flex-shrink: 0; box-shadow: none; }
        .del-btn:hover { background: var(--danger); color: #fff; box-shadow: none; }
        .empty { text-align: center; color: var(--muted); padding: 26px 12px; border: 1px dashed var(--border); border-radius: 14px; }
        .empty .big { font-size: 32px; display: block; margin-bottom: 6px; }

        /* ---------- Phones & small tablets ---------- */
        @media (max-width: 768px) {
            body { display: block; height: auto; min-height: 100vh; overflow-x: hidden; overflow-y: auto; }

            .sidebar { width: 100%; position: sticky; top: 0; z-index: 50; padding: 0; gap: 0; border-right: none; border-bottom: 1px solid var(--border); padding-top: env(safe-area-inset-top); background: var(--surface-solid); }
            .sidebar-header { display: flex; align-items: center; justify-content: space-between; padding: 8px 12px 8px 16px; }
            .brand { margin: 0; gap: 10px; }
            .brand-logo { width: 38px; height: 38px; font-size: 19px; border-radius: 10px; }
            .brand-name { font-size: 18px; }
            .brand-tag { display: none; }
            .menu-toggle { display: inline-flex; align-items: center; justify-content: center; width: 44px; height: 44px; min-height: 44px; padding: 0; margin: 0; background: transparent; color: var(--text); border: 1px solid var(--border); border-radius: 10px; box-shadow: none; }
            .menu-toggle:hover { background: var(--surface-2); transform: none; box-shadow: none; }
            .menu-toggle svg { width: 22px; height: 22px; }
            .menu-toggle .icon-close { display: none; }
            .sidebar.open .menu-toggle .icon-open { display: none; }
            .sidebar.open .menu-toggle .icon-close { display: block; }

            .sidebar-nav { display: none; flex-direction: column; gap: 8px; padding: 12px 12px 16px; border-top: 1px solid var(--border); max-height: calc(100vh - 60px); overflow-y: auto; }
            .sidebar.open .sidebar-nav { display: flex; }
            .nav-label { margin: 2px 4px 0; }
            .app-actions { margin-top: 6px; padding-top: 12px; display: grid; grid-template-columns: repeat(auto-fit, minmax(130px, 1fr)); }
            .app-actions > button { justify-content: center; }
            .lang-switch { grid-column: 1 / -1; }

            .main-content { padding: 22px 16px calc(28px + env(safe-area-inset-bottom)); overflow: visible; }
            h1 { font-size: 24px; }
            .card { padding: 18px; border-radius: 16px; }
            .stats { grid-template-columns: 1fr 1fr; }
            .stats .stat:first-child { grid-column: 1 / -1; }
            .quarter-grid { grid-template-columns: 1fr 1fr; }
            .chart-container { margin-top: 20px; padding: 10px; height: 260px; }
            .chart-container canvas { width: 100% !important; }
        }

        @media (max-width: 520px) {
            .field-row { grid-template-columns: 1fr; }
            .field-row > div + div label { margin-top: 16px; }
            .visit-form .actions button { width: 100%; }
        }

        @media (max-width: 360px) {
            .quarter-grid, .stats { grid-template-columns: 1fr; }
            ul#doctorList li { flex-wrap: wrap; }
            .del-btn { width: 100%; }
        }
    </style>
</head>
<body>

    <nav class="sidebar" id="sidebar" aria-label="Main">
        <div class="sidebar-header">
            <div class="brand">
                <div class="brand-logo" aria-hidden="true">💊</div>
                <div>
                    <div class="brand-name">Pharma<span>Pulse</span></div>
                    <div class="brand-tag" data-i18n="brandTag">Manager Dashboard</div>
                </div>
            </div>
            <button class="menu-toggle" id="menuToggle" aria-label="Open menu" aria-expanded="false" aria-controls="sidebarNav" onclick="toggleMenu()">
                <svg class="icon-open" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" aria-hidden="true"><path d="M4 6h16M4 12h16M4 18h16"/></svg>
                <svg class="icon-close" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" aria-hidden="true"><path d="M6 6l12 12M18 6L6 18"/></svg>
            </button>
        </div>
        <div class="sidebar-nav" id="sidebarNav">
            <div class="nav-label" data-i18n="menu">Menu</div>
            <button class="nav-btn active" onclick="showSection('strategy', this)"><span class="ico" aria-hidden="true">📊</span><span data-i18n="navStrategy">Strategy</span></button>
            <button class="nav-btn" onclick="showSection('analytics', this)"><span class="ico" aria-hidden="true">📈</span><span data-i18n="navAnalytics">Sales Analytics</span></button>
            <button class="nav-btn" onclick="showSection('mrTracker', this)"><span class="ico" aria-hidden="true">👨‍⚕️</span><span data-i18n="navMr">MR Tracker</span></button>

            <div class="app-actions">
                <div class="lang-switch" role="group" aria-label="Language / भाषा">
                    <button type="button" lang="en" data-lang="en" aria-pressed="true" onclick="setLang('en')">English</button>
                    <button type="button" lang="hi" data-lang="hi" aria-pressed="false" onclick="setLang('hi')">हिंदी</button>
                </div>
                <button type="button" id="themeBtn" onclick="toggleTheme()">🌙 Dark theme</button>
                <button type="button" id="installBtn" class="hidden" onclick="installApp()">⬇️ <span data-i18n="install">Install app</span></button>
                <button type="button" id="shareBtn" onclick="shareApp()">🔗 <span data-i18n="share">Share</span></button>
            </div>
        </div>
    </nav>

    <div class="toast" id="toast" role="status" aria-live="polite"></div>

    <main class="main-content">
        <!-- STRATEGY -->
        <section id="strategy" class="section active-section">
            <div class="page-head">
                <div class="eyebrow">🚀 <span data-i18n="eyebrowStrategy">Launch planner</span></div>
                <h1 data-i18n="strategyTitle">Product Launch Strategy</h1>
                <p class="subtitle" data-i18n="strategySub">Pick a drug type and a target market to see how a launch might perform.</p>
            </div>
            <div class="card">
                <div class="field-row">
                    <div>
                        <label for="drugType" data-i18n="drugType">Drug type</label>
                        <select id="drugType">
                            <option value="chronic" data-i18n="chronic">Chronic (Diabetes, BP)</option>
                            <option value="acute" data-i18n="acute">Acute (Fever, Pain)</option>
                        </select>
                    </div>
                    <div>
                        <label for="market" data-i18n="market">Target market</label>
                        <select id="market">
                            <option value="metro" data-i18n="metro">Metro Cities</option>
                            <option value="tier2" data-i18n="tier2">Tier 2/3 Cities</option>
                            <option value="rural" data-i18n="rural">Rural Areas</option>
                        </select>
                    </div>
                </div>
                <button onclick="simulateStrategy()">✨ <span data-i18n="simulate">Simulate Strategy</span></button>
                <div id="strategyResult" class="result-box hidden" aria-live="polite">
                    <div class="result-head">
                        <h3 data-i18n="analysis">Analysis</h3>
                        <span class="badge" id="resultBadge"></span>
                    </div>
                    <p id="resultText"></p>
                    <div class="meter" id="resultMeter">
                        <div class="meter-top"><span data-i18n="successRate">Success rate</span><strong id="rateText"></strong></div>
                        <div class="meter-bar"><div class="meter-fill" id="rateFill"></div></div>
                    </div>
                </div>
            </div>
        </section>

        <!-- ANALYTICS -->
        <section id="analytics" class="section">
            <div class="page-head">
                <div class="eyebrow">📈 <span data-i18n="eyebrowAnalytics">Performance</span></div>
                <h1 data-i18n="analyticsTitle">Sales Analytics Dashboard</h1>
                <p class="subtitle" data-i18n="analyticsSub">Change the numbers and the chart updates live.</p>
            </div>
            <div class="card">
                <div class="stats">
                    <div class="stat"><div class="stat-label" data-i18n="total">Total sales</div><div class="stat-value" id="statTotal">0</div></div>
                    <div class="stat"><div class="stat-label" data-i18n="best">Best quarter</div><div class="stat-value" id="statBest">-</div></div>
                    <div class="stat"><div class="stat-label" data-i18n="growth">Q1 → Q4 growth</div><div class="stat-value" id="statGrowth">-</div></div>
                </div>
                <div class="quarter-grid">
                    <div><label for="q1"><span>Q1</span> <span data-i18n="sales">Sales</span></label><input type="number" inputmode="numeric" min="0" id="q1" value="150" oninput="updateChart()"></div>
                    <div><label for="q2"><span>Q2</span> <span data-i18n="sales">Sales</span></label><input type="number" inputmode="numeric" min="0" id="q2" value="300" oninput="updateChart()"></div>
                    <div><label for="q3"><span>Q3</span> <span data-i18n="sales">Sales</span></label><input type="number" inputmode="numeric" min="0" id="q3" value="250" oninput="updateChart()"></div>
                    <div><label for="q4"><span>Q4</span> <span data-i18n="sales">Sales</span></label><input type="number" inputmode="numeric" min="0" id="q4" value="450" oninput="updateChart()"></div>
                </div>
                <div class="chart-container">
                    <canvas id="salesChart"></canvas>
                </div>
            </div>
        </section>

        <!-- MR TRACKER -->
        <section id="mrTracker" class="section">
            <div class="page-head">
                <div class="eyebrow">🩺 <span data-i18n="eyebrowMr">Field visits</span></div>
                <h1 data-i18n="mrTitle">MR Doctor Visit Tracker</h1>
                <p class="subtitle" data-i18n="mrSub">Log each doctor visit. Adding the hospital name is optional.</p>
            </div>
            <form class="card visit-form" onsubmit="addDoctor(event)" novalidate>
                <div class="field-row">
                    <div>
                        <label for="docName"><span data-i18n="docLabel">Doctor's name</span> <span style="color:var(--danger)" aria-hidden="true">*</span></label>
                        <input type="text" id="docName" autocomplete="off" required data-i18n-ph="docPh" placeholder="e.g. Dr. Sharma">
                    </div>
                    <div>
                        <label for="hospitalName"><span data-i18n="hospLabel">Hospital / clinic</span> <span class="opt" data-i18n="optional">(optional)</span></label>
                        <input type="text" id="hospitalName" autocomplete="off" data-i18n-ph="hospPh" placeholder="e.g. City Care Hospital">
                    </div>
                </div>
                <div class="actions">
                    <button type="submit">➕ <span data-i18n="logVisit">Log Visit</span></button>
                </div>
            </form>
            <div class="card">
                <div class="list-head">
                    <h3 data-i18n="recentVisits">Visit log</h3>
                    <span class="count-pill" id="visitCount"></span>
                </div>
                <ul id="doctorList"></ul>
            </div>
        </section>

    </main>

    <script>
        // --- TRANSLATIONS ---
        const I18N = {
            en: {
                brandTag: 'Manager Dashboard', menu: 'Menu',
                navStrategy: 'Strategy', navAnalytics: 'Sales Analytics', navMr: 'MR Tracker',
                install: 'Install app', share: 'Share', themeDark: '🌙 Dark theme', themeLight: '☀️ Light theme',
                toDark: 'Switch to dark theme', toLight: 'Switch to light theme',
                openMenu: 'Open menu', closeMenu: 'Close menu',
                eyebrowStrategy: 'Launch planner', strategyTitle: 'Product Launch Strategy',
                strategySub: 'Pick a drug type and a target market to see how a launch might perform.',
                drugType: 'Drug type', chronic: 'Chronic (Diabetes, BP)', acute: 'Acute (Fever, Pain)',
                market: 'Target market', metro: 'Metro Cities', tier2: 'Tier 2/3 Cities', rural: 'Rural Areas',
                simulate: 'Simulate Strategy', analysis: 'Analysis', successRate: 'Success rate',
                badge_excellent: 'Excellent', badge_good: 'Good', badge_average: 'Average',
                res_excellent: 'Tier 2 cities have rising lifestyle diseases. Strong demand for chronic therapies.',
                res_good: 'Rural markets are price sensitive. Focus on low-cost packaging.',
                res_average: 'High competition. You may need a higher marketing budget.',
                eyebrowAnalytics: 'Performance', analyticsTitle: 'Sales Analytics Dashboard',
                analyticsSub: 'Change the numbers and the chart updates live.',
                total: 'Total sales', best: 'Best quarter', growth: 'Q1 → Q4 growth', sales: 'Sales', units: 'Sales (Units)',
                eyebrowMr: 'Field visits', mrTitle: 'MR Doctor Visit Tracker',
                mrSub: 'Log each doctor visit. Adding the hospital name is optional.',
                docLabel: "Doctor's name", docPh: 'e.g. Dr. Sharma',
                hospLabel: 'Hospital / clinic', optional: '(optional)', hospPh: 'e.g. City Care Hospital',
                logVisit: 'Log Visit', recentVisits: 'Visit log', del: 'Delete', delAria: 'Delete visit to {name}',
                visits_one: '{n} visit', visits_other: '{n} visits',
                empty: 'No visits logged yet. Add your first doctor visit above.',
                enterName: "Please enter the doctor's name.", visitLogged: 'Visit logged ✅',
                installed: 'PharmaPulse installed ✅',
                iosInstall: 'Tap the Share icon in Safari, then "Add to Home Screen".',
                browserInstall: 'Use your browser menu and choose "Install app" or "Add to Home screen".',
                shareText: 'Check out PharmaPulse — pharma launch strategy, sales analytics and MR tracking.',
                copied: 'Link copied to clipboard 📋', copyPrompt: 'Copy this link:'
            },
            hi: {
                brandTag: 'मैनेजर डैशबोर्ड', menu: 'मेन्यू',
                navStrategy: 'रणनीति', navAnalytics: 'बिक्री विश्लेषण', navMr: 'MR ट्रैकर',
                install: 'ऐप इंस्टॉल करें', share: 'शेयर करें', themeDark: '🌙 डार्क थीम', themeLight: '☀️ लाइट थीम',
                toDark: 'डार्क थीम पर जाएँ', toLight: 'लाइट थीम पर जाएँ',
                openMenu: 'मेन्यू खोलें', closeMenu: 'मेन्यू बंद करें',
                eyebrowStrategy: 'लॉन्च प्लानर', strategyTitle: 'प्रोडक्ट लॉन्च रणनीति',
                strategySub: 'दवा का प्रकार और लक्षित बाज़ार चुनें, और देखें कि लॉन्च कैसा प्रदर्शन कर सकता है।',
                drugType: 'दवा का प्रकार', chronic: 'क्रॉनिक (डायबिटीज़, बीपी)', acute: 'एक्यूट (बुखार, दर्द)',
                market: 'लक्षित बाज़ार', metro: 'मेट्रो शहर', tier2: 'टियर 2/3 शहर', rural: 'ग्रामीण क्षेत्र',
                simulate: 'रणनीति सिम्युलेट करें', analysis: 'विश्लेषण', successRate: 'सफलता दर',
                badge_excellent: 'बेहतरीन', badge_good: 'अच्छा', badge_average: 'औसत',
                res_excellent: 'टियर 2 शहरों में लाइफस्टाइल बीमारियाँ बढ़ रही हैं। क्रॉनिक दवाओं की अच्छी माँग है।',
                res_good: 'ग्रामीण बाज़ार कीमत को लेकर संवेदनशील हैं। कम लागत वाली पैकेजिंग पर ध्यान दें।',
                res_average: 'प्रतिस्पर्धा ज़्यादा है। आपको ज़्यादा मार्केटिंग बजट की ज़रूरत हो सकती है।',
                eyebrowAnalytics: 'प्रदर्शन', analyticsTitle: 'बिक्री विश्लेषण डैशबोर्ड',
                analyticsSub: 'नंबर बदलें, ग्राफ़ तुरंत अपडेट होगा।',
                total: 'कुल बिक्री', best: 'सबसे अच्छी तिमाही', growth: 'Q1 → Q4 वृद्धि', sales: 'बिक्री', units: 'बिक्री (यूनिट)',
                eyebrowMr: 'फ़ील्ड विज़िट', mrTitle: 'MR डॉक्टर विज़िट ट्रैकर',
                mrSub: 'हर डॉक्टर विज़िट दर्ज करें। अस्पताल का नाम जोड़ना वैकल्पिक है।',
                docLabel: 'डॉक्टर का नाम', docPh: 'जैसे डॉ. शर्मा',
                hospLabel: 'अस्पताल / क्लिनिक', optional: '(वैकल्पिक)', hospPh: 'जैसे सिटी केयर हॉस्पिटल',
                logVisit: 'विज़िट दर्ज करें', recentVisits: 'विज़िट सूची', del: 'हटाएँ', delAria: '{name} की विज़िट हटाएँ',
                visits_one: '{n} विज़िट', visits_other: '{n} विज़िट',
                empty: 'अभी तक कोई विज़िट दर्ज नहीं है। ऊपर अपनी पहली डॉक्टर विज़िट जोड़ें।',
                enterName: 'कृपया डॉक्टर का नाम दर्ज करें।', visitLogged: 'विज़िट दर्ज हो गई ✅',
                installed: 'PharmaPulse इंस्टॉल हो गया ✅',
                iosInstall: 'Safari में शेयर आइकन दबाएँ, फिर "Add to Home Screen" चुनें।',
                browserInstall: 'ब्राउज़र मेन्यू खोलें और "Install app" या "Add to Home screen" चुनें।',
                shareText: 'PharmaPulse देखें — फ़ार्मा लॉन्च रणनीति, बिक्री विश्लेषण और MR ट्रैकिंग।',
                copied: 'लिंक कॉपी हो गया 📋', copyPrompt: 'यह लिंक कॉपी करें:'
            }
        };
        let lang = document.documentElement.getAttribute('lang') === 'hi' ? 'hi' : 'en';
        function t(key, vars) {
            let s = (I18N[lang] && I18N[lang][key]) || I18N.en[key] || key;
            if (vars) Object.keys(vars).forEach(k => { s = s.split('{' + k + '}').join(vars[k]); });
            return s;
        }
        const locale = () => (lang === 'hi' ? 'hi-IN' : 'en-IN');
        const fmt = (n) => Number(n).toLocaleString(locale());

        function setLang(next) {
            lang = next === 'hi' ? 'hi' : 'en';
            document.documentElement.setAttribute('lang', lang);
            try { localStorage.setItem('ppLang', lang); } catch (e) {}
            document.querySelectorAll('[data-i18n]').forEach(el => { el.textContent = t(el.dataset.i18n); });
            document.querySelectorAll('[data-i18n-ph]').forEach(el => { el.placeholder = t(el.dataset.i18nPh); });
            document.querySelectorAll('.lang-switch button').forEach(b => b.setAttribute('aria-pressed', String(b.dataset.lang === lang)));
            menuToggle.setAttribute('aria-label', t(sidebar.classList.contains('open') ? 'closeMenu' : 'openMenu'));
            if (typeof applyTheme === 'function') applyTheme(currentTheme(), true);
            if (typeof myChart !== 'undefined') { myChart.data.datasets[0].label = t('units'); updateChart(); }
            if (lastResult) renderResult();
            if (typeof loadDoctors === 'function') loadDoctors();
        }

        // --- 1. TAB SWITCHING ---
        function showSection(sectionId, btnElement) {
            document.querySelectorAll('.section').forEach(sec => sec.classList.remove('active-section'));
            document.querySelectorAll('.nav-btn').forEach(btn => btn.classList.remove('active'));
            document.getElementById(sectionId).classList.add('active-section');
            btnElement.classList.add('active');
            closeMenu();
            if(sectionId === 'analytics') { setTimeout(() => { myChart.resize(); }, 100); }
        }

        // --- MOBILE MENU ---
        const sidebar = document.getElementById('sidebar');
        const menuToggle = document.getElementById('menuToggle');
        function toggleMenu() {
            const open = sidebar.classList.toggle('open');
            menuToggle.setAttribute('aria-expanded', String(open));
            menuToggle.setAttribute('aria-label', t(open ? 'closeMenu' : 'openMenu'));
        }
        function closeMenu() {
            sidebar.classList.remove('open');
            menuToggle.setAttribute('aria-expanded', 'false');
            menuToggle.setAttribute('aria-label', t('openMenu'));
        }
        document.addEventListener('keydown', (e) => { if (e.key === 'Escape') closeMenu(); });
        document.addEventListener('click', (e) => { if (!sidebar.contains(e.target)) closeMenu(); });

        // --- 2. STRATEGY LOGIC ---
        let lastResult = null;
        function simulateStrategy() {
            const drug = document.getElementById('drugType').value;
            const market = document.getElementById('market').value;
            if (drug === 'chronic' && market === 'tier2') lastResult = { key: 'excellent', rate: 85 };
            else if (drug === 'acute' && market === 'rural') lastResult = { key: 'good', rate: 75 };
            else lastResult = { key: 'average', rate: null };
            renderResult(true);
        }
        function renderResult(animate) {
            const box = document.getElementById('strategyResult');
            const fill = document.getElementById('rateFill');
            box.classList.toggle('average', lastResult.key === 'average');
            document.getElementById('resultBadge').textContent = t('badge_' + lastResult.key);
            document.getElementById('resultText').textContent = t('res_' + lastResult.key);
            document.getElementById('resultMeter').classList.toggle('hidden', lastResult.rate === null);
            box.classList.remove('hidden');
            if (lastResult.rate !== null) {
                document.getElementById('rateText').textContent = fmt(lastResult.rate) + '%';
                if (animate) { fill.style.width = '0'; requestAnimationFrame(() => requestAnimationFrame(() => { fill.style.width = lastResult.rate + '%'; })); }
                else fill.style.width = lastResult.rate + '%';
            }
        }

        // --- THEME ---
        function cssVar(name) { return getComputedStyle(document.documentElement).getPropertyValue(name).trim(); }
        function currentTheme() { return document.documentElement.getAttribute('data-theme') === 'light' ? 'light' : 'dark'; }
        function chartGrid() { return currentTheme() === 'light' ? 'rgba(15,23,42,0.08)' : 'rgba(226,232,240,0.08)'; }
        function chartColors() {
            return currentTheme() === 'light'
                ? ['#7dd3fc', '#0ea5e9', '#0369a1', '#0891b2']
                : ['#38bdf8', '#0284c7', '#0369a1', '#06b6d4'];
        }

        function applyTheme(theme) {
            document.documentElement.setAttribute('data-theme', theme);
            try { localStorage.setItem('ppTheme', theme); } catch (e) {}
            document.querySelector('meta[name="theme-color"]').setAttribute('content', cssVar('--bg'));
            const btn = document.getElementById('themeBtn');
            btn.textContent = t(theme === 'light' ? 'themeLight' : 'themeDark');
            btn.setAttribute('aria-label', t(theme === 'light' ? 'toDark' : 'toLight'));
            if (typeof myChart !== 'undefined') {
                const text = cssVar('--muted');
                myChart.options.plugins.legend.labels.color = text;
                ['x', 'y'].forEach(axis => {
                    myChart.options.scales[axis].ticks.color = text;
                    myChart.options.scales[axis].grid.color = chartGrid();
                });
                myChart.data.datasets[0].backgroundColor = chartColors();
                myChart.update();
            }
        }
        function toggleTheme() { applyTheme(currentTheme() === 'light' ? 'dark' : 'light'); }

        // --- TOAST ---
        let toastTimer;
        function showToast(msg) {
            const el = document.getElementById('toast');
            el.textContent = msg;
            el.classList.add('show');
            clearTimeout(toastTimer);
            toastTimer = setTimeout(() => el.classList.remove('show'), 3500);
        }

        // --- 3. CHART.JS LOGIC ---
        const ctx = document.getElementById('salesChart').getContext('2d');
        let myChart = new Chart(ctx, {
            type: 'bar',
            data: {
                labels: ['Q1', 'Q2', 'Q3', 'Q4'],
                datasets: [{
                    label: t('units'),
                    data: [150, 300, 250, 450],
                    backgroundColor: chartColors(),
                    borderRadius: 8,
                    maxBarThickness: 64
                }]
            },
            options: {
                responsive: true, maintainAspectRatio: false,
                plugins: { legend: { labels: { color: cssVar('--muted'), font: { weight: 600 } } } },
                scales: {
                    y: { beginAtZero: true, ticks: { color: cssVar('--muted'), callback: (v) => fmt(v) }, grid: { color: chartGrid() }, border: { display: false } },
                    x: { ticks: { color: cssVar('--muted') }, grid: { display: false }, border: { display: false } }
                }
            }
        });

        function updateChart() {
            const vals = ['q1', 'q2', 'q3', 'q4'].map(id => Math.max(0, Number(document.getElementById(id).value) || 0));
            myChart.data.datasets[0].data = vals;
            myChart.update();
            const total = vals.reduce((a, b) => a + b, 0);
            const bestIdx = vals.indexOf(Math.max(...vals));
            document.getElementById('statTotal').textContent = fmt(total);
            document.getElementById('statBest').textContent = total ? 'Q' + (bestIdx + 1) : '-';
            const g = document.getElementById('statGrowth');
            g.classList.remove('up', 'down');
            if (vals[0] > 0) {
                const pct = Math.round(((vals[3] - vals[0]) / vals[0]) * 100);
                g.textContent = (pct > 0 ? '+' : '') + fmt(pct) + '%';
                g.classList.add(pct >= 0 ? 'up' : 'down');
            } else {
                g.textContent = '-';
            }
        }

        // --- INSTALL (PWA) ---
        let deferredInstall = null;
        const installBtn = document.getElementById('installBtn');
        const isStandalone = () => window.matchMedia('(display-mode: standalone)').matches || window.navigator.standalone === true;
        const isIOS = /iphone|ipad|ipod/i.test(navigator.userAgent) || (navigator.platform === 'MacIntel' && navigator.maxTouchPoints > 1);

        window.addEventListener('beforeinstallprompt', (e) => {
            e.preventDefault();
            deferredInstall = e;
            installBtn.classList.remove('hidden');
        });
        window.addEventListener('appinstalled', () => {
            deferredInstall = null;
            installBtn.classList.add('hidden');
            showToast(t('installed'));
        });
        if (isIOS && !isStandalone()) installBtn.classList.remove('hidden');

        async function installApp() {
            if (deferredInstall) {
                deferredInstall.prompt();
                const { outcome } = await deferredInstall.userChoice;
                deferredInstall = null;
                if (outcome === 'accepted') installBtn.classList.add('hidden');
            } else {
                showToast(t(isIOS ? 'iosInstall' : 'browserInstall'));
            }
        }

        // --- SHARE ---
        async function shareApp() {
            const data = { title: 'PharmaPulse - Manager Dashboard', text: t('shareText'), url: location.origin + '/' };
            if (navigator.share) {
                try { await navigator.share(data); } catch (e) { /* user cancelled */ }
                return;
            }
            try {
                await navigator.clipboard.writeText(data.url);
                showToast(t('copied'));
            } catch (e) {
                window.prompt(t('copyPrompt'), data.url);
            }
        }

        // --- SERVICE WORKER ---
        if ('serviceWorker' in navigator) {
            window.addEventListener('load', () => { navigator.serviceWorker.register('/sw.js').catch(() => {}); });
        }

        // --- 4. MR TRACKER (Local Storage) ---
        function getVisits() {
            try { return JSON.parse(localStorage.getItem('mrVisits')) || []; } catch (e) { return []; }
        }
        function saveVisits(visits) { localStorage.setItem('mrVisits', JSON.stringify(visits)); }

        const docInput = document.getElementById('docName');
        docInput.addEventListener('input', () => docInput.classList.remove('invalid'));

        function addDoctor(e) {
            if (e) e.preventDefault();
            const docName = docInput.value.trim();
            const hospInput = document.getElementById('hospitalName');
            const hospital = hospInput.value.trim();
            if (docName === '') {
                docInput.classList.add('invalid');
                docInput.focus();
                showToast(t('enterName'));
                return;
            }
            const visits = getVisits();
            visits.push({ id: Date.now(), name: docName, hospital: hospital || '', date: new Date().toISOString() });
            saveVisits(visits);
            docInput.value = '';
            hospInput.value = '';
            loadDoctors();
            showToast(t('visitLogged'));
        }

        function initials(name) {
            const words = name.replace(/^(dr\.?|डॉ\.?)\s*/i, '').trim().split(/\s+/).filter(Boolean);
            const chars = words.slice(0, 2).map(w => Array.from(w)[0]).join('');
            return (chars || Array.from(name)[0] || '?').toUpperCase();
        }

        function loadDoctors() {
            const list = document.getElementById('doctorList');
            list.innerHTML = '';
            const visits = getVisits().slice().reverse();
            const n = visits.length;
            document.getElementById('visitCount').textContent = t(n === 1 ? 'visits_one' : 'visits_other', { n: fmt(n) });

            if (!n) {
                const li = document.createElement('li');
                li.className = 'empty';
                li.style.display = 'block';
                const big = document.createElement('span');
                big.className = 'big';
                big.textContent = '🩺';
                li.append(big, document.createTextNode(t('empty')));
                list.appendChild(li);
                return;
            }

            visits.forEach(v => {
                const li = document.createElement('li');

                const avatar = document.createElement('div');
                avatar.className = 'avatar';
                avatar.setAttribute('aria-hidden', 'true');
                avatar.textContent = initials(v.name);

                const info = document.createElement('div');
                info.className = 'visit-info';
                const name = document.createElement('div');
                name.className = 'visit-name';
                name.textContent = v.name;
                const meta = document.createElement('div');
                meta.className = 'visit-meta';
                if (v.hospital) {
                    const h = document.createElement('span');
                    h.textContent = '🏥 ' + v.hospital;
                    meta.appendChild(h);
                }
                const when = new Date(v.date || v.id);
                if (!isNaN(when)) {
                    const d = document.createElement('span');
                    d.textContent = '🗓️ ' + when.toLocaleString(locale(), { day: 'numeric', month: 'short', year: 'numeric', hour: 'numeric', minute: '2-digit' });
                    meta.appendChild(d);
                }
                info.append(name, meta);

                const del = document.createElement('button');
                del.type = 'button';
                del.className = 'del-btn';
                del.textContent = t('del');
                del.setAttribute('aria-label', t('delAria', { name: v.name }));
                del.addEventListener('click', () => deleteDoctor(v.id));

                li.append(avatar, info, del);
                list.appendChild(li);
            });
        }

        function deleteDoctor(id) {
            saveVisits(getVisits().filter(v => v.id !== id));
            loadDoctors();
        }

        // --- INIT ---
        setLang(lang);
        updateChart();
    </script>
</body>
</html>
<script async src="/.netlify/scripts/ar" data-netlify-deploy-id="6af55f94da3295b6d7051dd3" data-netlify-site-id="f9aea178-60d2-4e33-8f6c-a81d305f569f" data-agent-runner-id="6af53f6dee4d2eda6613af49"></script>
