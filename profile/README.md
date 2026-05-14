<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:203A43,100:2C5364&height=220&section=header&text=AquaSumun&fontSize=70&fontColor=ffffff&fontAlignY=38&desc=AI-Powered%20Water%20Quality%20Management%20Platform&descSize=18&descAlignY=60" />

<br/>

<p>
  <img src="https://img.shields.io/badge/2026-AX%20경진대회-00BFA6?style=for-the-badge" />
  <img src="https://img.shields.io/badge/공공데이터-한국환경공단-6366F1?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Active-22C55E?style=for-the-badge" />
</p>

</div>

<br/>

## 🌊 About AquaSumun

> **AquaSumun**은 공공하수처리시설의 수질 데이터를 AI로 분석하는 관제 플랫폼입니다.  
> 한국환경공단 공공데이터(data.go.kr) 기반으로 **15,022개 시설**의 이상 감지·예측·자동 진단을 지원합니다.

**2026 AX 아이디어 경진대회** — 데이터 활용 제품·서비스(앱/AI Agent) 개발 사업 부문 출품작

<br/>

## 🎯 핵심 기능

| 기능 | 설명 |
| :--- | :--- |
| 🤖 **AI 에이전트** | Observe → Detect → Diagnose → Recommend 자율 진단 루프 |
| 📈 **수질 예측** | BOD/TN/TP 48시간 AI 예측 + 신뢰 구간 시각화 |
| 🔍 **XAI 설명** | SHAP 피처 기여도로 예측 근거 투명하게 제공 |
| 🚨 **이상 감지** | HGB + IsolationForest 앙상블 위험도 실시간 모니터링 |
| 📄 **보고서 자동생성** | 자가측정·일일보고·ESG 보고서 PDF/Excel 자동 생성 |
| 🔔 **알림 전송** | 경보 발생 시 담당자 즉시 통보 |

<br/>

## 🧪 기술 스택

#### Frontend
<p>
  <img src="https://img.shields.io/badge/Next.js_16-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/React_19-61DAFB?style=flat-square&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/Tailwind_CSS_v4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/Zustand-000000?style=flat-square&logo=react&logoColor=white" />
  <img src="https://img.shields.io/badge/Recharts-22B5BF?style=flat-square" />
</p>

#### Backend & AI / ML
<p>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" />
</p>

#### Export & Tools
<p>
  <img src="https://img.shields.io/badge/jsPDF-FF0000?style=flat-square" />
  <img src="https://img.shields.io/badge/SheetJS-217346?style=flat-square" />
  <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" />
</p>

<br/>

## 🚀 실행 방법

#### 사전 요건
- Node.js 20+
- 백엔드 서버 실행 중 (`http://localhost:8000`) → [Backend README](../Backend/README.md)

```bash
# 의존성 설치
cd Frontend
npm install

# 개발 서버 시작
npm run dev
# → http://localhost:3000
```

#### 환경변수 (`.env.local`)

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
NEXT_PUBLIC_USE_MOCK=false
```

> `NEXT_PUBLIC_USE_MOCK=true` 로 변경하면 목업 데이터로 백엔드 없이 실행 가능합니다.

<br/>

## 🔑 데모 계정

```yaml
email   : demo@example.com
password: demo123
```

<br/>

## 📂 프로젝트 구조

```bash
Frontend/src/
├── app/
│   ├── login/              # 로그인
│   ├── plants/             # 시설 목록
│   └── plants/[id]/        # 대시보드 · 예측 · 보고서
├── components/
│   ├── common/             # Button · Badge · Modal · Skeleton
│   ├── dashboard/          # ActionButtons · ForecastChart · AgentRunModal
│   ├── forecast/           # ShapChart · TimeSeriesChart
│   ├── plants/             # PlantCard
│   └── reports/            # ReportPreview
├── api/                    # 백엔드 API 호출 레이어
├── hooks/                  # useAuth · useStream
├── store/                  # Zustand 전역 상태
├── types/                  # TypeScript 인터페이스
└── utils/                  # constants · reportPdf · 유틸
```

<br/>

## 🤝 개발 방식

```yaml
architecture:
  frontend : "Next.js App Router + Zustand"
  backend  : "FastAPI REST API (Bearer token)"
  ml       : "HGB + IsolationForest Ensemble"
  rag      : "TF-IDF + cosine similarity"

data:
  source   : "한국환경공단 공공하수처리시설 현황 (2015–2024)"
  size     : "15,022개 시설 · 연도별 수질 및 처리 효율"
  forecast : "5,683개 시설 AI 예측 가능 (2년 이상 데이터)"
```

<br/>

## 📬 Contact

<p>
  <a href="mailto:wjdwoals000619@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
  <a href="https://github.com/AquSumun">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
</p>

<br/>

<div align="center">

---

<sub>Made with 🌊 by <strong>Aqu Sumun</strong> · AI for a cleaner water future.</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2C5364,50:203A43,100:0F2027&height=120&section=footer" />

</div>
