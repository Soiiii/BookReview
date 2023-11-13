# 02장. 구현 기술과 학습


# 2.1 구현 기술

구현 기술은 소프트웨어를 만드는 데 꼭 필요한 도구다. 개발자가 얼마나 구현 기술을 잘 활용하느냐에 따라 결과물이 달라진다.

```yaml
프로그래밍 언어 : Java, Javascript, Typescript, Kotlin
자바 웹 서비스 개발 : Spring Boot, HIbernate, MyBatis
자체적 API 개발 : Golang, React
데이터베이스 연동 작업 : MySQL
메시징 프로그램 : Kafka
클라우드 : AWS
운영체제 : OS
```

→ 위와 같이 개발자가 어떤 `역할, 직군`을 하느냐에 따라 선택해야 하는 기술이 달라진다.

# 2.2 학습 대상

학습을 하고자 하는 구현 기술을 정할 때 다음 2가지 기준을 적용하면 좋다.
- 현재 사용 중인 기술
사용 중인 기술을 학습할 때는 처음부터 완벽하게 모든 것을 익히려 하지 않아도 된다.
필요한 부분만 알고 있으면 필요 기능 개발에 문제가 없다

- 문제를 해결하기 위한 기술
우리가 마주칠 문제는
  - 당장 해결해야 하는 문제
  - 가까운 미래에 해결해야 할 문제
     
이므로 문제 해결 능력을 향상하기 위해 평소에 구현 기술을 탐색하고 학습해야 한다.


## 2.3 기술 파기

익혀야 하는 기술은 많고 모든 기술을 깊게 파기 어려울때 어떻게 하면 좋을까?
1. 처음 접하는 기술을 익힐때는 핸즈온, 동영상 강의, 튜토리얼 문서로 빠르게 감을 잡는다.
2. 기술이 손에 익도록 일상 업무에서 자주 사용하거나 연습한다.
3. 필요할 때마다 기술을 조금씩 더 깊게 학습한다.
4. 방법을 잘 모르거나 구현하기 어려운 문제가 생겼을 때 해결하기 위한 더 나은 방법이 있는지 찾아본다.


## 2.4 학습 전략

앵귤러 -> 리액트 (대세) -> 고 언어, 러스트, 스벨트 등등 새로운 언어
JSP -> 타임리프

대체 기술이 나오면 기존 기술은 한순간에 사라진다. 
- 유행하는 기술의 흐름이 자주 바뀌다 보니 전략적으로 구현 기술을 학습한다.
-> 일단 주력 기술을 집중적으로 학습한다.

- 여러 기술을 꾸준히 탐색할 필요도 있다.
주기적으로 어떤 기술이 주목받고 있는지 조사하고 핸즈온이나 별도 학습을 해서 빠르게 경험한다.

- 스터디 참여한다.
  
- 뉴스레터와 블로그를 구독해서 소식을 접한다.

## 2.5 유행에 상관없는 구현 기술


### 3.2.2.3 PASSWORD EXPIRE

비밀번호 유효 기간 설정

설정하지 않으면 default_password_lifetime 시스템 변수에 저장된 기간으로 설정

`PASSOWRD EXPIRE`에 설정 가능한 옵션

- PASSWORD EXPIRE
    - 계정 생성과 동시에 비밀번호의 만료 처리
- PASSWORD EXPIRE NEVER
    - 계정 비밀번호의 만료 기간 없음
- PASSWORD EXPIRE DEFAULT
    - default_password_lifetime에 저장된 기간으로 유효 기간 설정
- PASSWORD EXPIRE INTERVAL n
    - 비밀번호의 유효 기간을 오늘부터 n일자로 설정

### 3.2.2.4 PASSWORD HISTORY

한 번 사용했던 비밀번호 재사용 불가능

`PASSWORD HISTORY`에 설정 가능한 옵션

- PASSWORD HISTORY DEFAULT
    - password_history 시스템 변수에 저장된 개수만큼 재사용 불가능
- PASSWORD HISTORY n
    - n개까지만 저장, 저장 이력에 남아있는 비밀번호 재사용 불가능

예전에 사용한 비밀번호를 저장해두는 테이블은 pasword_history이다.

### 3.2.2.5 PASSWORD REUSE INTERVAL

한 번 사용했던 비밀번호 재사용 금지 기간

설정하지 않으면 `password_reuse_interval` 시스템 변수에 저장된 기간으로 설정

`PASSWORD REUSE INTERVAL`에 설정 가능한 옵션

- PASSWORD REUSE INTERVAL DEFAULT
    - password_reuse_interval에 저장된 기간 설정
- PASSWORD REUSE INTERVAL n DAY
    - n일자 이후에 비밀번호 재사용 가능
