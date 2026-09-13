# 염준환 | ML 엔지니어 포트폴리오 🔍

## 간략 소개

안녕하세요. `모델을 만드는 데서 그치지 않고 실제로 사용자에게 닿는 것까지` 만드는 ML 엔지니어 염준환입니다.

**AI 사주 리포트 서비스를 직접 만들어 운영 중입니다.** 2026년 9월 오픈, `실결제 200건 · 리포트 300건`이 나갔습니다. LLM이 명식에 없는 내용을 지어내는 문제를 `근거 주입 → 코드 재검증 → 폴백` 3단으로 막았고, 결제 승인 직전 네트워크 단절 같은 실패 케이스까지 처리했습니다.

한국 도서 추천 시스템은 `Streamlit 단일 앱에서 FastAPI + Docker + Cloud Run 구조로 전환`했습니다. 검색 백엔드를 `FAISS와 PGVector 두 가지로 구현해 비교`하다가, 유사도가 제 역할을 못 하고 있었다는 걸 발견해 고쳤습니다.

전기차 충전 수요 예측에서는 `단순 Baseline이 XGBoost를 이긴 결과`를 그대로 리포트하고, Feature Importance로 원인을 진단해 개선했습니다.

앞으로도 `예상과 다른 결과의 원인을 끝까지 검증`하고, `외부 의존성이 실패해도 서비스가 멈추지 않는 구조`를 고민하는 엔지니어로 성장하고자 합니다.

## 💼 프로젝트

- [`[AI 서비스 / LLM 제품화 · 실서비스 운영]` 사주 준명 — AI 사주 리포트 서비스](https://sajujunmyeong.com)
   - **실제 운영 중** — 2026.07 오픈, 실결제 200건 · 리포트 300건 · 상품 12종.
   - 전통 명리학을 결정론적 계산 엔진으로 구현하고, **계산 결과를 근거로 LLM에 넘겨 환각 억제.**
   - 프롬프트 지시만으로 부족해 **생성 결과를 코드로 재검증**하는 단계 추가.
   - 토스 결제 **승인 직전 단절·웹훅 위조**까지 방어, 실패 시 조회 기반 정합성 복구.
   - Vercel Workflow로 150p 리포트를 단계 분할, **실패한 챕터만 재생성**해 중복 비용 차단.
   - 기술스택: Next.js 15, TypeScript, Claude API, Supabase, Toss Payments, Vercel Workflow

- [`[이커머스·콘텐츠 / 추천시스템 + MLOps]` 한국 도서 하이브리드 추천 시스템](https://github.com/pssjun/korean-book-recommender)
   - 알라딘 도서 6,974권 콘텐츠 임베딩(SentenceBERT)과 협업필터링 6종 벤치마크 결합.
   - **FastAPI 서빙 → Docker 컨테이너화 → GitHub Actions CI → Cloud Run 배포**까지 확장.
   - **FAISS·PGVector 두 백엔드 구현 및 비교** — 결과가 소수점 4자리까지 일치함을 확인.
   - 비교 과정에서 **쿼리-문서 비대칭 문제 발견 및 해결** (소설 비중 2→6건, 유사도 0.73→0.83).
   - ALS가 Baseline 대비 NDCG@10 +72.4% 달성, NCF 실패까지 정직하게 리포트.
   - 기술스택: FastAPI, Docker, Cloud Run, GitHub Actions, SentenceBERT, FAISS, PGVector, Gemini API

- [`[에너지·모빌리티 / 시계열예측]` 전기차 충전소 시간대별 수요 예측](https://github.com/pssjun/ev-charging-forecast)
   - 공공데이터 6만 건을 aiohttp 비동기 병렬로 수집(체크포인트·재시도 포함).
   - **단순 Baseline(R²=0.270)이 초기 XGBoost(0.240)를 능가한 결과**를 원인 분석과 함께 리포트.
   - Feature Importance 진단 후 기상 변수·Optuna 튜닝 추가로 최종 R²=0.285 달성.
   - 운영 관점 지표 **Peak_MAE(수요 상위 20% 구간 오차)** 자체 설계.
   - 기술스택: XGBoost, Optuna, aiohttp, Streamlit, Python

- [`[금융 / 강화학습 재현연구]` ESG 통합 강화학습 기반 포트폴리오 최적화 (논문)](https://github.com/pssjun/esg-ppo-portfolio)
   - 원 논문 코드가 보존되지 않은 상태에서 PPO 환경을 전면 재구현.
   - MVO 대비 성능·안정성을 5개 시드로 검증, 원 논문과 다른 발견을 정직하게 규명.
   - 기술스택: Gymnasium, Stable-Baselines3, Optuna, PyPortfolioOpt, Python

## 🛠 기술 스택

- **LLM / RAG**: `Claude API` `Gemini API` `근거 주입` `환각 억제` `모델 폴백 체인`
- **ML / DL**: `XGBoost` `PyTorch` `scikit-learn` `SentenceBERT` `Optuna`
- **벡터 검색**: `FAISS` `PGVector` `PostgreSQL`
- **서빙 / 인프라**: `FastAPI` `Next.js` `Docker` `Cloud Run` `Vercel Workflow` `GitHub Actions`
- **서비스 운영**: `Toss Payments` `Supabase` `Resend` `회귀 테스트` `운영 알림`
- **데이터**: `pandas` `numpy` `aiohttp` `SQL`

## 읽어주셔서 감사합니다 :)

염준환 | ML 엔지니어  
Email: [pssjun8833@gmail.com](mailto:pssjun8833@gmail.com)  
GitHub: [pssjun](https://github.com/pssjun)
