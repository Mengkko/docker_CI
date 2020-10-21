# redis를 통해 이해하는 컨테이너

1. docker run redis
    - redis를 실행
2. redis-cli
    - redis-cli명령어를 전달해야하나 컨테이너로 감싸져있기에
    - exec명령어를 이용해서 명령어를 전달한다.
3. docker exec -it [redis_id] redis-cli
    - [-it] 옵션은 Interactive Terminel의 약자로 명령어 실행후 빠져나오는게 아니고 터미널 환경을 이어서 사용할수 있는 옵션.
