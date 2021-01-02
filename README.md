# shh2021_ULS
 2021 Seoul Hardware Hackathon, ULS Team
 ___
### 팀이름_ULS(Untact Logic Structure)

### 팀소개
 * 강준구(STM32CubeMX) (각자 맡은일 추가)
 * 이상혁(Android Application)
 * 권용찬(Cloude Data)
 * 정수빈(Planning and Design)

### 개요
 * 대상-요양원의 **노약자** 및 **요양병원의 환자**
 * 요양병원 및 요양시설 수 **증가**
 
 ![요양병원 및 요양시설 수 증가](https://github.com/Moderato-Swift/shh2021_ULS/blob/main/image/dataChartOne.png?raw=true)
 * 코로나19로 인한 **언택드시대**에서 **가정**에서의 **개개인의 요양**을 초점
 
 
 ![기존 의료용침대](https://github.com/Moderato-Swift/shh2021_ULS/blob/main/image/smartbed_resize.png?raw=true)
 
 * 기존의 Smart Bed 
 
  1. 수면 장애(불면증)를 겪는 사람들을 위한 침대로 수면의 질을 향상시키기 위한 목적
  2. 비싼 가격
  
  * 스마트폰 앱의 한계
  
  1. 스마트폰을 놓은 위치에 따라 결과의 변화율이 크다.
  2. 몸을 뒤척이는 소리나 코골이 소리가 작으면 측정되지 않는다.
  
 * 실제 센서를 침대에 부착해야하는 필요성을 느낌
 * 기존의 의료용침대에 ICT기술울 추가하여 사회적약자의 삶의 질을 개선
 
 ### 프로젝트 명_Smart Bed 
 
 ### 프로젝트 목표
 
* 수면패턴과 움직임 패턴의 누적 데이터를 통해 누워계시는 환자와 노인분들의 불편함을 미리 예측하여 도움을 주는 것이 목표입니다.
 
 ### 프로젝트 설명
  
  * Smart Bed Module를 침대에 직접장착 > 앱을 통한 정확한 데이터를 추출 > LCD 표시
  
   ![Smart Bed Case 도면](https://github.com/Moderato-Swift/shh2021_ULS/blob/main/image/drawing_2.png?raw=true)
   
   * Smart Bed Case에는 STM32,배터리,LCD 내장되어 있습니다.
   * 각 질병마다 환자를 분류해주는 케이스 디자인이나 사람들 취향에 따라 케이스 디자인을 지정할 수 있습니다.
  
   ![Smart Bed Module](https://github.com/Moderato-Swift/shh2021_ULS/blob/main/image/drawing_3.png?raw=true)
   
   어플 완성본 사진 넣기
  
  1. 온도 센서
  
  40도(?) 이상 시 >스마트폰 앱 알림>선풍기를 켜주세요. 몸을 뒤집어주세요.
  
  30도(?) 이하 시 >스마트폰 앱 알림>난방을 켜주세요. 전기장판을 켜주세요.
  
  2. 습도 센서
  
  습도 90%(?) 이상 시>스마트폰 앱 알림>기저귀 or 시트갈이
  습도 % 이하 시>스마트폰 앱 알림> 가습기를 켜주세요
  
  3. 자이로 센서(가속도 센서)
  
  움직임이나 충격>스마트폰 앱 알림>진동으로 알림
  침대의 기울기를 감지하여 일정시간동안 고정자세가 되지 않도록 함 > 욕창방지
  
  4. 압력 센서
  
  침대에 환자 유무 알림
  
  5. 적외선 센서(?)
  
  * 이외 기능
  
  ![어플 기능](https://github.com/Moderato-Swift/shh2021_ULS/blob/main/image/imageDescription_1.png)
  응급버튼
  
  발표 할 때[지정시간(식사,약)을 통해 보호자 앱으로 알림, 환자와 노인의 성별, 연령대를 분류할 수있고 같은 질병(파킨슨병,루게릭병)을 가지고 있는 사람들의 데이터를 누적하여 저장 > 향후 생리현상을 예측, 수면패턴과 움직임 패턴을 기록]
  
  ### 시스템 구성도
  
  (사진)
  
  ### 개발 환경
 
 ex)데이터 저장 - AWS Dynamodb
 
  
  ### 시연 영상 (2~3분 이내)
  
  
  
  
  ### 프로젝트 히스토리 (준비하면서 각자 맡았던 일정 정리)
  * 2020.12.7 (?) 서울하드웨어해커톤 신청서 제출
  * 2020.12. ~ 팀 전체회의
  * 2020.12. ~ 
  * 2020.12. ~
  * 2020.12.30 ~ IOT AWS 실시간 데이터 전송확인
  * 2020.12.30 ~ CUBE Monitor 상에서 데이터 그래픽으로 확인
  * 2020.12. ~
  * 2020.12. ~
  * 2020.12. ~
  * 2020.12. ~
  ___
 ##### 참고링크 (각자 참고하셨던 링크)
 
 * 국내외 스마트침대 [here](https://www.youtube.com/watch?v=BJTeHOZERnA&feature=youtu.be)
 * 스마트폰 앱의 한계 [here](https://www.youtube.com/watch?app=desktop&v=znju4QaRpok)
 * 의료용 침대 [here](https://www.youtube.com/watch?app=desktop&v=xHsvN7MNfRM)
 * 요양병원 및 요양시설 수 증가 사진 출처[here](http://www.docdocdoc.co.kr/news/articleView.html?idxno=1048036)
 * 기존 의료용침대 사진 출처 [here]()
 * Smart Bed Module 사진 출처 [here](https://www.youtube.com/watch?app=desktop&v=znju4QaRpok)
 
 
# 코드 파일 올리기
# 발표 2~3분 이내(시연 영상 합쳐서 5분 이내)
 
 
