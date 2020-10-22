# baseImage node 10버전 사용
FROM node:10

# 현재 폴더에 있는 파일을 컨테이너 내부로 복사해서 옮겨 준다. 
COPY ./ ./

# npm install로 package.json안에 디펜던시에 필요한 파일 설치를 해준다.
# ex ) express, mysql etc...
RUN npm install

CMD [ "node", "index.js" ]