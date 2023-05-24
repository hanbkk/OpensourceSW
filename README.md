# Open Source SW Task
---
## 1. top
#### - 실시간으로 CPU 사용률을 체크해주는 도구로 리눅스를 사용하는 서버의 성능이나 현재 돌아가고 있는 상황을 볼 때 사용한다
##### - 사용방법 : 터미널에 접속해 top 명령어와 옵션 등을 명령한다

###### _터미널에서 top 실행 화면_

<img width="882" alt="스크린샷 2023-05-24 오후 1 32 33" src="https://github.com/hanbkk/OpensourceSW/assets/133843565/8ecc8abe-9419-4cc7-a406-27a37cbbeb71"> 

#### - 위쪽 화면은 현재 시스템의 상태를 보여주는 화면 - 시스템 시간이나 uptime 등을 전체적으로 확인 가능

###### _top 실행 화면 중 위쪽_
<img width="888" alt="스크린샷 2023-05-24 오후 1 32 38" src="https://github.com/hanbkk/OpensourceSW/assets/133843565/7a48a299-c538-4f6e-8613-75ab4d006e3a">

#### - 아래쪽 화면은 현재 실행하고 있는 프로세스 현황을 보여주는 화면

###### _top 실행 화면 중 아래쪽_
<img width="876" alt="스크린샷 2023-05-24 오후 1 32 45" src="https://github.com/hanbkk/OpensourceSW/assets/133843565/23ec117d-6b75-453f-bbb2-b65bf75badec">


---
## 2. ps
#### - process status의 줄임말로 현재 실행중인 프로세스 목록과 상태를 보여준다
##### - 사용방법 : 터미널에 접속해 ps 명령어와 옵션 등을 명령한다

###### _터미널에서 ps 실행 화면_

<img width="339" alt="스크린샷 2023-05-24 오후 3 22 47" src="https://github.com/hanbkk/OpensourceSW/assets/133843565/e812a274-ed78-4743-9af9-4aedc2568b92">

### ps 주요 옵션
|   옵션   |     내용     | 
| ------- | ----------- |
|   - e   | 시스템 상의 모든 프로세스 정보를 출력 |
|   - f   | 상세한 정보를 출력 |


---
## 3. jobs
#### - 작업이 중지된 상태, 백그라운드로 진행 중인 작업상태, 변경 되었지만 보고 되지 않은 상태 등을 표시하는 명령어
##### - 사용방법 : 터미널에 접속해 jobs 명령어와 옵션, job ID 등을 명령한다

### jobs 주요 옵션
| 옵션 | 내용 |
| --- | --- |
| - ㅣ | 프로세스 그룹 ID를 state 필드 앞에 출력 |
| - n | 프로세스 그룹 중에 대표 프로세스 ID를 출력 |
| - p | 각  프로세스 ID에 대해 한 행씩 출력 |

### jobs로 알 수 있는 세션의 상태 값
| 상태 | 설명 |
| --- | --- |
| Running | 작업이 일시 중단되지 않았고 종료하지 않고 계속 진행 중임 |
| Done | 작업이 완료되어 0을 반환하고 종료했음을 의미 | 
| Done(code) | 작업이 정상적으로 완료되었으며, 0이 아닌 코드를 반환했음을 의미|
| Stopped | 작업이 일시중단 |
| Stopped(SIGHTP) | SIGHSTP 신호가 작업을 일시 중단 |
| Stopped(SIGSTOP) | SIGSTOP 신호가 작업을 일시 중단 | 
| Stopped(SIGTTIN) | SIGTTIN 신호가 작업을 일시 중단 |
| Stopped(SIGTTOU) | SIGTTOU 신호가 작업을 일시 중단 |

---
## 4. kill
#### - 프로세스에 시그널을 보내는 명령어이지만 대개 프로세스를 죽일 때 사용
##### - 사용방법 : 터미널에 접속해 'kill [options] <pid>'를 사용해 시그널을 보내거나 'kill [pid]' 죽이려는 프로세스의 pid를 넣어 프로세스를 죽인다

### kill 옵션
| 옵션 | 내용 |
| --- | --- |
| - s | default 시그널이 아닌 다른 시그널을 보냄 |
| - ㅣ | 지원하는 시그널의 목록을 확인 |
  
### 주요 시그널
| 시그널 | 영어 | 설명 |
| ---- | ---- | ---- |
| SIGHUP | Hang Up | 세션이 종료될 때 시스템이 내리는 시그널 |
| SIGINT | Interrupt | Ctil + C, 종료 요청 시그널 |
| SIGKILL | Kill | 강제 종료 시그널 |
| SIGSEGV | Segment Violation | 메모리 침범이 일어날 때 시스템이 보내는 시그널 |
| SIGTERM | Terminate | 기본 값, 종료 요청 시그널 |
| SIGTSTP | Temporary Stop | Ctrl + Z 일지 중지 요청 시그널 |
