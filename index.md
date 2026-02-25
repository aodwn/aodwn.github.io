---
layout: null
---

<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infrastructure Portfolio</title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap">
    <style>
        :root {
            --bg: #050505;
            --card-bg: rgba(23, 23, 26, 0.8);
            --accent: #3b82f6;
            --text-main: #ffffff;
            --text-sub: #9ca3af;
            --border: rgba(255, 255, 255, 0.1);
            /* 입체감을 위한 다중 그림자 */
            --shadow-3d: 0 20px 50px rgba(0, 0, 0, 0.5), 
                         0 0 1px rgba(255, 255, 255, 0.2) inset,
                         0 10px 20px rgba(0, 0, 0, 0.3);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Inter', sans-serif; }
        body { background-color: var(--bg); color: var(--text-main); line-height: 1.6; overflow-x: hidden; }

        /* 배경 조명 효과 */
        body::before {
            content: "";
            position: fixed;
            top: -10%; left: -10%;
            width: 40%; height: 40%;
            background: radial-gradient(circle, rgba(59, 130, 246, 0.1) 0%, transparent 70%);
            z-index: -1;
        }

        .wrapper { max-width: 1200px; margin: 0 auto; padding: 60px 20px; }

        /* Bento Grid 시스템 */
        .bento-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            grid-auto-rows: minmax(200px, auto);
            gap: 24px;
        }

        .card {
            background: var(--card-bg);
            border: 1px solid var(--border);
            border-radius: 32px;
            padding: 40px;
            box-shadow: var(--shadow-3d);
            backdrop-filter: blur(10px);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
        }

        .card:hover {
            transform: translateY(-8px) scale(1.02);
            border-color: rgba(59, 130, 246, 0.4);
            background: rgba(30, 30, 35, 0.9);
        }

        /* 카드 크기 조절 */
        .card-main { grid-column: span 2; grid-row: span 2; justify-content: flex-end; }
        .card-wide { grid-column: span 2; }
        .card-tall { grid-row: span 2; }

        /* Typography */
        .title-sub { color: var(--accent); font-weight: 600; font-size: 0.85rem; letter-spacing: 2px; text-transform: uppercase; margin-bottom: 12px; }
        .title-main { font-size: 2.8rem; font-weight: 800; line-height: 1.1; letter-spacing: -0.04em; margin-bottom: 20px; }
        .desc { color: var(--text-sub); font-size: 1rem; }

        h3 { font-size: 1.5rem; margin-bottom: 20px; font-weight: 700; }

        /* Skill Tags */
        .tags { display: flex; flex-wrap: wrap; gap: 10px; margin-top: auto; }
        .tag { background: rgba(255, 255, 255, 0.05); border: 1px solid var(--border); padding: 8px 16px; border-radius: 12px; font-size: 0.85rem; color: var(--text-main); font-weight: 600; }

        /* Experience List */
        .exp-item { margin-bottom: 24px; }
        .exp-date { color: var(--accent); font-size: 0.8rem; font-weight: 600; }
        .exp-title { font-weight: 600; font-size: 1.1rem; display: block; margin: 4px 0; }
        .exp-desc { font-size: 0.9rem; color: var(--text-sub); }

        /* 반응형 */
        @media (max-width: 1024px) {
            .bento-grid { grid-template-columns: repeat(2, 1fr); }
            .card-main { grid-column: span 2; }
        }

        @media (max-width: 640px) {
            .bento-grid { display: flex; flex-direction: column; }
            .title-main { font-size: 2rem; }
            .card { padding: 30px; }
        }
    </style>
</head>
<body>

<div class="wrapper">
    <div class="bento-grid">
        <div class="card card-main">
            <span class="title-sub">System & Infrastructure</span>
            <h1 class="title-main">고가용성 인프라<br>아키텍처 설계</h1>
            <p class="desc">리눅스 커널 분석 및 코어망 운영 경험을 기반으로 서비스의 안정성과 확장성을 보장하는 자동화된 시스템을 구축합니다.</p>
        </div>

        <div class="card card-tall">
            <h3>Infrastructure</h3>
            <div class="tags">
                <span class="tag">Linux</span>
                <span class="tag">Docker</span>
                <span class="tag">Kubernetes</span>
                <span class="tag">Ansible</span>
                <span class="tag">Terraform</span>
                <span class="tag">AWS</span>
            </div>
            <h3 style="margin-top: 30px;">Database</h3>
            <div class="tags">
                <span class="tag">MySQL</span>
                <span class="tag">MariaDB</span>
                <span class="tag">SQLD</span>
            </div>
        </div>

        <div class="card card-wide">
            <h3>Professional Experience</h3>
            <div class="exp-item">
                <span class="exp-date">2026.01 - Present</span>
                <span class="exp-title">SeSAC 청년취업사관학교</span>
                <p class="exp-desc">클라우드 데이터 인프라 및 가상화 시스템 과정 수료 중</p>
            </div>
            <div class="exp-item">
                <span class="exp-date">2024.01 - 2024.06</span>
                <span class="exp-title">에스넷아이씨티 R&D</span>
                <p class="exp-desc">Open5GS 분석 및 5G/LTE 코어망 시스템 운영 지원</p>
            </div>
        </div>

        <div class="card">
            <h3>Projects</h3>
            <p class="exp-desc">Terraform 기반 인프라 자동화 엔진 개발</p>
            <a href="/my-project" style="margin-top: 15px; color: var(--accent); text-decoration: none; font-size: 0.9rem; font-weight: 600;">상세보기 →</a>
        </div>

        <div class="card">
            <h3>Academic</h3>
            <p class="exp-desc">서일대학교 소프트웨어공학 전공</p>
            <p class="exp-desc" style="margin-top: 10px;">ADsP 자격 취득</p>
        </div>
    </div>
</div>

</body>
</html>
