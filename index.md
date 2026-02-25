---
layout: null
---
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infrastructure Portfolio</title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap">
    <style>
        :root {
            --bg: #050505;
            --card-bg: rgba(23, 23, 26, 0.9);
            --accent: #3b82f6;
            --text-main: #ffffff;
            --text-sub: #9ca3af;
            --border: rgba(255, 255, 255, 0.1);
            --shadow-3d: 0 20px 50px rgba(0, 0, 0, 0.5), 
                         0 0 1px rgba(255, 255, 255, 0.2) inset;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Inter', sans-serif; }
        body { background-color: var(--bg); color: var(--text-main); line-height: 1.6; overflow-x: hidden; }

        .wrapper { max-width: 1200px; margin: 0 auto; padding: 40px 20px; }

        .bento-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            grid-auto-rows: minmax(180px, auto);
            gap: 20px;
        }

        .card {
            background: var(--card-bg);
            border: 1px solid var(--border);
            border-radius: 28px;
            padding: 32px;
            box-shadow: var(--shadow-3d);
            backdrop-filter: blur(15px);
            transition: transform 0.3s ease, border-color 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .card:hover { transform: translateY(-5px); border-color: rgba(59, 130, 246, 0.5); }
        .card-main { grid-column: span 2; grid-row: span 2; justify-content: flex-end; }
        .card-wide { grid-column: span 2; }
        .card-tall { grid-row: span 2; }

        .title-sub { color: var(--accent); font-weight: 600; font-size: 0.8rem; letter-spacing: 1.5px; text-transform: uppercase; margin-bottom: 8px; }
        .title-main { font-size: 2.4rem; font-weight: 800; line-height: 1.1; margin-bottom: 16px; letter-spacing: -0.03em; }
        
        h3 { font-size: 1.3rem; margin-bottom: 15px; font-weight: 700; }
        .desc { color: var(--text-sub); font-size: 0.95rem; }

        .tags { display: flex; flex-wrap: wrap; gap: 8px; margin-top: auto; }
        .tag { background: rgba(255, 255, 255, 0.05); border: 1px solid var(--border); padding: 6px 12px; border-radius: 10px; font-size: 0.8rem; font-weight: 600; }

        .exp-item { margin-bottom: 20px; }
        .exp-date { color: var(--accent); font-size: 0.75rem; font-weight: 700; }
        .exp-title { font-weight: 600; font-size: 1rem; display: block; margin: 2px 0; }

        @media (max-width: 1024px) { .bento-grid { grid-template-columns: repeat(2, 1fr); } .card-main { grid-column: span 2; } }
        @media (max-width: 640px) { .bento-grid { display: flex; flex-direction: column; } }
    </style>
</head>
<body>

<div class="wrapper">
    <div class="bento-grid">
        <div class="card card-main">
            <span class="title-sub">System & Infrastructure</span>
            <h1 class="title-main">고가용성 인프라<br>아키텍처 설계</h1>
            <p class="desc">리눅스 커널 분석 및 코어망 운영 경험을 기반으로 시스템 가용성을 극대화합니다.</p>
        </div>

        <div class="card card-tall">
            <h3>Infrastructure</h3>
            <div class="tags">
                <span class="tag">Linux</span>
                <span class="tag">Docker</span>
                <span class="tag">Kubernetes</span>
                <span class="tag">Ansible</span>
                <span class="tag">Terraform</span>
            </div>
            <h3 style="margin-top: 25px;">Database</h3>
            <div class="tags">
                <span class="tag">MySQL</span>
                <span class="tag">MariaDB</span>
                <span class="tag">SQLD</span>
            </div>
        </div>

        <div class="card card-wide">
            <h3>Professional Experience</h3>
            <div class="exp-item">
                <span class="exp-date">2026.01 - 2026.04</span>
                <span class="exp-title">새싹 청년취업사관학교</span>
                <p class="desc" style="font-size: 0.85rem;">클라우드 데이터 인프라 과정 수료 중</p>
            </div>
            <div class="exp-item">
                <span class="exp-date">2024.01 - 2024.06</span>
                <span class="exp-title">에스넷아이씨티 R&D</span>
                <p class="desc" style="font-size: 0.85rem;">Open5GS 분석 및 코어망 시스템 운영 지원</p>
            </div>
        </div>

        <div class="card">
            <h3>Education</h3>
            <p class="desc" style="font-size: 0.9rem;">서일대학교 소프트웨어공학 학사</p>
        </div>

        <div class="card">
            <h3>Certifications</h3>
            <p class="desc" style="font-size: 0.9rem;">ADsP (2025.09.05 취득)</p>
            <p class="desc" style="font-size: 0.9rem;">SQLD (2026.03 예정)</p>
        </div>
    </div>
</div>

</body>
</html>
