-   컨테이너 실행
    -   docker run [ImageName] [CMD]
-   컨테이너 나열

    -   docker ps
    -   출력 ex
        -   CONTAINER ID : 컨테이너 고유 아이디 hash값 일부분만 표출
        -   IMAGE : 컨테이너 생성시 사용한 도커 이미지
        -   COMMAND : 컨테이너 시작시 실행될 명령어
            -   대부분 이미지에 내장되어 있으므로 별도 설정 할 필요 없음
        -   CREATED : 컨테이너 생성 시간
        -   STATUS : 컨테이너 상태
            -   Up 실행중
            -   Exited 종료
            -   Pause 일시정지
        -   PORTS : 컨테이너가 개방한 포트와 호스트에 연결한 포트 특별한 설정하지 않을시 출력되지 않음
        -   NAMES : 컨테이너 고유 이름 컨테이너 생성시 --name 옵션으로 설정가능
            -   설정하지 않을시 도커 엔진이 임의로 형용사와 명사를 조합해서 설정함 중복 불가능.
            -   rename으로 재설정 가능
    -   docker ps -a
        -   실행되지 않은 컨테이너도 모두 보여줌
    -   docker ps --format 'tables{{.Names}}
        -   NAMES 값만 출력

-   Container Life cycle

    1. 생성
        - docker create [ImageName]
            - 컨테이너만 만드는 역할
    2. 시작
        - docker start [실행할 컨테이너 ID/Name]
            - [-a] : attach의 준말이다.
                - docker 컨테이너가 실행될때 output을 화면에 출력해준다.
            - 만들어진 컨테이너를 실행
            - id값은 일부만 넣어줘도 인식한다.
    3. 실행
        - docker run [ImageName]
            - 생성부터 실행까지 한번에
    4. 중지
        - docker stop [중지할 컨테이너 ID/Name]
            - 자비롭게 그동안 하던 작업들을 완료하고 컨테이너 중지
        - docker kill [중지할 컨테이너 ID/Name]
            - 바로 중지
    5. 삭제
        - docker rm [삭제할 컨테이너 ID/Name]
            - 중지를 해야 삭제 가능
        - docker rm `docker ps -a -q`
            - 전체 삭제
        - docker rmi [image_ID]
            - 이미지 삭제
        - docker system prune
            - 한번에 컨테이너, 이미지, 네트워크 모두 삭제
            - 도커를 쓰지 않을때 모두 정리 가능
            - 실행중인 컨테이너엔 영향을 주지 않음

-   실행중인 컨테이너에 명령 전달
    -   docker exec [명령어를 전달할 컨테이너 ID/Name] [명령어]
