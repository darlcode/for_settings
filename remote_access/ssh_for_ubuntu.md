# Setting remote access in ubuntu 18.04 (not completed)
## 1. ssh server 구축

#### (1) ssh 다운받기

- **기존에 설치가 되어 있는 지 확인 하는 명령어**

  ```
  $dpkg -l |grep openssh
  ```

- **없다면 설치**

  ```
  $sudo apt-get install ssh
  ```

  혹은

  ```
  $sudo apt-get install openssh-server
  ```

**참고** [dpkg란?]()(추후에 추가할 예정)

![image](https://user-images.githubusercontent.com/61573968/78325045-8046b480-75b1-11ea-8077-887579a8ee60.png)

위의 사진은 이미 다운이 되어 있는 상태의 경우



#### (2) ssh 설정 파일 수정

```
$sudo vi /etc/ssh/sshd_config
```

![image](https://user-images.githubusercontent.com/61573968/78325187-e8959600-75b1-11ea-9d1b-e98f74f21de8.png)

위의 사진처럼 `PermitRootLogin prohibit-password` 부분을 `PermitRootLogin yes` 로 변경후

[vim 사용법에 대한 참고 링크(추후 올릴 예정)]()

`esc`버튼을 누르고 `:wq`를 입력하여 변경사항들 저장

**참고** 만약 port번호를 변경하고 싶다면 위 파일의 `Port 22` 부분을 원하는 port번호에 따라 변경



## 2. ssh server 실행

#### (1) 서버 실행 명령어

- 처음 ssh server를 실행하는 경우

  ```
  $sudo service ssh start
  ```

  

- 재시작 하는 경우

  ```
  $sudo service ssh restart
  ```



#### (2) 부가적인 명령어들

- **server의 실행 중단 명령어**

  ```
  $sudo service ssh stop
  ```

  

- **server의 실행상태 확인 명령어**

  ```
  $service ssh status
  ```



- **실행 중인 ssh server의 process확인 명령어**

  ```
  $ps -ef |grep sshd
  ```

  

- **실행중인 ssh server의 ip address와 port 번호 확인 명령어**

  ```
  $netstat -ntlp |grep sshd
  ```



#### (3) 내부 ip address 확인 명령어

```
$ifconfig
```

![image](https://user-images.githubusercontent.com/61573968/78326392-3cee4500-75b5-11ea-8dcb-0c72c1f6dae3.png)

inet에 적힌것이 내부 ip address





## 2. Windows에서 ssh server 접속





## 3. Ubuntu에서 ssh server 접속
