# 기본 이미지로 Python 3.8을 사용
FROM python:3.8

# 작업 디렉토리를 /app으로 설정
WORKDIR .

# 현재 디렉토리의 requirements.txt 파일을 컨테이너의 /app 디렉토리로 복사
COPY requirements.txt ./
COPY .idea ./.idea
COPY app ./app
COPY google_service_key.json ./

# ARG 및 ENV 설정 추가
ARG DATABASE_URL
ARG HTTPS
ARG GOOGLE_CLIENT_ID
ARG GOOGLE_CLIENT_SECRET
ARG KAKAO_CLIENT_ID
ARG KAKAO_CLIENT_SECRET
ARG NAVER_CLIENT_ID
ARG NAVER_CLIENT_SECRET
ARG SECRET_KEY
ARG SESSION_SECRET_KEY
ARG SMTP_PASSWORD
ARG SMTP_PORT
ARG SMTP_SERVER
ARG SMTP_USERNAME
ARG SSL_CRT_FILE
ARG SSL_KEY_FILE
ARG GCP_SERVICE_ACCOUNT_JSON
ARG AI_SERVER_URL

ENV DATABASE_URL=$DATABASE_URL
ENV HTTPS=$HTTPS
ENV GOOGLE_CLIENT_ID=$GOOGLE_CLIENT_ID
ENV GOOGLE_CLIENT_SECRET=$GOOGLE_CLIENT_SECRET
ENV KAKAO_CLIENT_ID=$KAKAO_CLIENT_ID
ENV KAKAO_CLIENT_SECRET=$KAKAO_CLIENT_SECRET
ENV NAVER_CLIENT_ID=$NAVER_CLIENT_ID
ENV NAVER_CLIENT_SECRET=$NAVER_CLIENT_SECRET
ENV SECRET_KEY=$SECRET_KEY
ENV SESSION_SECRET_KEY=$SESSION_SECRET_KEY
ENV SMTP_PASSWORD=$SMTP_PASSWORD
ENV SMTP_PORT=$SMTP_PORT
ENV SMTP_SERVER=$SMTP_SERVER
ENV SMTP_USERNAME=$SMTP_USERNAME
ENV SSL_CRT_FILE=$SSL_CRT_FILE
ENV SSL_KEY_FILE=$SSL_KEY_FILE
ENV GCP_SERVICE_ACCOUNT_JSON=$GCP_SERVICE_ACCOUNT_JSON
ENV AI_SERVER_URL=$AI_SERVER_URL

# 필요한 Python 패키지 설치
RUN pip install --no-cache-dir -r requirements.txt

# 애플리케이션 실행 커맨드 지정
CMD ["python", "app/main.py", "deploy"]
