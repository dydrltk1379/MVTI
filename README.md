<img width="785" height="369" alt="image" src="https://github.com/user-attachments/assets/68c17e5d-1d2b-47aa-9786-be544ccff18d" />## 1. 프로젝트 개요 (Overview)

**"백엔드 데이터와 머신러닝(ML)의 '흥미'를 '구현'으로 옮긴 첫걸음"**

MVTI는 사용자의 MBTI 성향을 분석하여, 개인의 성격 유형에 맞는 영화를 추천해주는 안드로이드 앱 서비스입니다. 2021년도 졸업작품으로 진행된 팀 프로젝트입니다.

이 프로젝트는 백엔드 API 서버 구축과 머신러닝 모델을 직접 API에 연동시켜 본 첫 번째 프로젝트로서, 백엔드 개발자로서의 성장 스토리를 시작하는 계기가 되었습니다.

-   **개발 기간:** 2021.09 ~ 2021.11
-   **팀 구성:** 팀 프로젝트 (본인: 팀장, 백엔드 개발)

<br>

## 2. 핵심 기능 (Features)

-   **회원가입 및 로그인:** `Firebase Authentication`을 이용한 사용자 인증 기능
-   **MBTI 테스트:** 사용자 성향 분석을 위한 MBTI 테스트 기능
-   **영화 추천:** `TensorFlow`의 협업 필터링(CF) 알고리즘을 기반으로 MBTI 및 사용자 평점을 분석하여 영화 추천
-   **영화 정보 제공:** 박스오피스, 영화 상세 정보, 평점 조회 기능

<br>

## 3. 기술 스택 (Tech Stack)

| 구분 | 기술 스택 |
| :--- | :--- |
| **Back-End** | `Python`, `Flask` |
| **ML** | `TensorFlow` (Collaborative Filtering) |
| **Database / Auth** | `Firebase` (Firestore, Authentication) |
| **Client** | `Android (Kotlin)` |

<br>

## 4. 시스템 구성도 (System Architecture)

*(포트폴리오 4페이지의 '시스템 구성도' 이미지를 이 위치에 삽입하세요)*
<img width="785" height="369" alt="image" src="https://github.com/user-attachments/assets/c5875c75-2429-4d2c-b4d8-35e086790ab4" />



-   **Client (Android):** `Firebase`에 인증을 요청하고, `Flask` API 서버에 영화 정보 및 추천을 요청합니다.
-   **Firebase:** 사용자 인증 및 MBTI 결과, 평점 등 주요 데이터를 저장/관리합니다.
-   **Back-End (Flask):** 클라이언트의 요청을 받아 `Firebase`의 데이터를 조회하고, `TensorFlow` 모델을 호출하여 추천 결과를 반환하는 RESTful API 서버 역할을 수행합니다.

<br>

## 5. 나의 주요 역할 및 기여 (What I Did)

본 프로젝트에서 **팀장** 및 **백엔드 개발** 역할을 수행했습니다.

-   **`Flask` 기반 RESTful API 서버 설계 및 구축**
    -   영화 정보 조회, MBTI 테스트 로직, 사용자 평점 저장/반환, 최종 추천 결과 반환 등 핵심 API 구현
-   **`TensorFlow` 협업 필터링(CF) 추천 알고리즘 구현**
    -   사용자 기반 협업 필터링 모델을 구현하고, `Flask` API 서버에 직접 연동하여 실시간 추천 서비스 제공
-   **팀장으로서 프로젝트 총괄**
    -   개발 일정, 기술 스택 선정, Git-flow 기반의 이슈 관리 등 프로젝트 전반의 방향성을 주도하고 관리

<br>

## 6. 주요 문제 및 배운 점 (Problems & Lessons Learned)

### [Problem] '구현'을 넘어선 '운영'의 과제 발견
API 서버와 ML 모델을 성공적으로 구축했으나, 서비스가 운영되고 데이터가 복잡해질 경우를 가정한 **'안정성'**과 **'효율(최적화)'** 문제가 새로운 과제로 대두되었습니다.

### [Learned] '최적화'와 '안정성'의 중요성 인식
단순히 기능을 '동작'하게 하는 것을 넘어, 데이터를 효율적이고 안정적으로 관리하는 **'데이터 최적화'**의 중요성을 깊이 깨달았습니다.
