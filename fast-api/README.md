# FastAPI 학습 가이드

FastAPI는 현대적이고 빠른(고성능) Python 웹 프레임워크입니다. 이 가이드는 FastAPI 공식 문서를 기반으로 단계별 학습을 위한 내용을 담고 있습니다.

## 목차

1. [시작하기](#시작하기)
2. [기본 개념](#기본-개념)
3. [고급 기능](#고급-기능)
4. [실전 프로젝트](#실전-프로젝트)

## 시작하기

### 1. 환경 설정
```bash
# 가상환경 생성 및 활성화
python -m venv venv
source venv/bin/activate  # Linux/Mac
# 또는
.\venv\Scripts\activate  # Windows

# FastAPI 및 필요한 패키지 설치
pip install fastapi uvicorn
```

### 2. 첫 번째 FastAPI 애플리케이션
```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def root():
    return {"message": "Hello World"}
```

### 3. 서버 실행
```bash
uvicorn main:app --reload
```

## 기본 개념

### 1. 경로 매개변수
- 경로 매개변수 정의 및 사용
- 타입 힌트를 통한 데이터 검증

### 2. 쿼리 매개변수
- 선택적 매개변수
- 필수 매개변수
- 기본값 설정

### 3. 요청 본문
- Pydantic 모델을 사용한 데이터 검증
- 요청 본문 파싱

### 4. 응답 모델
- 응답 모델 정의
- 응답 상태 코드 설정

## 고급 기능

### 1. 의존성 주입
- 의존성 시스템 이해
- 공통 의존성 생성

### 2. 보안
- OAuth2 인증
- JWT 토큰
- 비밀번호 해싱

### 3. 데이터베이스
- SQLAlchemy 통합
- 비동기 데이터베이스 작업

### 4. 미들웨어
- CORS 설정
- 사용자 정의 미들웨어

## 실전 프로젝트

### 1. TODO API
- CRUD 작업 구현
- 데이터베이스 연동
- 사용자 인증

### 2. 파일 업로드
- 파일 업로드 처리
- 대용량 파일 처리

### 3. WebSocket
- 실시간 통신 구현
- 채팅 애플리케이션

## 유용한 리소스

- [FastAPI 공식 문서](https://fastapi.tiangolo.com/)
- [FastAPI GitHub 저장소](https://github.com/tiangolo/fastapi)
- [FastAPI 커뮤니티](https://fastapi.tiangolo.com/community/)

## 학습 순서

1. 기본적인 API 엔드포인트 생성
2. 경로 및 쿼리 매개변수 사용
3. Pydantic 모델을 통한 데이터 검증
4. 의존성 주입 시스템 이해
5. 데이터베이스 연동
6. 인증 및 보안 구현
7. 고급 기능 학습 및 실전 프로젝트 진행

각 섹션별로 실습 예제를 만들고, 단계별로 진행하면서 FastAPI의 기능을 익혀나갈 수 있습니다.
