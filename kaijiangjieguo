<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>福彩开奖 | 极客与奢华重塑版</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;500;800;900&family=ZCOOL+XiaoWei&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-obsidian: #050507;
            --glass-bg: rgba(20, 20, 25, 0.4);
            --glass-border: rgba(255, 255, 255, 0.05);
            --text-primary: #ffffff;
            --text-muted: #8a8a93;
            --gold-accent: #d4af37;
            --gold-glow: rgba(212, 175, 55, 0.3);
            --red-sphere: linear-gradient(135deg, #ff2a54 0%, #ff0844 100%);
            --blue-sphere: linear-gradient(135deg, #00c6ff 0%, #0072ff 100%);
            --font-cn: 'ZCOOL XiaoWei', serif;
            --font-num: 'Outfit', sans-serif;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: var(--bg-obsidian);
            color: var(--text-primary);
            font-family: var(--font-num);
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
            padding: 4rem 2rem;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        /* 环境光效 (Ambient Glow) */
        .ambient-light {
            position: fixed;
            border-radius: 50%;
            filter: blur(120px);
            z-index: -1;
            opacity: 0.5;
            animation: breathe 8s infinite alternate ease-in-out;
        }
        .light-1 {
            top: -10vw; left: -10vw;
            width: 50vw; height: 50vw;
            background: rgba(255, 8, 68, 0.15);
        }
        .light-2 {
            bottom: -10vw; right: -10vw;
            width: 40vw; height: 40vw;
            background: rgba(0, 198, 255, 0.15);
            animation-delay: -4s;
        }
        .light-3 {
            top: 40%; left: 50%;
            transform: translate(-50%, -50%);
            width: 30vw; height: 30vw;
            background: rgba(212, 175, 55, 0.1);
        }

        /* 背景噪点肌理 */
        body::before {
            content: '';
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)' opacity='0.04'/%3E%3C/svg%3E");
            pointer-events: none;
            z-index: 0;
        }

        header {
            text-align: center;
            margin-bottom: 5rem;
            position: relative;
            z-index: 2;
            animation: fadeDown 1s cubic-bezier(0.2, 0.8, 0.2, 1);
        }

        .main-title {
            font-family: var(--font-cn);
            font-size: 4rem;
            font-weight: 400;
            letter-spacing: 8px;
            background: linear-gradient(to right, #fff, #a3a3b5);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1rem;
        }

        .sys-date {
            font-family: var(--font-cn);
            font-size: 1.1rem;
            color: var(--gold-accent);
            letter-spacing: 2px;
            text-transform: uppercase;
            border-bottom: 1px solid rgba(212, 175, 55, 0.3);
            padding-bottom: 0.5rem;
            display: inline-block;
        }

        .board-grid {
            width: 100%;
            max-width: 1200px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
            gap: 2rem;
            z-index: 2;
        }

        /* 玻璃拟态卡片 */
        .glass-card {
            background: var(--glass-bg);
            backdrop-filter: blur(24px);
            -webkit-backdrop-filter: blur(24px);
            border: 1px solid var(--glass-border);
            border-radius: 24px;
            padding: 2.5rem;
            position: relative;
            overflow: hidden;
            transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            opacity: 0;
            transform: translateY(30px);
        }

        .glass-card::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0; height: 1px;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
        }

        .glass-card:hover {
            transform: translateY(-10px);
            background: rgba(30, 30, 38, 0.5);
            border-color: rgba(255, 255, 255, 0.1);
            box-shadow: 0 30px 60px rgba(0,0,0,0.6), 0 0 40px var(--gold-glow);
        }

        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-end;
            margin-bottom: 2rem;
            border-bottom: 1px solid rgba(255,255,255,0.05);
            padding-bottom: 1.5rem;
        }

        .lottery-name {
            font-family: var(--font-cn);
            font-size: 2.5rem;
            font-weight: bold;
            color: #fff;
            line-height: 1;
            text-shadow: 0 2px 10px rgba(0,0,0,0.5);
        }

        .issue-badge {
            background: rgba(212, 175, 55, 0.15);
            color: var(--gold-accent);
            padding: 0.4rem 1rem;
            border-radius: 100px;
            font-size: 0.9rem;
            font-weight: 800;
            letter-spacing: 1px;
            border: 1px solid rgba(212, 175, 55, 0.3);
        }

        .meta-info {
            display: flex;
            justify-content: space-between;
            font-size: 0.85rem;
            color: var(--text-muted);
            margin-bottom: 2rem;
            font-family: var(--font-cn);
        }

        .meta-info .highlight {
            color: #fff;
            font-family: var(--font-num);
            font-weight: 300;
        }

        /* 悬浮微重叠球体组 */
        .balls-container {
            display: flex;
            flex-wrap: wrap;
            gap: 0; /* 初始无间隙，依靠 margin 负值产生重叠 */
            transition: gap 0.4s ease;
        }

        .glass-card:hover .balls-container {
            gap: 8px; /* Hover 时散开 */
        }

        .glass-card:hover .ball {
            margin-left: 0 !important; /* 取消重叠 */
        }

        .ball {
            width: 52px;
            height: 52px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.5rem;
            font-weight: 900;
            color: #fff;
            position: relative;
            margin-left: -12px; /* 默认重叠 */
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: -4px 0 10px rgba(0,0,0,0.4);
            border: 2px solid rgba(255,255,255,0.1);
        }

        .ball:first-child { margin-left: 0; }

        /* 摒弃老旧的高光，改用极简渐变与柔和发光 */
        .ball.red {
            background: var(--red-sphere);
            box-shadow: -4px 0 10px rgba(0,0,0,0.4), inset 0 0 15px rgba(0,0,0,0.2);
        }
        
        .ball.blue {
            background: var(--blue-sphere);
            box-shadow: -4px 0 10px rgba(0,0,0,0.4), inset 0 0 15px rgba(0,0,0,0.2);
        }

        .ball.blue:first-of-type {
            margin-left: 15px; /* 蓝球和红球稍微隔开 */
        }
        .glass-card:hover .ball.blue:first-of-type {
            margin-left: 20px !important;
        }

        /* 骨架屏设计 */
        .skeleton .lottery-name { width: 120px; height: 40px; background: rgba(255,255,255,0.1); border-radius: 8px; }
        .skeleton .issue-badge { width: 80px; height: 28px; background: rgba(255,255,255,0.1); }
        .skeleton .ball { background: rgba(255,255,255,0.05); border-color: transparent; box-shadow: none; }
        .skeleton { animation: pulse 1.5s infinite alternate; }

        @keyframes pulse {
            0% { opacity: 0.6; }
            100% { opacity: 1; }
        }

        @keyframes fadeDown {
            from { opacity: 0; transform: translateY(-30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes breathe {
            from { transform: scale(1); opacity: 0.4; }
            to { transform: scale(1.1); opacity: 0.6; }
        }

        @media (max-width: 768px) {
            .main-title { font-size: 2.8rem; letter-spacing: 4px; }
            .board-grid { grid-template-columns: 1fr; }
            .glass-card { padding: 2rem; }
            .ball { width: 44px; height: 44px; font-size: 1.2rem; margin-left: -8px; }
        }
    </style>
</head>
<body>

    <div class="ambient-light light-1"></div>
    <div class="ambient-light light-2"></div>
    <div class="ambient-light light-3"></div>

    <header>
        <h1 class="main-title">福利彩票公告</h1>
        <div class="sys-date" id="systemDate">CALCULATING ALIGNMENT...</div>
    </header>

    <main class="board-grid" id="lotteryBoard">
        <div class="glass-card skeleton" style="opacity: 1; transform: translateY(0);">
            <div class="card-header">
                <div class="lottery-name"></div>
                <div class="issue-badge"></div>
            </div>
            <div class="meta-info">
                <span>Loading Data...</span>
            </div>
            <div class="balls-container">
                <div class="ball"></div><div class="ball"></div><div class="ball"></div><div class="ball"></div>
            </div>
        </div>
    </main>

    <script>
        const initSysDate = () => {
            const now = new Date();
            const days = ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'];
            const dateStr = now.toLocaleDateString('zh-CN', { year: 'numeric', month: '2-digit', day: '2-digit' }).replace(/\//g, '.');
            document.getElementById('systemDate').innerText = `${dateStr} // ${days[now.getDay()]}`;
        };

        const fetchLotteryData = () => {
            return new Promise(resolve => {
                setTimeout(() => {
                    resolve([
                        {
                            id: 'ssq', name: '双色球', issue: '2026038',
                            drawDate: '2026.04.02', rules: '每周二、四、日',
                            reds: ['03', '08', '11', '14', '18', '23'], blues: ['16']
                        },
                        {
                            id: '3d', name: '福彩 3D', issue: '2026085',
                            drawDate: '2026.04.04', rules: '每日开奖',
                            reds: ['08', '00', '05'], blues: []
                        },
                        {
                            id: 'qlc', name: '七乐彩', issue: '2026037',
                            drawDate: '2026.04.03', rules: '每周一、三、五',
                            reds: ['01', '05', '09', '15', '22', '26', '28'], blues: ['12']
                        },
                        {
                            id: 'kl8', name: '快乐 8', issue: '2026085',
                            drawDate: '2026.04.04', rules: '每日开奖',
                            reds: ['02', '05', '13', '18', '22', '29', '34', '35', '41', '44'], blues: []
                        }
                    ]);
                }, 600);
            });
        };

        const createCard = (data, index) => {
            const card = document.createElement('div');
            card.className = 'glass-card';
            
            // 错落进场动画
            setTimeout(() => {
                card.style.opacity = '1';
                card.style.transform = 'translateY(0)';
            }, index * 150 + 50);

            const redHtml = data.reds.map((n, i) => `<div class="ball red" style="z-index: ${20-i}">${n}</div>`).join('');
            const blueHtml = data.blues.map((n, i) => `<div class="ball blue" style="z-index: ${10-i}">${n}</div>`).join('');

            const todayStr = new Date().toLocaleDateString('zh-CN', { year: 'numeric', month: '2-digit', day: '2-digit' }).replace(/\//g, '.');
            const isToday = data.drawDate === todayStr;
            const dateHtml = isToday ? `<span class="highlight" style="color: var(--gold-accent); text-shadow: 0 0 8px var(--gold-glow);">Today</span>` : `<span class="highlight">${data.drawDate}</span>`;

            card.innerHTML = `
                <div class="card-header">
                    <div class="lottery-name">${data.name}</div>
                    <div class="issue-badge">NO. ${data.issue}</div>
                </div>
                <div class="meta-info">
                    <div>DATE / ${dateHtml}</div>
                    <div>FREQ / <span class="highlight">${data.rules}</span></div>
                </div>
                <div class="balls-container">
                    ${redHtml}
                    ${blueHtml}
                </div>
            `;
            return card;
        };

        const renderBoard = async () => {
            initSysDate();
            const board = document.getElementById('lotteryBoard');
            const data = await fetchLotteryData();
            
            board.innerHTML = '';
            data.forEach((item, index) => {
                board.appendChild(createCard(item, index));
            });
        };

        window.addEventListener('DOMContentLoaded', renderBoard);
    </script>
</body>
</html>
