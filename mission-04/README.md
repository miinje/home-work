# Mission-04
grid를 활용한 새소식 게시판 만들기

### 조건
1. grid 실습을 위한 과제 파일은 mission-04/grid.html 파일과 mission-04/grid.css 파일을 생성 후 각각 마크업과 스타일을 작성
2. 더보기 링크 앞에 플러스 기호는 생략해도 무방
3. 이미지는 “W3C 리뉴얼”이라는 캡션 위에 썸네일 이미지를 사용(해당 이미지는 배경으로 지정하지 말고 <img> 요소를 사용하여 콘텐츠 이미지로 배치)
4. grid를 활용하여 레이아웃을 구현
5. mission-04/README.md 파일을 생성한 후 마크업 코드와 CSS 코드에 대한 설명을 적고 아래 이미지와 같이 완성된 UI 스크린샷을 삽입


### Stacks 🐈
<div>
  <img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
  <img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white">
</div>


## 마크업
```html
<div class="grid">
        <h2 class="grid-Title">새소식</h2>
        <span class="grid-Add">더보기</span>

    <figure class="grid-news">
      <img src="./images/news 1.png" alt="Grid news" class="gird-Img" />
      <figcaption class="grid-caption">W3C 리뉴얼</figcaption>
    </figure>

    <div class="grid-ttDate">
      <span class="grid-subTitle">W3C 사이트가 리뉴얼 되었습니다.</span>
      <span class="grid-date">2022.07.18</span>
    </div>
    <span class="grid-txt">디자인 및 다양한 view 환경을 고려하여 구성되어 있으며,
      기존보다 최신 정보 및 개발자를 위한 기술 가이드도 찾기 쉽도록 구성되어 있습니다.</span>
  </div>
```
- 기본 마크업 구조 레이아웃 작업

기본적은 구조를 잡아 두고 폰트와 같은 기본 스타일, 그리드, 그라디언트 등이 필요한 요소에 클래스를 주었습니다.

뉴스 사진은 Background가 아닌 `<img>` 태그를 사용했고 피규어로 묶고 피그캡션을 활용했습니다. 

## 스타일
```css
@import url(./../base-css/css-reset.css);
```
- css 초기 스타일 제거

본격적으로 css를 넣기 전에 요소의 초기 스타일을 제거하기 위해 css-reset.css를 연결하여 초기화시켰습니다.


```css
.grid-caption,
.grid-Add,
.grid-date,
.grid-txt {
  font-weight: 400;
  font-size: 14px;
  line-height: 150%;
}

.grid-Title,
.grid-subTitle {
  font-weight: 700;
  font-size: 14px;
  line-height: 150%;
}

.gird-Img {
  margin-bottom: 15px;
  width: 112px;
  height: 66px;
  box-shadow: 0px 15px 15px 5px #AAAAAA;
}

.grid-caption {
  text-align: center;
}

.grid-txt {
  text-align: justify;
}
```
- 기본 스타일 적용

텍스트의 크기, 폰트 등을 적용시키고 그외의 꾸밈 요소를 넣어 시안과 비슷하게 적용시켰습니다.

```css
.grid {
  margin: 20px; 
  display: grid;
  gap: 10px;
  max-width: 380px;
  margin-left: auto;
  margin-right: auto;
  grid-template-columns: repeat(6, 1fr);
  grid-template-rows: auto;
}

.grid-Title {
  grid-area: 1/ 1/ 2/ 2;
}

.grid-Add {
  grid-area: 1/ 6/ 2/ 7;
}

.grid-news {
  grid-area: 3/ 1/ 5/ 2;
}

.grid-ttDate {
  grid-area: 3/ 2/ 7/ 6;
}

.grid-txt {
  grid-area: 4/ 2/ 8/ 7;
}
```
- 그리드 적용

시안과 비슷한 구조를 만들기 위해 그리드를 활용했습니다. 

새소식(.grid-Title), 더보기(.grid-Add), 사진과 캡션(.grid-news), 소제목과 날짜(.grid-ttDate), 뉴스 내용(.grid-txt)으로 구분지었고 각각의 위치에 맞는 grid-area 값을 넣었습니다.

```css
.grid-Title {
  padding-bottom: 15px;
  border-bottom: 1px solid; 
  border-image:linear-gradient(09deg, #a9a9a9 0%, white 60%); 
  border-image-slice: 1;
}
```
- 그라디언트 border

새소식이라는 글자 밑쪽으로 그라디언트를 입힌 선이 지나가게 하기 위해 border 요소들을 주었습니다



---
### 결과물
![결과](./images/스크린샷%202023-06-13%20오후%2011.24.26.png)