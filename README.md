# 데이터 사이언티스트 염준환 포트폴리오

## 간략 소개

안녕하세요. `시계열 예측부터 추천 시스템, 강화학습까지` 서로 다른 방법론을 `기획부터 배포까지 직접 완결`한 데이터 사이언티스트 염준환입니다.

전기차 충전 수요를 예측하며 `Baseline 대비 XGBoost 모델의 성능을 직접 검증`했고, 
이 과정에서 모델 복잡도보다 데이터 특성에 대한 이해가 우선이라는 걸 체감했습니다.

이후 한국 도서 추천 시스템에서는 `콘텐츠 임베딩과 협업 필터링을 결합한 하이브리드 구조`를 설계했고, 
졸업논문의 강화학습 모델을 `코드 없이 처음부터 재구현`하며 재현 연구의 가치를 배웠습니다.

앞으로도 `예상과 다른 결과의 원인을 끝까지 검증`하는 데이터 사이언티스트로 성장하고자 합니다.

## 💼 목차

- **`[에너지·모빌리티 / 시계열예측]`** [전기차 충전소 시간대별 수요 예측](https://github.com/pssjun/ev-charging-forecast)
   - 공공데이터 6만 건 기반 XGBoost 4단계 모델링, Baseline 대비 검증 후 최종 R²=0.285 달성.
   - Streamlit 운영 대시보드로 실제 활용 가능한 형태까지 배포 완료.
   - 기술스택: XGBoost, Optuna, aiohttp, Streamlit, Python

- **`[이커머스·콘텐츠 / 추천시스템]`** [한국 도서 하이브리드 추천 시스템](https://github.com/pssjun/korean-book-recommender)
   - 알라딘 도서 6,974권 콘텐츠 임베딩(SentenceBERT+FAISS)과 협업필터링 6종 벤치마크 결합.
   - ALS가 Baseline 대비 NDCG@10 +72.4% 달성, NCF 실패까지 정직하게 리포트.
   - 기술스택: SentenceBERT, FAISS, PyTorch, Streamlit, Python

- **`[금융 / 강화학습 재현연구]`** [ESG 통합 강화학습 기반 포트폴리오 최적화](https://github.com/pssjun/esg-ppo-portfolio) *(논문)*
   - 원 논문 코드가 보존되지 않은 상태에서 PPO 환경을 전면 재구현, Optuna로 보상 가중치 탐색.
   - MVO 대비 성능·안정성을 다중 시드로 검증, 원 논문과 다른 발견을 정직하게 규명.
   - 기술스택: Gymnasium, Stable-Baselines3, Optuna, PyPortfolioOpt, Python

읽어주셔서 감사합니다 :)

데이터 사이언티스트 염준환
Email: [pssjun8833@gmail.com]
GitHub: [pssjun](https://github.com/pssjun)
