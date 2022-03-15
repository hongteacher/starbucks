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
```plaintext
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
```plaintext
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

## gsap을 이용해 애니메이션 효과주기
GSAP(The GreenSock Animation Platform)은 자바스크립트로 제어하는 타임라인 기반의 애니메이션 라이브러리입니다. ScrollToPlugin은 스크롤 애니메이션을 지원하는 GSAP 플러그인입니다.
[https://cdnjs.com/libraries/gsap](https://cdnjs.com/libraries/gsap)
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.5.1/gsap.min.js" integrity="sha512-IQLehpLoVS4fNzl7IfH8Iowfm5+RiMGtHykgZJl9AWMgqx0AmJ6cRWcB+GaGVtIsnC4voMfm8f2vwtY+6oPjpQ==" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.5.1/ScrollToPlugin.min.js" integrity="sha512-nTHzMQK7lwWt8nL4KF6DhwLHluv6dVq/hNnj2PBN0xMl2KaMm1PM02csx57mmToPAodHmPsipoERRNn4pG7f+Q==" crossorigin="anonymous"></script>
```

## Youtube API
IFrame Player API를 통해 YouTube 동영상을 제어할 수 있습니다.    

유튜브 영상이 출력될 위치에 요소를 지정(생성)합니다.    
```html
<!-- in HEAD -->
<script defer src="./js/youtube.js"></script>

<!-- in BODY -->
<div id="player"></div>
```
onYouTubePlayerAPIReady 함수 이름은 Youtube IFrame Player API에서 사용하는 이름이기 때문에 다르게 지정하면 동작하지 않습니다!   
그리고 함수는 전역(Global) 등록해야 합니다!   

플레이어 매개변수(playerVars)에서 더 많은 옵션을 확인할 수 있습니다.   
```javascript
// Youtube IFrame API를 비동기로 로드합니다.
var tag = document.createElement('script');
tag.src = "https://www.youtube.com/iframe_api";
var firstScriptTag = document.getElementsByTagName('script')[0];
firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);

function onYouTubePlayerAPIReady() {
  // <div id="player"></div>
  new YT.Player('player', {
    videoId: 'An6LvWQuj_8', // 재생할 유튜브 영상 ID
    playerVars: {
      autoplay: true, // 자동 재생 유무
      loop: true, // 반복 재생 유무
      playlist: 'An6LvWQuj_8' // 반복 재생할 유튜브 영상 ID 목록
    },
    events: {
      // 영상이 준비되었을 때,
      onReady: function (event) {
        event.target.mute(); // 음소거!
      }
    }
  });
}
```

## 랜덤한 숫자를 생성하는 함수
```javascript
// 범위 랜덤 함수(소수점 2자리까지)
function random(min, max) {
  // `.toFixed()`를 통해 반환된 문자 데이터를,
  // `parseFloat()`을 통해 소수점을 가지는 숫자 데이터로 변환
  return parseFloat((Math.random() * (max - min) + min).toFixed(2))
}
```

## ScrollMagic
ScrollMagic은 스크롤과 요소의 상호 작용을 위한 자바스크립트 라이브러리입니다.   
대표적으로 어떤 요소가 현재 화면에 보이는 상태인지를 확인할 때 사용합니다.   
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.8/ScrollMagic.min.js"></script>
```
```javascript
new ScrollMagic
  .Scene({ // 감시할 장면(Scene)을 추가
    triggerElement: spyEl, // 보여짐 여부를 감시할 요소를 지정
    triggerHook: .8 // 화면의 80% 지점에서 보여짐 여부 감시
  })
  .setClassToggle(spyEl, 'show') // 요소가 화면에 보이면 show 클래스 추가
  .addTo(new ScrollMagic.Controller()) // 컨트롤러에 장면을 할당(필수!)
  ```
  
  ## Swiper Slider
  > css
  ```html
<link rel="stylesheet" href="https://unpkg.com/swiper@8/swiper-bundle.min.css" />
<script src="https://unpkg.com/swiper@8/swiper-bundle.min.js"></script>
```
>html
```html
<!-- Slider main container -->
<div class="swiper">
  <!-- Additional required wrapper -->
  <div class="swiper-wrapper">
    <!-- Slides -->
    <div class="swiper-slide">Slide 1</div>
    <div class="swiper-slide">Slide 2</div>
    <div class="swiper-slide">Slide 3</div>
    ...
  </div>
  <!-- If we need pagination -->
  <div class="swiper-pagination"></div>

  <!-- If we need navigation buttons -->
  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>

  <!-- If we need scrollbar -->
  <div class="swiper-scrollbar"></div>
</div>
```

> swiper option
```javascript
new Swiper('변경 .swiper', {
    direction: 'horizontal', //방향
    loop: true, //무한반복
    autoplay : true, //자동시작
    slidesPerView: 5, //한 번에 보여지는 슬라이드 개수
    spaceBetween: 30, //슬라이드와 슬라이드 간격
    navigation : {
        prevEl : "변경 .swiper-prev",
        nextEl : "변경 .swiper-next"
    },
});
```


