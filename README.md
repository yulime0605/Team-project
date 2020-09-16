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
