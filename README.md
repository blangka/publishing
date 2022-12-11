# publishing

파편적으로 css html을 학습해서 작업하고 있었지만 이번에는 더 깊게 공부하고 싶어서 책을 구매했다. 책과 함께 publishing에 대한 전반적인 개념을 정리 할 예정이다.  
github : https://github.com/ezwebpublishing/with_coding_web

## HTML 기초

HTML tag 및 구성의 기초 적인 부분을 정리 할 예정이다.  
가장 많이 쓰는 tag부터 tag별 속성에 대해서도 기존에 그냥 썻던것들은 한번 리마인드 한다.

1. html basic 폴더

## CSS 기초(2. css basic 폴더)

CSS 의 심화 과정이 아닌 초급 과정을 리마인드 할 예정이다. grid , flex, position등 이미 알고 있지만  
업무하면서 익힌것들이 대부분이다. 파편적인 지식들을 한번 정리해서 복습 할 예정이다.

1. CSS 문법 기본
    1. HTML 에서 CSS 를 통해 스타일 설정하는 방법은 3가지 이다.
        1. inline style : HTML 태그에 직접 style을 적용하는 방법
        2. style 태그 : HTML에서 header에 style 태그를 사용하는 방법
        3. css 파일을 연결 하는 방식
    2. 색상의 경우에는 3가지로 표현가능하다.
        1. 색상 이름 : color: navy;
        2. 16진수 HEX : color: #0000ff; 같은 값이 2개 인경우 하나로 줄일수 있다. #0000ff -> #00f
        3. RGB : color: rgb(0, 0, 255); RGB 값은 www.photopea.com 에서 색상을 선택하면 RGB 값을 알수 있다.
    3. 색상 투명도 : rgba(0, 0, 255, 0.5); 뒤에 0.5는 투명도를 의미한다.
    4. 색조, 채도, 명도 : 색상의 색조 h 채도 s 명도 l을 활용하여 hsl 로 표현 가능하다.
    5. 단위 : px , % ,em , rem , vw , vh , vmin , vmax 등이 있다. (https://webclub.tistory.com/356)
        1. em : 부모의 font-size를 기준으로 한다. 부모의 font-size가 16px 이고 자식의 font-size가 2em 이면 자식의 font-size는 32px 이다.
        2. rem : root의 font-size를 기준으로 한다. root의 font-size가 16px 이고 자식의 font-size가 2rem 이면 자식의 font-size는 32px 이다.
        3. vw : viewport width의 1%를 의미한다. 100vw는 viewport width의 100%를 의미한다.
        4. vh : viewport height의 1%를 의미한다. 100vh는 viewport height의 100%를 의미한다.
        5. vmin : viewport width와 height중 작은값의 1%를 의미한다. 100vmin은 viewport width와 height중 작은값의 100%를 의미한다.
        6. vmax : viewport width와 height중 큰값의 1%를 의미한다. 100vmax은 viewport width와 height중 큰값의 100%를 의미한다.

2. CSS 선택자
    1. 선택자의 종류
        1. 전체 선택자 : * { color: red; }
        2. 태그 선택자 : h1 { color: red; }
        3. 클래스 선택자 : .class { color: red; }
        4. 아이디 선택자 : #id { color: red; }
        5. 자식 선택자 : .parent > .child { color: red; }
        6. 자손 선택자 : .parent .child { color: red; }
        7. 인접 형제 선택자 : .prev + .next { color: red; }
        8. 일반 형제 선택자 : .prev ~ .next { color: red; }
        9. 속성 선택자 : [type="text"] { color: red; }
        10. 가상 클래스 선택자 : a:hover { color: red; }
        11. 가상 요소 선택자 : p::before { content: "앞에 추가"; }
        12. 그룹 선택자 : h1, h2, h3 { color: red; }
    2. 선택자의 우선순위
        1. !important > 인라인 > 아이디 > 클래스, 속성, 가상 클래스 > 태그, 가상 요소 > 전체 선택자
        2. 같은 우선순위의 선택자가 여러개 있을 경우 나중에 선언된 선택자가 우선순위가 높다.
        3. !important는 우선순위가 가장 높다. 하지만 사용하지 않는것이 좋다.
        4. 인라인 선택자는 우선순위가 높다. 하지만 사용하지 않는것이 좋다.

3. font
    1. font 요소별 정의
        1. font-family : 폰트를 지정한다. font-family: "Times New Roman", Times, serif; 처럼 여러개의 폰트를 지정할 수 있다.
        2. font-size : 폰트의 크기를 지정한다. font-size: 16px; 처럼 px, em, rem, % 등을 사용할 수 있다.
        3. font-weight : 폰트의 굵기를 지정한다. font-weight: bold; 처럼 bold, normal, 100 ~ 900 등을 사용할 수 있다.  
           initial 은 기본 값으로 돌리는 것이고 inherit은 부모 요소의 값을 상속 받는다
        4. font-style : 폰트의 스타일을 지정한다. font-style: italic; 처럼 italic, normal 등을 사용할 수 있다.
        5. font-variant : 폰트의 변형을 지정한다. font-variant: small-caps; 처럼 small-caps, normal 등을 사용할 수 있다.
        6. font : font-family, font-size, font-weight, font-style, font-variant를 한번에 지정할 수 있다. font: italic bold
           12px/30px Georgia, serif; 처럼 사용할 수 있다.
    2. @font-face
        1. @font-face를 사용하면 웹페이지에서 사용할 폰트를 지정할 수 있다.
        2. @font-face { font-family: "NanumGothic"; src: url("fonts/NanumGothic.woff") format("woff"), url("
           fonts/NanumGothic.ttf") format("truetype"); }
        3. font-family에 지정한 이름으로 폰트를 사용할 수 있다.
        4. src에 지정한 url을 사용하여 폰트를 불러온다.
        5. format에 지정한 형식으로 폰트를 불러온다.
        6. @font-face를 사용하기 위해서는 폰트 파일이 서버에 있어야 한다.
        7. @font-face를 사용하기 위해서는 폰트 파일의 형식이 woff, woff2, ttf, otf, svg 중 하나여야 한다.
        8. @font-face를 사용하기 위해서는 폰트 파일의 크기가 50KB 이하여야 한다.
        9. @font-face를 사용하기 위해서는 폰트 파일의 라이센스가 무료여야 한다.
    3. 실제 font 사용 사례
        1. local에 저장해서 쓰는 방법
        2. CDN 방식의 폰트로 https://fonts.google.com/ 에서 원하는 폰트를 선택해서 사용하는 방법
        3. AWS s3에 올려서 사용하는 방법
    4. text-align
        1. text-align: left; 처럼 left, right, center, justify 등을 사용할 수 있다.
        2. text-align은 block 요소 안에 있는 inline 요소들을 정렬할 때 사용한다.
    5. 글자 간격
        1. letter-spacing : 글자 간격을 지정한다. letter-spacing: 2px; 처럼 px, em, rem, % 등을 사용할 수 있다.
        2. word-spacing : 단어 간격을 지정한다. word-spacing: 2px; 처럼 px, em, rem, % 등을 사용할 수 있다.
    6. 글자 수직 정렬  
       vertical-align : 글자 수직 정렬을 지정한다. vertical-align: top; 처럼 top, middle, bottom, baseline 등을 사용할 수 있다.
    7. vertical-align : top 으로 이미지 들어간 곳의 공백을 없앨수 있다.


4. list style
    1. list-style-type : 리스트의 마커를 지정한다. list-style-type: square; 처럼 disc, circle, square, decimal, lower-roman,
       upper-roman, lower-alpha, upper-alpha 등을 사용할 수 있다.
    2. list-style-image : 리스트의 마커를 이미지로 지정한다. list-style-image: url("images/marker.png"); 처럼 url을 사용할 수 있다.
    3. list-style-position : 리스트의 마커의 위치를 지정한다. list-style-position: inside; 처럼 inside, outside 등을 사용할 수 있다.
    4. list-style : list-style-type, list-style-image, list-style-position을 한번에 지정할 수 있다. list-style: inside square; 처럼
       사용할 수 있다.

5. display 속성
    1. block : 블록 요소로 지정한다. width, height, margin, padding 등을 사용할 수 있다.  
       inline 요소 들은 width 를 주어도 적용되지 않는데 이때 display: block; 을 사용하면 width를 줄 수 있다. 세로로 배치 된다.
    2. inline : 인라인 요소로 지정한다. width, height, margin, padding 등을 사용할 수 없다. 가로로 배치 된다.
    3. inline-block : block 과 inline의 특성을 합한것으로 가로로 배치 되지만 크기를 줄수 있다.   
       인라인 블록 요소로 지정한다. width, height, margin, padding 등을 사용할 수 있다. 가로로 배치 된다.
    4. table, table-cell : inline-block 은 넘어가면 아래로 가게 되는데 table을 이용하면 딱 화면에 맞춰서 넣는 것이 가능하다.
    5. 안보이게 하는 방법 :  display none , visibility hidden, opacity 0

6. overflow 속성
    1. auto : 넘치는 내용을 자동으로 처리한다.
    2. hidden : 넘치는 내용을 숨긴다.
    3. scroll : 넘치는 내용을 스크롤바로 처리한다.
    4. visible : 넘치는 내용을 그대로 보여준다.
    5. overflow-x : 가로축으로 넘치는 내용을 처리한다.
    6. overflow-y : 세로축으로 넘치는 내용을 처리한다.

7. background 속성
    1. background-color : 배경색을 지정하고 #00f 처럼 16진수로 지정하거나 blue 와 같은 이름 rgb, rgba 를 사용해서 지정가능하다. 투명도의 경우에는 opacity 를 사용한다.
    2. background-image : 배경 이미지를 지정한다. url("images/bg.jpg") 처럼 url을 사용한다.
    3. background-repeat : 배경 이미지를 반복할지 지정한다. repeat, repeat-x, repeat-y, no-repeat 등을 사용할 수 있다.
    4. background-attachment : 배경 이미지를 고정할지 지정한다. fixed, scroll 등을 사용할 수 있다. fixed 를 사용하면 고정되어서 스크롤을 내려도 유지 된다.
    5. background-position : 배경 이미지의 위치를 지정한다. left top, center center, 100px 100px 등을 사용할 수 있다. 기본 값은 0 0 이고 첫번쨰는 가로축
       두번쨰 값은 세로축 값이다. % 혹은 px로 선택 가능하다
    6. background-size : 배경 이미지의 크기를 지정한다. cover, contain 등을 사용할 수 있다. cover 는 이미지가 화면을 꽉 채우고 contain 은 이미지가 화면을 꽉 채우지
       않는다.

## 반응형 web 참고 자료

- [뷰포트 메타태그와 미디어 쿼리](https://nykim.work/84)
- [vw, vh, vmin, vmax, em, rem 속성](https://nykim.work/85)
- [image size 맞추기](https://nykim.work/86?category=692675)

## flex grid 기초(3. flex grid 폴더)

### flex

기본적인 flex 만 사용하면 inline-block 처럼 내용물의 넓이 만큼 가로 정렬 을 한다.

### flex-direction

방향을 결정 할때 사용한다.

1. row : 기본값으로 가로 정렬
2. row-reverse : 가로 정렬을 반대로
3. column : 세로 정렬
4. column-reverse : 세로 정렬을 반대로

### flex-wrap

줄바꿈을 어떻게 할지를 결정한다.

1. nowrap : 기본값으로 내용물이 넘치면 줄바꿈을 하지 않는다.
2. wrap : 내용물이 넘치면 줄바꿈을 한다.
3. wrap-reverse : 내용물이 넘치면 줄바꿈을 한다. 줄바꿈을 반대로 한다.

### flex-flow

direction 과 wrap 을 한번에 사용할 수 있다.

### justify-content

메인축 방향으로 아이템을 정렬 하는 속성

1. flex-start : 기본값으로 왼쪽 정렬
2. flex-end : 오른쪽 정렬
3. center : 가운데 정렬
4. space-between : 아이템 사이에 동일한 간격을 둔다.
5. space-around : 아이템 주위에 동일한 간격을 둔다.
6. space-evenly : 아이템 사이에 동일한 간격을 둔다. 아이템 주위에 동일한 간격을 둔다.

### align-items

수직축 방향 정렬

1. stretch : 기본값으로 아이템의 높이를 부모의 높이로 맞춘다.
2. flex-start : 아이템을 위쪽 정렬
3. flex-end : 아이템을 아래쪽 정렬
4. center : 아이템을 가운데 정렬
5. baseline : 아이템을 기준선에 정렬

정 가운데로 주려면 justify-content : center 와 align-items : center 를 같이 사용해야 한다.

### align-content

여러 행 정렬로 아이템들의 행이 2줄 이상 되었을때의 수직축 방량 정렬을 결정하는 속성 입니다.

1. stretch : 기본값으로 아이템의 높이를 부모의 높이로 맞춘다.
2. flex-start : 아이템을 위쪽 정렬
3. flex-end : 아이템을 아래쪽 정렬
4. center : 아이템을 가운데 정렬
5. space-between : 아이템 사이에 동일한 간격을 둔다.
6. space-around : 아이템 주위에 동일한 간격을 둔다.
7. space-evenly : 아이템 사이에 동일한 간격을 둔다. 아이템 주위에 동일한 간격을 둔다.

### align-self

align-items 와 같은 속성이지만 개별 아이템에 적용 할 수 있다.

1. auto : 기본값으로 부모의 align-items 속성을 상속 받는다.
2. stretch : 아이템의 높이를 부모의 높이로 맞춘다.
3. flex-start : 아이템을 위쪽 정렬
4. flex-end : 아이템을 아래쪽 정렬
5. center : 아이템을 가운데 정렬
6. baseline : 아이템을 기준선에 정렬

### flex 아이템에 적용하는 속성들

### flex-basis

유연한 박스의 기본 영역으로 아이템의 기본 크기를 설정합니다. flex-direction이 row 일때는 너비, column 일때는 높이를 설정합니다.

### flex-grow

유연하게 늘리기로 0이 기본 값이고 1로 넣으면 같은 비율로 증가한다.

### flex-shrink

flex-grow 와 쌍을 이루는 속성으로 0으로 세팅하면 flex-basis보다 작아지지 않기 때문에 고정폭의 컬럼을 쉽게 만들수 있다.

### order

아이템의 순서를 지정합니다. 기본값은 0이고 음수도 가능합니다.

## Grid

flex 가 1차원 이라면 grid는 2차원으로 flex와 grid를 같이 사용하면 더욱 유연한 레이아웃을 만들 수 있다.
