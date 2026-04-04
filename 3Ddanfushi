<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>3D 推荐玩法 - 极限一屏版</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        :root {
            --lucky-red: #da251d;
            --dark-red: #a11312;
            --gold: #ffd700;
            --pure-yellow: #FFFF00;
            --text-dark: #333333;
        }

        /* 强制保留打印颜色 */
        html {
            -webkit-print-color-adjust: exact !important;
            print-color-adjust: exact !important;
        }

        body {
            background: #111; 
            color: var(--text-dark);
            font-family: 'PingFang SC', 'Microsoft YaHei', sans-serif;
            display: flex;
            justify-content: center;
            align-items: flex-start; /* 顶部对齐 */
            padding: 2px; 
            min-height: 100vh;
            margin: 0;
        }

        /* 移动端紧凑卡片容器 */
        .poster-container {
            background: linear-gradient(135deg, var(--lucky-red) 0%, #c62828 100%);
            width: 100%;
            max-width: 420px; 
            /* 顶部保留刘海/安全余量，但比之前更紧凑 */
            padding: 24px 6px 8px 6px; 
            border: 3px double var(--gold);
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.8);
            position: relative;
            overflow: hidden;
            margin-top: 5px;
        }

        /* 变淡的水印 */
        .poster-container::before {
            content: "💰";
            position: absolute;
            font-size: 15rem;
            color: rgba(255, 215, 0, 0.04);
            top: 50%; left: 50%;
            transform: translate(-50%, -50%) rotate(-15deg);
            pointer-events: none;
            z-index: 0;
        }

        .poster-container > * { position: relative; z-index: 1; }

        /* 极简大标题，省空间 */
        .header-title { text-align: center; margin-bottom: 18px; }
        .header-title h1 {
            font-size: 1.8rem;
            font-weight: 900;
            color: var(--gold);
            letter-spacing: 4px;
            margin: 0;
            text-shadow: 0 2px 0 #b71c1c, 0 3px 5px rgba(0,0,0,0.6);
        }

        /* 内容区块极限紧凑排版 */
        .section-card {
            background: #fff;
            border: 2px solid var(--gold);
            border-radius: 6px;
            margin-bottom: 16px; /* 缩小板块间距 */
            /* 确保内部有足够空间不挡住标题，同时底部极限压缩 */
            padding: 18px 2px 2px 2px; 
            position: relative;
        }

        /* 短幅标题背景条 */
        .section-header {
            background: linear-gradient(to right, #d32f2f, #f44336, #d32f2f);
            color: var(--gold);
            width: auto; 
            padding: 2px 20px; 
            border-radius: 6px 6px 0 0;
            position: absolute;
            top: -12px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 1.05rem;
            font-weight: 900;
            letter-spacing: 3px; 
            border: 1px solid var(--gold);
            box-shadow: 0 1px 3px rgba(0,0,0,0.3);
            white-space: nowrap;
            text-align: center;
        }

        /* 玩法说明高亮 */
        .rule-container { text-align: center; margin-top: 2px; margin-bottom: 4px; }

        @keyframes pulse-glow {
            0% { box-shadow: 0 0 2px var(--pure-yellow); }
            50% { box-shadow: 0 0 8px var(--pure-yellow); }
            100% { box-shadow: 0 0 2px var(--pure-yellow); }
        }

        .rule-explanation {
            display: inline-block;
            background: var(--pure-yellow);
            color: var(--lucky-red);
            font-size: 0.8rem; /* 字号缩小 */
            font-weight: 900;
            padding: 1px 10px;
            border-radius: 4px;
            border: 2px solid #000;
            box-shadow: 2px 2px 0px rgba(0,0,0,0.2);
            letter-spacing: 0.5px;
            animation: pulse-glow 1.5s infinite ease-in-out;
        }

        /* 表格极限压缩排版 */
        table {
            width: 100%;
            border-collapse: collapse;
            background: var(--light-gold);
            border: 2px solid #ffca28;
        }
        th {
            background: var(--gold) !important;
            color: var(--dark-red);
            font-weight: 900;
            font-size: 0.85rem; 
            padding: 2px 1px;
            border-bottom: 2px solid #f57c00;
            line-height: 1.1;
        }
        td {
            padding: 1px; /* 极限压缩单元格高度 */
            text-align: center;
            border-bottom: 1px dashed #f57c00;
            font-size: 0.95rem; /* 保持数据可读 */
            font-weight: 800;
            background-color: #fffde7 !important; 
            line-height: 1.2;
        }
        tr:nth-child(even) td { background-color: #fff9c4 !important; }
        .price-col { color: #1b5e20; }
        .reward-col { color: var(--lucky-red); font-size: 1.05rem; font-weight: 900; }

    </style>
</head>
<body>

    <div class="poster-container">

        <div class="header-title">
            <h1>福彩3D 复式玩法明细</h1>
        </div>

        <div class="section-card">
            <div class="section-header">单选玩法</div>
            <div class="rule-container">
                <div class="rule-explanation">【 包串投注 即3个不同的号 】</div>
            </div>
            <table>
                <thead>
                    <tr><th width="33%">单选包串</th><th width="33%">投入(元)</th><th width="34%">单选奖金(元)</th></tr>
                </thead>
                <tbody>
                    <tr><td>3码复式</td><td class="price-col">12</td><td class="reward-col">1040</td></tr>
                    <tr><td>4码复式</td><td class="price-col">48</td><td class="reward-col">1040</td></tr>
                    <tr><td>5码复式</td><td class="price-col">120</td><td class="reward-col">1040</td></tr>
                    <tr><td>6码复式</td><td class="price-col">240</td><td class="reward-col">1040</td></tr>
                    <tr><td>7码复式</td><td class="price-col">420</td><td class="reward-col">1040</td></tr>
                    <tr><td>8码复式</td><td class="price-col">672</td><td class="reward-col">1040</td></tr>
                    <tr><td>9码复式</td><td class="price-col">1008</td><td class="reward-col">1040</td></tr>
                </tbody>
            </table>
        </div>

        <div class="section-card">
            <div class="section-header">组选六</div>
            <div class="rule-container">
                <div class="rule-explanation">【 包串投注 即3个不同的号 】</div>
            </div>
            <table>
                <thead>
                    <tr><th width="33%">组六包串</th><th width="33%">投入(元)</th><th width="34%">组六奖金(元)</th></tr>
                </thead>
                <tbody>
                    <tr><td>3码单式</td><td class="price-col">2</td><td class="reward-col">173</td></tr>
                    <tr><td>4码复式</td><td class="price-col">8</td><td class="reward-col">173</td></tr>
                    <tr><td>5码复式</td><td class="price-col">20</td><td class="reward-col">173</td></tr>
                    <tr><td>6码复式</td><td class="price-col">40</td><td class="reward-col">173</td></tr>
                    <tr><td>7码复式</td><td class="price-col">70</td><td class="reward-col">173</td></tr>
                    <tr><td>8码复式</td><td class="price-col">112</td><td class="reward-col">173</td></tr>
                    <tr><td>9码复式</td><td class="price-col">168</td><td class="reward-col">173</td></tr>
                </tbody>
            </table>
        </div>

        <div class="section-card" style="margin-bottom: 2px;">
            <div class="section-header">组选三</div>
            <div class="rule-container">
                <div class="rule-explanation">【 包串投注 即对子玩法 】</div>
            </div>
            <table>
                <thead>
                    <tr><th width="33%">组三包串</th><th width="33%">投入(元)</th><th width="34%">组三奖金(元)</th></tr>
                </thead>
                <tbody>
                    <tr><td>2码复式</td><td class="price-col">4</td><td class="reward-col">346</td></tr>
                    <tr><td>3码复式</td><td class="price-col">12</td><td class="reward-col">346</td></tr>
                    <tr><td>4码复式</td><td class="price-col">24</td><td class="reward-col">346</td></tr>
                    <tr><td>5码复式</td><td class="price-col">40</td><td class="reward-col">346</td></tr>
                    <tr><td>6码复式</td><td class="price-col">60</td><td class="reward-col">346</td></tr>
                    <tr><td>7码复式</td><td class="price-col">84</td><td class="reward-col">346</td></tr>
                    <tr><td>8码复式</td><td class="price-col">112</td><td class="reward-col">346</td></tr>
                    <tr><td>9码复式</td><td class="price-col">144</td><td class="reward-col">346</td></tr>
                    <tr><td>10码复式</td><td class="price-col">180</td><td class="reward-col">346</td></tr>
                </tbody>
            </table>
        </div>

    </div>

</body>
</html>
