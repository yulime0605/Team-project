# Team-building

-      카카오톡 단톡방 개설 완료하였습니다

-      Github 링크 : https://github.com/software-engineering-team8/

-      팀 빌딩은 첨부 파일과 깃 허브 Team building 레파지토리의 read me로 확인하실 수 있습니다.

-      주제는 아직 정하지 못하여 팀원들과 상의 하에 정하도록 하겠습니다.

|Participant|Poles|Skills|Training needs|
|-----------|-----|------|--------------|
|최소원|Team leader|Management : team leader<br>Programming : C, Python, Java<br>Configuration management : Github|UML<br>Communication skills|
|김유림|Implementor|Programming : Python, Java<br>Configuration management : Github|UML modeling|
|박지환|Liaison<br>tester|Programming : Python<br>Databases : MySQL<br>Testing : whitebox, blackbox|Java, C, C++|
|김효민|Implementor|Programming : Python, Java|UML<br>Tensonflow<br>Communication skills|
|정순인|Implementor|Programming : python, java, Android|UML<br>Communication skills|

# Problem Statement

> 주제 후보 : 
* 약 시간 알람
* **청각 장애인을 위한 위험 요소 파악 어플리케이션**
* 날씨에 맞는 옷 추천하는 옷장이나 디바이스
* 상한 음식이 생겼을 때에 알려주는 냉장고
* 외국인을 위한 AR 길 찾기 어플리케이션
* 여행 기간, 비용, 관심사, 나이, 지역 상황 및 날씨 고려하여 여행지 추천해주는 서비스
* 청각 장애인을 위한 비대면 강의 수화 통역 서비스
* 비콘을 활용한 출퇴근 시스템
<br>

> ## 주제 : 청각 장애인을 위한 위험 요소 알림 어플리케이션
본 프로젝트는 경적 소리, 화재 경보 등 음성으로 인지할 수 있는 위험 요소를 청각장애인에게 전달하기 위하여 고안되었다. 프로젝트는 딥러닝을 활용하여 마이크로 수집된 음성을 분석하고 위험 요소를 구분해낸다. 음성이 위험 요소로 분석될 경우 진동 발생 및 이미지를 띄움으로써 사용자에게 전달하고 일정한 규칙에 따라 보호자에게 알림을 전달합니다.
- 문제 : 청각 장애인은 청각을 제외한 감각으로만 위험 요소를 알 수 있음, 음성 위험 요소를 파악하기 어려움
- 해결 : 경적 소리, 화재 경보 등 음성 위험 요소를 진동 효과 및 이미지 시각화를 통하여 청각 장애인에게 전달하고자 함.
- 위험 요소 : 경적소리, 화재 경보, 짖는 소리
- 위험 요소가 있음을 감지했을 경우 , 진동과 함께 이미지를 통하여 인지시킨다
					웨어러블 기기와 연동
- 사용자 : 청각장애인 및 보호자
- 필요한 기술 : 앱 개발(android, ios), 딥러닝, 서버, database, Tensorflow

> ## Requirement
-	본 서비스를 사용하는 주체는 청각 장애인 및 보호자이다.
-	청각 장애인은 휴대전화에 어플리케이션을 설치하여 본 서비스를 사용할 수 있음
-	어플리케이션은 항상 백그라운드에서 실행 중이어야 한다.
-	어플리케이션은 마이크를 통하여 수집된 소리를 분석하여 경적소리, 경보 등 위험 요소를 구분해 냄
-	어플리케이션은 위험 요소를 인지하였을 경우 사용자의 휴대전화 또는 웨어러블 장치에 진동을 발생시키고 위험 요소에 해당하는 이미지를 띄움
-	어플리케이션은 새로운 위험이 발생하였을 경우 보호자에게 위치 정보와 함께 알림을 보내며, 같은 알림이 반복하여 발생하였을 경우에는 총 반복 시간과 횟수를 알림
-	위험 음성이 마이크를 통해 수집된 후 1초 안에 해당 음성을 분석하여 사용자에게 전달


# Use case Diagram ( 최소원 )
![Use Case Diagram - ATM](https://user-images.githubusercontent.com/48286887/95674300-34bd3500-0bea-11eb-835b-dcf4e1a419c2.jpg)

# Scenario Description ( 최소원 )
![시나리오 디스](https://user-images.githubusercontent.com/48286887/95674721-1573d700-0bed-11eb-87a2-28bab9caa1dc.JPG)

# Use Case Description ( 최소원 )
![Use case description](https://user-images.githubusercontent.com/48286887/93861737-f96ecb00-fcfb-11ea-96bb-1f98bb655dd7.PNG)

# 상용화된 유사한 서비스와의 비교 ( 최소원 )
> 1. skt코액터스 **'고요한M'** 서비스 : T케어 스마트워치와 청각장애인 전용 첨단 운전자 지원 시스템(ADAS)을 연계하여 차선 이탈이나 전방 추돌 경고 등의 상호아을 손목의 진동으로 인지할 수 있다. 
* 본 문서에서 제안하는 시스템과의 차이점 : '고요한M' 서비스는 차량의 시스템과 연계하여 주행 시 위험 알림으로 국한된 시스템이다. 본 시스템은 어떤 상황에 제약없이 모든 음성 위험 알림에 반응한다.

> 2. **sign to text** : 주변 소리를 인식하여 사용자들에게 위험 상황을 알려주는 컨셉이다. 주변 소리를 못 듣는 청각장애인들에게 알림 피드백을 제공한다.
* 본 문서에서 제안하는 시스템과의 차이점 : 'sign to text' 서비스는 휴대전화에 설치하는 어플리케이션으로 기능을 제공한다. 본 시스템은 손목에 착용할 수 있는 웨어러블 휴대전화를 쥐고있지 않은 상황에서도 기기로 기능을 제공한다.
# Sequence Description ( 박지환, 정순인 )
![image](https://user-images.githubusercontent.com/48286887/95866906-77763d00-0da3-11eb-94d1-16fac5ad26b3.png)
![image](https://user-images.githubusercontent.com/48286887/95866965-8a890d00-0da3-11eb-9f8f-ecaa0930f7f9.png)


# Class Diagram ( 김유림 )
![Object Diagram1](https://user-images.githubusercontent.com/48286887/95870021-f9b43080-0da6-11eb-8089-2e82197b3c7d.jpg)

# Object diagram ( 김효민 )
![image](https://user-images.githubusercontent.com/48286887/95867012-9bd21980-0da3-11eb-9eb6-d38b7c340383.png)

# design goal
 - usability - 남녀노소가 모두 사용하기 쉽도록 어플리케이션으로 제작한다.
 - response time - 위험 요소가 발생한 후 1 초 이내에 Guardian Android 앱에 알림을 보낸다.
 - extensibility - 새로운 위험 요소의 소리를 구분하기 위한 기능 추가 작업이 필요하다.
