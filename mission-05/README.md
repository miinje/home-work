# Mission-05
sprite 이미지를 활용한 인기 사이트 리스트 만들기

### 조건
1. 더보기 링크 앞에 플러스 기호는 생략해도 무방
2. rank.png(webcafe-RWD/assets 폴더에 있음) 이미지를 활용하여 스프라이트 기법으로 스타일링
3. 각 인기 사이트의 순위를 나타내는 영역은 기존 <ol> 요소에서 제공하는 기본 숫자를 보이지 않도록 한 후 CSS로 구현
4. 목록에 마우스를 올리면 5개의 목록이 펼쳐지도록 구현

### Stacks 🐈
<div>
  <img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
  <img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white">
</div>


## 마크업
```html
<div class="famous">
  <h2 class="famous__title">
    인기 <span class="famous__titleRed">사이트</span>
  </h2>
  <ol class="famous__list">
    <li class="famous__item sprite sprite__W3C">
      <a href="/" class="famous__link">W3C</a>
    </li>
    <li class="famous__item sprite sprite__Standards">
      <a href="/" class="famous__link">Web Standards</a>
    </li>
    <li class="famous__item sprite sprite__CSS">
      <a href="/" class="famous__link">CSS ZenGarden</a>
    </li>
    <li class="famous__item sprite sprite__MDN">
      <a href="/" class="famous__link">MDN</a>
    </li>
  </ol>
  <a href="/" class="famous__more">더보기</a>
</div>
```
- 기본 마크업

마크업 순서는 인기 사이트-리스트-더보기 순으로 진행했다. 

사이트는 `<h2>` 태그를 사용했고 리스트는 조건대로 `<ol>` 사용하고 그 안에 앵커 태그를 넣었다.

더보기 또한 눌렸을 때 인기 사이트 목록으로 이동해야 하기 때문에 앵커 태그를 사용했다.
<br>

- 클래스 지정

꾸밈 요소가 들어가는 태그에 줬다. 전체에 *famous* 클래스를 주고 순서대로 *title, list, item, more*로 줬다.

클래스 네이밍은 BEM 방식을 사용했다. 

스프라이트 이미지를 사용해야 하는 `<li>` 태그에는 *sprite* 클래스를 추가로 주었다.

## 스타일
```css
@import url(./../base-css/css-reset.css);
```
- css 에이전트 스타일 리셋

본격적으로 스타일에 들어가기 전에 모든 요소의 에이전트 스타일을 삭제하는 css 파일을 연결시켰다.

```css
.famous {
  margin: 20px;
  width: 190px;
  height: 147px;
  background: linear-gradient(180deg, #CCCCCC 0%, #EEEEEE 100%);
  border: 1px solid #A3A3A3;
  border-radius: 5px;
  padding: 13px;
  position: relative;
}
```
- .famous 스타일 적용
  
가장 먼저 `<div>` 태그의 스타일을 만들었다. 배경에 그라디언트와 보더, 보더 레디우스를 넣어 모양을 잡았다.

안쪽에 *padding*을 줘 요소가 들어갈 위치를 정했다. *margin*은 요소가 모서리에 너무 붙지 않게 하기 위해 넣었다.

```css
.famous__title {
  font-size: 15px;
  font-weight: 700;
  line-height: 150%;
  color: #181818;
}

.famous__titleRed {
  color: #ED552F;
}
```
- .title 스타일 적용

타이틀에 스타일을 넣었다. 인기라는 단어와 사이트라는 단어의 색이 다르기 때문에 `<span>`으로 묶어 따로 스타일을 적용시켰다.