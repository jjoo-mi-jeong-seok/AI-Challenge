![speech](https://capsule-render.vercel.app/api?type=speech&height=200&fontSize=40&color=FD5B43&text=이미지로%20묻고,%20AI로%20답하다.&animation=NONE&fontAlign=30,60&fontAlignY=35,55&fontColor=ffffff)

# 1. 이미지 기반 질의응답 모델 개발
<img width="1200" height="100" alt="image" src="https://github.com/user-attachments/assets/627c27d6-5a18-42d8-b75f-57ef2ffaccc9" />

삼성청년SW·AI아카데미(SSAFY) 14기 과정 중 Kaggle에서 진행된 이미지 기반 질의 응답(VQA) 모델 개발 AI 챌린지 대회에 참가했습니다.<br/>

### ■ 대회 개요
이미지 속 세상을 ‘읽고, 이해하고, 답하는’ 인공지능, VQA(Visual Question Answering)는 인간의 시각적 사고에 가장 가까운 형태의 AI 기술입니다.

AI 챌린지는 이미지와 텍스트를 함께 이해하는 멀티모달 인공지능을 직접 개발하고 평가하는 대회로, <br/>본 대회를 통해 실제 환경에서 활용 가능한 AI 모델을 개발하는 것을 목표로 합니다.

- `Start`: Oct 23, 2025
- `Close`: Oct 27, 2025

### ■ VQA 모델이 필요한 이유
1. 시각 정보 해석 능력의 확장
기존 AI는 '보거나 말할 수 있는' 수준에 머물렀습니다.<br/>
하지만 VQA 모델은 "이 이미지에 뭐가 있지?", "이 장면은 어디일까?" 같은 질문에 스스로 답하며, AI가 단순 인식에서 '이해'로 나아가는 중요한 전환점을 만들어냅니다.

2. 실제 서비스에 적용 가능한 기술<br/>
   > VQA는 'AI가 세상을 설명하는 기술'로서 산업 전반에 파급력을 가집니다.
   - 스마트 팩토리: 영상 데이터 기반 품질 이상 탐지 및 설명
   - 의료 영상 분석: 진단 보조를 위한 시각적 질의응답
   - 자율주행 및 CCTV: 상황 인식 및 위험 설명
   - 교육 및 접근성 분야: 시각장애인을 위한 이미지 설명 AI 등<br/>
  
3. AI 혁신의 교차점, 멀티모달 러닝 이미지와 자연어를 동시에 다루는 VQA 모델은 ChatGPT, Gemini, Claude 등 최신 멀티모달 모델의 핵심 구조와 동일합니다. 이번 대회를 통해 "멀티모달 AI의 작동 원리"를 직접 구현하게 됩니다.


## 2. 팀원 소개
| [박준우](https://github.com/Joonw00) | [서미영](https://github.com/SeoMiYoung) | [한정희](https://github.com/Jeonghee-Han) | [이주석](https://github.com/commentLee) |
| :--: | :--: | :--: | :--: |
| <img src="https://github.com/Joonw00.png" width="150"/> | <img src="https://github.com/SeoMiYoung.png" width="150"/> | <img src="https://github.com/Jeonghee-Han.png" width="150"/> | <img src="https://github.com/commentLee.png" width="150"/> |


## 3. 아티클
- [추론 안정화 및 메모리 최적화 개선 과정 (Qwen3-VL-32B + LoRA)
](https://velog.io/@joonw00/%EC%B6%94%EB%A1%A0-%EC%95%88%EC%A0%95%ED%99%94-%EB%B0%8F-%EB%A9%94%EB%AA%A8%EB%A6%AC-%EC%B5%9C%EC%A0%81%ED%99%94-%EA%B0%9C%EC%84%A0-%EA%B3%BC%EC%A0%95-Qwen3-VL-32B-LoRA)
- [A100 환경에서 VQA에 적합한 모델 찾기](https://velog.io/@comment/A100-%ED%99%98%EA%B2%BD%EC%97%90%EC%84%9C-VQA%EC%97%90-%EC%A0%81%ED%95%A9%ED%95%9C-%EB%AA%A8%EB%8D%B8-%EC%B0%BE%EA%B8%B0)

## 4. 결과
- `Public` 정확도: 0.96244
- `Private` 정확도: 0.96963

대회는 실제 데이터셋을 기반으로 리더보드를 통해 실시간 점수를 확인하며, AI 모델의 정확도를 겨루는 방식으로 진행되었습니다.<br/>
대회 기간 중에는 public 데이터셋(공개된 테스트 데이터) 을 기준으로 참가자들이 실시간 점수를 확인할 수 있었고, 대회 종료 후에는 참가자에게 공개되지 않았던 private 데이터셋 을 기반으로 최종 정확도를 측정하여 순위를 산정했습니다.

저희 팀은 public 데이터셋 기준으로는 13위를 기록했지만, 대회 종료 후 private 데이터셋으로 다시 평가한 최종 결과에서는 4위라는 성과를 얻었습니다.

public 데이터셋은 실험 과정에서 점수를 지속적으로 확인할 수 있기 때문에, 해당 데이터에 맞춰 모델이 튜닝되거나 과적합될 가능성이 있습니다.
반면 private 데이터셋은 참가자에게 공개되지 않은 데이터로 평가가 이루어지기 때문에, 모델의 일반화 성능을 더 잘 반영합니다.

**저희 팀이 private 데이터셋 기준에서 더 좋은 성과를 거두었다는 점은, 개발한 모델이 공개 데이터에 과적합되지 않았고, 실제 분포의 unseen 데이터에 대해 더 안정적으로 일반화되었기 때문이라고 생각합니다.**

<img width="1920" height="1080" alt="14888  연산자 끼워넣기" src="https://github.com/user-attachments/assets/e51ca833-734c-464b-9219-aa12e9593ccc" />


