# 0149James-web_hitgub.io
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>藍禛 | 醫學預科實驗室中心</title>
    <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Noto+Sans+TC:wght@300;500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --lab-blue: #0ea5e9;
            --lab-cyan: #06b6d4;
            --lab-bg: #0b0f1a;
            --lab-card: #161d2f;
            --lab-border: #1e293b;
            --lab-text: #e2e8f0;
            --lab-accent: #10b981; /* 實驗室成功綠 */
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }

        body {
            font-family: 'Noto Sans TC', sans-serif;
            background-color: var(--lab-bg);
            color: var(--lab-text);
            background-image: 
                radial-gradient(circle at 2px 2px, rgba(255,255,255,0.05) 1px, transparent 0);
            background-size: 30px 30px;
            line-height: 1.6;
        }

        /* 實驗室頂部掃描線特效 */
        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 2px;
            background: var(--lab-blue);
            opacity: 0.3;
            z-index: 100;
            animation: scan 4s linear infinite;
        }

        @keyframes scan {
            0% { top: 0; }
            100% { top: 100%; }
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        /* 個人資料面板 */
        .profile-header {
            display: flex;
            align-items: center;
            gap: 30px;
            background: var(--lab-card);
            padding: 30px;
            border-radius: 20px;
            border-left: 5px solid var(--lab-blue);
            margin-bottom: 40px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.5);
            flex-wrap: wrap;
        }

        .avatar-frame {
            width: 150px;
            height: 150px;
            border-radius: 15px;
            overflow: hidden;
            border: 2px solid var(--lab-blue);
            box-shadow: 0 0 15px rgba(14, 165, 233, 0.3);
            background: #000;
        }

        .avatar-frame img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .header-info h1 {
            font-size: 2.5rem;
            color: var(--lab-blue);
            font-family: 'JetBrains Mono', monospace;
        }

        .status-badge {
            display: inline-block;
            background: rgba(16, 185, 129, 0.1);
            color: var(--lab-accent);
            padding: 4px 12px;
            border-radius: 5px;
            font-size: 0.85rem;
            border: 1px solid var(--lab-accent);
            margin-top: 10px;
        }

        /* 多元成果網格 */
        .section-title {
            font-family: 'JetBrains Mono', monospace;
            font-size: 1.5rem;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-title::before {
            content: ">";
            color: var(--lab-blue);
        }

        .archive-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 20px;
        }

        .archive-card {
            background: var(--lab-card);
            border: 1px solid var(--lab-border);
            border-radius: 12px;
            padding: 25px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .archive-card:hover {
            border-color: var(--lab-blue);
            transform: translateY(-5px);
            background: rgba(30, 41, 59, 0.8);
        }

        .archive-card h3 {
            margin-bottom: 10px;
            color: var(--lab-blue);
            font-size: 1.2rem;
        }

        .archive-card p {
            font-size: 0.9rem;
            color: #94a3b8;
            margin-bottom: 20px;
        }

        /* 檔案預覽按鈕 */
        .file-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(14, 165, 233, 0.1);
            color: var(--lab-blue);
            text-decoration: none;
            padding: 8px 16px;
            border-radius: 6px;
            font-size: 0.9rem;
            border: 1px solid var(--lab-blue);
            transition: 0.2s;
            font-weight: bold;
        }

        .file-link:hover {
            background: var(--lab-blue);
            color: #fff;
        }

        .file-icon {
            width: 18px;
            height: 18px;
        }

        /* 實驗數據儀表板樣式 */
        .stats-row {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-bottom: 40px;
        }

        .stat-box {
            background: rgba(30, 41, 59, 0.5);
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            border: 1px solid var(--lab-border);
        }

        .stat-value {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--lab-cyan);
            display: block;
        }

        .stat-label {
            font-size: 0.75rem;
            color: #64748b;
            text-transform: uppercase;
        }

        footer {
            text-align: center;
            padding: 60px 20px;
            color: #475569;
            font-size: 0.8rem;
            border-top: 1px solid var(--lab-border);
        }

        /* 手機版適應 */
        @media (max-width: 768px) {
            .profile-header { flex-direction: column; text-align: center; }
            .stats-row { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

<div class="container">
    
    <!-- 頂部實驗員資料 -->
    <header class="profile-header">
        <div class="avatar-frame">
            <!-- 替換為你的個人頭貼路徑 -->
            <img src="https://lh3.googleusercontent.com/d/1EZukgJQXpME_lLDd6aTM8syxu7TrKNw8" alt="藍禛的頭貼">
        </div>
        <div class="header-info">
            <span class="status-badge">● EXPERIMENTER_ID: LAN_ZHEN</span>
            <h1>藍禛 / Lan Zhen</h1>
            <p>醫學預科候選人 | 三類組研究員 | 科學探索者</p>
            <div class="inventory" style="margin-top: 15px; font-size: 1.5rem;">
                🧬 🩺 🧪 🔬 💻
            </div>
        </div>
    </header>

    <!-- 實驗室數據看板 -->
    <div class="stats-row">
        <div class="stat-box">
            <span class="stat-value">3+ Years</span>
            <span class="stat-label">三類組專研年資</span>
        </div>
        <div class="stat-box">
            <span class="stat-value">7 Reports</span>
            <span class="stat-label">多元成果存檔</span>
        </div>
        <div class="stat-box">
            <span class="stat-value">PASS</span>
            <span class="stat-label">生物化學安全認證</span>
        </div>
    </div>

    <!-- 多元表現檔案庫 -->
    <h2 class="section-title">多元表現成果庫 / ARCHIVE_STUDY</h2>
    <div class="archive-grid">
        
        <!-- 自主學習 -->
        <div class="archive-card">
            <h3>自主學習成果</h3>
            <p>深入探討特定學術領域，展現高度自律與研究深度。</p>
            <a href="https://drive.google.com/file/d/1lj77CcqjNlQQE0iGIUXnKUsq7Lsinfmd/view?usp=drivesdk" target="_blank" class="file-link">
                📄 開啟實驗報告
            </a>
        </div>

        <!-- 新藥研發營 -->
        <div class="archive-card">
            <h3>新藥研發營</h3>
            <p>參與專業藥學研究課程，實際模擬藥物篩選與開發流程。</p>
            <a href="https://drive.google.com/file/d/1Gqb1jlv8IinYatX0fzkhvHTnQL1LbTav/view?usp=drivesdk" target="_blank" class="file-link">
                📄 研發紀錄
            </a>
        </div>

        <!-- 物理探究 -->
        <div class="archive-card">
            <h3>物理探究成果</h3>
            <p>嚴謹的物理實驗設計，從假設到結論的完整科學論證。</p>
            <a href="https://drive.google.com/file/d/1hBx6P_XktdBl8ct5l-UAQSGjwmVIycVg/view?usp=drivesdk" target="_blank" class="file-link">
                📄 物理數據集
            </a>
        </div>

        <!-- Arduino課程 -->
        <div class="archive-card">
            <h3>Arduino 控制系統課程</h3>
            <p>跨領域結合電子電路與程式設計，體現智慧科技應用能力。</p>
            <a href="https://drive.google.com/file/d/1Vlavf5enHwnKZ2Sf_gPzjWcwhw0RsAvL/view?usp=drivesdk" target="_blank" class="file-link">
                📄 原始碼與硬體成果
            </a>
        </div>

        <!-- 竹子湖淨灘活動 -->
        <div class="archive-card">
            <h3>竹子湖環境守護行動</h3>
            <p>實踐環境保護與生態永續，展現對土地的關懷與責任感。</p>
            <a href="https://drive.google.com/file/d/1gWKKNQyo_nFYGR2eOSe0AiN1xxpRsL41/view?usp=drivesdk" target="_blank" class="file-link">
                📄 服務證明
            </a>
        </div>

        <!-- 校園社區服務活動 -->
        <div class="archive-card">
            <h3>校園社區服務活動</h3>
            <p>與社區互動合作，培養團隊協作與公共服務精神。</p>
            <a href="https://drive.google.com/file/d/1e0Yd5yXiiDyy0oe2FWny1qRv5IYQvrZT/view?usp=drivesdk" target="_blank" class="file-link">
                📄 服務紀錄表
            </a>
        </div>

        <!-- 英語話劇 -->
        <div class="archive-card">
            <h3>英語話劇演展成果</h3>
            <p>外語表達能力與藝術涵養的結合，展現全方位的軟實力。</p>
            <a href="https://drive.google.com/file/d/1CSAYtzmhrtYz5_YMOiI7vUWTIbLbFj6u/view?usp=drivesdk" target="_blank" class="file-link">
                📄 展演錄像與劇本
            </a>
        </div>

    </div>

    <!-- 底部資訊 -->
    <div style="margin-top: 50px; text-align: center;">
        <h2 class="section-title" style="justify-content: center;">聯絡通道 / COMMS</h2>
        <a href="mailto:your_email@example.com" class="file-link" style="padding: 15px 30px; font-size: 1.1rem;">
            🧬 啟動通訊序列 (E-mail)
        </a>
    </div>

</div>

<footer>
    <p>SYSTEM STATUS: SECURE | CORE_VOLTAGE: STABLE | EXPERIMENTER: LAN_ZHEN</p>
    <p>&copy; 2026 藍禛的醫學研究存檔系統</p>
</footer>

</body>
</html>

