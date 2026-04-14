<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wayne Enterprises | Bat-Computer v6.0</title>
    <style>
        /* GOTHAM OS - SYSTEM STYLING 
        */
        :root {
            /* 默认：哥谭夜间战术模式 (蝙蝠侠) */
            --bg-base: #050505;
            --bg-grid: rgba(0, 255, 65, 0.05);
            --main-color: #00ff41; 
            --text-color: #00ff41;
            --panel-bg: rgba(0, 15, 0, 0.85);
            --border-color: #00ff41;
            --accent-glow: 0 0 15px rgba(0, 255, 65, 0.4);
            --bruce-comm: #888;
        }

        .theme-day {
            /* 日间韦恩模式 (布鲁斯) */
            --bg-base: #e0e0e0;
            --bg-grid: rgba(0, 0, 0, 0.05);
            --main-color: #222;
            --text-color: #111;
            --panel-bg: rgba(255, 255, 255, 0.9);
            --border-color: #333;
            --accent-glow: 0 0 10px rgba(0, 0, 0, 0.1);
            --bruce-comm: #555;
        }

        * { box-sizing: border-box; }

        body {
            background-color: var(--bg-base);
            color: var(--text-color);
            font-family: 'Segoe UI', 'Courier New', monospace;
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            transition: all 0.8s ease;
            background-image: 
                linear-gradient(var(--bg-grid) 1px, transparent 1px),
                linear-gradient(90deg, var(--bg-grid) 1px, transparent 1px);
            background-size: 40px 40px;
        }

        /* 隐藏蝙蝠标志水印 */
        .watermark {
            position: absolute;
            width: 60%;
            opacity: 0.02;
            filter: invert(1);
            pointer-events: none;
            z-index: 0;
        }

        /* HUD 容器 */
        #hud-interface {
            width: 95%;
            max-width: 1000px;
            height: 600px;
            position: relative;
            z-index: 10;
            display: flex;
            gap: 20px;
        }

        /* 左侧全息雷达面板 */
        .side-panel {
            flex: 1;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .radar-box {
            height: 200px;
            border: 1px solid var(--border-color);
            position: relative;
            background: var(--panel-bg);
            box-shadow: var(--accent-glow);
            overflow: hidden;
        }

        .radar-circle {
            width: 160px;
            height: 160px;
            border: 1px solid var(--border-color);
            border-radius: 50%;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        .radar-sweep {
            width: 50%;
            height: 50%;
            background: linear-gradient(45deg, var(--main-color), transparent);
            position: absolute;
            top: 0; left: 0;
            transform-origin: bottom right;
            animation: sweep 4s linear infinite;
        }

        @keyframes sweep { 
            from { transform: rotate(0deg); } 
            to { transform: rotate(360deg); } 
        }

        /* 主终端面板 */
        .main-terminal {
            flex: 3;
            border: 2px solid var(--border-color);
            background: var(--panel-bg);
            box-shadow: var(--accent-glow);
            display: flex;
            flex-direction: column;
            padding: 20px;
            backdrop-filter: blur(5px);
        }

        .terminal-header {
            display: flex;
            justify-content: space-between;
            font-size: 0.7rem;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 10px;
            margin-bottom: 20px;
        }

        h1 { font-size: 1.2rem; text-align: center; letter-spacing: 10px; margin: 0 0 20px 0; }

        .input-area {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }

        input {
            flex: 1;
            background: transparent;
            border: 1px solid var(--border-color);
            color: var(--text-color);
            padding: 10px;
            outline: none;
        }

        button {
            background: var(--main-color);
            color: var(--bg-base);
            border: none;
            padding: 0 20px;
            cursor: pointer;
            font-weight: bold;
            text-transform: uppercase;
        }

        /* 任务列表 */
        #task-list {
            flex: 1;
            overflow-y: auto;
            list-style: none;
            padding: 0;
            margin: 0;
        }

        .task-card {
            background: rgba(255,255,255,0.03);
            border-left: 4px solid var(--main-color);
            padding: 15px;
            margin-bottom: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            animation: fadeInUp 0.4s ease;
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .comm-text { font-size: 0.8rem; color: var(--bruce-comm); font-style: italic; margin-top: 5px; }

        .delete-btn { color: #ff4444; cursor: pointer; font-size: 0.8rem; }

        /* 右侧实时数据流 */
        .data-panel {
            flex: 1;
            font-size: 0.65rem;
            color: var(--main-color);
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .status-dot {
            width: 8px; height: 8px; background: var(--main-color);
            border-radius: 50%; display: inline-block;
            animation: blink 1s infinite;
        }

        @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0.2; } }

    </style>
</head>
<body>

    <img src="https://upload.wikimedia.org/wikipedia/commons/c/ce/Batman_Logo.svg" class="watermark" alt="bat-logo">

    <div id="hud-interface">
        <div class="side-panel">
            <div class="radar-box">
                <div style="padding: 10px; font-size: 0.6rem;">GCPD_SCANNER</div>
                <div class="radar-circle">
                    <div class="radar-sweep"></div>
                </div>
            </div>
            <div class="data-panel" id="system-logs">
                <p>> BOOT_SEQUENCE_COMPLETE</p>
                <p>> LINK_ESTABLISHED_WITH_CAVE</p>
                <p>> BATMOBILE_STATUS: IDLE</p>
                <p>> GOTHAM_CRIME_INDEX: HIGH</p>
            </div>
        </div>

        <div class="main-terminal">
            <div class="terminal-header">
                <div>SYSTEM: <span id="sys-mode">NIGHT_CRUSADER</span></div>
                <div id="clock">00:00:00</div>
                <div>SECURE_LINE: <span class="status-dot"></span> ACTIVE</div>
            </div>

            <h1 id="title">MISSION CONTROL</h1>

            <div class="input-area">
                <input type="text" id="taskInput" placeholder="输入新的任务指令..." autocomplete="off">
                <button onclick="deployTask()">部署任务</button>
            </div>

            <ul id="task-list">
                </ul>

            <div id="bruce-comm-box" style="margin-top: 15px; font-size: 0.8rem; color: var(--bruce-comm); border-top: 1px solid #333; padding-top: 10px;">
                Wayne: 正在监听。
            </div>
        </div>
    </div>

    <script>
        const quotes = [
            "如果你能改变这世界，那就从今天开始。",
            "我们是谁并不重要，我们的所作所为才最重要。",
            "现在就去，别等阿福催你。",
            "这件任务比抓住小丑还要紧迫吗？那就快做。",
            "哪怕在最黑暗的时刻，也要保持专注。"
        ];

        // 昼夜系统
        function updateTheme() {
            const hour = new Date().getHours();
            const isNight = hour >= 18 || hour < 6;
            const body = document.body;
            const sysMode = document.getElementById('sys-mode');
            const title = document.getElementById('title');

            if (isNight) {
                body.classList.remove('theme-day');
                sysMode.innerText = "NIGHT_CRUSADER";
                title.innerText = "MISSION CONTROL";
            } else {
                body.classList.add('theme-day');
                sysMode.innerText = "WAYNE_CEO_ACCESS";
                title.innerText = "EXECUTIVE TASKS";
            }
        }

        // 实时时钟
        function updateClock() {
            const now = new Date();
            document.getElementById('clock').innerText = now.toLocaleTimeString();
        }

        // 部署任务
        function deployTask() {
            const input = document.getElementById('taskInput');
            const text = input.value.trim();
            if (!text) return;

            const list = document.getElementById('task-list');
            const li = document.createElement('li');
            li.className = 'task-card';

            const quote = quotes[Math.floor(Math.random() * quotes.length)];
            
            li.innerHTML = `
                <div>
                    <div><strong>OBJ:</strong> ${text}</div>
                    <div class="comm-text">Wayne: "${quote}"</div>
                </div>
                <div class="delete-btn" onclick="this.parentElement.remove()">[已完成]</div>
            `;

            list.prepend(li);
            input.value = "";
            document.getElementById('bruce-comm-box').innerText = "Wayne: 任务已录入。立即行动。";
        }

        // 初始化
        setInterval(updateClock, 1000);
        setInterval(updateTheme, 60000);
        updateTheme();
        updateClock();

        // 回车支持
        document.getElementById('taskInput').addEventListener('keypress', (e) => {
            if (e.key === 'Enter') deployTask();
        });
    </script>
</body>
</html>
