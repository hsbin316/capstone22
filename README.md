# 201840235 허성빈
    팀명 : 아몬드   
    이름 : 허성빈( 팀원 : 작품제작(프론트엔드 작업), 자료 취합, 타임키퍼(시간관리), 노션관리, 오픈웨더 전담 ), 최선아 ( 팀장 : 프론트엔드 작업, 회의주관, 일정조율, 활동독려, 회의록 정리, 사진촬영, 관광지 전담 등 ), 정서연 ( 팀원 : 작품제작, 자료 취합, 프레젠테이션 등 )   
    졸업작품 소개 사이트 : https://almond-daelim.github.io/NALJOMBWA/
    포트폴리오 소개 사이트 : URL (개인이 만든 GitHub 페이지) [ 안만들어도 상관없음 ]

## [ 졸업 작품 소개 ]   
 - 작품명 : 날좀봐
 - 개발환경 : 리엑트, HTML5, CSS, 테스트코드, eslint, prettier, Git, tailwind [ 추후 변경될 수 있음 ]
 - 작품 소개 : 현재 기상 상태를 사용자에게 전달해 주고 날씨가 좋은 지역의 관광장소와 명소를 사용자에게 추천해주는 사이트이다.
 - 작품의 특징 : 오픈웨더 api와 관광지 api를 사용하여 기상 정보를 가져온다.
 
 ## [ 개발 일지 ] ( 최소한 일주일에 한번 , 개인 수행평가 )
 ## (11월16일)
 - 12주차 수업진행 내용 정리   
    `[지난주 부터 오늘날 까지 한 작업]`   
    - 메인페이지 퍼블리싱작업
        - 피그마 사이트를 참고하여 디자인 함
        - <img src="./image/publishing-light.PNG" />
        - 기본 페이지
        - <img src="./image/publishing-dark.PNG" />
        - 다크모드를 적용한 페이지
        - <img src="./image/publishing-size.PNG" />
        - widht값에 변화에 따른 페이지
    - 기존 dark모드의 스위치를 헤더에 있는 dark버튼으로 바꿔서 적용
        - 위 이미지 오른쪽위 버튼을 참고
    - API호출 과정에서 시간이 걸리는 경우 발생
        - spinner기능 추가
            - <img src="./image/spinner.PNG" />
            - 위 이미지와 같이 값이 호출되기전에 spinner가 돌게 만듬   
     
    `[ 오늘날 부터 다음주까지 할 작업 ]`
    - MapPage 만들기
        - weatherMap.js파일에 구현한 기능을 토대로 만듬
        - 피그마를 참고하여 만들 것
        - Router기능을 사용하여 지도보기를 누를시 Map 페이지로 이동하게 만들 것
    - darkmode가 적용되지 않은 부분을 찾아본 후 수정할 것
        - 지금 확인한 바로는 상세페이지에 darkmode가 적용이 되지 않음
    - 위 작업을 마친 후 github에 commit 후 머지 시킬것
        - 졸업프로젝트 작업의 거의 마무리 되었기에 오류 체크할 것
        - 체크후 발생한 오류에 대해 수정할 것
        
 ## (11월09일)
 - 11주차 수업진행 내용 정리   
    `[ 지난주 부터 오늘날 까지 한 작업] `
    - 날씨지도 완성
        - <img src="./image/weather-map-fin.PNG" />
        - 각 지역별로 좌표를 지정하여 자리를 맞춤
        - weathermap api의 데이터를 호출하여 날씨상태 온도 날씨아이콘 등을 호출해옴
        - 이미지와 같이 배치하여 사용자에게 보여줌
    - weather.js에서 tour.js로 데이터를 보내는 과정에서 발생했던 오류 수정
        - mainpage에서 tour.js로 데이터를 보내는 과정에서 weather.js를 호출하기 전에 tour.js에 데이터를 보내 undefinded값이 들어가는 문제가 발생
        - 삼항연산자를 이용하여 weather.js가 먼저 호출된 후 tour.js가 호출 되도록 바꿔 문제를 해결함
    - mainpage의 퍼블리싱 작업을 시작함
        - <img src="./image/mainpage.PNG" />
        - 이미지와 같이 구성요소를 배치하였음   
        
    `[ 오늘날 부터 다음주까지 할 작업 ]`
    - mainpage 퍼블리싱 작업 마무리
        - 피그마 페이지를 참고하여 배치할 것
        - 피그마 페이지를 참고하여 글꼴사이즈, 폰트 굵기 등을 맞출것
    - mainpage의 다크모드를 적용할 것
        - 현재 날씨카드와 푸터에만 적용되어있음 
        - 피그마 페이지를 참고하여 디자인 혹은 색상을 적용할 것
 ## (11월02일)
 - 10주차 수업진행 내용 정리<br>
    ` [ 지난주 부터 오늘날 까지 한 작업 ]`
    - 새로고침 할때 마다 지속적으로 openweathermap api를 호출하는 문제를 해결함
        - localStorage에 weather-data를 저장하는 방식 채용
        - 아래의 이미지 참고
        - <img src="./image/localStorage.PNG" /><br>
            - localStorage에 저장한 시간의 한시간 기준으로 새로고침 시 localStorage의 데이터값 변경 가능
            - 새로고침을 할때 마다 변경되는 날씨 데이터 값이 바뀌는 현상을 막았음
            - openweathermap api를 호출을 최소화함으로써 처음을 제외한 로딩 시간이 단축됨
        - 날씨지도를 만들때 사용할 17지역의 weather data를 가져옴 ( 지역이름, 날씨아이콘, 기온 등) 

    ` [ 오늘날 부터 다음주까지 할 작업 ]`
    - 가져온 날씨데이터를 날씨지도위 화면에 구현할 것
        - Absolute를 사용하여 구현할 것임
        - WebPage의 width값에 따라 반응하는 날씨지도로 만들 것
        - 메인페이지의 퍼블리싱을 할 것
            - 피그마 사이트에 올라온 디자인을 참고하여 반응형으로 만들 것
        - 지난주에 다 못한 weatherCard의 아이콘 가운데 정렬을 시킬 것

 ## (10월26일)
 - 9주차 수업진행 내용 정리
    - openweathermap api를 이용하여 전국의 날씨데이터를 구한후 랜덤으로 화면에 출력하는 기능 구현
        - 도시이름이 영어로 나왔던 문제 또한 해결
        - 아래의 이미지 참고
        - <img src="./image/weather-card-ver2.PNG" style="width:300px" />
    - 자식컴포넌트(weather.js)에서 부모컴포넌트(index.js)로 데이터(도시이름)를 이동하는 기능 구현
    - openweathermap의 날씨 아이콘이 강제로 다크모드가 적용되었던 문제 해결
        - 위의 작업들을 통해 hook의 규칙에 대해 다시한번 상기할 수 있었으며 map이 어떤방식으로 돌아가는지 가끔식 배열에 undefinded값이 들어가는 지에 대해 알 수 있었음
    - 다음주까지 할 것들
        - openweathermap api를 이용하여 다음주 까지 한반도 지도에 17여개의 도시에 날씨 데이터 값을 적용시킬 것
            - 피그마 사이트를 참조하여 width값과 height값을 정하고 반응형을 어떤식으로 만들지에 대해 공부하기
        - weathercard 내부의 값 정렬 및 폰트처리

    

 ## (10월19일)
 - 8주차 수업진행 내용 정리 (중간고사)
    - openweathermap api를 이용하여 전국 17곳의 데이터 값을 가져오는 작업 완료
        - axios multiple requests기능을 사용하려 하였으나 두개 이상의 데이터를 호출하는 방식을 하기에는 기술 부족
        - openweathermap api의 group기능을 이용하여 전국 17곳의 아이디값을 가져와 호출 성공
        - 아직 17곳의 데이터를 가지고 랜덤으로 하나의 지역을 화면에 가져오는 기능은 구현하지 못함
        - <b>이번주 혹은 다음주까지 완성할 것</b>
    - openweathermap api의 데이터값을 연속 두번 호출이 발생하는 것을 확인
        - 확인결과 `React.StrictMode`로 인하여 발생한 문제라는 것을 알게됨
        - `React.StrictMode` 에 대한 [설명](https://velog.io/@kysung95/%EC%A7%A4%EB%A7%89%EA%B8%80-react-strict-%EB%AA%A8%EB%93%9C%EB%9E%80) 
    - openweathermap api의 데이터를 아래의 지도를 수정한 후 지도위에 올리는 작업을 수행할 것
        - <img src="./image/map.jpg" style="width:300px"/><br>`https://m.blog.naver.com/hakarashi/221868934187`
        - 지역명(한글), 날씨 아이콘, 온도 등을 표시할 것
    - darkmode의 스위치를 버튼형식으로 바꿀것
        - 다음주는 아니여도 앞으로의 사이트 UI디자인을 위하여 최대한 빠른시에 완성할 것
        - [flaticon](https://www.flaticon.com/)의 무료 아이콘 혹은 직접 이미지를 만들어 사용할 것


 ## (10월12일)
> 7주차 수업진행 내용 정리
 - openweathermap api를 이용하여 값 호출 작업 1차 완료
    - <img src="./image/weather-card.png" />
    - 앞으로 전국의 날씨 데이터(17지역)를 호출한 후 종합하여 맑은날씨의 데이터를 가진 지역의 데이터를 하나 랜덤으로 선택하여 화면에 뿌려주는 작업을 할 것
    - 영어로 나오는 지역 이름 및 날씨상태를 한글로 호출할 수 있도록 수정할 것
 - openweathermap api를 Github에 올리면서 발생한 오류를 수정할 것
    - 오류코드 : 'error: process completed with exit code 1.'
 - 저번주에 만든 ppt자료를 다시한번 확인하여 잘못된 부분이 있으면 수정할 것
 - openweathermap api중 지도 api를 호출하여 아래이미지 처럼 화면에 출력할 것
    - ex) <img src="./image/weathermap-ex.png" />
- 지난주에 만든 openweather api 호출 값에 darkmode를 적용할 것
    - weather icon의 경우 api호출하는 과정에서 강제로 다크모드로 호출되는 경우가 있기에 이를 수정할 것
    - card의 color색상은 '1F2937으로 border색상은 none으로 처리
    - 폰트의 색상은 FFFFFF로 설정
 
 ## (10월05일)
 > 6주차 수업진행 내용 정리
 - openweathermap api를 이용하여 값 호출
    - 온도, 아이콘, 날씨 등을 호출하였음
    - <img src="./image/weather-api.PNG" />
 - 피그마 사이트에 올린 디자인 편집
    - 다크모드를 활성화 했을 때 나올 페이지를 아래의 이미지와 같이 제작 (추후 수정될 수 있음)
    - <img src="./image/darkmode-ver.PNG" />
    - 사이트 홈페이지 로고를 올바르게 수정
        - 기존
        - <img src="./image/logo-before.PNG" />
        - 적용후
        - <img src="./image/logo-after.PNG" />
 - 다음주 까지 해야할 것
    - 이번주 일요일(10월09일)까지 졸업작품 ppt완성
        - 포스터에 들어갈 내용 지난주에 작성한 내용과 동일
    - openweathermap api에서 불러온 값을 이용하여 아래와 같이 만들기
        - <img src="./image/openweathermap-api.PNG" />
    - openweathermap 의 'weather maps' api를 호출할 것
    - 피그마 사이트에 올린 모든 디자인 편집
        - 모든 페이지에 다크모드를 적용했을때의 디자인을 만들 것
        - header,footer,body의 다크모드 색상은 '1F2937'으로 설정하였음
        - header,footer,body의 구별은 stroke를 이용하여 구분 stroke의 색상은 '374151'으로 설정


 ### (09월28일)
 >5주차 수업진행 내용 정리
 - 지난번 담당 했던 기능 github에 올리기
 - Button 기능
    - Button, ArrowButton 기능 완성
    - <img src="./image/button_arrowbutton.PNG">
    - 노션에 올려둔 팀 규칙에 작성방식을 참고하여 push함
    - github에 올리는 과정에서 아래와 같은 상황 발생
    - <img src="./image/github-err.PNG"> 발생
    - visual studio code에 <b>prettier</b>와 <b>eslint</b>를 설치하여 코드의 오류를 찾아 수정하여 정상화 하였음
 - DarkMode 기능
    - DarkMode 기능 github에 올리기
    - 노션에 올려둔 팀 규칙에 작성방식을 참고하여 push함
    - <img src="./image/github-err.PNG"> 또 다시 발생 
    - 위에서 나온것 처럼 코드를 수정하여 정상화 완료
 - openweathermap api
    - <b>axios</b>를 사용하여 api를 가져오는 기능까지 완료
    - 다음주 까지 온도,습도,날씨아이콘 등을 가져오는 기능 활성화 할것
 - 다음주까지 해야할 것
    - A1사이즈의 세로로 포스터 만들것 (<b>일러스트를 사용하여 만들어야한다</b>)
        - 포스터에 필수적으로 들어갈 요소 (CMYK)
            - 팀명(아몬드)
            - 팀장 (최선아), 팀원이름 (허성빈,정서연)
            - 대학명, 로고 (<b>대학 [홈페이지](https://www.daelim.ac.kr/cms/FrCon/index.do?MENU_ID=260)에 로고 일러 있음</b>)
            - 학과명 (컴퓨터정보학부) - outLine
        - 피그마에 올리 홈페이지 화면 디자인을 활용할 것
    - 졸업작품 PPT를 만들 것
        - 내용으로 팀원소개,작품소개,사용언어,구동방식,이벤트처리 방식등을 넣어 만들 것
        - 피그마에 올리 홈페이지 화면 디자인을 활용할 것
    


 ### (09월21일)
 >4주차 수업진행 내용 정리
 - 지난번 담당 했던 기능 완성
    - Footer(완성)
    <img src="./image/footer-design.PNG"> <br>위 이미지 같이 디자인 구현 ( 디자인은 추후 변경될 수 있음 )   
    - DarkMode(완성) <br>
    <img src="./image/darkmode.PNG"> <br> 위 이미지 같은 기능과 스위치로 구현 ( 디자인은 추후 변경될 수 있음 ) 
        - darkmode button을 누르면 위의 이미지와 같이 css가 변경됨
        
    - Base Button, Arrow Button(미완성)
 - [tailwind css](https://tailwindcss.com/)의 사용법 숙지
 - 이번주 내 담당
    - openweathermap api : api구현 후 아래의 디자인과 같이 만들 것 <br>
    <img src="./image/openweathermap-api.PNG"> <br>
    - darkmode button ,footer : 지난주의 완성한 부분의 수정 및 보완작업
    - base button, left/right arrow button : 지난주의 작성한 대로 만들 것 <br>
 - 이번주 목표
    - 지난번에 완성하지 못한 기능(button)을 구현
    - [openweathermap](https://openweathermap.org/api)의 api를 구현할 것
        - 팀 노션사이트의 규칙 및 참고사이트를 이용하여 만들것
        - 팀 피그마사이트를 참고하여 디자인 할 것

### (09월14일)
>3주차 수업진행 내용 정리
- 팀 로고 디자인 작업 시작
    - 완성된 로고디자인    
    <img src="./image/logo.png">
- 각 팀원별 역활 분담 ( 팀 github의 'components/common' 폴더란에 들어갈 기능을 구현하는것)
- 내 담당 
    - footer : 대림대학교 홈페이지 footer를 참고하여 만들 것 <br>
    - base button : 'width : 285px / height : 101px' 로 만들 것  <br>
    <img src="./image/base-button.PNG"> <br>
    - left/right arrow button : 각각 'width: 30px / height : 45px' 로 만들 것 <br>
    <img src="./image/left_right-button.PNG"> <br>
    - darkmode button: 'width: 50px / height: 48px' 로 만들 것 <br>
- 이번주 목표
    - 내가 담당하는 부분( footer, button, darkmode )을 디자인 부터 기능 까지 모두 구현할 것
        - 팀 노션사이트의 규칙 및 참고사이트를 이용하여 만들것

### (09월07일)
> 2주차 수업진행 내용 정리
- 팀 결성 ( 팀장 : 최선아, 팀원 : 허성빈, 주서연 )
- 팀 프로젝트 주제 정하기 ( 사용자의 날씨 정보 확인과 지역별 날씨에 따른 관광지 추천 사이트 )
- 팀 프로젝트에 사용될 api 검색 ( [openweatherAPi](https://openweathermap.org/api)를 사용할 것)
- 팀원 역활 분담 및 팀 규칙 정하기
    - 나의 경우 작품제작, 참여인원 체크, 자료 취합, 타입키퍼, 노션관리의 역활을 수행할 것

### (08월31일)   
> 1주차 수업진행 내용 정리
- [공유리스트](https://bit.ly/3AupOKk)에 자신의 github repo주소 , 역활 등 올리기 및 조편성 
- 졸업 작품에 관한 생각 설문조사 [실시](https://docs.google.com/forms/d/e/1FAIpQLSfGDeNXpHiORS5-yfNuk5ZC9uGqSlD8vCRrlB9KgsstDqCtag/viewform)  
- README.md 작성시 [Markdown](https://gist.github.com/ihoneymon/652be052a0727ad59601) 을 활용하여 작성
- README.md 작성 요령 및 GitHub Commit 방법 [설명](https://sudo-minz.tistory.com/10)
