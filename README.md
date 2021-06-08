# 프론트 엔드 코딩 노트 

프론트 엔드 코딩 노트

<!DOCTYPE html>
<html lang="ko">
<head>
    - HTML의 문서 제목 (브라우저 탭에 나타나는 이름)
      <title> HTML 요소 레퍼런스 </title>
    - 메타태그는 빈태그, 빈태그는 닫히는 태그가 없다! 빈태그는 속성을 가지지 않으면 역할을 충실히 하기 어려움
       <meta name, charset, content>등의 종류가 있음
      <meta charset="UTF-8"> UTF-8은 문자가 인토딩 되는 방식 ->이게 가장 위쪽에 작성되는게 좋음! 
      EUC-KR : 완성형 이 루 어 진 => 완성형 글이 없으면 문자가 깨질 수 있어
      UTF-8 : 조합형  ㅇㅣ ㄹ ㅜ ㅇ ㅓ ㅈ ㅣ ㄴ  => 문자를 조합해서 원활하게 만들어냄 
      <meta name= "author" content = "이루어진">
      <meta name="description" content="이루어진의 사이트 입니다"> 
      <meta http-equiv="X-UA-Compatible" content="IE=edge"> 이 내용이 있는 인터넷 익스플로어에서 랜더링 될 때 최신의 방식으로 랜더링 되도록
      content는 name 또는 http-equiv 값을 작성할 때 사용 
      name은 작성자, http-equiv 인터넷 익스플로어 브라우저에서 렌더링 방식을 명시 할 때 주로 사용
      <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
       반응형 웹사이트를 위한 코드, 화면에 정보를 랜더링 하기 위한 영역을 설정 할때 사용
       우리가 일반적으로 보는 화며의 흰색영역이 일종의 뷰포트를 어떤방식으로 선언하는지 명시하는 부분
       코텐트에 이 가로를 디바이스에 최적화 시키고, 이니셜은 확대 축소를 1로 출발하겠다.
    - 스타일 외부에서 가져와서 연결
        <link rel="stylesheet" href="">
        rel은 릴레리션쉽의 약자 외부에서 가져오는 문서와 현재 문서와의 관계를 지정하는 필수 속성!!
        href 하이퍼텍스트레퍼런스의 약어!! 링크된 소스의 URL이며 URL은 절대적이거나 상대적임!! ./ 주변에!! 라는 뜻!! ./main.css를 입력!! 주변에서 찾아오는 상대적 방법 
    - 스타일 내부
        <style>
            div {
                color: red;
                background: blue;
            }
        </style>

        type 이라는 속성을 추가 할 수 있다
        <style type="text/css"></style>
        스타일 태그 안에 어떤 타잎의 내용을 작성할거냐 / 텍스트고 css이다. 
        HTML5버전에서는 text/css를 생략!! 가능 기본적으로 이것이 들어 있다고!
        정보를 지칭해서 헤드태그안에서 작성하는게 기본적이지만, 바디태그안에도 작성은 가능 그러나 헤드태그에 작성하는 것이 기본
        MIME type : 연결하는 문서에 해당하는 타입의 종류를 명시 
                    text/html, imag/png 등.. 필요에 따라서 찾아서 쓰면 됨
        BASE : 되도록 경로를 작성하는 곳 위에 작성하면 좋음!! 
               베이스 태그를 통해서 상대경로로 입력할 수 있는 특정경로를 기본적으로 정해버려서 기준으로 삼는 
               이제 기준이 된 경로이하의 경로를 작성 할 때는, 특정경로를 모두 작성하지 않아도 상대경로가 저것을 기준으로 시작
               베이스 태그는 단 한번만 작성 가능!!
               특정 경로에서 계속해서 데이터를 가져와서 쓸것 이라면 베이스 태그를 사용하면 편리 
               <base href="./css/">
</head>
<body>
    - 문서의 구조
    <header></header>
        해드를 만드는 부분에 해더를 사용 
        보통 해더 안에 로고, 메뉴, 검색바, 로그인, 로그아웃, 회원가입 등이 들어감
        해더태그안에는 해더를 넣을 수 없고, 푸터도 추가 할 수 없다
        <address>태그엔에도 해더를 넣을 수 없어!!!</address>
        <ul>언 오덜 더 리스트 </ul>
        <li>리스트 아이템의 약장 </li>
            ul, li 메뉴를 리스트화해서 작성했다!!! 
    <footer></footer>
        웹에서 가장 하단에 있는 바!! 
        푸터안에 푸터와 헤더가 또 들어갈 수 없다!! 전역속성만 포함
          
    헤더와 푸터는 div 대신 사용 할 수 있어, 그러나 얘네는 의미를 가지고 있는!!
    div는 의미를 가지지 않는 태그!! 
    <h1></h1>
        6단계의 문세 제목을 구현!!!
        h1~h6까지!! 글씨가 작아지면서 그러나, 제목크키를 줄이는 용도로 사용하지마<!DOCTYPE html>
        보통 글자 크기를 초기와 하고 재정의해서 사용
        구조를 나타내는 용도로만 사용!!
        모두 전역 속섬만 사용
        문서의 목차를 만드는 것처럼 사용 할 수 있다
        제목단계의 숫자를 건너 뛰지 마세요!
        h1->h2->h3....
        첫번째 단계는 한페이지에 하나만!! 즉 h1은 한번만!! (무조건은 아니고, 추천)
       <h1>
           <p>
               요런식의 구조! 
           </p>
       </h1>
       1. <h1>
           1. <h2></h2>
           2. <h2></h2>
           3. <h2>
               1. <h3></h3>
               2. <h3></h3>
               3. <h3>
                   1. <h4></h4>
               </h3>
           </h2>
       </h1>
    <main></main>
        핵심 포스터 부분!! 핵심 컨텐츠 부분
        메인은 문서에 하나만 존재 해야함
        메인태그는 인터넷 익스플로어에서 사용 불가
        블록 요소
    <article></article>
       독립적으로 구분되거나 재사용 가능한 영역을 설정
       일반적으로 블로그의 포스트나, 신문기사같은 묶음을 지정할 때 사용
       h1-h6중 하나를 포함 해야하며 
       작성일자나 시간을 <time>의 datetime의 속성으로 작성가능
        블록요소
        중간의 아티클 부분의 그룹이 어떤 특정부분의 바깥에 존재하더라도 이 컨텐츠로서의 가치가 유지된다면 article태그를 사용하는 것이 좋다
    <section></section>
        문서의 일반적인 영역을 설정하며 h1-h6를 포함
        블록요소
        섹션태그 내부에는 <article>을 넣을 수있으며
        </article>에 도 섹션이 들어갈 수 있다. 
        div 와의 차이점은 section은 의미를 가지고 있다! 
        특정 구역을 설정한다는 역할은 비슷!
        article은 독립적으로 사용 가능해야한다는 차이가 있다. 
    <aside></aside>
        문서의 별도 콘텐츠, 광고나 링크 등의 사이드바
        블록요소
    <nav></nav>
        네비게이션의 약자로 다른 링크를 제공
        보통 메뉴 홈, 어바웃, 컨텐츠 등의 목차, 색인 등을 설정
        블록요소
        <header>
            <nav>
                <ul>
                    <li>메뉴</li>
                    <li>리스트</li>
                    <li>여기에</li>
                    <li>나열</li>
                </ul>
            </nav>
        </header>

        ul은 언오덜드리스트 순서가 지정되지 않은 목록
        li, 리스트의 항목
    <address></address>
        실제 주소나, 연락처 정보를 입력
        블록 요소
        <a href=""></a> 특정 링클 내보내주는 앵커 태그
        mailto:이메일 = 이메일로 연결
        tel:+전화번호 = 전화번로 연결
    <div></div>
        본질적으로 아무 것도 나타내지 않는 콘텐츠의 영역을 설정
        의미가 없는 막사용 가능한 태그
        대표적으로 css, javascript를 삽입해서 div가 존재하는 특정영역을 찾아서 꾸미거나 제어할 때 사용
        블록요소
</body>
</html>


- 문자태그 -
   
- ol, ul,li / 사용은 ol+ li , ul + li 이런식의 세트로 사용  
    <li></li> : 각각의 항목을 의미하는 태그
    <ol></ol> : odered list 정렬된 목록을 의미하는 태그, 순서가 있는 목록을 만들때, 순서는 중요도를 의미할 수 있다. 
    <ul></ul> : unordered list 정렬되지 않은 목록을 의미, 순서가 필요 없는 목록
    li는 단독으로 사용 불가하며 ol, ul은 자식으로 li만 가능!! 
    ol, ul 는 블록 요소
    li는 리스트 아이템! list item 
    예제
        <ul>
            <li>
                Apple
                <ul>
                    <li>banana</li>
                    <li>mango</li>
                </ul>
            </li>
        </ul>
    => 리스트 안에 ul작성 가능 하며 이렇게 되면 화면에서 들여 쓰기 한것 처럼 작성됨! 앞에 점으로 항목이 나타남! 
       ol도 당연 가능 ol은 순서가 있는 목록이라서 앞에 숫자가 뜸!! 
       ol이 사용가능한 속성은 
       reversed : 익스플로어에서는 안되고, 항목을 역순으로 설정  <ol type="a" reversed="reversed">, <ol type="a" reversed>이런식으로 사용 
       start : 항목에 매겨지는 번호의 시작 값 <ol start="4"> 이런식으로 사용하며, 4부터 숫자가 매겨진다. 즉, 지정한 숫자로 시작 가능
       type : 항목에 매겨지는 번호의 유형, 로마자 숫자, 영어, 숫자 등 <ol type="a"> , <ol type="I"> 이런식으로 사용 
    li는 이하 항목을 순서를 설정
       <li value="7"> 이런식으로 사용 하며 li의 항목을 7부터 시작하도록 하며, 다른 값도 벨류를 설정하면 해당 값을 가지게 된다. 
    일반적으로 ol보다는 ul을 더 많이 사용함
    리스트라는 목록을 만드는 경우는 순서가 없는 경우가 더 많아서 ul을 주로 씀! 
    
- dl, dt, dd태그
    dt는 용어
    dd는 용어에 대한 정의 
    dl는 용어와 설명의 전체 집합! 
    dl 태그는 dt, dd만 사용 가능
    용어 - 설명 의 구조 
    ㅇㅇ은 ㅇㅇ이다 라는 정의를 kye = value 라는 형태로 표시할 때 유용 할 수 있다. 
    예제
        <dl>
            <dt>coffee</dt>
            <dd>coffee is a brewed~~~~</dd>
            <dt>milk</dt>
            <dd>milk is a nurtient-rich ~~~~</dd>
        </dl>
        => 용어 설명, 용어 설명!!!! 
    블록 요소
    div 안에 들어가기 어려워서 dl태그보다 보통 ul, ol 태그를 사용함
            <ul>
                <li>
                    <dfn>coffee</dfn>
                    <p>coffee is a ~~</p>
                </li>
                <li>
                    <dfn>milk</dfn>
                    <p>milk is a ~~~</p>
                </li>
            </ul>
    => 요런식으로 li로 바꿔서 사용!!1
- p 태그
    하나의 문단을 설정 
    문장 문단 단락을 지칭 할 때 사용
    블록요소
- hr/ 태그
    문단의 분리를 위한 태그 
    수평선으로 표현되나 시각적인 표현이 아니라 의미적 관점으로 사용 해야 한다
    수평선을 넣기 위해서 사용하는 것이 아님
    수평선을 없애려면, css를 통해서 수정이 가능 
    블록 요소

    예제
    
       <p>
           동해물과 백두산이 마르고 닳도록 <br>
           하느님이 보우하사 우리나라 만세 <br>
           무궁화 삼천리 화려강산 <br>
           대한 사람, 대한으로 길이 보전하세 <br>
       </p>
       <hr/>
       <p>
           남산위에 저 소나무, 철갑을 두른 듯
           바람서리 불변함은 우리 기상일세,
           무궁화 삼천리 화려강산
           대한 사람, 대한으로 길이 보전하세
       </p>
       <p>
           가을 하늘 공활한데 높고 구름 없이
           밝은 달은 우리 가슴 일편단심일세
           무궁화 삼천리 화려강산
           대한 사람, 대한으로 길이 보전하세
       </p>
       <p>
           이 기상과 이 맘으로 충성을 다하여
           괴로우나 즐거우나 나라 사랑하세
           무궁화 삼천리 화려강산
           대한 사람, 대한으로 길이 보전하세
       </p>

    => br은 줄바꿈 태그 
       
        1. css에서 hr줄 삭제하는 방법
        hr {
            border: none:
        }

        2. hr 줄을 변경하는 방법
        hr {
            border: 2px dashed red:
        }

        3. 요소는 사각형이기 때문에 패딩을 넣으면 사각형으로 보임
        그래서 선을 추가할 때 위, 아래 다 넣지 말고 위, 아래 하나만!! 
            hr {
                border: none;
                border-top: 2px dashed red;
            }
        => 일단 없애고 다시 입힌다! 
- pre 태그
    서식이 미리 지정된 텍스트를 설정
    텍스트의 공백이나, 줄바꿈, 글꼴을 유지하여 표시 할 수 있어
    내가 넣는 줄바꿈, 띄어쓰기 그대로 사용 가능
    기본적으로 monospace 글꼴 계열로 표시됨 
    ( monospace ) 형식은 코드가 있는 부분에 대한 글꼴 설정 이며, 글자 한글자 한글자의 너비가 다 동일한 글꼴을
    블록요소
    
    예제
        <pre>
            동해물과     백두산이 마르고 닳도록
            하느님이 보우하사 우리나라 만세.
            무궁화 삼천리 화려강산
            대한 사람, 대한으로 길이 보전하세.
        </pre>

    => 코드의 가독성을 위한 탭키 여백도 표현되기 때문에 
    공백을 다 지워줘야함

    <pre>동해물과     백두산이 마르고 닳도록
    하느님이 보우하사 우리나라 만세.
    무궁화 삼천리 화려강산
    대한 사람, 대한으로 길이 보전하세.</pre>

        => 요런식으로 앞에 공백을 다 빼줘야함

    주로 블로그 등에서 포스트 할때 사용자가 입력한 그대로 출력 되도록 할 때!! 
    내가 작성한 그대로 출력 되도록 하기위해서

- </blockquote>
    일반적인 인용문을 작성 할 때 사용
    cite 인용정보의url url

    예제
        <blockquote cite = "url">
            내용
        </blockquote>




인라인 요소 , 텍스트

- <a></a>
    현재문서에서 외부의 문서로 내보낼때 사용 "링크를 건다" Anchor의 약어
    다른페이지, 같은페이지 위치, 파일, 이메일 주소, 저화번호등 다른 URL로 연결 할 수 있는 하이퍼 링크를 설정
    a에 해당 되는 속성
        download : 링크를 통해 해당 요소를 다운 받는 용도로 사용됨을 명시해주는 요소,
                   해당 요소가 다운로드를 받게 해주지는 않음, 브라우저가 해당 링크가 다운로드가 되는 용도의 링크다 하고 힘트를 주는!!!!!!
                   ex)
                   <a href="./REDME.md" download="download">REDME.md</a>
                   <a href="./REDME.md" download>REDME.md</a> 요렇게 줄일 수 있어 
                   다운로드를 입력하징 않으면 다운로드할 파일이 창에서 열림
                   <a href="./images/heropy_log.png">image download</a>
                   <a href="./images/heropy_log.png" download>image download</a>
                    md : 마크다운이라는 확장자
        href : 하이퍼텍스트레퍼런스의 약어, 링크 URL을 설정을 해서 현재 문서에서 다른문서 어디로 나갈 것이냐를 명시
                    <a href=""></a> 이렇게 필수로 써줘야하는데, HTML5에서 생략이 가능하도록 바뀜!!!! 그러나 생략을 하면 링크로써의 기능은 상실 한다. 
        herflang : href language 나가는 경로에 해당하는 페이지의 언어를 설정
        rel : 릴레이션쉽의 약자로 관계를 설정. a태그를 통해서 빠져나가는 페이지가 현재 문서와 어떤 관계가 있는지 설정 
                    ex) license, prev, next
        target : 링크 URL의 표시 위치를 설정, 어떤 링크를 눌렀을때 현재 화면에서 뜨는거가 있고, 새로운탭이 열리면서 뜨는것이 있는데 그것을 설정 하는 것! 
                    ex) _self : 현재창에 해당 페이지를 뛰우겠어용. (기본값)으로 명시하지 않으면 해당 값으로 열림
                        _blank : 새로운 창에 띄울거엥요 
        type : 링크를 보낼때 자동으로 MINE 타입으로 되기 때문에 굳이 text/html을 명시 할 필요는 없다
    => 인라인 요소이며 주로 버튼 형식으로 많이 사용
    누르면 다른 페이지로 넘어가는
    인라인 요소는 가로세로값을 지정할 수 없어, 일반적으로 텍스트를 다루는데 사용하며 레이아웃을 다루는데는 사용하지 않아
    현대의 웹에서 버튼형식으로 모양을 가지는 경우가 많이 생겼는데, 인라인요소이기에 디스플레이를 블록으로 바꾸어 사용!!!!!

        페이지 내 에서 이동
        <ul>
            <li><a href="#tilte1">제목1</a></li>
            <li><a href="#title2">제목2</a></li>
        </ul>
        <h2 id="title1">제목1</h2> 
        <h2 id="title2">제목2</h2>
        <h2 id="title3">제목3</h2>
        
        # 부분으로 바로 열리는!! 

- <abbr title=""></abbr>
    abbreviation의 약어 / 뜻이 약어!!! 
    약어로 사용된 단어가 있다면 abbr이라는 태그를 통해 묶은 후 설명을 추가 할 수있어
        ex)
        <abbr title="Hyper Text Markup Language">HTML</abbr> is fun and easy
      이런식으로하면 창을 열어서 글자에 커서를 가져다 대면 약자의 풀어진 정의를 볼 수 있다. 

- <b></b>
    문체가 다른 글자의 범위를 설정
    특별한 의미를 가지지 않으며 읽기 흐름에 도움을 주는 용도 정도로 사용
    다른 태그가 적합하지 않은 경우 마지막 수단을 사용하며 기본적으로 글자가 두껍게 표시되나,
    두껍게 하기 위해 사용하지 않는다. 글자의 속성은 css에서 하는 것! 

- mark
    사용자의 관심을 끌기 위해 하이라이팅 할 때 사용
    의미 보다는 시각 적인 부분에 특화 되어있는 태그
    이것또한 css를 통해 충분히 커버가능.

- <em></em>
    의미를 강조 하기 위해 사용
    중첩이 가능하고  =><em><em><em>여기</em></em></em> 요런식으로 안에 또 넣을 수 있음
    중첩 될 수 록 의미가 강해짐
    정보통신 기기 등에서 구두 강조로 발음 됨
    기본적으로 이탤릭체로 표시 됨 

- <strong></strong>
    의미의 중요성을 나타내기 위해서 사용 
    기본 적으로 글자가 두껍게 사용됨 

- <i></i>
    위의 태그에서 표현할 수 있는 적합한 태그가 아닐때 사용
    평범한 글자와 구분하기 위해 사용 
    이탤릭체로 사용
    b태그와 유사하나 b는 일반적인 택스트, i는 이미지나 특수기호와 같은 것에 사용

    => 예제
    <body>
        <p>
            <b>1절</b>
            <mark>동해물과 백두산이 마르고</mark> 닳도록
            하느님이 보우하사 우리나라 만세
            
            <b>2절</b>
            남산위에 저 소나무 철갑을 두른 듯
            <em>바람서리 <em>불변함</em>은</em> 우리 기상일세 
    
            <b>3절</b>
            <strong>가을 하늘 공활한데 높고 구름 없이</strong>
            밝은 달은 우리 가슴 일편단심일세
    
            <b>4절</b>
            이 기상과 이 맘으로 충성을 다하여
            괴로우나 즐거우나 나라 사랑하세 
    
            <b>(후렴)</b>
            무궁화 삼천리 화려강산
            대한사람 대한으로 길이 보전하세 
        </p>
    </body>

- <dfn></dfn>
    용어를 정의 할때 사용
    전체의 문장에서 특정한 용어 하나를 정의할 때 주로 사용
    dl dt dd는 나열하거나 많은 정의 
    <dfn id="def-validator">validator</dfn> is a program that~~~

- <cite></cite>
    창작물에 대한 참조 설정
    기본적으로 이탤릭체 
    <cite>The Scream</cite> by Edward Munch. painted in 1893.

- <q></q>
    짤은 인용문을 정의 할 때 
    인용문의 내용이 길면 <blockquote></blockquote>를 사용하면됨!!! 
    사이트 + 인용되정보의 URL + URL

- <u></u>
    underline 의 약자! 
    순수하게 꾸미는 용도, 특별한 의미는 없음. CSS활용가능한 환경이라면 CSS를 활용!!! 
    a태그와 헷갈릴 수 있으니까 그럴 위치에선는 사용 주의 

- <code></code>
    컴퓨터 코드 범위를 설정
    
- <kbd></kbd>
    키보드의 약어로 키보드 키를 나타낼 때 사용
    예제
    <p>
        <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>K</kbd>
    </p>
    <kbd>ESC</kbd>
        kbd { 
            padding: 0 3px;
            border-radius: 3px;
            border-top: 2px solid rgb(240, 240, 240);
            border-bottom: 2px solid rgb(205, 205, 205);
            border-left: 2px solid rgb(240, 240, 240);
            border-right: 2px solid rgb(225, 225, 225);
        }

- <sup></sup> / <sub></sub>
    위첨자, 아래첨자 
    X<sup>4</sup> + Y<sup>2</sup>, H<sub>2</sub>O

- time
    날짜나 시간을 나타내기 위한 목적으로 사용
    datetime + 유효한 날짜 + 년월일(date)

- <span></span>
    div 태그와 유사 하나 div는 블록 요소 span 은 인라인 요소
    본질적으로 아무런 의미를 가지지 않는 컨텐츠 영역을 설정
    예제
    <body> 
        동해물과 <div>백두산</div>이 마르도 닳도록
        하느님이 보우하사 우리나라 만세
    </body>
    => 이경우에는 문단이 구분된다!! 

    <body> 
        동해물과 <span class="bord">백두산</span>이 마르도 닳도록
        하느님이 보우하사 우리나라 만세
    </body>

- <br/>
    줄바꿈을 설정
    예제
    동해물과 백두산이 마르도 닳도록 <br/>
    하느님이 보우하사 우리나라 만세

- <del></del>
    특정한 컨텐츠가 제거 된것을 나타낼때
    삭제된 텍스트의 범위를 지정
- <ins></ins>
    없었는데 추가된 태그

    => my favorite color is <del>blue</del> <ins>red</ins> !
    이러면 중앙 삭제선이나오고 추가된 부분에 밑줄 그어짐

- <img/>
    빈태그 
    src = 소스의 약어로 이미지를 삽입하기 위해 필수로 있어야함
    alt = 이미지의 대체 택스트!!!! 
    예시 
    <img src="./images/heropy.png" alt="HEROPY" width="333">
    사이즈는 가로든 세로든 한가지만 입력하면 그 값을 유지하면서 바뀜!!! 
    CSS를 통해서 이미지릐 크기를 조정 할 수 있어어!!! 
    img { 
        width: 666px;
    }
    이런식으로!!!! 

    srcset : 브라우저에게 제시할 이미지의 URL이나 웜본크기의 목록을 정의 , 이미지선택을 위한 목록 후보!! , 이미지의 경로와 사이즈를 적어 줘야지 적절한 이미지를 골라서 활용, 한장만 사용할 거면 src를 활용!!! 
            픽셀단위가 아니고 W, X단위를 사용해야 한다. 작은 사이즈의 이미지부터 순서 대로 작성 
            w는이미지의 가로너비, 즉 실제 가로 너비를 적으면 됭!!! 
    sizes : 미디어의 조건과 해당 조건일 때 이미지 최적롸 크기의 목록을 정의 ,  최적화된 조건의 이미지를 선택
    => 반응형 웹사이트를 작성할때 
    일반적으로 반응형 웹에서 이미지를 지원하기 위해, ‘미디어쿼리’라고 부르는 CSS Media Rule(@media)에서 background-image 속성을 많이 사용하는데, 
    반응형 이미지를 처리하기 위해 뷰포트(Viewport)의 크기부터 사용자 화면의 해상도 등 많은 환경을 고려해야 합니다.
    하지만 우리는 HTML IMG의 srcset과 sizes를 통해 쉽게는 이미지의 크기를 설정하는 것만으로 대부분의 고려 사항을 사용자 브라우저(User agent)에 떠넘길 수 있습니다.

    srcset 예시
    images/heropy_medium.png 700w,
    images/heropy_large.png 1000w"
    src="images/heropy.png"
    alt="HEROPY"/>
    
    sizes 예시 
    images/heropy_medium.png 700w,
    images/heropy_large.png 1000w"
    src="images/heropy.png"
    alt="HEROPY"/> 
    
    width : 일반 출력
    sizes : 최적화 출력 

    width 는 이미지의 출력크기만 지정하는데 반해, 
    sizes는 이미지의 출력 크기 + 최적 크기도 함께 지정하는 개념 


- <audio src=""></audio>
    오디오 태그
    autoplay : 준비 되면 바로 재생
    controls : 제어 버튼을 출력하기 위해 서 속성이 추가 되어야 한다. 
    loop : 재생이 끝나면 처음부터 다시 재생하는 
    preload : 페이지가 로드 될 때 파일을 로드할지를 지정, none 로드하지 않다 플레이가 되면 로드. metadata 메타 데이터만 로드(기본값), auto 전체파일 미리 로드 
    src : 오디오 태그의 경로 명시 
    muted : 음소거 여부 
    예시
    <audio src="https://interactive-examples.mdn.mozilla.net/media/cc0-audio/t-rex-roar.mp3" 
            controls 
            autoplay
            loop
            muted></audio>


- <video src=""></video>
    autoplay : 준비 되면 바로 재생
    controls : 제어 버튼을 출력하기 위해 서 속성이 추가 되어야 한다. 
    crossorign : 외부에서 콘첸츠를 가져올 때 동일한 출처인지 확인 할 것인가의 여부를 설정!!! 
    loop : 재생이 끝나면 처음부터 다시 재생하는 
    preload : 페이지가 로드 될 때 파일을 로드할지를 지정, none 로드하지 않다 플레이가 되면 로드. metadata 메타 데이터만 로드(기본값), auto 전체파일 미리 로드 
    src : 오디오 태그의 경로 명시 
    muted : 음소거 여부 
    poster : 동영상의 썸네일 이미지 URL 
    예시
    <video src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.webm"
    controls
    loop
    muted
    poster="./images/heropy.png"></video>

- <figure></figure> / <figcaption></figcaption>
    이미지나, 삽화 도표 등의 영역을 설정하고 
    피규어캐션으로 삽화등의 설명을 표시 한다 
    예제
    <figure>
        <img src="./images/heropy.png" alt="HEROPY">
        <figcaption>HEROPY 이미지 입니다!</figcaption>
        </figure>

    => 사용자 보다는 일반적으로 브라우저나, 검색엔진이나, 정보통신 보조기기들이 볼때 구조를 확인할 수 있다. 

- <iframe src="" frameborder="0"></iframe>
    다른 HTML 페이지를 현재 페이지에 삽입 하고 중첩된 브라우저 컨텍스트를 표시 한다. 
    브라우저를 통해서 해당하는 사이트를 볼수 있는데, 해당하는 페이지는 하나자나, 
    이럴때 이 안에 다른 페이지 사이트를 넣어서 활용 할 수 있어!!1
    유튜브나, 동영상 컨텐츠 페이지에 넣을 떄 사용 많이 해 !! 
    예제 
    <body>
        <p>우리 페이지야!</p>
        <div>
            <img src="./images/heropy.png" alt="HEROPY">
        </div>
        <div>
            <iframe src="http://google.com" 
            frameborder="0"
            width="70%"
            height="400px"
            style="border: 4px solid red;"></iframe>
        </div>
    </body>
    
    유튜브 링크 소스 긁어온거  예시 
    <iframe width="1235" height="677" src="https://www.youtube.com/embed/-Gv8HRJiKVc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    

        들어갈수  있는 거 
        name : 프렌임 이름
        src : 포합할 문서의 URL
        width : 가로 너비
        height : 세로 너비
        alllowfillscreen : 전체화면 모드 사용여부
        frameborder : 프레임 테두리 사용 여부 / 기본은 1인데 주로 0으로 설정을 많이 하는 편 
        sdanbox : 보안을 위한 읽기 전용으로 삽입. 
            alllow-form : 양식 제출 가능
            alllow-script : 스크립트 실행가능
            allow-same-origin : 같은 출처 리소스 사용 가능 

- <canvas></canvas>
    자바스크립트를 활용해서 canvas API,WebGL API를 사용하여 그래픽이나. 애니메이션을 랜더링

- <script></script>
    스크립트 태그 내부에 자바스크립트를 삽입하거나, 외부 슽크립트를 src라는 속성를 통해서 가져오기를 할때ㅔ 사용
    자바스크립트를 가져올때는 script, css 를 가져올때는 link라는 태그 
    스크립트 코드를 문서에 포함 하거나 외부스크립트를 참조 
    사용 가능하 속성
    async : 어씽크, 자바스크립트의 비동기적인 실행여부를 정하는 
            자바스크립트 코드가 순차적으로 실헹 되는 것이 동기적인 방식, 
            비동기적은 필요에 따라서 순서를 건너뛰거나, 돌아가거나 하는 것이 가능
            이러한 형식에서 비동기적 형식을 할지 여부를 어씽크를 통해서 결정 할 수 있다. 
    crossorigin :  
    defer : 문서파싱, 구문을 모두 먼저 분석한 후 작동시키는!!!!  / 실행시점을 제어 할 수 있다
            예제 
            <!DOCTYPE html>
            <html lang="ko">
            <head>
                <meta charset="UTF-8">
                <title>Document</title>
                <link rel="stylesheet" href="./main.css">
                <script src="./js/main.js"></script>
            </head>
            <body>
                <div id="my-name">HERORY!</div>
            </body> 
            </html>>
            의 경우, 위에서부터 문서를 읽으면서 실행이 되는데,
            스크립트가 네임내용보다 위에 있어서 해당 내용일 읽기 전에 실행이 됨!!! 
            그래서 오류가 남!!! 이럴경우에 바디태그 제일 하단에 입력하면 실행이 되나, 이것은 물리적으로 실행위치를 바꾼것.
            defer를 써주면 구문을 전부 분석한 후 작동 시키기 때문에 오류가 나지 않음!! 
            실무에서 두가지 방법 둘다 많이 사용 
            <!DOCTYPE html>
            <html lang="ko">
            <head>
                <meta charset="UTF-8">
                <title>Document</title>
                <link rel="stylesheet" href="./main.css">
                <script src="./js/main.js" defer></script>
            </head>
            <body>
                <div id="my-name">HERORY!</div>
            </body>
            </html> 
            => 요런식으로!!!! 

    src : 참조할 외부 스크립트의 URL을 사용!!!! 이경우 스크립트 내부의 작성 내용은 무시된다. 
    type : MIME 타입 , 텍스트 자바스크립트가 기본갑으로 작성하지 않아도 된다. 

- <noscript></noscript>
    자바스크립트를 지원하지 않는 경우!!!!  삽입할 HTML을 정의 


- <table></table>
    talble : 테이블 표를 만들때 사하는는 태그
            {display : table} => 블록 요소와 유사
    tr : 행과 줄 table row
            {dispaly : row}
    th : 열과 칸 . 제못느낌!! table header, 머릿글 칸을 지정
            abbr : 열에 대한 간단한 설명
            headers : 관련돤 하나 이상의 다른 머리글 칸 id 속성값, 다른 th 와 연결할 때 사용
            colspan : 표 병합, 열의 몇열, 몇칸 까지 병합할 것인가/ 수평
            rowspan : 표 병합, 행 병합, 줄을병합 / 수직
            scope : 자신이 누구의 머릿글 칸인지, 기본값은 aut 
    td : 열과 칸 일반적으로 사용 table data 
            {display : table-cell}

    예제
    <table>
        <tr>
            <th colspan="2" id="th-data">데이터</th>
        </tr>
        <tr>
            <th abbr="type" scope="col" headers="th-data">타입</th>
            <th abbr="value" scope="col" headers="th-data">값</th>
        </tr>
        <tr>
            <td>알파벳</td>
            <td>A</td>
        </tr>
        <tr>
            <td>숫자</td>
            <td>7</td>
        </tr>
    </table>

    예제2 
    <table>
        <tr>
            <th rowspan="2" id="th-data">데이터</th>
            <th headers="th-data">타입</th>
            <td>알파벳</td>
            <td>숫자</td>
        </tr>
        <tr>
            <th>값</th>
            <td>A</td>
            <td>7</td>
        </tr>
    </table>

- 표를 보조하는 역할의 태그 
<caption></caption>
    =>  표의 제목을 설정
    열리는 TABLE 태그 바로 다음에 작성해야함.
    table 당 하나의 caption 만 사용 가능, 제목이기때문에!!! 
    caption의 display-tablecaption

<colgroup></colgroup>
    => 표의 열들을 공통적으로 정의하는 컬럼 col과 그 집합 colgroup 
    col 태그는 caption 위에 적으면 안된다.
    수직방향으로 그룹이 지어져서 설정값이 들어감!!! 
    span 연속적으로 몇개의 colum까지 연결을 할것인가를 지정 하는 태그 
    예를 들어 span 2라면 두번째 열까지 설정값을 입히겠다는 뜻 

아래의 태그들은 기본적으로 레이아웃에는 영향을 주지 않는 태그들!!!! 
    <thead></thead>
        => 표의 머릿글
    <tbody></tbody>
        => 표의 본문
    <tfoot></tfoot>
        => 표의 바닥글

 

- 양식
<form></form>
    => 웹서버에 정보를 제출하기 위한 범위를 지정, form태그 안에 form 태그를 포함 할 수 없다. 

    action : 전송한 정보를 처리할 웹페이지의 URL, 입력받은 정보를 제출할때 form이라는 태그로 묵고, 어떤 페이지로 넘길지 그 페이지의 주소를 입력 
            <form action="/login">
                <input type="email" name="email">
                <input type="password" name="password">
                <button type="submit"> 로그인</button>
            </form>
            이런식으로 form태그 안의 내용이 로그인 이라는 버튼을 누르면 action="" 의 ""안의 주소로 전송 된다.

    autocomplete : 사용자가 이전에 입력한 값이 있다면, 자동완성을 통해서 사용자에게 제공 할 것인지 여부를 표시하는 속성, 기본 값은 on
    method : 우리가 정보를 서버로 전송할 때, 전송될 HTTP방식을 설정!! 대표적으로 GET과 POST 방식이 있는데 기본 값으로 GET 
    name : 우리가 서버로 정보를 제출할 때, 그 양식에 해당되는 이름을 설정해서 다른 이름과 구별되도록 할 수 있다. 
    novaildata : 서버로 데이터를 전송 할 때, 그 데이터가 우리가 사용자에게 강요한 특정한 양식이 맞는지 확인을 해야하는데, 그 양식을 검사하는 것이 '유효성검사'
    target : 서버로 전송후 응답 받을 방식을 설정, 현재 브라우저 탭에 띄울지, 새로운 탭에 띄울지를 결정 

<input/>
=> 기본적으로 text!!!! 
    autofocus : 페이지가 로드 될때에 자동으로 포커스
    checked : 양식이 선택되었음을 표시하는데 radio나, checkbox일때 사용 가능
    disabled :
    form : form태그 안이 아니라 바깥쪽에 데이터양식을 작성하게 될 경우, form의 id 값을 input의 form이라는 속성에 연결을 해주면 form태그 바깥에 양식을 작성했다 할 지라도 연결해서 사용 할 수 있다.
           ex)
            <form action="/login" id="login-form">
            
            </form>

            <input type="text" form="login-form">
    list : 
    max :
    min : 
    maxlength :
    muliple : 다중선택
    name : 양식의 이름
    type : 사용자에게 데이터를 입력받을 때 사용 되는 태그가 <input>인데, type은 어떤 종류의 데이터를 입력받을 것인가를 명시하는 속성  
            type에 입력하는 데이터값 종류
            botton : 일반 버튼, 특정한 기능이 없는 버튼
            checkbox : 체크박스 
            color : 색상 
            email : 이메일
            file : 파일
                => <input type="file">
                => 여러개 파일 사입 <input type="file" multiple>
            hidden : 보이지 않지만 전송할 양식 
            image : 이미지 제출 버튼
                     => <input type="image" src="images/heropy.png" alt="HEROPY">
                이미지를 제출 버튼으로 활용 
                    <form action="/login">
                        <input type="image" src="images/heropy.png" alt="HEROPY">
                    </form>
            number : 숫자
            password : 비밀
            radio : 라이도 버튼
                    여러개중 택 1을 하도록 하는 그런 환경을 만들때 
                    <input type="radio" name="radio1">
                    <input type="radio" name="radio1">
                    <input type="radio" name="radio1">
                    원하는 칸이 체크가 기본으로 되어있도록 하고 싶으면 원하는 칸순서에 checked를 달아주면 된다.
            range : 범위컨트롤
            reset : 초기화, 자기의 태그 안에 내용만 초기화!!
                    <form action="/login">
                        <input type="text" name="id">
                        <input type="password" name="pw">
                        <input type="submit" value="로그인">
                        <input type="reset" value="초기화">
                    </form>
                    <input type="text">
            search : 검색
            tel : 전화번호
            text : 일반 텍스트
            submit : 제출 버튼 
            url : 일반 URL

<label for=""></label>
    라벨, 버튼이나 인풋 등에 붙이는 캡션 등 
    예제
    <input type="checkbox" id="user-agreement" />
    <label for="user-agreement">동의하십니까?</label>
                    혹은
    <label><input type="checkbox" /> 동의하십니까? </label>

        => for는 참조할 라벨가능요소를 id에 적어서 사용 

<button></button>
    일반 버튼은 타입을 지정해주지 않아도 된다. 
    예제
    <button onclick="doit()">클릭하세요</button>

    <script>
        function doit() {
            alert('클릭했습니다!');
        }
    </script>

<textarea></textarea>
    => 여러줄의 일반 텍스트 양식 
    rows : 화면에 보이는 줄의 수 
    placeholder : 사용자가 입력한 값의힌트, ex 설명을 입력하시오. 등 내용 예시 

<fieldset></fieldset> / <legend></legend>
    => 같은 목적의 양식을 그룹화 하여 제목을 지정
    예제
    <form>
        <fieldset>
            <legend>Coffee Size</legend>
            <label>
                <input type="radio" name="size" value="tall" />
                Tall
            </label>
            <label>
                <input type="radio" name="size" value="grande" />
                Grande
            </label>
            <label>
                <input type="radio" name="size" value="venti" />
                Venti
            </label>
        </fieldset>
    </form>

<select></select> / datalist / <optgroup></optgroup> / <option ></option>
    => 옵션(<option>, <optgroup>)의 선택 메뉴(<select>)나 자동완성(<datalist>)을 제공.
        
        selct 예시
        <select name="fruits" size="3" multiple disabled>
            <option>Apple</option>
            <option>Orange</option>
            <option>Banana</option>
            <option>Mango</option>
            <option>Fineapple</option>
        </select>

        option, optgroup ㅇㅖ시
        <select name="fruits">
            <optgroup label="내가 좋아하는 과일">
                <option>Apple</option>
                <option>Orange</option>
                <option>Banana</option>
            </optgroup>
            <optgroup label="내가 싫어하는 과일">
                <option>Mango</option>
                <option>Fineapple</option>
            </optgroup>
        </select>

        datalist ㅇㅖ시
        <input type="text" list="fruits">

        <datalist id="fruits">
            <option>Apple</option>
            <option>Orange</option>
            <option>Banana</option>
            <option>Mango</option>
            <option>Fineapple</option>
        </datalist>
        =>리스트 값과 id값이 동일 해야한다.

progress
    => 작업의 완료 진행률을 표시 
    예시
    <progress value="70" max="100">70%</progress>
    max를 사용하지 않으면 0~1사이의 값으로 표현해야한다. 0.7 이런식으로 


전역속성, 기타 속성
class 는 중복이 가능, id는 중복 불가 하나의 고유한 요소 
    css에서 .을 찍는것이 class를 찾는거고 id는 #을 통해서 찾는다. 
    자바스크립트에서도 class는 .을 통해서 검색, id는 id값을 입력해서 검색 
style 요소에 적용할 CSS를 선언
title 마우스를 가져다 댔을때 나오는 작은 설명들, 요소의 특정한 정보나 설명 
lang 요소의 언어를 설정 
data 사용자의 데이터 속성을 지정 / data-0000-0000="000" => HTML에서 보관하다가 자바스크립트에서 사용 
draggable 요소가 drag, drop 이 가능하는 한지 여부를 지정 true or fals로 표현 안지정하면 auto=브라우저에서 맞추어 판단 
hidden 요소를 숨김.  
tabindex 탭키를 눌러 이동되는 순서를 정할 수 있음 / 일반적으로 1이상의값은 사용을 지양하기 권유 순서가 짜여진 대로 순차적으로 가는 것이 좋음. -1의 음수 값을 통해서 탭에서 제외 가능하고 , tabindex=0을 통해서 탭 이동이 가능하도록 만들 수 있다. 
상대경로 ./:주변에서 검색하며 생략이 가능하다 , ../:폴더 밖으로 나가서 검색!  절대경로 http, / 
주석처리 : cmd + /  하면 주석 처리 됨 
자바스크립트 주석처리 : cmd + / 주석처리됨, */ 이거나 // 이렇게 표시됨 
띄어쓰기 : &nbsp; 띄어쓰기 한칸  
코드용어를 화면에 출력하고싶을때 : &lt; 열리는 꺽쇠 괄호 , &gt; 닫히는 꺽쇠 괄호 



css

@import : css에서 css를 가져오는!!
          import를 통해서 호출하는 것은. 1을 부르고 도착하면 2를 부르고 도착하면 3을 부르고 이런식으로 작렬방식으로 호출 한다. 

-선택자 
 전체 선택자 : 요소 내부의 모든 요소를 선택 * 표시를 사용해서 표현 
 태그 선택자 : 태그를 선택해서, 태그이름이 000인 요소를 선택
 클래스 선택자 : 태그앞에 .을 찍어서 표시 
 id선택자 : HTML에 ID라는 속성이 있고 이것은 #을 붙여서 표현, 

 -복합선택자
 일치선택자, 선택자 a와 c를 동시에 만족하는 요소를 선택!!!! 
    ex) span.orange : 태그선택자와 클래스선택자가 붙어있는 형태, 이러한 것을 일치 선택자라고 함!! 
    span태그이면서 orange 라는 클래스를 가진 것이여야 함. 
 자식선택자 : c자식의 요서 d를 선텍!! 
    ex) ul> .orange ul의 자식 요소 중에서 .orang의 클래스의 값을 가지고 있는 부분, 자식선택자에서 앞은 조건이고 뒤가 검색!! 
 후손(하위)선택자 x의 후손요소 s를 선택, 띄어쓰기가 선택자의 기호로 사용 됨
    ex) div .orange  div 태그와 .orange 라는 클래스, 띄어씌기가 있으니까 이것은 후손 선택자, 후손선택자는 div태그 범위안에있는 모든 요소를 이야기 
        first-child , last-child, nth-child(n) 
        첫번째, 마지막, n번째 

 인접 형제 선택자 c의 다음 형제 요소 f하나만 선택
    ex) .orange + li : 인접해 있는 형제 요소를 찾는 다. li class="orange" 라는거 바로 다음에 있는 것을 선탣함!!! 
 일반 형제 선택자 : c라는 다음 형제 요소 f모두!! 
    ex) .orange ~ li : .orange 라는 클래스의 "다음"에 있는 모든 요소  

-가상클래스 선택자 
기본선택자에 붙여서 사용 :기호를 사용해서 가상클래스 선태자를 사용한다. ::이렇게 두개 이으명 가상요소
    ex)1. hover : 특정한 곳에 마우스 포인터가 올라가있는 동안에만 해당부분을 선택
                a:hover { 00000000 }
        2. active : 마우스로 클릭하는 동안에먼 해당부분을 선택 
                a:active 
        3. focus : 대화형 콘텐츠(input, img, tabindex) 에서 해당부분이 포커스 된 동안에만 해당부분을 선택  
    
    
    
    
    

