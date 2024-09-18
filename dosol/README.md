# 1. LLM 지도

## 1.1 챗GPT의 등장과 LLM
2022년 말, 챗GPT가 등장하면서 대규모 언어 모델(LLM)이 세상을 뒤흔들었다. 기존의 언어 모델과는 달리, 챗GPT는 다음 단어를 확률적으로 예측하고 그 예측을 바탕으로 문장을 생성하는 방식으로 다양한 작업에서 뛰어난 성능을 보여준다. 이는 텍스트를 단순히 처리하는 기존 모델과 달리 사람과 자연스러운 대화를 할 수 있을 정도로 발전했다.

챗GPT의 혁신적인 성능에도 불구하고 그 동작 원리는 매우 단순한 방식에서 시작된다. 주어진 입력에서 다음에 올 적절한 단어를 예측하고, 그 단어를 입력에 추가해 문장이 완성될 때까지 반복한다.

## 1.2 딥러닝과 언어 모델링
LLM은 딥러닝 기술에 기반을 두고 있으며, 딥러닝은 신경망을 통해 데이터를 학습하는 기계 학습의 한 분야이다. 딥러닝은 텍스트와 이미지 같은 비정형 데이터에서 뛰어난 성능을 보여주며, 자연어 처리(NLP) 분야에서 텍스트를 생성하는 자연어 생성(NLG)을 연구하는 핵심 기술로 자리 잡았다.

2013년 구글의 **Word2Vec** 모델 발표를 시작으로, 2017년에는 **트랜스포머(Transformer)** 아키텍처가 등장하여 기존의 RNN을 대체하였으며, 2018년에는 OpenAI의 **GPT-1** 모델이 공개되었다. 이를 통해 언어 모델의 성능이 비약적으로 향상되었다.

### 1.2.1 임베딩
딥러닝 모델은 데이터를 처리하기 위해 임베딩(embedding)이라는 방식을 사용한다. 임베딩은 데이터를 숫자로 표현하여, 데이터 간의 유사성을 계산하거나 클러스터링에 활용할 수 있다. 대표적인 예로 **Word2Vec** 모델이 있다. 이를 통해 텍스트 데이터가 숫자의 집합으로 변환되고, 텍스트 간의 유사도를 기반으로 다양한 작업을 수행할 수 있다.

### 1.2.2 전이 학습(Transfer Learning)
전이 학습은 대량의 데이터로 학습된 모델을 다른 과제에 맞게 추가 학습하는 방식이다. 이 방식은 특히 학습 데이터가 적을 때 유용하다. LLM은 이 전이 학습 방식을 사용해 사전 학습된 모델을 특정 작업에 맞게 미세 조정하여 성능을 높인다.

## 1.3 트랜스포머 아키텍처와 GPT 시리즈
### 1.3.1 트랜스포머 아키텍처
2017년에 공개된 트랜스포머 아키텍처는 이전의 RNN을 대체하며, 텍스트 처리 성능을 크게 향상시켰다. 트랜스포머는 RNN과 달리, 입력 데이터를 순차적으로 처리하는 대신 모든 입력 데이터 간의 관계를 동시에 고려한다. 이를 통해 더 긴 문장을 처리할 때에도 성능 저하가 발생하지 않으며, 병렬 처리가 가능하여 학습 속도가 크게 향상된다.

### 1.3.2 GPT 시리즈
- **GPT-1 (2018년)**: 1억 1,700만 개의 파라미터를 사용한 첫 번째 모델로, 트랜스포머 아키텍처를 기반으로 개발되었다.
- **GPT-2 (2019년)**: 15억 개의 파라미터로, 모델 크기가 크게 확장되었다.
- **GPT-3 (2020년)**: 1,750억 개의 파라미터를 가진 모델로, 언어 생성 능력이 사람과 유사한 수준으로 발전했다.

## 1.4 챗GPT의 혁신과 RLHF
**챗GPT**는 기존 GPT 모델에 **인간 피드백을 활용한 강화 학습(RLHF)** 기술을 도입하여, 단순히 텍스트를 생성하는 것을 넘어 사용자의 요청에 맞춘 답변을 생성할 수 있게 되었다. RLHF는 사용자의 선호를 반영하여 더 나은 답변을 생성할 수 있도록 모델을 학습시키는 기술이다.

이 기술을 통해 LLM은 사용자의 요청에 맞춰 더욱 정교한 답변을 제공하며, 이를 정렬(alignment)이라고 부른다. 정렬을 통해 LLM이 사용자에게 도움이 되는 정보를 제공하는 방향으로 학습된다.

## 1.5 LLM 애플리케이션의 시대
챗GPT의 성공 이후, 많은 조직에서 LLM을 활용한 애플리케이션을 개발하고 있다. 이 장에서는 대표적인 두 가지 기술, **sLLM (Small LLM)**과 **RAG (Retrieval Augmented Generation)**을 간략히 소개한다.

- **sLLM**: 특정 작업이나 도메인에 맞게 추가 학습된 작은 모델로, 적은 파라미터로도 높은 성능을 발휘한다.
- **RAG**: 검색 증강 생성 기술로, LLM이 환각 현상을 일으키는 문제를 해결하기 위해 외부 지식을 검색하여 응답의 정확도를 높인다.

## 1.6 LLM의 확장: 멀티모달과 에이전트
LLM은 텍스트 처리 능력을 넘어 **멀티모달(Multi-modal)** 데이터 처리로 확장되고 있다. 멀티모달 LLM은 텍스트뿐만 아니라 이미지, 비디오, 오디오 등의 데이터를 처리할 수 있으며, 다양한 작업에서 활용될 수 있다.

또한, LLM을 활용한 **에이전트(Agent)** 연구도 활발히 진행 중이다. LLM은 텍스트 생성뿐만 아니라 의사결정과 계획 수립에도 활용될 수 있으며, **AutoGPT**와 같은 자동화 시스템이 이에 대한 대표적인 예시이다.


# 2. LLM의 중추, 트랜스포머 아키텍처 살펴보기

## 2.1 트랜스포머 아키텍처란
트랜스포머 아키텍처는 2017년 구글에서 발표된 모델로, 기존의 RNN(Recurrent Neural Network)의 한계를 극복하기 위해 개발되었다. 순차적으로 데이터를 처리하지 않고, 셀프 어텐션(Self-Attention) 메커니즘을 통해 병렬 연산이 가능하며, 더 긴 입력 데이터도 효율적으로 처리할 수 있다.

## 2.2 텍스트를 임베딩으로 변환하기
임베딩은 텍스트 데이터를 모델이 이해할 수 있는 숫자형 데이터로 변환하는 과정이다. 텍스트는 토큰화 과정을 통해 나누어진 뒤, 임베딩 층을 통해 숫자로 변환된다. 여기에 위치 인코딩(Positional Encoding)을 더하여 순서를 반영한 임베딩을 생성한다.

## 2.3 어텐션 이해하기
어텐션 메커니즘은 입력된 문장에서 중요한 단어들 사이의 관계를 파악하는 과정이다. 트랜스포머의 핵심은 이 어텐션 메커니즘을 활용하여 모든 입력 단어 간의 상관관계를 계산하는 것이다.

### 2.3.1 쿼리, 키, 값
- **쿼리(Query)**: 현재 처리 중인 단어
- **키(Key)**: 비교 대상이 되는 단어
- **값(Value)**: 키에 해당하는 단어의 임베딩 값
쿼리와 키의 관계를 계산하여 값에 반영하는 방식으로 동작한다.

## 2.4 정규화와 피드포워드 층
정규화는 입력 데이터의 분포를 일정하게 유지하기 위해 사용되며, 피드포워드 층은 입력 데이터의 특징을 학습하는 역할을 한다. 트랜스포머 아키텍처에서 정규화는 각 층의 입력을 안정적으로 만들어 준다.

## 2.5 인코더
인코더는 입력 텍스트를 이해하는 역할을 한다. 트랜스포머 인코더는 멀티 헤드 어텐션과 피드포워드 층을 반복적으로 적용하여 입력 데이터를 처리한다. 인코더는 텍스트의 문맥을 파악하여 디코더에 필요한 정보를 전달한다.

## 2.6 디코더
디코더는 인코더에서 전달된 정보를 바탕으로 출력 텍스트를 생성하는 역할을 한다. 인코더의 출력을 받아 다시 멀티 헤드 어텐션과 피드포워드 층을 거쳐 최종 출력을 생성한다.

## 2.7 BERT, GPT, T5 등 트랜스포머를 활용한 아키텍처
트랜스포머 아키텍처를 기반으로 한 대표적인 모델로는 BERT, GPT, T5가 있다. 
- **BERT**: 양방향으로 문맥을 학습하며, 텍스트 이해에 최적화된 모델.
- **GPT**: 텍스트 생성에 최적화된 모델로, 주로 생성 작업에 사용됨.
- **T5**: 텍스트 변환 작업에 최적화된 모델로, 다양한 자연어 처리 작업에 활용됨.

## 2.8 주요 사전 학습 메커니즘
트랜스포머 기반 모델을 학습시키기 위해서는 사전 학습(Pre-training)과 미세 조정(Fine-tuning)이 필요하다. 대규모 데이터를 통해 모델이 언어의 일반적인 패턴을 학습하고, 이후 특정 작업에 맞게 미세 조정된다.


# 3. 트랜스포머 모델을 다루기 위한 허깅페이스 트랜스포머 라이브러리

## 3.1 허깅페이스 트랜스포머란
허깅페이스 트랜스포머는 다양한 트랜스포머 모델을 통일된 인터페이스로 사용할 수 있도록 지원하는 오픈소스 라이브러리이다. 이를 통해 서로 다른 모델을 동일한 방식으로 쉽게 불러오고 사용할 수 있다. 트랜스포머 모델을 학습하고 추론하는 과정을 간소화해 연구와 개발의 속도를 높이는 데 기여하고 있다.

## 3.2 허깅페이스 허브 탐색하기
허깅페이스 허브는 사전 학습된 다양한 모델과 데이터셋을 제공하는 온라인 플랫폼이다. 사용자는 자신이 원하는 모델이나 데이터셋을 허브에서 검색하고 활용할 수 있으며, 자신이 만든 모델이나 데이터셋을 공유할 수도 있다. 

### 3.2.1 모델 허브
모델 허브에서는 NLP뿐만 아니라 컴퓨터 비전, 오디오 처리 등 다양한 작업을 위한 모델을 제공하며, 각 모델은 작업 유형, 언어, 라이선스 등을 기준으로 분류되어 있다.

## 3.3 허깅페이스 라이브러리 사용법 익히기
허깅페이스 라이브러리는 트랜스포머 모델과 토크나이저를 불러와 간단하게 모델 학습과 추론을 수행할 수 있다. 모델은 바디(body)와 헤드(head)로 구분되며, 같은 바디를 사용해 다른 작업을 수행할 수 있도록 설계되었다.

### 3.3.1 모델 불러오기
AutoModel과 AutoTokenizer 클래스를 사용해 BERT나 GPT-2 같은 모델을 불러올 수 있다. 예를 들어 BERT 모델과 GPT-2 모델을 거의 동일한 코드로 불러와 텍스트 토큰화를 수행한 뒤 모델에 입력할 수 있다.

### 3.3.2 토크나이저 사용하기
토크나이저는 텍스트를 토큰 단위로 나누고, 각 토큰을 아이디로 변환하는 역할을 한다. AutoTokenizer 클래스를 통해 쉽게 토크나이저를 불러와 사용할 수 있으며, 여러 문장을 한 번에 처리하거나, 패딩을 추가하여 길이를 맞출 수도 있다.

## 3.4 모델 학습하기
허깅페이스 트랜스포머는 Trainer API를 제공하여 모델 학습 과정을 간단하게 처리할 수 있다. Trainer API는 학습에 필요한 다양한 기능을 제공하여 학습을 자동화하고, 필요한 학습 인자와 평가 함수만 정의하면 된다. 또한, 트레이너 API를 사용하지 않고 직접 모델을 학습시키는 방법도 제공한다.

## 3.5 모델 추론하기
학습이 완료된 모델을 사용하여 새로운 데이터에 대한 추론을 수행할 수 있다. 학습된 모델은 텍스트 분류, 감정 분석 등 다양한 작업에 활용되며, 허깅페이스 허브에 업로드하여 공유할 수 있다.


# 4. 말 잘 듣는 모델 만들기

## 4.1 코딩 테스트 통과하기: 사전 학습과 지도 미세 조정

대규모 언어 모델(LLM)은 대량의 텍스트 데이터를 학습해 뛰어난 텍스트 생성 능력을 보여주었다. 하지만, 기본적으로 LLM은 사용자의 요청에 맞춰 답변하는 것이 아니라, 다음에 올 단어를 예측하는 방식으로 학습된 모델이기 때문에 한계가 있다. 이를 해결하기 위해 LLM은 **사전 학습**과 **지도 미세 조정(Supervised Fine-Tuning)** 단계를 거친다.

### 4.1.1 사전 학습
LLM의 사전 학습은 기본적인 프로그래밍 개념을 학습하는 과정과 유사하다. LLM은 파이썬 문법, 변수 선언, 반복문, 조건문과 같은 기초적인 개념을 학습하고, 대규모 텍스트 데이터를 통해 다음 단어를 예측하는 언어 모델링을 학습한다. 이 과정에서 LLM은 언어의 구조를 이해하고, 다양한 문장에서 다음에 올 단어를 예측하는 능력을 갖추게 된다.

사전 학습은 LLM이 언어에 대한 전반적인 이해도를 높이는 과정으로, 대규모 텍스트 데이터(예: 웹 페이지, 블로그, 코드 데이터 등)를 사용하여 이루어진다. 사전 학습을 통해 LLM은 다양한 언어적 상황에서 적절한 단어를 예측할 수 있는 능력을 가지게 된다.

### 4.1.2 지도 미세 조정
사전 학습을 거친 LLM은 지도 미세 조정 과정을 통해 특정 작업에 맞게 조정된다. **지도 미세 조정**은 사용자의 지시와 그에 따른 응답으로 이루어진 데이터셋을 기반으로 모델을 학습시키는 과정이다. 예를 들어, 사용자가 코딩 테스트에서 문제를 풀기 위해 작성한 코드와 그에 대한 피드백 데이터를 학습하게 된다. 이를 통해 LLM은 특정 요구에 맞는 정제된 응답을 제공할 수 있도록 조정된다.

이 과정에서 사용되는 데이터는 **지시 데이터셋(instruction dataset)**이라고 하며, 이는 사용자의 요청과 그에 대한 적절한 응답으로 구성된다. OpenAI는 챗GPT를 개발하면서 13,000개 이상의 지시 데이터셋을 수집해 모델을 학습시켰다.

## 4.2 채점 모델로 코드 가독성 높이기

코드 가독성은 개발자들이 코드 리뷰와 협업을 할 때 중요한 요소이다. 이를 위해 **코드 가독성 채점 모델**이 사용되며, 이 모델은 LLM을 기반으로 학습된다. 채점 모델은 두 가지 코드 중 어느 코드가 더 가독성이 높은지를 선택하는 **선호 학습(preference learning)** 방식을 사용한다. 

### 4.2.1 선호 학습을 위한 데이터셋 구축
채점 모델을 학습시키기 위해서는 사람이 더 선호하는 코드와 그렇지 않은 코드를 비교한 데이터를 수집한다. 이러한 데이터를 **선호 데이터셋(preference dataset)**이라고 하며, 더 가독성이 높은 코드를 **선호 데이터(chosen data)**로, 그렇지 않은 코드를 **비선호 데이터(rejected data)**로 분류한다. LLM은 이 데이터를 학습하여 가독성이 높은 코드를 선택하는 능력을 갖추게 된다.

이 과정에서 중요한 것은, 가독성 점수를 평가하기보다는 두 코드를 비교하여 더 가독성이 높은 코드를 선택하는 방식으로 데이터를 수집하는 것이 효과적이라는 점이다. 이 방식은 **지도 미세 조정(Supervised Fine-Tuning)** 방식으로 학습된다.

## 4.3 강화 학습이 꼭 필요할까?

OpenAI는 챗GPT를 학습시키기 위해 **강화 학습(Reinforcement Learning from Human Feedback, RLHF)**을 사용했다. RLHF는 LLM이 사람의 선호도를 반영하여 더 나은 답변을 생성할 수 있도록 학습하는 방법이다. 그러나 강화 학습은 하이퍼파라미터에 민감하고 학습이 불안정해 많은 연구자들이 어려움을 겪어 왔다. 이를 해결하기 위해 강화 학습을 사용하지 않고 선호를 학습하는 여러 방법들이 개발되었다.

### 4.3.1 기각 샘플링 (Rejection Sampling)
기각 샘플링은 리워드 모델을 통해 가장 높은 점수를 받은 응답만을 선택하여 학습하는 방식이다. 이는 간단하고 직관적인 방법으로, 리워드 모델로 평가한 결과 중 점수가 가장 높은 응답만을 지도 미세 조정에 사용한다. 이를 통해 안정적이고 효율적으로 사람의 선호도를 반영한 학습이 가능하다.

### 4.3.2 직접 선호 최적화 (Direct Preference Optimization, DPO)
DPO는 리워드 모델 없이 선호 데이터셋을 직접 학습하는 방법이다. 기존의 RLHF와 달리, DPO는 리워드 모델을 만들지 않고 바로 선호 데이터를 기반으로 LLM을 학습시킨다. 이 방식은 학습 과정이 단순하며, 선호 학습의 성능을 빠르게 높일 수 있다. DPO는 2024년 기준으로 가장 많이 사용되는 선호 학습 방법이다.


# 5. GPU 효율적인 학습

## 5.1 GPU에 올라가는 데이터 살펴보기
딥러닝 모델은 많은 행렬 곱셈을 통해 학습과 추론을 수행하며, 이 과정에서 GPU가 효율적으로 활용된다. 그러나 LLM의 크기가 커짐에 따라 하나의 GPU에 모델을 모두 올리기 어려운 경우가 많아졌다. 이 장에서는 GPU의 한정된 메모리를 효율적으로 사용하는 방법을 설명한다.

### 5.1.1 딥러닝 모델의 데이터 타입
딥러닝 모델은 보통 32비트 부동소수점(float32)을 사용하지만, 모델의 크기가 커지면서 16비트 부동소수점(fp16)과 bfloat16 형식으로 변환해 메모리 사용을 줄이는 양자화 기술이 개발되었다. 이 기술을 통해 더 적은 메모리로도 LLM을 학습하고 추론할 수 있다.

### 5.1.2 양자화로 모델 용량 줄이기
양자화는 모델의 파라미터를 적은 비트의 형식으로 변환해 메모리 사용을 줄이는 방법이다. fp32 형식을 fp16이나 int8로 변환하면 모델의 용량을 크게 줄일 수 있지만, 정보 손실이 발생할 수 있어 이를 최소화하는 것이 중요하다.

## 5.2 단일 GPU 효율적으로 활용하기
GPU의 메모리는 제한적이므로, 이를 효율적으로 활용하기 위한 두 가지 주요 기법이 소개된다.
> 그레이디언트 누적과 그레이디언트 체크포인팅.

### 5.2.1 그레이디언트 누적
그레이디언트 누적은 배치 크기를 제한적으로 설정하여 메모리 부족 문제를 해결하는 방법이다. 여러 배치의 학습 결과를 누적한 후 모델을 업데이트하여 마치 더 큰 배치를 사용하는 것과 같은 효과를 낸다.

### 5.2.2 그레이디언트 체크포인팅
그레이디언트 체크포인팅은 순전파 과정에서 모든 데이터를 저장하지 않고, 일부만 저장하여 메모리 사용을 줄이는 방법이다. 메모리 효율성은 높아지지만, 계산 시간이 증가할 수 있다.

## 5.3 분산 학습과 ZeRO
분산 학습은 여러 GPU를 사용해 모델 학습을 가속화하거나 큰 모델을 학습하는 방법이다.

### 5.3.1 데이터 병렬화와 모델 병렬화
데이터 병렬화는 동일한 모델을 여러 GPU에 올려 학습 데이터를 병렬로 처리하는 방법이며, 모델 병렬화는 모델을 여러 GPU에 나누어 학습하는 방법이다. 각각의 방법은 모델 크기와 학습 속도 요구에 따라 선택된다.

### 5.3.2 ZeRO(Zero Redundancy Optimizer)
ZeRO는 중복되는 메모리 사용을 줄이기 위한 방법으로, 모델 파라미터, 그레이디언트, 옵티마이저 상태를 여러 GPU에 나눠 저장해 메모리 사용을 최소화한다. 이를 통해 대규모 모델도 효율적으로 학습할 수 있다.

## 5.4 효율적인 학습 방법(PEFT): LoRA
LoRA(Low-Rank Adaptation)는 LLM의 일부 파라미터만 학습하여 메모리 사용을 줄이는 PEFT(Param Efficient Fine-Tuning) 방법이다.

### 5.4.1 LoRA의 원리
LoRA는 파라미터 행렬을 두 개의 더 작은 행렬로 분해하여 학습함으로써, 전체 파라미터 대신 일부 파라미터만 학습하는 방법이다. 이를 통해 학습에 필요한 메모리와 연산량을 줄일 수 있다.

## 5.5 효율적인 학습 방법(PEFT): QLoRA
QLoRA는 LoRA에 양자화를 추가하여 더 적은 메모리로 모델을 학습하는 방법이다. 16비트 대신 4비트로 모델을 저장하고, 양자화 상수에 대한 2차 양자화도 적용한다. 페이지 옵티마이저 기능을 사용해 OOM(Out of Memory) 에러를 방지한다.


# 6. sLLM 학습하기

## 6.1 Text2SQL 데이터셋

### 6.1.1 대표적인 Text2SQL 데이터셋
이번 장에서는 범용 LLM에 비해 비용 효율적이며 특정 작업에 특화된 **sLLM(Specialized Large Language Model)**에 대해 다룬다. **Text2SQL**은 자연어로 작성된 요청을 SQL로 변환하는 작업을 말한다. 대표적인 데이터셋으로 **WikiSQL**과 **Spider**가 있으며, 이 두 데이터셋은 주로 영어로 구성되어 있다. WikiSQL은 단순한 SQL 쿼리로 구성된 반면, Spider는 더 복잡한 SQL 쿼리를 포함한다.

한국어 데이터셋으로는 **AI 허브**에서 제공하는 NL2SQL 데이터가 있지만, 현재 공개가 중단된 상태이다. -> 실습에서는 합성 데이터셋을 사용.

## 6.2 성능 평가 파이프라인 준비하기

### 6.2.1 Text2SQL 평가 방식
기존의 평가 방식으로는 **EM(Exact Match)** 방식과 **실행 정확도(Execution Accuracy)** 방식이 있지만, 이번 실습에서는 **GPT-4**를 활용하여 평가를 수행한다. 평가 데이터셋은 8개의 데이터베이스로 구성되며, 게임 도메인(db_id = 1)을 평가용 데이터셋으로 사용힌다.

### 6.2.2 SQL 생성 프롬프트
SQL 생성을 위한 프롬프트는 `make_prompt` 함수를 사용하여 생성되며, DDL과 자연어 질문을 기반으로 SQL 쿼리를 생성하는 명령을 포함한다. 학습 데이터는 정답 SQL을 포함하고, 생성 시에는 SQL 부분을 빈 문자열로 남겨두어 학습과 추론을 구분한다.

## 6.3 실습: 미세 조정 수행하기

### 6.3.1 기초 모델 평가하기
실습에서는 한국어 사전 학습 모델인 **beomi/Yi-Ko-6B**를 사용한다. `make_inference_pipeline` 함수를 통해 기초 모델을 불러와 SQL 쿼리를 생성하고, 그 결과를 평가한다. 기초 모델은 기본적인 SQL 생성 능력이 있지만 추가적인 학습이 필요하다.

### 6.3.2 미세 조정 수행
미세 조정에는 **autotrain-advanced** 라이브러리를 사용하며, 학습 데이터를 준비한 후 `make_prompt` 함수를 이용해 프롬프트를 생성한다. 미세 조정은 LoRA 설정을 적용해 메모리 효율을 높이고, 학습을 진행한다.

### 6.3.3 성능 평가
미세 조정 후, GPT-4를 활용해 평가를 수행하고, LoRA 파라미터에 따른 성능 차이를 확인한다. **lora_r**과 **lora_alpha** 값을 조정하여 실험을 진행했으며, 성능을 비교한 결과 미세 조정 후 성능이 크게 향상되었다.

### 6.3.4 데이터 정제 및 성능 비교
GPT-4를 활용해 학습 데이터셋을 필터링하고, 필터링된 데이터를 이용한 학습 결과 성능이 개선되었다. 데이터셋 크기와 성능 간의 관계를 확인하기 위해 데이터를 20%씩 증가시키며 실험을 진행한 결과, 더 많은 데이터를 사용할수록 성능이 향상되었다.

### 6.3.5 기초 모델 변경
더 큰 모델인 **beomi/OPEN-SOLAR-KO-10.7B**를 사용하여 동일한 실험을 진행한 결과, 더 높은 성능을 달성할 수 있었다. 미세 조정 후 성능이 82.1%로, 기초 모델보다 월등히 높았다.


# 7장: LLM의 추론 효율화
이번 장에서는 추론 과정에서 GPU 자원을 효율적으로 사용하는 방법을 중점적으로 다룬다.

## 7.1 언어 모델 추론 이해하기

### 7.1.2 중복 연산을 줄이는 KV 캐시
**KV 캐시**는 셀프 어텐션 연산 과정에서 동일한 입력 토큰에 대해 중복 계산이 발생하는 비효율을 줄이기 위해 먼저 계산했던 키와 값 결과를 메모리에 저장해 활용하는 방법을 말한다.

### 7.1.3 GPU 구조와 최적의 배치 크기
서빙이 효율적인지 판단하는 기준: 비용, 처리량, 지연 시간
**메모리 바운드**: 최적의 배치 크기보다 배치 크기가 작으면 모델 파라미터를 이동시키느라 연산이 멈추는 비효율 발생.
**연산 바운드**: 배치 크기가 최적 크기보다 커지면 연산에 더 오랜 시간이 걸려 지연 시간이 길어지는 경우.

### 7.1.4 KV 캐시 메모리 줄이기
멀티 쿼리 어텐션: 모든 쿼리 벡터가 하나의 키와 값 벡터를 공유
**그룹 쿼리 어텐션**: 멀티 헤드 어텐션과 멀티 쿼리 어텐션의 절충안

## 7.2 양자화로 모델 용량 줄이기
**양자화(Quantization)**는 모델의 파라미터를 적은 비트로 변환하여 GPU 메모리를 절약하는 방법이다. 주로 4비트, 8비트 양자화가 사용되며, 이를 통해 메모리 사용량을 크게 줄일 수 있다.

대표적인 양자화 기법: 비츠앤바이츠(BitsAndBytes), GPTQ(GPT Quantization), AWQ(Activation-aware Weight Quantization)

### 7.2.1 비츠앤바이츠
**비츠앤바이츠(BitsAndBytes)**는 8비트 행렬 연산과 4비트 양자화를 지원하는 라이브러리. 특히 4비트 양자화는 성능 저하 없이 메모리 사용을 크게 줄일 수 있는 방법으로, 모델 파라미터를 적은 비트로 변환하면서도 중요한 파라미터의 손실을 최소화한다.

### 7.2.2 GPTQ
**GPTQ(GPT Quantization)**는 모델이 양자화되기 전후의 성능 차이를 최소화하는 방식으로, 학습 후 양자화를 수행한다. GPTQ는 입력 데이터를 기반으로 최적의 양자화를 수행하여, 성능 저하를 최소화하는 동시에 메모리 사용을 줄인다.

### 7.2.3 AWQ
**AWQ(Activation-aware Weight Quantization)**는 모델의 활성화 값에 따라 중요한 파라미터를 구분하고, 중요한 파라미터는 원래의 비트 크기로 유지하는 방식. 이를 통해 성능 손실을 최소화하면서도 양자화를 효과적으로 적용할 수 있다.

## 7.3 지식 증류 활용하기
**지식 증류(Knowledge Distillation)**는 성능이 좋은 대형 모델(선생 모델)의 결과를 작은 모델(학생 모델)로 전이하는 방법. 이 방식은 대형 모델의 추론 결과를 사용해 작은 모델을 학습시키는 방식으로, 더 작은 모델이 더 큰 모델의 성능을 모방할 수 있도록 한다.

최근에는 GPT-4와 같은 대형 모델을 활용해 **sLLM(Small LLM)**을 학습시키는 방식이 일반적으로 사용되고 있음.


# 8장: LLM의 효율적인 서빙 전략

## 8.1 효율적인 배치 전략
언어 모델 추론에서는 효율적인 배치 전략이 중요하다. 모델이 입력 데이터를 한 번에 처리할 수 있도록 배치 크기를 적절히 설정하면 GPU 자원을 효율적으로 사용할 수 있다.

### 8.1.1 일반 배치(정적 배치)
가장 기본적인 배치 방식으로, 여러 개의 입력을 한 번에 처리하는 방식. 모든 입력이 처리될 때까지 대기하며, 배치 내의 데이터는 처리량이 줄어들 수 있다. 이 방식은 단순하지만, 배치 내의 일부 데이터가 빠르게 완료되더라도 모든 데이터가 끝날 때까지 기다리므로 비효율성이 존재.

### 8.1.2 동적 배치
동적 배치는 비슷한 시간에 들어오는 여러 요청을 묶어 배치 크기를 최적화하는 방식. 이를 통해 처리량을 높이고, 처리 시간이 더 길어질 수 있지만 GPU 자원의 효율을 높일 수 있다. 그러나 토큰 생성 시간이 다를 경우 배치 크기는 다시 줄어들 수 있다.

### 8.1.3 연속 배치
연속 배치는 배치 내에서 생성이 끝난 데이터는 제거하고, 새로운 데이터를 추가해 계속해서 배치를 유지하는 방식. 이 방식은 GPU 자원을 보다 효율적으로 활용하며, 대기 시간을 줄일 수 있다.

## 8.2 효율적인 트랜스포머 연산
**플래시어텐션(FlashAttention)**과 **페이지어텐션(PagedAttention)**을 통해 트랜스포머의 연산 효율성을 높이는 방법을 설명한다.

### 8.2.1 플래시어텐션
**플래시어텐션**은 트랜스포머 모델이 더 긴 시퀀스를 처리할 수 있도록 어텐션 연산을 블록 단위로 처리하는 방식. 이 방법은 메모리 사용을 줄이고 연산 속도를 높이는 데 중점을 두고 있다. 더 긴 시퀀스를 처리하면서도 GPU 자원을 효율적으로 사용하게 된다.

### 8.2.2 상대적 위치 인코딩
기존의 절대적 위치 인코딩은 긴 시퀀스를 처리할 때 성능 저하가 발생할 수 있다. 이를 해결하기 위해 **상대적 위치 인코딩** 방식이 도입되었다. 입력 토큰 간의 상대적 거리를 기반으로 위치 정보를 모델에 입력하여, 더 긴 시퀀스에서도 성능 저하를 방지함.

## 8.3 효율적인 추론 전략

### 8.3.1 커널 퓨전
**커널 퓨전**은 GPU에서 반복적으로 발생하는 연산을 하나로 묶어 연산 효율을 극대화하는 기법. 각각의 연산을 독립적으로 수행하는 대신, 여러 연산을 한 번에 처리함으로써 GPU 오버헤드를 줄이고 성능을 높일 수 있다.

### 8.3.2 페이지어텐션
기존의 **KV 캐시**는 메모리 사용량이 크고, 배치 크기가 제한되는 단점이 있다. 이를 해결하기 위해 **페이지어텐션**이 도입되었다. 페이지어텐션은 키-값(KV) 캐시를 더 작은 블록 단위로 나누어 관리함으로써 메모리 사용량을 줄이고, 동시에 더 많은 배치를 처리할 수 있게 한다.

### 8.3.3 추측 디코딩
**추측 디코딩(Speculative Decoding)**은 작은 모델이 쉬운 단어를 예측하고, 더 큰 모델이 어려운 단어를 예측하는 방식으로 추론 속도를 높이는 기법이다. 이 기법과 드래프트 모델(draft model)과 타깃 모델(target model)을 함께 사용하여 추론 속도를 극대화하면서도 성능을 유지할 수 있다.

## 8.4 실습: LLM 서빙 프레임워크
**vLLM 프레임워크**를 사용한 실습을 진행. vLLM은 허깅페이스의 모델을 기반으로 다양한 LLM 모델의 추론을 지원하며, 오프라인 및 온라인 서빙을 모두 지원함.

### 8.4.1 오프라인 서빙
**오프라인 서빙**은 미리 준비된 데이터셋에 대해 대규모 배치로 추론을 수행하는 방식. 배치 크기를 최적화함으로써 처리량을 극대화할 수 있다.

### 8.4.2 온라인 서빙
**온라인 서빙**은 사용자의 요청이 실시간으로 들어올 때마다 추론을 수행하는 방식. 이를 통해 동적으로 들어오는 요청에 대해 배치 크기를 자동으로 조절할 수 있으며, GPU 자원을 효율적으로 활용할 수 있다.


# 9장: LLM 애플리케이션 개발하기

## 9.1 검색 증강 생성(RAG)
LLM은 단독으로 정확한 응답을 제공하는 데 한계가 있다. **검색 증강 생성**(Retrieval Augmented Generation, RAG) 기법을 사용하면 모델이 질문에 답변할 때 필요한 정보를 검색하고, 이를 바탕으로 응답의 정확성을 높일 수 있다. 

### 9.1.1 데이터 저장
검색 증강 생성을 위한 첫 단계는 **데이터 저장**이다. 데이터 소스에서 필요한 데이터를 벡터로 변환하고, 이 임베딩 벡터를 **벡터 데이터베이스**에 저장한다. 벡터 데이터베이스는 임베딩 벡터 간의 유사도를 비교하여 관련된 데이터를 빠르게 검색할 수 있다.

### 9.1.2 검색 결과 통합
데이터를 벡터 데이터베이스에 저장한 후, 사용자의 요청과 관련된 데이터를 검색하여 LLM에 제공하는 단계. **프롬프트 통합** 과정에서 검색된 데이터를 프롬프트에 반영하여 LLM이 더욱 정확한 답변을 생성할 수 있도록 도와준다.

## 9.2 LLM 캐시
LLM을 사용하는 애플리케이션에서 비용과 시간을 절약하기 위해 **LLM 캐시**를 사용할 수 있다. 캐시는 동일하거나 유사한 요청이 있을 때 LLM이 다시 추론하지 않고 이전 결과를 반환하는 방식이다.

### 9.2.1 일치 캐시
**일치 캐시**는 사용자의 요청이 이전에 완전히 동일했던 경우, 즉 문자열 그대로 일치하는 요청이 있을 때 그에 해당하는 응답을 캐시에서 가져오는 방식이다. 이 방식은 가장 간단하지만 완전히 동일한 요청만 처리할 수 있다는 제한이 있다.

### 9.2.2 유사 검색 캐시
**유사 검색 캐시**는 사용자의 요청이 이전과 유사한 경우, 임베딩 벡터를 사용해 유사도를 계산하여 관련된 응답을 캐시에서 가져오는 방식이다. 임베딩 모델을 통해 요청을 벡터로 변환하고, 벡터 데이터베이스에서 가장 유사한 벡터를 찾아내는 과정을 거친다. 이 방법은 일치 캐시보다 더 유연하게 동작하지만, 임베딩 및 검색에 추가적인 연산이 필요하다.

## 9.3 데이터 검증
LLM 애플리케이션을 운영할 때는 부적절한 요청이나 결과가 발생하지 않도록 **데이터 검증**이 필수적이다. 데이터 검증을 통해 민감한 정보를 걸러내고, 부적절한 요청에 대해 LLM이 응답하지 않도록 설정할 수 있다.

### 9.3.1 규칙 기반 검증
**규칙 기반 검증**은 정규 표현식이나 문자열 매칭을 사용해 특정 패턴을 검출하는 방식이다. 예를 들어, 전화번호나 이메일과 같은 개인정보를 필터링하기 위해 사용할 수 있다.

### 9.3.2 분류 또는 회귀 모델
**분류 모델**이나 **회귀 모델**을 통해 데이터를 검증할 수 있다. 예를 들어, 부정적인 감정 표현을 검출해 특정 스코어 이상인 경우 다시 생성하게 하거나, 부적절한 내용을 자동으로 검출하는 방식을 사용한다.

### 9.3.3 임베딩 유사도 기반 검증
**임베딩 유사도 기반 검증**은 임베딩 모델을 사용해 요청이나 생성 결과가 특정 기준과 유사한지를 계산하는 방식이다. 예를 들어, 정치적인 질문에 대한 응답을 제한하고자 할 때, 정치와 관련된 임베딩 벡터와 요청을 비교하여 응답 여부를 결정할 수 있다.

### 9.3.4 LLM을 활용한 검증
LLM 자체를 활용하여 생성된 결과를 검증할 수 있다. 예를 들어, LLM에게 응답이 정책에 맞는지 확인하도록 요청하고, 부적절한 응답이 감지되면 다시 생성하거나 응답을 거부할 수 있다.

## 9.4 데이터 로깅
LLM 애플리케이션에서 **데이터 로깅**은 LLM의 입력과 출력을 기록함으로써 애플리케이션의 상태를 추적하고, 문제가 발생했을 때 원인을 파악할 수 있도록 한다. 동일한 입력이라도 매번 다른 결과를 생성할 수 있기 때문에 로깅은 특히 중요.

### 9.4.1 로깅 도구
대표적인 로깅 도구로는 **W&B(Weights and Biases)**, **MLflow**, **PromptLayer** 등이 있다. 이러한 도구들은 LLM의 입력, 출력, 생성에 걸린 시간, 에러 여부 등을 기록하며, 이를 통해 성능을 모니터링하고 개선할 수 있다.


# 10장: 임베딩 모델로 데이터 검색하기

## 10.1 텍스트 임베딩 이해하기
임베딩은 텍스트의 의미를 압축해 벡터 형식으로 변환하는 방법이다. 이 장에서는 밀집 임베딩 방식을 중심으로 문장을 임베딩하는 다양한 기법을 다룬다.

### 10.1.1 문장 임베딩 방식의 장점
문장 임베딩은 단순히 단어의 빈도를 넘어 문장 간의 의미적 관계를 계산할 수 있다는 장점이 있다. 예를 들어, ‘학교’와 ‘공부’는 0.595의 유사도를 보이며, 서로 의미적으로 관련이 있다는 것을 확인할 수 있다.

### 10.1.2 원핫 인코딩
원핫 인코딩은 각 단어를 독립적으로 표현하는 방법으로, 단어 간의 관계를 고려하지 않는다는 단점이 있다. 예를 들어, ‘학교’와 ‘공부’는 완전히 독립적인 벡터로 표현되며, 그 사이의 관계는 표현되지 않는다.

### 10.1.3 백오브워즈
백오브워즈(Bag of Words)는 문서에 등장한 단어의 빈도를 기반으로 문서를 표현하는 방식이다. 하지만 단순한 빈도만을 고려하기 때문에 의미적으로 관련이 없는 단어들도 중요하게 간주될 수 있다.

### 10.1.4 TF-IDF
TF-IDF(Term Frequency-Inverse Document Frequency)는 백오브워즈의 단점을 보완한 방식으로, 문서에서 자주 등장하지만 여러 문서에서 흔히 등장하는 단어의 가중치를 낮추는 기법이다.

### 10.1.5 워드투벡
워드투벡(Word2Vec)은 주변 단어의 빈도를 바탕으로 단어 간의 의미적 관계를 학습하는 방식이다. 이는 밀집 임베딩 방식을 사용하여 단어 간의 의미적 유사성을 반영할 수 있게 한다.

## 10.2 문장 임베딩 방식
단어 임베딩의 성공 이후, 문장을 임베딩으로 변환하는 방법이 개발되었다. 문장 임베딩을 통해 문장 간의 유사도를 벡터 연산으로 계산할 수 있으며, 특히 트랜스포머 기반의 인코더 모델들이 그 성능을 입증하고 있다.

### 10.2.1 문장 사이의 관계를 계산하는 두 가지 방법
문장 간의 관계를 계산하는 대표적인 방법은 바이 인코더와 교차 인코더.
바이 인코더는 각각의 문장을 독립적으로 처리하고, 그 임베딩 벡터 간의 유사도를 계산하는 방식. 반면 교차 인코더는 두 문장을 동시에 입력하여 직접적인 유사도를 계산하는 방식.

### 10.2.2 바이 인코더 모델 구조
바이 인코더는 문장의 길이가 달라도 고정된 차원의 임베딩 벡터를 반환하기 위해 풀링 층을 사용한다. 이 층을 통해 문장 간의 유사도를 쉽게 계산할 수 있다.

### 10.2.3 Sentence-Transformers로 임베딩 생성하기
Sentence-Transformers 라이브러리를 활용하면 허깅페이스 모델 허브에서 제공하는 다양한 사전 학습 모델을 쉽게 사용할 수 있다. 이를 통해 텍스트뿐만 아니라 이미지도 임베딩으로 변환할 수 있다.

## 10.3 실습: 의미 검색 구현하기

### 10.3.1 의미 검색이란?
의미 검색은 단순히 키워드 매칭이 아닌, 문장 임베딩을 기반으로 문서 간의 의미적 유사성을 바탕으로 검색하는 방식. 이를 통해 키워드가 동일하지 않더라도 의미적으로 관련된 문서를 검색할 수 있다.

### 10.3.2 라마인덱스에서 Sentence-Transformers 모델 사용하기
라마인덱스(LlamaIndex)는 기본적으로 OpenAI의 임베딩 모델을 사용하지만, Sentence-Transformers와 같은 오픈소스 모델을 활용할 수도 있다.

## 10.4 검색 방식을 조합해 성능 높이기

### 10.4.1 키워드 검색 방식: BM25
BM25는 TF-IDF를 기반으로 문서의 길이에 대한 가중치를 추가한 검색 알고리즘. 이는 주로 일래스틱서치와 같은 검색 엔진에서 사용된다.

### 10.4.2 키워드 검색과 의미 검색 조합하기
키워드 검색과 의미 검색은 각자의 장단점이 있다. 이를 보완하기 위해 두 가지 방식을 조합한 **하이브리드 검색**을 사용할 수 있다. 하이브리드 검색은 키워드와 의미 검색 결과의 순위를 결합해 최종 검색 결과를 산정한다.

## 10.5 실습: 하이브리드 검색 구현하기
실습에서는 BM25와 의미 검색을 조합해 하이브리드 검색을 구현한다. 이를 통해 검색의 정확성을 높일 수 있다.


# 11장: 임베딩 모델 만들기와 RAG 개선하기

## 11.1 검색 성능을 높이기 위한 두 가지 방법
**바이 인코더**와 **교차 인코더**를 결합하는 방법을 사용. 
- **바이 인코더**: 대규모 데이터를 빠르게 처리할 수 있는 장점이 있지만, 정확도가 떨어질 수 있다.
- **교차 인코더**: 유사도를 더 정확하게 계산하지만 느리기 때문에 소수의 데이터에만 적용한다.
위 두 방법을 결합하여 먼저 바이 인코더로 대량의 데이터를 빠르게 처리한 후, 교차 인코더로 소수의 후보군을 정밀하게 재정렬하는 방식으로 검색 성능을 향상시킬 수 있다.

## 11.2 언어 모델을 임베딩 모델로 만들기
BERT나 RoBERTa 같은 언어 모델을 기반으로 **문장 임베딩 모델**을 만들 수 있다. 문장 임베딩 모델은 입력 문장의 길이와 상관없이 고정된 차원의 벡터로 변환한다. 이 과정에서 **풀링 층**을 사용하여 문장의 의미를 추출한다.
- **대조 학습(Contrastive Learning)**: 관련이 있는 데이터는 가까워지고, 관련이 없는 데이터는 멀어지도록 학습하는 방식.

## 11.2.1 대조 학습(Contrastive Learning)
대조 학습은 임베딩 모델을 학습시킬 때 주로 사용하는 방식. 예를 들어, 두 문장이 서로 유사하다면 임베딩 벡터 간의 거리를 가깝게 만들고, 그렇지 않다면 거리를 멀게 학습한다.

## 11.2.2 실습: 학습 준비하기
KLUE의 STS(Sentence Textual Similarity) 데이터셋을 사용하여 문장 임베딩 모델을 학습한다. (두 문장 간의 유사도를 점수로 매긴 데이터셋) 데이터를 전처리하여 학습, 검증, 평가 데이터셋으로 나눈 후 학습에 사용할 배치 데이터를 준비한다.

## 11.3 임베딩 모델 미세 조정하기
검색 증강 생성(RAG)에서 중요한 역할을 하는 임베딩 모델을 사용자의 데이터에 맞춰 **미세 조정(Fine-tuning)** 하면 성능을 크게 향상시킬 수 있다. 이번 실습에서는 **KLUE MRC 데이터셋**을 사용해 임베딩 모델을 미세 조정한다.

### 11.3.1 실습: 학습 준비
KLUE MRC 데이터셋을 사용하여 문장 간의 유사도를 학습하기 위한 데이터를 준비한다. 이 데이터셋은 기사 본문과 해당 기사와 관련된 질문을 포함하고 있어 문장 간 유사도를 학습하는 데 적합하다는 특징이 있다.

### 11.3.2 MNR 손실을 활용해 미세 조정하기
**MNR(Multiple Negatives Ranking)** 손실 함수는 학습 데이터에 포함된 관련 없는 데이터를 배치 내에서 자동으로 샘플링하여 학습한다. 이 방법을 통해 MRC 데이터셋으로 임베딩 모델을 미세 조정한 후 성능을 평가힌다.

## 11.4 검색 품질을 높이는 순위 재정렬
**순위 재정렬(Reranking)**은 검색된 결과를 다시 정렬하여 더 정확한 순서로 제공하는 방법이다. 
- 바이 인코더는 빠른 검색을 제공하지만 정확도가 떨어질 수 있으므로, 교차 인코더를 사용하여 순위를 재정렬하면 검색 품질을 높일 수 있다.

## 11.5 바이 인코더와 교차 인코더로 개선된 RAG 구현하기
바이 인코더와 교차 인코더를 결합하여 **RAG(Retrieval Augmented Generation)** 시스템을 개선할 수 있다. 바이 인코더로 검색된 상위 30개의 결과에서 교차 인코더로 상위 10개의 결과를 재정렬하여 더 정확한 검색 결과를 제공한다.

### 11.5.1 기본 임베딩 모델로 검색하기
기본 임베딩 모델을 사용하여 상위 10개의 검색 결과를 확인한다. 성능을 **Hit Rate**로 평가하며, 기본 임베딩 모델로 검색했을 때 88%의 정답률을 기록했음.

### 11.5.2 미세 조정한 임베딩 모델로 검색하기
미세 조정한 임베딩 모델을 사용해 검색 성능을 평가한다. 미세 조정 후 검색 성능은 94.6%로 향상되었으며, 처리 시간은 크게 증가하지 않았다.

### 11.5.3 미세 조정한 임베딩 모델과 교차 인코더 조합하기
미세 조정한 임베딩 모델과 교차 인코더를 조합하여 성능을 평가한 결과, 97.3%의 정답률을 기록했다. 성능은 더욱 향상되었지만, 처리 시간이 증가했다.