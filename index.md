---
layout: default
title: Main Portfolio
---

<style>
    /* 입체감 및 그리드 디자인 레이아웃 */
    :root {
        --bg-dark: #0f172a;
        --card-bg: #1e293b;
        --accent: #3b82f6;
        --text-p: #94a3b8;
        --text-h: #f8fafc;
        --shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.3), 0 8px 10px -6px rgba(0, 0, 0, 0.3), inset 0 1px 1px rgba(255, 255, 255, 0.05);
    }

    #main_content { background: var(--bg-dark); color: var(--text-p); max-width: 1200px; padding: 40px 20px; }
    header { display: none; } /* 기존 테마 헤더 숨김 */

    .bento-wrapper {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-auto-rows: minmax(160px, auto);
        gap: 20px;
    }

    .bento-card {
        background: var(--card-bg);
        border: 1px solid rgba(255, 255, 255, 0.1);
        border-radius: 20px;
        padding: 24px;
        box-shadow: var(--shadow);
        transition: transform 0.2s ease;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .bento-card:hover { transform: translateY(-5px); border-color: var(--accent); }
    .card-l { grid-column: span 2; grid-row: span 2; }
    .card-w { grid-column: span 2; }

    .title-main { color: var(--text-h); font-size: 2.2rem; font-weight: 800; line-height: 1.2; margin-bottom: 15px; }
    .title-sub { color: var(--accent); font-weight: 600; font-size: 0.9rem; text-transform: uppercase; letter-spacing: 1px; }
    h3 { color: var(--text-h); margin-bottom: 12px; font-size: 1.2rem; }

    .badge-group { display: flex; flex-wrap: wrap; gap: 8px; }
    .badge { background: rgba(59, 130, 246, 0.1); color: var(--accent); padding: 4px 10px; border-radius: 6px; font-size: 0.75rem; font-weight: 600; border: 1px solid rgba(59, 130, 246, 0.2); }

    .list-item { border-bottom: 1px solid rgba(255, 255, 255, 0.05); padding: 10px 0; }
    .list-item:last-child { border-bottom: none; }
    .item-date { font-size: 0.8rem; color: var(--accent); display: block; }

    @media (max-width: 1024px) { .bento-wrapper { grid-template-columns: repeat(2, 1fr); } }
    @media (max-width: 640px) { .bento-wrapper { display: flex; flex-direction: column; } }
</style>

<div class="bento-wrapper">
    <div class="bento-card card-l">
        <span class="title-sub">System Infrastructure Engineer</span>
        <h1 class="title-main">고가용성 인프라 아키텍처<br>설계 및 자동화</h1>
        <p>Linux 커널 및 코어망 분석 경험을 바탕으로, 안정적이고 확장 가능한 시스템 인프라를 구축합니다. IaC를 통한 운영 자동화에 주력하고 있습니다.</p>
    </div>

    <div class="bento-card">
        <h3>Infrastructure</h3>
        <div class="badge-group">
            <span class="badge">Linux</span>
            <span class="badge">Docker</span>
            <span class="badge">Kubernetes</span>
            <span class="badge">Ansible</span>
            <span class="badge">Terraform</span>
        </div>
    </div>

    <div class="bento-card">
        <h3>Database</h3>
        <div class="badge-group">
            <span class="badge">MySQL</span>
            <span class="badge">MariaDB</span>
            <span class="badge">SQLD</span>
        </div>
    </div>

    <div class="bento-card card-w">
        <h3>Professional Experience</h3>
        <div class="list-item">
            <span class="item-date">2026.01 - Present</span>
            <strong>SeSAC Youth Academy</strong>
            <p style="font-size: 0.85rem; margin: 0;">클라우드 데이터 인프라 및 가상화 시스템 과정 수료 중</p>
        </div>
        <div class="list-item">
            <span class="item-date">2024.01 - 2024.06</span>
            <strong>Snet ICT R&D</strong>
            <p style="font-size: 0.85rem; margin: 0;">Open5GS 분석 및 5G/LTE 코어망 시스템 운영 지원</p>
        </div>
    </div>

    <div class="bento-card card-w">
        <h3>Featured Project</h3>
        <strong>Infrastructure Automation Engine</strong>
        <p style="font-size: 0.85rem;">온프레미스 및 클라우드 환경의 프로비저닝 자동화 파이프라인 구축 (Terraform, Ansible 활용)</p>
        <a href="/my-project" style="color: var(--accent); text-decoration: none; font-size: 0.8rem; font-weight: 700; margin-top: 10px;">VIEW DETAILS →</a>
    </div>

    <div class="bento-card">
        <h3>Education</h3>
        <p style="font-size: 0.85rem; margin: 0;">서일대학교<br>소프트웨어공학 학사 졸업</p>
    </div>

    <div class="bento-card">
        <h3>Certifications</h3>
        <div class="badge-group">
            <span class="badge">ADsP</span>
            <span class="badge">SQLD (Candidate)</span>
            <span class="badge">FE (Candidate)</span>
        </div>
    </div>
</div>

---

### 구성 설명
* **파일 단일화**: 디자인(CSS)과 내용(HTML/MD)을 `index.md` 하나에 통합하여 관리 편의성을 극대화했습니다.
* **Bento Grid**: 4컬럼 기반 그리드 레이아웃을 통해 정보를 시각적으로 위계 있게 배치했습니다.
* **반응형 대응**: 모바일에서는 1컬럼, 태블릿에서는 2컬럼으로 자동 전환됩니다.
* **입체감**: `box-shadow`의 다중 레이어와 내부 그림자(`inset`)를 사용하여 카드가 떠 있는 듯한 깊이감을 주었습니다.
* **전문성 유지**: 불필요한 수식어나 이모지를 배제하고 엔지니어링 용어와 핵심 성과 중심으로 텍스트를 구성했습니다.

이제 이 파일들을 GitHub 저장소 루트 폴더에 업로드하면 바로 적용됩니다. `my-project` 상세 페이지도 이와 동일한 방식으로 `index.md` 파일 하나로 만들어 드릴까요?
