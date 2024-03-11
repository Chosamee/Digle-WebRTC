# Digle - AI Ada face 기반의 얼굴 인식 시스템

[ 최종산출.PDF ](https://github.com/Chosamee/Digle-WebRTC/blob/master/%EC%B5%9C%EC%A2%85%EC%82%B0%EC%B6%9C.pdf)

-   1. 소개

-   2. 목표

-   3. 환경 설정

-   4. 과제 수행 결과

-   5. 기대 효과 및 활용 방안

-   6. 팀원 소개

### 1. 소개

최근 인공지능의 얼굴인식 기술이 급격히 발전하면서, 디지털 교육 분야에 혁신을 가져오고 있습니다. 딥러닝과 컴퓨터 비전의 결합으로, 복잡한 얼굴 표정과 감정을 구별할 수 있는 얼굴인식이 가능해졌습니다. 이러한 기술 진보는 온라인 화상 시험 서비스 개발에도 큰 영향을 미치고 있습니다. 얼굴인식은 시험 감독 과정에서 자동화와 보안을 강화하며, 사용자 식별에 필요한 오프라인 환경에서도 활용될 수 있습니다.

우리 프로젝트는 이러한 얼굴인식 기술을 통합하여 온라인 화상 시험 서비스를 혁신하고자 합니다. 이 서비스는 디스코드와 유사한 화상 채팅 기능, 파일 전송, 귓속말 기능을 제공하여 사용자에게 편리한 시험 환경을 제공합니다. 관리자는 테스트방 생성 권한을 갖고, 참가자의 얼굴을 실시간으로 모니터링할 수 있습니다.

### 2. 과제 목표

-   프로젝트는 온라인 화상 시험 서비스를 개발하여 시험 감독을 자동화하고, 비즈니스 계정 사용자만이 시험방을 생성하여 참가자 신원을 실시간으로 확인할 수 있습니다.

-   WebRTC 기반의 실시간 커뮤니케이션 시스템을 목표로 하며, Janus를 사용하여 효율적인 실시간 데이터 전송을 제공합니다.

-   백엔드는 FASTAPI를 사용하여 빠른 속도와 우수한 성능의 RESTful API를 구축할 예정입니다.

-   프론트엔드는 React와 Tailwind CSS를 사용하여 사용자 친화적인 인터페이스를 만들 계획입니다.

-   미디어 서버 구성에는 Docker를 사용하여 다양한 환경에서 일관된 성능을 제공하고, 관리의 용이성을 높일 것입니다.

-   GPU 서버에는 주피터 노트북을 사용하여 데이터 처리 및 분석을 관리하고, 프로젝트는 최첨단 기술을 결합해 빠르고 안정적인 서비스를 제공할 것입니다.

## 3. 환경설정

### miniconda 가상환경 설정

#### miniconda 다운로드

-   https://docs.conda.io/projects/miniconda/en/latest/ 에 접속해서 miniconda 설치

#### 가상환경 생성 및 접속

-   본 프로젝트는 python version 3.8로 진행

-   myenv는 본인이 설정할 환경 이름

```
conda create --name {myenv} python=3.8
```

-   생성한 환경 접속

```
conda activate {myenv}
```

#### 필요한 라이브러리 설치

```
pip install -r requirement.txt
```

### postgreSQL 다운로드

-   https://www.postgresql.org/download/ 에 접속해서 postgreSQL 설치

-   .env에 다음 코드 추가

```
DATABASE_URL=postgresql://postgres:ssafy@localhost/postgres
```

### FastAPI 실행

-   'back' 디렉토리에서 다음 코드 실행

```
uvicorn app.main:app --reload
```

## 4. 과제 수행 결과

[ 최종산출.PDF ](https://github.com/Chosamee/Digle-WebRTC/blob/master/%EC%B5%9C%EC%A2%85%EC%82%B0%EC%B6%9C.pdf)

## 5. 기대 효과 및 활용 방안

## 기대 효과

-   기업 관점에서의 기대 효과

    -   본인 인증 과정에서 보안 강화
    -   원격 근무 관리의 효율성이 증가합니다.
    -   부정 행위 방지를 통한 투명성 증진

-   개발자 관점에서의 기대 효과

    -   본인 인증, 보안, 원격 모니터링 등 새로운 기능 및 서비스 개발 기회

-   소비자 관점에서의 기대효과

    -   개인 정보 보호가 향상되고, 사기 및 해킹 위험이 감소
    -   온라인 시험, 원격 근무, 원격 교육 등에서의 공정성 및 투명성 증진은 소비자들의 신뢰를 쌓고, 디지털 서비스에 대한 긍정적 인식

    ## 활용 방안

-   코로나 19 이후 비대면 시험이 활발해지고 있다. 하지만 수험자들의 부정행위 또한 의심되는데, 코딩 테스트 같은 시험에서 사용자의 프로필 정보와 실시간 영상정보를 비교하는 기능을 제공하여 감독관들의 수고를 덜어줄 수 있다.

-   온라인 보안 및 인증기능: 사용자가 서비스에 로그인할 때 프로필 사진과 실시간 캡처를 비교하여 본인 확인 절차의 일환으로 사용될 수 있다. 피싱이나 계정 도용을 방지하는데 도움이 될 수 있다.

-   원격 교육에서의 출석 확인: 원격 교육을 진행하는데 사용자가 접속해있는 상태인지 확인하고 사용자의 정보가 정확한지 확인할 수 있다.

-   원격 근무 관리: 원격 근무자가 업무에 참여하는 동안 본인 확인을 위해 실시간 화면과 프로필 사진을 비교하는 방식으로 활용할 수 있다. 특히 민감한 데이터를 다루는 기업에서 원격 근무 정책의 일환으로 적용될 수 있다.

-   대규모 행사나 모임: 참석자들의 신원을 확인하고 행사에서의 규정을 준수하도록 관리하는데 얼굴 인식기능이 활용될 수 있다.

## 6. 팀원소개

김보근 | 김치욱 | 복영석 | 안현성 | 이민수 | 이재민 |