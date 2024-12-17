# 평가

평가는 언어 모델을 개발하고 배포하는 데 있어 매우 중요한 단계입니다. 이 단계를 통해 모델이 가진 다양한 영역에서 얼마나 잘 동작하는지 이해하고 개선이 필요한 부분을 파악할 수 있습니다. 이 모듈에서는 표준 벤치마크와 도메인별 평가를 위한 접근 방식을 모두 다루면서 소형 언어 모델을 종합적으로 평가합니다. 

Hugging Face에서 개발한 강력한 평가 라이브러리인 [`lighteval`](https://github.com/huggingface/lighteval)을 사용할 예정이며, 이 라이브러리는 Hugging Face 생태계와 자연스럽게 통합됩니다. 평가에 관한 개념적인 내용과 모범 사례에 대해 더 깊이 알아보고 싶다면 [가이드북](https://github.com/huggingface/evaluation-guidebook)을 확인하세요.

## 모듈 개요

철처한 평가 전략은 모델의 성능을 여러 측면에서 검토합니다. 모델이 다양한 문제를 얼마나 잘 처리하는지 이해하기 위해 질의응답이나 요약과 같은 특정 태스크 수행 능력을 평가하고 일관성 및 사실적 정확성 등을 바탕으로 출력 결과의 품질을 측정합니다. 안전성 평가는 유해한 출력 결과나 편향을 확인하는 데 도움이 됩니다. 마지막으로, 도메인 전문성 테스트를 통해 모델이 특정 분야에 대한 전문 지식을 가지고 있는지 검증합니다.

## 목차

### 1️⃣ [자동 벤치마크](./automatic_benchmarks.md)

표준화된 벤치마크와 평가 지표로 모델을 평가하는 법을 배워봅시다. MMLU 및 TruthfulQA와 같은 일반적인 벤치마크를 살펴보고, 주요 평가 지표와 설정을 이해하며, 재현 가능한 평가를 위한 모범 사례도 알아볼 것입니다.

### 2️⃣ [사용자 정의 도메인 평가](./custom_evaluation.md)

특정 사례에 대한 평가 파이프라인을 만드는 방법을 배워봅시다. 사용자 정의 평가 태스크 설계, 특화된 평가 지표 구현, 요구사항에 맞는 평가 데이터셋 구축 과정을 단계별로 살펴보겠습니다.

### 3️⃣ [도메인 평가 프로젝트](./project/README.md)

도메인 특화 평가 파이프라인 구축하는 과정 전체를 따라가봅시다. 평가 데이터셋 생성부터 Argilla를 활용한 데이터 어노테이션, 표준화된 데이터셋 제작, 그리고 LightEval을 사용한 모델 평가까지 단계별로 학습할 수 있습니다.

### 실습 노트북

| 목표 | 설명 | 실습 내용 | 링크 | Colab |
|-------|-------------|----------|------|-------|
| LLM 평가 및 결과 분석 | LightEval을 이용해 특정 도메인에서 모델을 평가하고 비교하는 방법 학습 | 🐢 의료 도메인 태스크를 활용해 모델 평가하기 <br> 🐕 다양한 MMLU 태스크로 새로운 도메인 평가 만들기 <br> 🦁 사용자 정의 도메인 평가 태스크 만들기 | [Notebook](./notebooks/lighteval_evaluate_and_analyse_your_LLM.ipynb) | <a target="_blank" href="https://colab.research.google.com/github/huggingface/smol-course/blob/main/4_evaluation/notebooks/lighteval_evaluate_and_analyse_your_LLM.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |

## 참고

- [평가 가이드북](https://github.com/huggingface/evaluation-guidebook) - LLM 평가에 대한 종합적인 가이드 제공
- [Hugging Face LightEval 문서](https://github.com/huggingface/lighteval) - LightEval 라이브러리 공식 문서
- [Argilla 문서](https://docs.argilla.io) - Argilla 어노테이션 플랫폼에 대한 학습 내용 제공
- [MMLU 논문](https://arxiv.org/abs/2009.03300) - MMLU 벤치마크 설명 논문
- [Creating a Custom Task](https://github.com/huggingface/lighteval/wiki/Adding-a-Custom-Task)
- [Creating a Custom Metric](https://github.com/huggingface/lighteval/wiki/Adding-a-New-Metric)
- [Using existing metrics](https://github.com/huggingface/lighteval/wiki/Metric-List)