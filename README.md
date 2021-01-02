# shh2021_ULS
 2021 Seoul Hardware Hackathon, ULS Team
 ___
### 팀이름_ULS(Untact Logic Structure)
### 팀소개
 * 강준구(STM32CubeMX)
 * 이상혁(Android Application)
 * 권용찬(Cloude Data)
 * 정수빈(Design)
 ### 프로젝트 명_Smart Bed
### 개요
 * 대상-요양원의 노약자 및 요양병원의 환자
 * 요양병원 및 요양시설 수 증가
 
 ![요양병원 및 요양시설 수 증가](https://github.com/Moderato-Swift/shh2021_ULS/blob/main/image/dataChartOne.png?raw=true)
 * 코로나19로 인한 언택드시대에서 가정에서의 개개인의 요양을 초점
 
 * 기존의 의료용침대에 ICT기술울 추가하여 사회적약자의 삶의 질을 개선
 
 ![기존 의료용침대](https://github.com/Moderato-Swift/shh2021_ULS/blob/main/image/smartbed_resize.png?raw=true)
 
 * 기존의 Smart Bed 개발현황
 
  1. 일반인 대상
  2. 수면 질 향상의 목적
  3. 비싼 가격
  * 스마트폰 앱의 한계
  1. 스마트폰을 놓은 위치에 따라 결과가 달라짐
  2. 소리(코골이)가 작으면 측정되지 않음
 * 실제 센서를 침대에 부착해야하는 필요성을 느낌
 
 ### 프로젝트 목표
 
 수면패턴과 움직임 패턴의 누적 데이터를 통해 누워계시는 환자와 노인분들의 불편함을 미리 예측하여 도움을 주는 것
 
 ### 프로젝트 설명
  
  * Smart Bed Module를 침대에 직접장착 > 앱을 통해 정확한 데이터를 추출 > LCD 표시
  
   ![Smart Bed Case 도면](https://github.com/Moderato-Swift/shh2021_ULS/blob/main/image/drawing_2.png?raw=true)
   
   STM32,배터리,LCD 내장
   각 환자를 분류하여 취향에 맞는 케이스 디자인을 지정
  
   ![Smart Bed Module](https://github.com/Moderato-Swift/shh2021_ULS/blob/main/image/drawing_3.png?raw=true)
  
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
  
  
  6. 긴급버튼
  
  7. 지정시간(식사,약)을 통해 보호자 앱으로 알림
  
  8. 환자와 노인의 성별, 연령대를 분류할 수있고 같은 질병(파킨슨병,루게릭병)을 가지고 있는 사람들의 데이터를 누적하여 저장   > 향후 생리현상을 예측
  
  9. 수면패턴과 움직임 패턴을 기록
  
  ### 시스템 구성도
  
  ### 개발 환경
 
 ex)데이터 저장 - AWS Dynamodb
 
  
  ### 시연 영상 
  
  
  
  
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
 
 

 
 
