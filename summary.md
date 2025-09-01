# 2025년 방학 현장실습 7–8월 주요 성과

## 🗓 개요
- **기간**: 2025-07-01 ~ 2025-08-31

---

## 🏆 주요 성과

### 1. 데이터셋 및 모델 분석
- 라벨링 전 주요 모델 **DocLayout-YOLO 논문 분석**
-  DocLayent 데이터셋 특성 및 구조 분석

### 2. 데이터 라벨링
- 모델 학습을 위한 **데이터 라벨링 직접 수행**
- 모델이 진행한 **1차 자동 라벨링 결과 검토 및 수정**
- 1차 라벨링 결과에 대한 **분석 및 검증**

### 3. 데이터 크롤링 및 사이트 분석
- **사이트별 데이터셋 분석**  
  - 학술 논문 및 연구자료  
  - 정부 및 공공기관 문서  
  - 교육자료 및 프레젠테이션  
  - 일반 문서 및 도서  
- 데이터 크롤링에 적합한 사이트를 선별하여 수집 진행

### 4. 데이터셋 분류 체계 확립
- 카테고리 기준:  
  - `invoice` (영수증)  
  - `report` (보고서, 리포트)  
  - `book` (도서)  
  - `newspaper_or_magazine` (잡지, 신문)  
  - `academic_paper` (논문, 연구자료)  
  - `exam_paper` (시험지)  
  - `slide` (발표자료)  
  - `note` (노트)  
  - `infographic` (인포그래픽)  
  - `other` (기타, 명시)

### 5. 데이터 정제 및 자동화
- `url.txt` 파일을 **JSON 형식으로 자동 변환**  
- 크롤링 데이터에 대해 **모델 1차 라벨링 → 검토 및 수정** 프로세스 정립

### 6. 분석 대상 사이트
- **학술/연구**: arXiv, PubMed Central (PMC), SSRN, bioRxiv  
- **정부/공공기관**: data.gov, data.go.kr, EUR-Lex, 국회도서관, **국가정책연구포털**
- **교육/프레젠테이션**: MIT OpenCourseWare, SlideShare, OpenStax, Khan Academy, **한국교육과정평가원**
- **문헌/기타 자료**: Project Gutenberg, Internet Archive, Wikimedia Commons


# 2025년 방학 현장실습 7–8월 활동 요약

## 🗓 개요
- **기간**: 2025-07-01 ~ 2025-08-31

---

## 🏆 주요 성과
- **DocLayout-YOLO 논문 분석** 및 DocLayNet 데이터셋 구조 파악  
- **모델 학습용 데이터 라벨링 총 953장 수행** 및 1차 자동 라벨링 검토·수정  
- **데이터 크롤링 환경 세팅** 및 주요 사이트별 데이터 특성 분석  
- **PubMed Central, data.gov** 크롤링 실험 및 한계 파악  
- **데이터셋 카테고리 체계 확립**, url → JSON 변환 자동화  

---

## 📅 월별 활동 내역

### 📌 7월

#### 🗓 1주차 (7/1 ~ 7/6)
- **활동**  
  - 활용 모델 관련 자료 학습
  - **활용 모델 관련 자료 학습**
  - [DocLayout-YOLO](https://github.com/opendatalab/DocLayout-YOLO)  
  - [DocLayNet](https://github.com/DS4SD/DocLayNet)  
  - [OmniDocBench](https://github.com/opendatalab/OmniDocBench)  
  - [Upstage Document Parsing Docs](https://console.upstage.ai/docs/capabilities/document-digitization/document-parsing)  
  - 라벨링 툴 익히기 및 데이터 라벨링 시작  
  - 모델 1차 라벨링 결과 검토 및 수정  
  - 피드백 반영 (key-value 항목 통합, 동의/비동의 묶기, line number 단일 text 처리)  

- **라벨링 성과**  
  - **460장** (모델 학습용 라벨링 & 1차 라벨링 검토 및 수정)

| 날짜     | GitHub 링크                                                                 |
|----------|------------------------------------------------------------------------------|
| 20250701 | [20250701](https://github.com/daanhaa/Data-analysis/blob/main/20250701.md) |
| 20250702 | [20250702](https://github.com/daanhaa/Data-analysis/blob/main/20250702.md) |
| 20250703 | [20250703](https://github.com/daanhaa/Data-analysis/blob/main/20250703.md) |
| 20250704 | [20250704](https://github.com/daanhaa/Data-analysis/blob/main/20250704.md) |

---

#### 🗓 2주차 (7/7 ~ 7/13)
- **활동**  
  - 모델 1차 라벨링 검토·수정 지속  
  - 데이터 크롤링 환경 세팅 
  - 사이트별 데이터 분석 및 크롤링 실험
  -  크롤링 기준 확립(PDF, Image 위주, background image 포함 문서 우선 수집)
  -  크롤링된 데이터셋 정제(페이지 수, 너무 단조로운형태, 파일오류)

  **🧬 PubMed Central (PMC)**  
  - API로 PMC ID 추출 → PDF URL 변환 → HTML 파싱 → 매크로 다운로드  
  - 문제: ftp URL, 자동 다운로드 불안정 → 수동 검토 필요  

  **🏛 data.gov**  
  - API로 데이터셋 URL 50개 추출 → 상세페이지 PDF 탐색 및 다운로드  
  - 문제: 실제 다운로드 가능한 PDF 소수, 용량 과대·파일 다운 오류 → 수동 정제 필요  

- **라벨링 성과**  
  - **493장** (1차 라벨링 검토 및 수정)

| 날짜     | GitHub 링크                                                                 |
|----------|------------------------------------------------------------------------------|
| 20250707 | [20250707](https://github.com/daanhaa/Data-analysis/blob/main/20250707.md) |
| 20250708 | [20250708](https://github.com/daanhaa/Data-analysis/blob/main/20250708.md) |
| 20250709 | [20250709](https://github.com/daanhaa/Data-analysis/blob/main/20250709.md) |
| 20250710 | [20250710](https://github.com/daanhaa/Data-analysis/blob/main/20250710.md) |
| 20250711 | [20250711](https://github.com/daanhaa/Data-analysis/blob/main/20250711.md) |

---

#### 🗓 3주차 (7/14 ~ 7/20)
- **활동**
  - **EUR-Lex (EU 법률 문서)**  
    - 키워드 검색 결과 페이지 요청 → BeautifulSoup으로 PDF 링크 추출  
    - 영어 문서(/EN/)만 필터링 후 저장  
    - **문제**: 파일명이 임의 제목으로 저장 → 관리 어려움  
    - **해결**: CELEX 번호를 추출하여 고유 번호 기반 파일명 지정 성공  
    - **특징**: 대부분이 법률 문서, 유사한 구조  

  - **Internet Archive**  
    - `advancedsearch API` + `metadata API` 활용 → identifier 추출  
    - Text PDF 형식만 선택 후 다운로드  
    - PyPDF2로 페이지 수 검증(50p 이하만 저장)  
    - **성과**: 다양한 카테고리/형식의 자료 성공적으로 다운로드, URL(book_urls.txt) 기록  

  - **국회도서관**  
    - F12(개발자 도구)로 다운로드 버튼 위치 추적  
    - 코드 반영했으나 로그인/세션 구조 문제로 자동화 실패  
    - **해결**: 직접 다운로드 방식으로 카테고리별 60개 PDF 확보  

  - **MIT OpenCourseWare**  
    - 키워드 검색 → 강의 접속 → Download Course 버튼 경유 필요  
    - 구조가 복잡해 코드 기반 자동 다운로드 실패  
    - **해결**: 일부 강의는 수동 다운로드 진행  

  - **Gutenberg.org**  
    - Gutendex API로 영어 PDF 목록 수집(최대 100개)  
    - PyPDF2로 페이지 수 검증 후 50p 이하만 저장  
    - **문제**: API timeout, 중복 PDF 반복 출력, PDF 부족 → epub·mobi·zip 위주  
    - **해결**: 최대 5회 재시도 로직 추가 / epub은 Calibre 툴로 수동 변환  
    - **성과**: PDF 일부 확보 + epub 수동 변환으로 자료 추가 확보  

  - **PRISM → NKIS 전환**  
    - PRISM: 공개자료만 활용 가능, API 미제공 → 자동화 한계  
    - 대체: 국가정책연구포털(NKIS, API 제공)로 전환  
    - **성과**: 카테고리별 60개 데이터 확보 (API 신청 진행 중)  

| 날짜     | GitHub 링크                                                                 |
|----------|------------------------------------------------------------------------------|
| 20250714 | [20250714](https://github.com/daanhaa/Data-analysis/blob/main/20250714.md) |
| 20250715 | [20250715](https://github.com/daanhaa/Data-analysis/blob/main/20250715.md) |
| 20250716 | [20250716](https://github.com/daanhaa/Data-analysis/blob/main/20250716.md) |
| 20250717 | [20250717](https://github.com/daanhaa/Data-analysis/blob/main/20250717.md) |
| 20250718 | [20250718](https://github.com/daanhaa/Data-analysis/blob/main/20250718.md) |


---
#### 🗓 4주차 (7/21 ~ 7/27)
- **활동**
  - **Internet Archive**  
    - infographic, book 중심 자료 검색  
    - 유사·연속된 형태의 자료 다수(예: 잡지 연속 간행물) → 정제 필요  
  - **한국교육과정평가원(KICE)**  
    - 수능 기출 문제 PDF 다운로드  
    - 카테고리별 분류 및 URL 정리 진행  
  - **URL JSON 자동화 정리**  
    - 기존: url.txt 파일을 수동으로 JSON 변환  
    - 개선: Python 코드로 자동화  
      - 입력: (파일명, URL) txt 파일  
      - 출력: JSON 파일  
      - JSON 구조 예시:  
        ```json
        {
            "file_name": "다운로드된 파일명",
            "document_type": "카테고리 분류",
            "url": "파일의 url입력",
            "source": "다운 사이트"
        }
        ```
      - data.gov, Internet Archive, MIT, OpenStax, PMC, NKIS(신문/잡지) JSON 변환 완료  

- **라벨링 진행**
  - 크롤링 데이터셋 기반 라벨링 시작  
  - LLM 기반 1차 라벨링 → 사람이 검토·수정  
  - **실패 사례 캡처 및 기록 파일화**  
  - 단순 구조 우선 처리, 복잡 문서는 별도 모아 진행 예정  

- **라벨링 성과**  
  - **202장** (1차 라벨링 검토 및 수정)
---

## 📊 자료 수집 비율
| 출처                       | 수집량 | 비고                           |
|----------------------------|-------:|--------------------------------|
| 국회도서관                  | 60     | 카테고리별 분류 완료            |
| 국가정책연구포털 (NKIS)     | 60     | API 신청 진행                  |
| Internet Archive            | 80     | API 기반 수집, 페이지 제한 적용 |
| data.gov                   | 40     | PDF 확보율 낮음, 수동 정제 필요 |
| PubMed Central (PMC)       | 20     | API 기반 ID 추출, 매크로·수동 병행 |
| MIT OCW                    | 20     | 자동화 실패, 수동 일부 확보     |
| OpenStax                   | 20     | 교육자료 라벨링 데이터셋        |
| KICE (수능 시험지)          | 20     | 시험지 기반 자료 확보           |

➡️ **총합: 약 300개 문서 확보**

| 날짜     | GitHub 링크                                                                 |
|----------|------------------------------------------------------------------------------|
| 20250721 | [20250721](https://github.com/daanhaa/Data-analysis/blob/main/20250721.md) |
| 20250722 | [20250722](https://github.com/daanhaa/Data-analysis/blob/main/20250722.md) |
| 20250723 | [20250723](https://github.com/daanhaa/Data-analysis/blob/main/20250723.md) |
| 20250724 | [20250724](https://github.com/daanhaa/Data-analysis/blob/main/20250724.md) |
| 20250725 | [20250725](https://github.com/daanhaa/Data-analysis/blob/main/20250725.md) |


---
5주차

#### 🗓 5주차 (7/28 ~ 8/3)
- **활동**
  - **Internet Archive 크롤링 데이터 라벨링 집중 진행**
  - 신문·잡지 등 복잡한 형태 문서가 많아 처리 시간 증가
  - AI Labeling 결과 검토 → 순서 누락, 미라벨링 데이터 다수 확인 → 수동 보완
  - 범위: **216번 ~ 904번 데이터 라벨링 완료**
  
- **라벨링 성과**
  - **총 642장 라벨링 완료**

| 날짜     | GitHub 링크                                                                 |
|----------|------------------------------------------------------------------------------|
| 20250728 | [20250728](https://github.com/daanhaa/Data-analysis/blob/main/20250728.md) |
| 20250729 | [20250729](https://github.com/daanhaa/Data-analysis/blob/main/20250729.md) |
| 20250730 | [20250730](https://github.com/daanhaa/Data-analysis/blob/main/20250730.md) |
| 20250731 | [20250731](https://github.com/daanhaa/Data-analysis/blob/main/20250731.md) |
| 20250801 | [20250801](https://github.com/daanhaa/Data-analysis/blob/main/20250801.md) |

---
#### 🗓 8월 2주차 (8/4 ~ 8/10)
- **활동**
  - **Internet Archive 데이터 라벨링 완료** 
  - **Nanet(국회도서관) 데이터 라벨링**
    - 보고서 형태 문서는 AI 라벨링 정확도가 높아 빠른 진행 가능  
    - 반면, 이미지 위 텍스트·슬라이드 첨부 페이지 등은 라벨링 실패 빈번  
    - 형태가 유사·단순한 데이터가 많아 라벨링 속도 개선  
    - 직접 수집한 데이터셋 라벨링 → 실제 모델 학습 참여 감각 경험  

- **NaNet 데이터 라벨링 오류 분석**
  - Text → Footer 중복 인식  
  - Footer → Page Header로 잘못 인식  
  - Text ↔ Title 중복 또는 오인식  
  - 슬라이드 전체를 사진(Picture)로만 인식 → 개별 객체 인식 불가  
  - Caption 미인식  
  - Title 옆 그림 미분류 → bounding box 부정확  
  - 문자가 아닌 요소를 Footer·Header로 잘못 인식  
  - 일부 문서는 Label이 거의 생성되지 않음  

- **라벨링 성과**
  - **총 1,018장 라벨링 완료**

| 날짜     | GitHub 링크                                                                 |
|----------|------------------------------------------------------------------------------|
| 20250804 | [20250804](https://github.com/daanhaa/Data-analysis/blob/main/20250804.md) |
| 20250805 | [20250805](https://github.com/daanhaa/Data-analysis/blob/main/20250805.md) |
| 20250806 | [20250806](https://github.com/daanhaa/Data-analysis/blob/main/20250806.md) |
| 20250807 | [20250807](https://github.com/daanhaa/Data-analysis/blob/main/20250807.md) |
| 20250808 | [20250808](https://github.com/daanhaa/Data-analysis/blob/main/20250808.md) |

---
#### 🗓 8월 3주차 (8/11 ~ 8/17)
- **활동**
  - **MIT 강의자료 데이터 라벨링**
    - 총 180/180 문서 라벨링 완료  
  - **OpenStax 교재 데이터 라벨링**
    - 1차: 288/2607 완료  
    - 2차: 527/2607 완료  
    - 3차: 797/2607 완료  
    - 진행 상황: 전체 2,607개 중 797개 라벨링 완료  
  - 라벨링 실패 케이스 URL 목록 txt 파일로 별도 정리
    
- **라벨링 오류 분석**
  - Picture 여러 개를 하나로 묶어 인식하는 오류 발생  
  - Caption을 Text로 중복 인식  
  - 수식(Math)을 인식하지 못하거나 → Text로 잘못 인식  
  - Text 자체를 인식하지 못하는 경우 존재  
  - 수식 + Text 전체를 Picture로 잘못 인식  
  - Title ↔ Text 구분이 불명확 → 중복 인식 빈번  
  - 라벨링 결과에 **일관성 부족**  

- **라벨링 성과**
  - MIT 강의자료: **180장 라벨링 완료**  
  - OpenStax 교재: **797장 라벨링 완료**  
  - **총 977장 라벨링 완료**

| 날짜     | GitHub 링크                                                                 |
|----------|------------------------------------------------------------------------------|
| 20250811 | [20250811](https://github.com/daanhaa/Data-analysis/blob/main/20250811.md) |
| 20250812 | [20250812](https://github.com/daanhaa/Data-analysis/blob/main/20250812.md) |
| 20250813 | [20250813](https://github.com/daanhaa/Data-analysis/blob/main/20250813.md) |
| 20250814 | [20250814](https://github.com/daanhaa/Data-analysis/blob/main/20250814.md) |



---

#### 🗓 8월 4주차 (8/18 ~ 8/24)
- **활동**
  - **OpenStax 교재 데이터 라벨링**
    - 진행 범위: **798 ~ 1,540**  
  - **OpenStax URL 정리**
    - 라벨링 실패 케이스 URL 목록 txt 파일로 별도 정리

- **라벨링 성과**
  - OpenStax 데이터 라벨링 누적: **1,540/2,607 완료**  
  - **총 743장 라벨링 완료**
    


---

#### 🗓 8월 5주차 (8/25 ~ 8/31)
- **활동**
  - **OpenStax 교재 데이터 라벨링**
    - 진행 범위: **1,768 ~ 2,607**  
 
    - OpenStax 데이터셋 전체 라벨링 완료  
  - **OpenStax URL 정리**
    - 라벨링 실패 케이스 URL 목록 txt 파일로 별도 정리 
  - **현장실습 제출 서류 정리**
    - 제출용 보고서 및 활동 내역 자료 정리  
  - **활동 내역 정리**
    - 전체 라벨링 성과 및 크롤링 시행착오, 데이터셋 분류 체계 최종 정리

- **라벨링 성과**
  - **839장 라벨링 완료**


---


## 📊 라벨링 총합 (7~8월 누적)

| 주차          | 라벨링 장수 |
|---------------|------------:|
| 7월 1주차     | 460장       |
| 7월 2주차     | 493장       |
| 7월 4주차     | 202장       |
| 7월 5주차     | 642장       |
| 8월 2주차     | 1,018장     |
| 8월 3주차     | 977장       |
| 8월 4주차     | 743장       |
| 8월 5주차     | 839장       |
| **누적 총합** | **5,374장** |

---

## 🌱 활동 의의 및 배운 점

### 1. 데이터셋 수집 및 정제 과정의 이해
- 다양한 사이트(PubMed, data.gov, Internet Archive, 국회도서관, NKIS, OpenStax, MIT 등)에서 데이터를 크롤링하면서, **사이트별 구조 차이와 API 제공 여부**가 데이터 수집 난이도에 큰 영향을 준다는 점을 배움.  
- 크롤링 과정에서 발생하는 **파일 손상, 중복, 과도한 용량, 비표준 형식(epub, mobi 등)** 문제를 경험하고, 자동화만으로는 한계가 있음을 체감 → **자동화 + 수동 정제의 균형**이 중요하다는 것을 깨달음.  
- JSON 변환 자동화 과정을 통해 **데이터 전처리 파이프라인의 효율성**을 직접 구현하고 개선할 수 있었음.  

---

### 2. 데이터 라벨링 경험
- 총 **5,374장 라벨링**을 수행하면서, **라벨링 가이드라인 통일과 일관성 유지**의 중요성을 깊이 이해함.  
- 단순 문서(report, note 등)에서는 라벨링이 빠르게 진행되었으나, **신문·잡지·슬라이드·수식 포함 문서**에서는 AI 라벨링 실패율이 높았고, 이를 직접 검토·수정하며 **모델 보완 가능성**을 확인함.  
- 라벨링 오류 유형(중복 인식, 오인식, 객체 누락 등)을 분석하고 문서화한 경험은 향후 **모델 개선 및 평가 지표 설계**에 기여할 수 있음.  

---

### 3. 모델 학습 데이터 구축 참여
- 실제 연구·산업에서 사용하는 데이터셋 구축 과정(수집 → 정제 → 분류 → 라벨링)을 **처음부터 끝까지 직접 경험**하면서, 단순한 데이터 핸들링을 넘어 **모델 학습의 기반이 되는 데이터 품질 확보**의 중요성을 체감.  
- “내가 라벨링한 데이터가 곧 모델 학습에 쓰인다”는 경험을 통해 **현업 참여감**과 함께 데이터 과학자로서의 **책임감**을 느끼게 됨.  

---

### 4. 문제 해결 및 시행착오 경험
- PubMed, data.gov, 국회도서관 등에서 자동화 한계를 겪고, **매크로·수동 다운로드·대체 사이트(NKIS 전환)** 등 유연한 문제 해결 방법을 적용.  
- Gutenberg의 epub → pdf 변환 시 **Calibre 도구**를 활용하여, 기술적 한계를 도구 사용으로 보완하는 **실용적 접근**을 배움.  
- 시행착오 과정을 통해 **“완벽한 자동화는 어렵지만, 데이터 수집 목표를 달성하기 위해 다양한 차선책을 활용하는 능력”** 이 중요함을 학습.  

---

### 5. 협업 및 보고서 작성 능력 강화
- 라벨링 피드백 반영 과정에서 **팀원 간 가이드라인 공유·수정**이 필수적임을 경험.  
- 활동 내역을 체계적으로 기록하고, 시행착오 및 성과를 정리하여 보고서로 문서화하면서 **연구 활동 기록 능력** 및 **기술 문서 작성 능력**이 향상됨.  

