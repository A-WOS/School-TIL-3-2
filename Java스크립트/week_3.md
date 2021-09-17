# Java스크립트 3주차 

### google fonts를 import    
> [google fonts](https://fonts.google.com/)    
> 해당 url을 들어가서 아래 이미지의 빨간색으로 '[' 해놓은 부분들을 복사하여 붙여넣기 한다.
<img src="https://user-images.githubusercontent.com/71562490/133732526-bd5ea529-b42b-40e4-b2f9-683f8f8cb7f6.jpg" width="70%" height="65%">

> 아래의 소스코드와 같이 해당 웹 폰트들을 import하여 p태그에 적용하여 사용할 수 있다.   
```
@import url(해당 폰트의 url)
적용시키고자 하는 태그(p) {복사해온 font;}
```
```
<!DOCTYPE html>
<html>
    <head>
        <title>
            Web Font Test
        </title>
        <style>
        @import url('https://fonts.googleapis.com/css2?family=Abel&family=Are+You+Serious&display=swap');
        p {font-family: 'Abel', sans-serif; font-family: 'Are You Serious', cursive;}
        </style>
    </head>
    <body>
        <p>안녕하세요. I love you!</p>
    </body>
</html>
```
> 유의사항은 폰트에 따라서 한글 지원이 안되는 폰트들은 깨질 수도 있기 때문에 꼭 아래와 같이 써줘야 한다.
```
p { font-family: '쓰고 싶은 폰트', 기본적인 폰트;} 
```
-----------------
### 의사 클래스
> a:link -> <a>태그에 클래스 link가 선언된 것처럼 생각하고 선택자를 만드는 것
```
a:link -> 링크 걸린 글자색이나 글자 모양을 변형
a:visited -> 마우스 클릭 후 글자색이나 글자 모양을 변형
a:hover -> 마우스를 링크에 가져다 댔을 때(올렸을 때) 글자색이나 글자 모양을 변형
a:active -> 마우스 클릭한 순간에 글자색이나 글자 모양을 변형
```
> > 아래의 코드와 같이 선택자에 옵션을 주면 글자색을 바꾸거나 글자 모양을 바꿀 수 있다.
```
<!DOCTYPE html>
<html>
    <head>
    <style>
        a:link {color:red;}
        a:visited {color:green;}
        a:hover {color: blue;}
        a:active {color: yellow;}
    </style>
    </head>
    <body>
        <p><a href="https://wwww.google.co.kr" target="_blank">google</a></p>
    </body>
</html>    
```
-----------------
### 스타일 시트의 적용 규칙
	1. 웹 브라우저의 디폴트 값
    2. 외부 스타일 시트
    3. 헤드 섹션에 저장된 내부 스타일 시트
    4. 인라인 스타일 시트
-----------------
### 많이 사용되는 속성들
    color : 텍스트 색상
    
    font-size : 폰트의 크기
    font-weight : 볼드체 설정
    font-style : 폰트 스타일 설정
    
    text-align : 텍스트 정렬
    text-decoration : 텍스트 밑줄
    
    padding : 요소의 가장자리와 내용 간의 간격
    
    background-color : 배경색
    background-image : 배경 이미지
    
    border : 요소를 감싸는 경계선
    
    list-style : 리스트 스타일
-----------------    
### 폰트 속성
    font-family : 폰트 패밀리 설정(font-family:"Times New Roman", Times, serif)
    font-size : 폰트 크기 설정(px, %, em)
    font-style : 폰트 스타일 설정(italic)
    font-weight : 폰트의 볼드체 여부 설정(normal)

### ※주의 사항※
    font-family 속성을 설정할 때는 여러 개의 폰트 이름을 제공하는 것이 좋다.
    브라우저가 HTML 파일을 표시할 때, 클라이언트 컴퓨터에 지정된 폰트가 없는 경우도 있기 때문.
    브라우저는 첫 번째 폰트가 없으면 자동적으로 다음 폰트를 불러온다.
    폰트를 나열할 때 첫 번째 폰트는 개발자가 가장 원하는 폰트, 
    맨마지막에는 가장 일반적인 폰트를 지정.
    만약 폰트 이름이 여러 단어로 되어 있다면 큰 따옴표를 사용하여 묶어야 한다.
위의 코드에서 보면 제일 선호하는 폰트는 Times New Roman 폰트이고 일반적인 폰트는 serif이다.
```
body {
    font-family:"Times New Roman", Times, serif;
}
```    
-----------------
### 텍스트 스타일 속성
    text-align : 텍스트의 수평 정렬을 지정(center)
    text-decoration : 텍스트 장식을 지정(underline)
    text-shadow : 그림자 효과를 지정(3px 3px 5px #넣고싶은 그림자 색)
    line-height : 텍스트 줄의 높이 간격(%)

	
