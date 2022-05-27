# ***assignment***
*20191646 노은아 OSS 과제 2*

### *1. 리눅스 명령어*
-----
### 1) top
+ **top 명령어**

>리눅스는 멀티태스킹 운영체제로, 다수의 프로세스가 실행되면 CPU의 처리량과 메모리 소비량이 높아지는 문제점이 있다. 그래서 top 명령어를 통해 CPU의 사용량과 메모리 사용량을 확인하고, 서버에서 구동 중인 것들을 CPU 사용률이나 메모리 사용률이 많은 순서대로 나열하여 확인할 수 있다.

+ **명령어 설명**

top 명령어를 입력하면 나오는 결과
![top](https://user-images.githubusercontent.com/105151146/170634656-24c7fa0d-b86f-4423-af75-fea87c01f844.PNG)

1. 첫 번째 줄 : 현재 시간을 표시하고, 서버가 구동된 시간을 알 수 있다.
![top(1)](https://user-images.githubusercontent.com/105151146/170634988-a8120b0b-6ed5-4db7-806a-82a7220e4690.PNG)

2. 두 번째 줄 : 총 10개의 프로세스가 수행 중이며, 1개의 프로세스기 실행 중이다.
![top(2)](https://user-images.githubusercontent.com/105151146/170635277-10b6c31c-3afb-4b45-b621-4e8956b37090.PNG)

3. 세 번째 줄 : CPU 사용률을 볼 수 있다.
![top(3)](https://user-images.githubusercontent.com/105151146/170635380-d28185d2-4a5d-488b-ab25-e1dccdb1c94c.PNG)

4. 네 번째 줄 : 메모리 사용률을 볼 수 있다.
![top(4)](https://user-images.githubusercontent.com/105151146/170635460-bdf54763-6f31-4216-a03f-f9ec3c8f9ff8.PNG)

+ **옵션**

|옵션|설명|
|----|----|
|d|갱신주기를 초 단위로 설정|
|1|CPU를 각 코어별로 모니터링|
|m|메모리 사용률을 시각화|
|shift+p|CPU 사용률이 높은 프로세스를 기준으로 나열|
|shift+m|메모리 사용률이 높은 프로세스를 기준으로 나열|
|shift+t|수행 시간이 긴 프로세스를 기준으로 나열|
|u|모니터링할 user을 선택하여, 해당 권한 프로세스 감시|

+ **출처**

<https://blog.naver.com/hongganz/222456616664>

### 2) ps
+ **ps 명령어**
+ **명령어 설명**
+ **옵션**

### 3) jobs
+ **jobs 명령어**
+ **명령어 설명**
+ **옵션**

### 4) kill
+ **kill 명령어**
+ **명령어 설명**
+ **옵션**

### *2. vim 에디터*
-----
### 매크로(q)
