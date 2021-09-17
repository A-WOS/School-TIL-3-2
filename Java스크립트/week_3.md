## Java스크립트 3주차 

> google fonts를 import    
> > [google fonts](https://fonts.google.com/)    
> > 해당 url을 들어가서 아래 이미지의 빨간색으로 '[' 해놓은 부분들을 복사하여 붙여넣기 한다.
<img src="https://user-images.githubusercontent.com/71562490/133732526-bd5ea529-b42b-40e4-b2f9-683f8f8cb7f6.jpg" width="70%" height="65%">

> > 아래의 소스코드와 같이 해당 웹 폰트들을 import하여 p태그에 적용하여 사용할 수 있다.   
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
> > 유의사항은 폰트에 따라서 한글 지원이 안되는 폰트들은 깨질 수도 있기 때문에 꼭 아래와 같이 써줘야 한다.
```
p { font-family: '쓰고 싶은 폰트', 기본적인 폰트;} 
```
-----------------
