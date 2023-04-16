## 코딩초보의 html 공부
### HTML은 처음 작성할때
~~~HTML
<!DOCTYPE html>
~~~
> 으로 시작한다고 한다. ~처음 배우고 겉만 핥다가 때려치웠던 C보다는 직관적으로 보여서 좋았다.~
### HTML의 기본적인 구조
~~~HTML
<!DOCTYPE html>
<html lang="ko"> <!-- 한국어를 주언어로 사용하는 경우의 html 태그-->
  <head>
  </head>
  <body>
  </body>
</html>
~~~
> \<head>에는 언어설정이나 화면에 주로 보이지 않는 것들을 담당하고, <br>
\<body>에는 시각적요소들을 기입한다고한다.

*** 

## HEAD 부분
~~~HTML
<html lang="ko">
~~~
> 한국어를 주언어로 사용하는 경우의 html태그이다.
~~~HTML
<meta charset="utf-8">
~~~
> 언어가 깨지지 않도록 HTML파일의 인코딩을 알려주는 태그이다. <br>
> 안하면 문자가 깨진다고 하니 꼭 써야함
> 바로 위의 것과의 차이점은 번역기, 스크린리더 등을 사용할때와 <br>
> 실제 언어를 쓸때 사용 한다는 점이다.
~~~HTML
<meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript, 의류쇼핑몰, 만들고싶다, 노래방">
~~~
> SEO(검색엔진 최적화)기능을 활용하고 싶을때 이렇게 키워드를 지정해놓으면 검색엔진에 쉽게 관련 키워드로 노출될 수 있다. <br>
> ~~키워드는 뇌비우고 막 넣은거니 무시좀..~~
~~~HTML
<meta name="description" content="프론트엔드 뉴비가 만들었어요 응애">
~~~
> description 라는 뜻 그대로 웹페이지 설명을 정의하는 태그다.
~~~HTML
<meta name="author" content="김진모">
~~~
> author 라는 뜻 그대로 웹페이지의 저자를 정의하는 태그다.
~~~HTML
<meta http-equiv="refresh" content="5">
~~~
> http-equiv 속성은 http 헤더에 정보값을 제공하는 콘텐트 속성임. <br>
> http 헤더에 refresh(새로고침)이라는 정보를 content에 제공하는데 그 값이 5초라는 뜻.
~~~HTML
<title>Hello World</title>
~~~
> 웹페이지 상단 탭창에 보이는 타이틀 문구를 설정하는 태그.
~~~HTML
<link rel="stylesheet" href="style.css">
~~~
> link요소는 외부 리소스와 연계. 주로 css파일을 연동하는데 쓰임. <br>
> html에 직접 작성하는 방법도 있는데,
~~~HTML
<style>
            body {
                background-color: green;
                color: white;
            }
        </style>
~~~
> \<style> 태그를 활용하여 직접 넣을 수 도 있다. 하지만, 코드가 지저분해지기 때문에 <br>
> link로 밖에서 직접 끌어와 쓰는 방법이 더 깔끔하다.
~~~HTML
        <script>
            document.addEventListener('click', function () {
                alert('Clicked!');
            });
        </script>
~~~
> 자바스크립트를 HTML에 직접 삽입하는 태그는 \<script>
~~~HTML
<script src="main.js"></script>
~~~
> link와 마찬가지로 외부에서 자바스크립트 파일을 로드하고싶을 때. \src="~.js"를 추가.

***

## BODY 부분
~~~HTML
<h1>Hello World</h1>
~~~
> 제목(Headings)태그는 1-6까지 있으며 h1은 가장 중요한 제목을 의미. <br>
> 시맨틱 웹의 의미를 살려서 제목 이외에는 사용하지 않는 것이 좋음.

~~~HTML
<p>안녕하세요! HTML5</p> <!-- <p>는 단락을 의미함 태그를 붙일때마다 2줄 띄워서 표현됨 --> 

<font size="6"><b>코딩은 어려워</b></font> <!-- 폰트 사이즈를 조정하는 태그와 <b>는 볼드체 태그 -->

<em>강조, 중요한 텍스트 지정. 이텔릭체로 표기됨 시맨틱 요소로서 활용.</em>

<h2>그냥 텍스트<mark>하이라이티드 텍스트</mark>그냥 텍스트</h2>
<!-- 태그 안에 사용할 수 있는 <mark>태그는 하이라이트를 표현하고 싶을때 사용 -->

<i>이탤릭체</i>

<h1 id="top">This is a heading. also top of page!</h1>
<!-- 하단의 부분식별자 태그로 특정 부분으로 이동하려고 미리 id를 지정해놓음.
id는 중복지정이 불가함. -->

<hr> <!--수평줄 삽입 태그-->

&nbsp;et dolore magna aliqua. <!-- &nbsp; 는 문장안에 스페이스를 넣고싶을 때 사용. 근데 뉴비 시점에선 굳이 필요한가 싶긴함.. -->

<img src="model1.jpg" width="1000" height="1000"> <!--이미지 삽입 태그-->

<a href="http://weever.kr">Visit weever.kr!</a> <!--a태그. a는 앵커의 약자로 앵커는 html에서 웹 하이퍼링크의 출발지와 도착지. -->

~~~
## BODY 부분2
~~~html
        <!--rel="noopener noreferrer"는 tabnabbing 피싱공격 방지-->
        <a href="http://weever.kr" target="_blank" rel="noopener noreferrer">절대 URL http://weever.kr _blank 타겟 어트리뷰트로 새로운 창에서 페이지를 열기.</a><br>
~~~
> \<a href="">로 링크를 연결하고 target="\_blank"는 새로운 창에서 페이지를 연다는 뜻.
> \rel="noopener noreferrer"은 피싱공격 방지를 해준다던데 뉴비입장에선 아직 원리를 잘 모르겠다.

~~~html
<a href="html/Hello World.html">상대 URL 자신 위치 기준 대상 URL html/Hello World.html</a><br>
~~~
> 상대 URL은 자신의 위치를 기준으로한 대상URL이라고 한다. 깃허브로는 어떻게 경로를 연결해야할지 아직 잘모르겠다. 물어봐야지.

~~~html
<a href="file/model.jpg" download>파일 다운로드</a><br>
~~~
> 다운로드 경로를 연결해줌. 이것도 마찬가지로 딱히 떠오르는 다운로드 링크가 없어서 본인의 리포지토리에 같이 올린 <br>
> 이미지파일을 다운로드 하게끔 하고싶었는데 깃허브는 경로설정을 잘 모르겠다.

~~~html
<a href="#top">fragment identifier(부분 식별자) 웹 페이지 안에서 특정 부분으로 이동하고 싶을 때 이용.</a>
~~~
> 아까 \<h1 id="top">This is a heading. also top of page!</h1> 이 부분에 id 식별자를 통하여 id를 top으로 미리 지정을 해놓았고, <br>
> 앵커태그로 지정한 id로 이동하게끔 연결했다.

오늘 공부는 여기까지!
