# 염준환 | ML 엔지니어 포트폴리오 🔍

## 간략 소개

안녕하세요. `모델을 만드는 데서 그치지 않고 API 서빙·컨테이너화·클라우드 배포까지 직접 완결`하는 ML 엔지니어 염준환입니다.

전기차 충전 수요 예측에서는 `단순 Baseline이 XGBoost를 이긴 결과`를 그대로 리포트하고, Feature Importance로 원인을 진단해 개선했습니다.

한국 도서 추천 시스템은 `Streamlit 단일 앱에서 FastAPI + Docker + Cloud Run 구조로 전환`하고, `Gemini 기반 RAG`로 추천 근거 설명까지 확장했습니다. GitHub Actions가 push마다 컨테이너를 실기동해 7가지 항목을 검증합니다.

졸업논문의 강화학습 모델은 `코드 없이 처음부터 재구현`하며, 원 논문과 다른 결과를 정직하게 규명했습니다.

앞으로도 `예상과 다른 결과의 원인을 끝까지 검증`하고, `외부 의존성이 실패해도 서비스가 멈추지 않는 구조`를 고민하는 엔지니어로 성장하고자 합니다.

## 💼 프로젝트

- [`[이커머스·콘텐츠 / 추천시스템 + MLOps]` 한국 도서 하이브리드 추천 시스템](https://github.com/pssjun/korean-book-recommender)
   - 알라딘 도서 6,974권 콘텐츠 임베딩(SentenceBERT+FAISS)과 협업필터링 6종 벤치마크 결합.
   - **FastAPI 서빙 → Docker 컨테이너화 → GitHub Actions CI → Cloud Run 배포**까지 확장.
   - Gemini 기반 **RAG 추천 근거 설명** 추가 (환각 억제·캐싱·모델 폴백 체인 설계).
   - ALS가 Baseline 대비 NDCG@10 +72.4% 달성, NCF 실패까지 정직하게 리포트.
   - 기술스택: FastAPI, Docker, Cloud Run, GitHub Actions, SentenceBERT, FAISS, Gemini API, Python

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

- **ML / DL**: `XGBoost` `PyTorch` `scikit-learn` `SentenceBERT` `FAISS` `Optuna`
- **LLM / RAG**: `Gemini API` `google-genai`
- **서빙 / 인프라**: `FastAPI` `Docker` `Cloud Run` `GitHub Actions` `Secret Manager`
- **데이터**: `pandas` `numpy` `aiohttp` `SQL`

## 읽어주셔서 감사합니다 :)

염준환 | ML 엔지니어  
Email: [pssjun8833@gmail.com](mailto:pssjun8833@gmail.com)  
GitHub: [pssjun](https://github.com/pssjun)
