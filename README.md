# shh2021_ULS
 2021 Seoul Hardware Hackathon, ULS Team
 ___
# ULS(Untact Logic Structure)

### 팀소개
 * 강준구(STM32CubeMX) (각자 맡은일 추가)
 * 이상혁(Android Application)
 * 권용찬(Cloude Data)
 * 정수빈(Planning and Design)

### 개요
 * 대상-요양원의 **노약자** 및 **요양병원의 환자**
 * 요양병원 및 요양 시설 수 **증가**
 * 코로나19로 인한 **언택드시대**에서 **가정**에서의 **개개인의 요양**을 초점
 
 * 기존의 Smart Bed 
 
  1. **수면 장애(불면증)** 를 겪는 사람들을 위한 침대로 수면의 질을 향상시키기 위한 목적
  2. 비싼 가격
  
  * 스마트폰 앱의 한계
  
  1. 스마트폰을 놓은 **위치**에 따라 결과의 **변화율이 크다.**
  2. 몸을 뒤척이는 소리 나 코골이 소리가 작으면 **측정되지 않는다.**
  
 * 실제 센서를 침대에 **부착**해야하는 필요성을 느낌
 
 * 기존의 의료용 침대에 ICT 기술울 추가하여 사회적 약자의 삶의 질을 개선
 
 # 프로젝트 명-Smart Bed 
 
 ### 프로젝트 목표
 
* 수면패턴과 움직임 패턴의 누적 데이터를 통해 누워계시는 환자와 노인분들의 불편함을 미리 예측하여 도움을 주는 것이 목표입니다.
 
 ### 프로젝트 설명
  
   ![Smart Bed Case 도면](https://github.com/Moderato-Swift/shh2021_ULS/blob/main/image/Case.PNG)
   
   * **Smart Bed Case**에는 **STM32, 배터리, LCD**가 내장되어 있습니다.
   * **Smart Bed Module**를 **침대에 직접 장착 > 앱을 통한 정확한 데이터를 추출 > LCD 표시
   * 케이스 디자인은 각 질병마다 환자를 분류해 주거나 일반인들 취향에 따라 디자인할 수 있습니다.
  
   ![Smart Bed Module](https://github.com/Moderato-Swift/shh2021_ULS/blob/main/image/drawing_3.png?raw=true)
   
   ![어플 사진](어플 사진 링크)
  
  **1. 온도 센서**
  
  40도(?) 이상 시 >스마트폰 앱 알림>선풍기를 켜주세요. 몸을 뒤집어주세요.
  
  30도(?) 이하 시 >스마트폰 앱 알림>난방을 켜주세요. 전기장판을 켜주세요.
  
  **2. 습도 센서**
  
  습도 90%(?) 이상 시>스마트폰 앱 알림>기저귀 or 시트갈이
  습도 ??% 이하 시>스마트폰 앱 알림> 가습기를 켜주세요
  
  **3. 자이로 센서(가속도 센서)**
  
  움직임이나 충격>스마트폰 앱 알림>진동으로 알림
  침대의 기울기를 감지하여 일정 시간 동안 고정자세가 되지 않도록 함 > 욕창방지
  
  **4. 압력 센서**
  
  침대에 환자 유무 알림
  
  ((. 적외선 센서(?))
  
  * 이외 기능
  
  ![어플 기능](https://github.com/Moderato-Swift/shh2021_ULS/blob/main/image/imageDescription_1.png)
  
   
  [발표 >> 응급버튼을 통해 사용자의 ~~ 지정시간(식사,약)을 통해 보호자 앱으로 알림, 환자와 노인의 성별, 연령대를 분류할 수있고 같은 질병(파킨슨병,루게릭병)을 가지고 있는 사람들의 데이터를 누적하여 저장 > 향후 생리현상을 예측, 수면패턴과 움직임 패턴을 기록]
  
  ### 시스템 구성도
  
  ![시스템 구성도](https://github.com/Moderato-Swift/shh2021_ULS/blob/main/image/system_image.png?raw=true)

  ### 구성도 역할

  - Hardware
    - STM32L4S5I Discovery Kit 
      - Kit에 내장된 온도, 압력, 습도, 가속도 센서에서 받은 값을 AWS에 전송
    -  전원부
       - Micro 5pin 충전핀과 다양한 환경에서 사용 가능하도록 9V Battery 소켓을 내장
    - 출력
      - LCD와 BUZZER를 통해 간병인에게 상황을 신속하게 전달
  - Software
    - Android
      - Smart Bed에 필요한 센서값들을 불러서 Chart 표현 및 분석, 알림 설정, 센서값 확인 등의 역할
    - AWS IoT Core
      - Android SDK 버전을 이용하여, MQTT 통신에 맞는 Topic에 Subscribe / Publish 역할(센서값 데이터 송수신)
    - AWS Lambda
      - IoT Core에 설정된 Rules 진행 -> DynamoDB 읽기/쓰기(특정 데이터 포함), API Gateway 데이터 전송 역할
    - AWS DynamoDB
      - 센서값 및 가속도 크기 데이터 실시간 저장 역할
    - AWS API Gateway
      - Lambda에 설정된 코드에 의해, 특정 RestAPI 주소를 호출하면 알맞은 데이터 값을 가져올 수 있는 역할

  ### 개발 환경
 
 - Hardware
   - CUBE PROGRAMMER, CUBE MONITOR
   - 전원부 : 9V Battery + Regulator[LM7805]
 - Software
   - APP : Android(Java)
   - IoT 서비스 : AWS IoT Core(Android SDK Version)
   - AWS 서비스 : AWS Lamdba(Node.js), DynamoDB, API Gateway
  
  ### 시연 영상 (2~3분 이내)
  
  
  
  
  ### 프로젝트 히스토리 (준비하면서 각자 맡았던 일정 정리)
  * 2020.12.7 (?) 서울하드웨어해커톤 신청서 제출
  * 2020.12. ~ 팀 전체회의
  * 2020.12. ~ 
  * 2020.12. ~
  * 2020.12.30 ~ IOT AWS 실시간 데이터 전송확인
  * 2020.12.30 ~ CUBE Monitor 상에서 데이터 그래픽으로 확인
  * 2021.1.1 ~
  * 2021.1.1 ~
  * 2021.1.2 ~
  * 2021.1.2 ~
  ___

  ### 향후 진행
  - Hardware
    - 
  - Software
    - TensorFlow을 이용한 데이터 모델 만들기
      - DynamoDB에 저장된 데이터들을 CSV 파일 형태로 변환하여, TensorFlow에서 비지도학습 중 K-means Clustering 알고리즘을 이용해 이용자(노인)분들의 동작 상태를 분류할 수 있는 모델
    - UI 수정
      - Animation 적용 및 디자인 수정
    - Web 제작
      - 이미 구축된 AWS SDK를 이용해 홈페이지 만들기

 ##### 참고링크 (각자 참고하셨던 링크)
 
 * 국내외 스마트침대 [here](https://www.youtube.com/watch?v=BJTeHOZERnA&feature=youtu.be)
 * 스마트폰 앱의 한계 [here](https://www.youtube.com/watch?app=desktop&v=znju4QaRpok)


 
# 발표 2~3분 이내(시연 영상 합쳐서 5분 이내)
 
 
