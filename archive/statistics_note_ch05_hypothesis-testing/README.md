# 우연의 과학통계학 — 3장 통계적 가설검정

**박사·하루(조수)·초파리 연구원·주판봇** 네 캐릭터가 진행하는 인터랙티브 통계 해설 시리즈의 3장입니다.
치료제 10명 중 7명이 나았다면 효과가 있다고 해도 될까? 흡연자의 폐가 더 상했다는 차이는 우연일까? 교육 프로그램 세 개 중 무엇이 나을까?
귀무가설과 p값, t·z·χ² 검정, 두 집단 비교, 분산분석까지 직접 돌려 보며 익히고, 100문항 모의고사로 정리합니다.
서버나 설치 없이 브라우저에서 바로 열리는 정적 HTML이라 GitHub Pages에 그대로 올릴 수 있습니다.

**사이트 주소:** https://adminmrobo.github.io/statistics_note_ch05_hypothesis-testing/

## 해설 페이지

| 번호 | 제목 | 다루는 개념 | 대결 | 파일 |
|---|---|---|---|---|
| 3.1 | 추정과 가설검정 | 추론통계, 신뢰구간과 검정의 짝, 귀무·대립가설, 양측·단측, p값, 1종·2종 오류, 검정력, z 검정 | 조건부 | [`3-1_hypothesis_testing.html`](3-1_hypothesis_testing.html) |
| 3.2 | "바"선생 평균의 추정과 검정 | t 신뢰구간, 단일표본 t 검정, 질문에 맞는 단측 방향, t와 z, 선택 편향 | 주판봇 승 | [`3-2_cockroach_mean.html`](3-2_cockroach_mean.html) |
| 3.3 | 가설검정 예제 연습 | 음료 t 검정, 생활폐기물 z 검정(양측·단측), 배터리 분산 χ² 검정, 검정 고르기 계산기 | 초파리 승 | [`3-3_test_exercises.html`](3-3_test_exercises.html) |
| 3.4 | 두 집단의 가설검정 | 독립·대응표본, 등분산(F·Levene), 합동분산 t, Welch t, 대응 t, 교란 | 주판봇 승 | [`3-4_two_sample_tests.html`](3-4_two_sample_tests.html) |
| 3.5 | 세 집단 이상 — 분산분석 | 다중 비교와 가족 오류율, 변동 분해, 분산분석표와 F 검정, Bonferroni·Tukey 사후검정 | 초파리 승 | [`3-5_anova.html`](3-5_anova.html) |
| 3.6 | 모의·연습문제 퀴즈 | 100문항(객관식 50·OX 25·단답 25), 전체 50문제·묶음별 20문제 | — | [`3-6_mock_exam.html`](3-6_mock_exam.html) |

## 3.6 모의고사

- **모드:** 전체 모의고사 50문제(다섯 묶음에서 객관식 5·단답 3·OX 2씩) 또는 묶음별 20문제 — A 추정과 가설검정의 기초 · B 단일표본 t 검정 · C z·t·χ² 검정 연습 · D 두 집단의 가설검정 · E 분산분석과 다중 비교
- 매번 무작위로 뽑고 보기 순서도 섞음. 타이머(객관식 40초·OX 20초·단답 60초)와 효과음은 켜고 끌 수 있음
- 단답식은 답을 떠올린 뒤 정답을 보고 스스로 채점
- 문항마다 해설과 **다시 읽을 페이지 위치 링크**, 결과 화면에 묶음별 막대와 틀린 문항 다시 보기
- 키보드: 객관식 1~4, OX는 O/X, 다음 문제 Enter
- 인쇄용: [`pdfs/mock-exam-ch3.pdf`](pdfs/mock-exam-ch3.pdf) (50문항 → 정답표 → 해설)

## 폴더 구조

```
.
├── index.html                        # 3장 목차 (사이트 첫 화면)
├── 3-1_hypothesis_testing.html       # 3.1 ~ 3.5 해설 페이지 — 각각 그림·데이터를 모두 품은 단일 파일
├── 3-2_cockroach_mean.html
├── 3-3_test_exercises.html
├── 3-4_two_sample_tests.html
├── 3-5_anova.html
├── 3-6_mock_exam.html                # 3.6 모의·연습문제 퀴즈 게임
├── data/                             # 예제 데이터 CSV 5개 (3.2~3.5)
├── pdfs/
│   └── mock-exam-ch3.pdf             # 인쇄용 모의고사
├── assets/
│   ├── thumb_3_*.png                 # 목차 카드 썸네일 (600×400)
│   ├── og_3_*.png                    # 링크 공유 미리보기 (1200×630)
│   └── characters/                   # 목차 등장인물 카드용 표정 4장 (WebP)
├── production/                       # 제작 문서 (사이트에서 링크하지 않음)
│   ├── IMG_00_index.md               # 이미지 명세서 · 외부 의뢰 프롬프트
│   └── KG_00_registry.json           # 시리즈 지식 그래프 등록부 v0.5 (1~3장)
├── .nojekyll                         # Jekyll 처리 끄기
└── README.md
```

## GitHub Pages로 공개하기

1. 저장소 **Settings → Pages**에서 **Source: Deploy from a branch**, **Branch: `main` / `/ (root)`**를 고르고 저장한다.
2. 1~2분 뒤 위 사이트 주소에서 목차가 열린다.

> 페이지 안의 주소(공유 미리보기 `og:image`, 인용 주소, `page_meta.json`의 `url`)는 모두 위 저장소 이름을 기준으로 적혀 있다. 저장소 이름을 바꾸면 각 HTML에서 `statistics_note_ch05_hypothesis-testing`을 새 이름으로 일괄 바꾼다.

## 로컬에서 보기

`index.html`을 더블클릭하면 된다. 페이지끼리의 링크(목차 ↔ 각 페이지 ↔ 이전·다음, 모의고사 해설 링크)는 같은 폴더 안의 상대 경로라 그대로 동작한다. 인터넷이 끊기면 글꼴만 시스템 글꼴로 바뀐다.

## 페이지 안에 든 것

- 개념 사다리와 칸마다 직접 만지는 시뮬레이션·계산기(시드 고정 설명용 모형)
- 초파리 연구원 vs 주판봇 대결 — 결과는 페이지 안 계산으로 정해짐 (초파리 2 · 주판봇 2 · 조건부 1)
- "한 번 더 짚어 보기" 상자 — 계산·해석에서 헷갈리기 쉬운 점을 정리한 부분
- 확인 퀴즈 35문항(페이지 안) + 모의고사 100문항, 용어 말풍선, 읽은 곳·퀴즈 진행 도우미
- 지식 색인(검색·관계 그래프)과 온톨로지·서지 꾸러미(JSON-LD, Turtle, CSV, CSL-JSON, BibTeX, RIS를 ZIP으로 내려받기)
- 외부 스크립트·브라우저 저장소를 쓰지 않음. 외부 요청은 Google Fonts 글꼴 하나

## 데이터에 대해

- 3.1~3.3의 수치(치료제 10명 중 7명, 평균수명 71.8년, "바"선생 14마리, 음료·폐기물·배터리)는 강의 노트의 예시값을 그대로 썼다.
- 3.4(흡연·면역)와 3.5(교육 프로그램)의 데이터는 이 시리즈를 위해 만든 **실습용 예시 데이터**다(실제 환자·수강생 자료 아님). 3.4는 노트의 분석 결과와 같은 결론이 나오도록 숫자를 정했다.
- 모든 예제 데이터는 `data/` 폴더에 CSV로 있다: `cockroach_length.csv`, `battery_weight.csv`, `smoking_lung.csv`, `immune_pre_post.csv`, `training_programs.csv`. 각 페이지의 R·파이썬 코드와 함께 실습할 수 있다.

## 출처와 크레딧

- 글·구성: 안상선 ((주)M-Robo 대표) · AI 보조 제작
- 캐릭터 그림: [adminmrobo/fruitfly-lab-expressions](https://github.com/adminmrobo/fruitfly-lab-expressions)
- 각 페이지의 참고 자료(ASA p값 성명 2016, 검정·분포 문서, R·SciPy 함수 문서)는 페이지 맨 아래 출처 표와 꾸러미의 `references.*` 파일에 있다.

## 이 시리즈 인용하기

안상선 (2026). 우연의 과학통계학 — 3장 통계적 가설검정. https://adminmrobo.github.io/statistics_note_ch05_hypothesis-testing/

## 라이선스

(정해지면 적는다. 글·코드와 캐릭터 그림의 라이선스를 따로 적는 것을 권한다.)
