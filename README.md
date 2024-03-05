# Prediction_IndustriesSales
Prediction emerging industries and sales trends in Apgujeong and Sinchon-dong using SARIMA and LSTM

# ⌛ 프로젝트 기간
- 약 8주

# 📂 데이터셋 출처
- [서울시 공공데이터](https://data.seoul.go.kr/dataList/datasetList.do#)
    - 상권 - 매출, 점포 데이터
    - 상권배후지 - 점포 데이터
    - 자치구, 행정동 데이터

- [업종 정보 데이터](https://golmok.seoul.go.kr/images/100_v2.pdf)
    - 중분류의 경우 대분류 및 업종명을 고려하여 직접 생성


# 🚩 기획 배경 및 분석 목적

> 상권은 정성적, 정량적인 외생적 요인에 의해 변화됩니다.  
**①매출, ②생활인구, ③점포 수** 위 3가지를 지표로 서울시 행정동 별 3개의 행정구를 집중 분석하고, 뉴스 기사로 조사해본 결과  
"강남구 압구정동"은 팬데믹에 불구하고 굳건히 성장하는 행정동으로 확인 되었으며,  
"마포구 신촌동"은 쇠락을 면치 못하고 있었습니다.

> 이에 본 프로젝트에서는 위 두 지역에서 창업을 준비 중인 예비 창업자의 의사 결정에 도움을 주고자,  
상권 별 매출, 점포 수 드으이 정보가 담긴 지난 6년(24분기, 2017~2022年) 간의 데이터를 기반으로 매출 예측을 시각화하여 성장할 만한 업종을 추천하고자 합니다.

## 🎯 세부 목표
- [1차 목표] 압구정동과 신촌동 집중 분석하여 가설 설정
    - 집중 분석할 내용
        1. 업종별, 요일별 매출 금액 및 비율
        1. 업종별 성별 매출 비율(ex. 남 xx% 여 yy%)
        1. 업종별 시간당 매출
        1. 업종별 해당 지역의 동종업좀 점포 수 및 전분기 대비 증/감
        1. 업종별 매출 건수
        1. 업종별 해당 지역의 개업률 / 폐업률
        1. 업종별 연령별 매출
        1. 상관관계 분석
    

- [2차 목표] 통계(Statsmodel OLS), SARIMA, LSTM, Chat-GPT 활용하여 업종 별 예측 매출액 시각화하여 2023년의 추천 업종 선정

- [3차 목표] 추천 업종으로 예측한 결과와 실제 동향 비교 (기사, 레포트 등 참고)


# ✨ 기대 효과
> 서울시에서 제공하는 상권분석 서비스는 1개년의 데이터만을 가지고 제공 중이었으나,
본 프로젝트는 6년 간의 데이터를 가지고 예측을 진행하여 성장 가능성이 있는 업종 추천에 보다 정확성이 높은 결과낼 수 있습니다.

> 이로써 해당 지역의 예비 창업자는 추천 업종과 예측 매출 양상을 참고하여 상권에 따른 업종을 분석하여 소비자 니즈 파악 능력을 향상할 수 있습니다.

# 💪🏻 한계 및 아쉬운 점
- 분기별 데이터셋만 확보가 가능했기에 실질적으로 분석한 행은 24분기, 24개행에 불과하여 오차를 줄이기 어려웠습니다.
- 팀프로젝트 당시에는 두 번의 주제 변경으로 시간을 확보하지 못해 해당 결과를 서비스화 하지 못했습니다. 이후 개인적으로 Streamlit으로 시각화 대시보드를 구현하려고 시도해보았으나 업종 별로 나누어진 데이터셋에 막혀 구현하기 어려웠습니다.
