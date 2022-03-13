## Favicon(파비콘, favorites icon)   
웹페이지를 나타내는 아이콘, 웹페이지의 로고를 설정합니다.  
대부분의 경우 루트 경로에 `favicon.ico` 파일을 위치하면 자동으로  
로딩하기 때문에 `<link />` 를 작성할 필요가 없습니다.  
`favicon.png` 파일을 사용하려면 다음과 같이 `<link />`를 작성하세요.  
  
```html
<link rel="shortcut icon" href="favicon.ico" /> 
<link rel="icon" href="./favicon.png" />
```
favicon.ico 64 x 64 (px) 또는 32 x 32 또는 16 x 16  
favicon.png 500 x 500 (px)  

## Reset.css   
각 브라우저의 기본 스타일을 초기화합니다.   
[jsdelivr이동](https://www.jsdelivr.com/package/npm/the-new-css-reset)
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reset-css@5.0.1/reset.min.css" />
```

## 오픈 그래프(The Open Graph protocol)  
웹페이지가 소셜 미디어(페이스북 등)로 공유될 때 우선적으로 활용되는 정보를 지정합니다.      
[더 많은 오픈그래프 속성 보기](https://ogp.me/)   
```
og:type: 페이지의 유형(E.g, website, video.movie)
og:site_name: 속한 사이트의 이름
og:title: 페이지의 이름(제목)
og:description: 페이지의 간단한 설명
og:image: 페이지의 대표 이미지 주소(URL)
og:url: 페이지 주소(URL)
```
## 트위터 카드(Twitter Cards)   
웹페이지가 소셜 미디어(트위터)로 공유될 때 우선적으로 활용되는 정보를 지정합니다.
[더 많은 트위터 카드 보기](https://developer.twitter.com/en/docs/twitter-for-websites/cards/guides/getting-started)
```
twitter:card: 페이지(카드)의 유형(E.g. summary, player)
twitter:site: 속한 사이트의 이름
twitter:title: 페이지의 이름(제목)
twitter:description: 페이지의 간단한 설명
twitter:image: 페이지의 대표 이미지 주소(URL)
twitter:url: 페이지 주소(URL)
```

## SEO (검색 엔진 최적화, Search Engine Optimization)
구글이나 네이버 등에 자신의 웹 사이트/페이지를 노출 할 수 있도록 정보를 최적화하는 작업을 말한다.   
```html
<meta property="og:image" content="./images/starbucks_seo.jpg" />
<meta property="twitter:image" content="./images/starbucks_seo.jpg" />
```
## Google Fonts
페이지에서 사용할 '나눔고딕' 폰트를 지정합니다.   
```html
<link rel="preconnect" href="https://fonts.gstatic.com" />
<link href="https://fonts.googleapis.com/css2?family=Nanum+Gothic:wght@400;700&display=swap" rel="stylesheet" />
```
main.css보다 먼저 읽혀 들어갈 수 있도록 위에다가 선언한다.   

## Google Material Icons
main.css보다 먼저 읽혀 들어갈 수 있도록 위에다가 선언한다.
```html
<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons" />
```  
사용할 부분에는 다음과 같이 사용한다.

```html
<div class="material-icons">upload</div>
```
## HTML 클래스 속성의 작명법 BEM (Block Element Modifier)
`요소__일부분` Underscore(Lodash) 기호로 요소의 일부분을 표시   
`요소--상태` Hyphen(Dash) 기호로 요소의 상태를 표시

## lodash를 활용하여 scroll함수 제어하기
scroll이벤트가 계속 실행되면 사이트가 무거워 질 수 있으므로 이런 부분을 제어 할 수 있는 플러그인이 lodash를 설치하여 보자.
[https://cdnjs.com/libraries/lodash.js](https://cdnjs.com/libraries/lodash.js)




