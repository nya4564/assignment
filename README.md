-----
# ***assignment***
*20191646 노은아 OSS 과제 2*

-----
## *1. 리눅스 명령어*

### 1) top
+ **top 명령어**

>리눅스는 멀티태스킹 운영체제로, 다수의 프로세스가 실행되면 CPU의 처리량과 메모리 소비량이 높아지는 문제점이 있다. 그래서 top 명령어를 통해 CPU의 사용량과 메모리 사용량을 확인하고, 서버에서 구동 중인 것들을 CPU 사용률이나 메모리 사용률이 많은 순서대로 나열하여 확인할 수 있다.

+ **명령어 설명**

top 명령어를 입력하면 나오는 결과
![top](https://user-images.githubusercontent.com/105151146/170634656-24c7fa0d-b86f-4423-af75-fea87c01f844.PNG)

1. 첫 번째 줄 : 현재 시간을 표시하고, 서버가 구동된 시간을 알 수 있음
![top(1)](https://user-images.githubusercontent.com/105151146/170634988-a8120b0b-6ed5-4db7-806a-82a7220e4690.PNG)

2. 두 번째 줄 : 총 10개의 프로세스가 수행 중이며, 1개의 프로세스가 실행 중
![top(2)](https://user-images.githubusercontent.com/105151146/170635277-10b6c31c-3afb-4b45-b621-4e8956b37090.PNG)

3. 세 번째 줄 : CPU 사용률
![top(3)](https://user-images.githubusercontent.com/105151146/170635380-d28185d2-4a5d-488b-ab25-e1dccdb1c94c.PNG)

4. 네 번째 줄 : 메모리 사용률
![top(4)](https://user-images.githubusercontent.com/105151146/170635460-bdf54763-6f31-4216-a03f-f9ec3c8f9ff8.PNG)

+ **옵션**

|옵션|설명|
|---|---|
|d|갱신주기를 초 단위로 설정|
|1|CPU를 각 코어별로 모니터링|
|m|메모리 사용률을 시각화|
|shift+p|CPU 사용률이 높은 프로세스를 기준으로 나열|
|shift+m|메모리 사용률이 높은 프로세스를 기준으로 나열|
|shift+t|수행 시간이 긴 프로세스를 기준으로 나열|
|u|모니터링할 user을 선택하여, 해당 권한 프로세스 감시|

+ **출처**

<https://blog.naver.com/hongganz/222456616664>

-----

### 2) ps
+ **ps 명령어**

> top과 유사한 명령어로, top은 그때그때의 CPU 사용률이라면 ps는 프로세스 전체 사용시간 동안의 CPU 사용률이다. top은 proc에서 일정 주기로 합산해 CPU 사용률을 출력하고, ps는 ps를 실행한 시점에 proc에서 검색한 CPU 사용량을 출력한다. 
>
> proc 디렉토리에는 실행 중인 프로세스의 정보, CPU, 메모리 등 시스템 정보가 들어있다. 리눅스 부팅 시 커널이 메모리 상에 가상으로 만들어놓은 파일시스템이다.

+ **명령어 설명**

1. ps 명령어를 입력하면 나오는 결과
![ps](https://user-images.githubusercontent.com/105151146/170639546-ad27b932-1b82-4661-a1d3-40a6c6add520.PNG)

|PID|TTY|TIME|CMD|
|---|---|---|---|
|프로세스 번호|프로세스와 연결된 터미널|총 CPU 사용 시간|프로세스의 실행 명령행|

2. ps aux 명령어를 입력하면 나오는 결과
![ps aux](https://user-images.githubusercontent.com/105151146/170640778-527d4103-bae2-4223-ab99-ab254ae8ecbf.PNG)

|%CPU|%MEM|VSZ|RSS|STAT|
|---|---|---|---|---|
|CPU 사용률|메모리 사용률|가상 메모리 크기|실제 메모리 크기|프로세스 상태|

+ **옵션**

|옵션|설명|
|---|---|
|-A|모든 프로세스 출력|
|a|터미널과 연관된 프로세스 출력|
|u|프로세스 소유자를 기준으로 출력|
|x|터미널에 종속되지 않은 프로세스 출력|
|-e|커널 프로세스를 제외한 모든 프로세스 출력|
|-f|풀 포맷으로 출력|
|-r|현재 실행 중인 프로세스 출력|


+ **출처**

<https://roadofdevelopment.tistory.com/43>

<https://jhnyang.tistory.com/268>

-----
### 3) jobs
+ **jobs 명령어**

> 작업이 중지된 프로세스, 백그라운드에서 진행 중인 프로세스, 변경되었지만 보고 되지 않은 프로세스 등을 작업 목록(작업 번호, 상태, 명령어)을 출력하는 명령어다.

+ **명령어 설명**

jobs 명령어를 입력하면 나오는 결과
![jobs](https://user-images.githubusercontent.com/105151146/170646548-79703eea-e914-4592-91d8-f72e14123fc4.PNG)

1. 첫 번째 열 : 1, 2, 3의 숫자는 job 번호를 의미함. 중지되거나 백그라운드에서 사용하고 싶은 작업이 있을 때 이 job번호를 이용해서 실행시킴.

3. 두 번째 열 : +, - 기호로, +는 fg 나 bg 명령어를 쳤을 때 디폴트로 가장 먼저 가져와서 수행하게 될 프로세스임. 즉 현재 실행되고 있거나 실행 예정인 것. -는 현재 진행 중인 job이 끝나면 바로 다음에 수행될 프로세스.

+ **옵션**

|옵션|설명|
|---|---|
|-l|프로세스 그룹 ID를 state필드 앞에 출력|
|-n|프로세스 그룹 중 대표 프로세스 ID를 출력|
|-p|각 프로세스 ID에 대해 한 행씩 출력|

+ **출처**

<https://shaeod.tistory.com/968>

<https://jhnyang.tistory.com/395>

<https://zetawiki.com/wiki/%EB%A6%AC%EB%88%85%EC%8A%A4_jobs>

-----
### 4) kill
+ **kill 명령어**

프로세스를 종료시키는 명령어로, 프로세스에 종료 메시지를 보낸다.

+ **명령어 설명**

kill 명령어를 입력하면 나오는 결과
![kill](https://user-images.githubusercontent.com/105151146/170651027-08a2444d-33a3-48b4-9570-5e247620e0cf.PNG)

kill [옵션][pid] 또는 kill [%][작업 번호]를 통해 프로세스를 종료시킴.

+ **옵션**

|옵션|설명|
|---|---|
|-s[작업 번호]|보낼 시그널을 지정|
|-l|시그널 목록 출력|
|-9[pid]|응답없어도 강제종료|

+ **출처**

<https://blog.naver.com/tmk0429/222322701794>

<https://zetawiki.com/wiki/%EB%A6%AC%EB%88%85%EC%8A%A4_%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4_%EC%A4%91%EC%A7%80_kill>

-----
## *2. vim 에디터*

### 매크로(q)
