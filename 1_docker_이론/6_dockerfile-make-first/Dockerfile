# 베이스 이미지를 명시해준다.
FROM alpine
# 이미지 생성ㅅ ㅣ기반이 되는 이미지 레이어입니다.
# <이미지이름>:<태그> 형식으로 작성
# 태그 미작성시 자동으로 가장 최신 이미지로 받는다.
# ex ubuntu:14.04

# 추가적으로 필요한 파일들을 다운로드 받는다.
# hello world 출력시 따로 해줄 작업이 없어 주석 처리
# RUN command

# 컨테이너 시작시 실행 될 명령어를 명시해준다.
CMD ["echo", "hello"]
# 시작시 실행할 실해파일 또는 쉘 스크립트 1회만 쓸수 있음

# Dockerfile 작성 -> docker cli -> docker server -> Image 순으로 작동
# Dockerfile 작성후 빌드 실행 명령어
# docker build ./
# build시 이미지 이름 명시가 가능함 -t johnahn/hello:latest
# -t [docker ID]/[저장소 또는 프로젝트 이름]:[버전] 형식으로 쓰는게 좋다.