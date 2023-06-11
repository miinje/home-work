# Mission-03
Transition을 활용한 드롭 다운 메뉴 만들기

### 조건
1. transition 실습을 위한 과제 파일은 mission-03/transition.html 파일과 mission-03/transition.css 파일을 생성 후 각각 마크업과 스타일을 작성
2. 관련 사이트는 제목으로 각각 항목은 링크로 구현
3. 링크 목록은 5개이며 CSS를 사용하여 화면에 1개의 목록만 보이도록 구현
4. 목록에 마우스를 올리면 5개의 목록이 펼쳐지도록 구현
5. transition 속성을 활용하여 애니메이션 효과를 적용
6. mission-03/README.md 파일을 생성한 후 마크업 코드와 CSS 코드에 대한 설명을 적고 아래 이미지와 같이 완성된 UI 스크린샷을 삽입
   

### Stacks 🐈
<div>
  <img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
  <img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white">
</div>


## 마크업
```html
<div class="dropDown">
  <h1 class="dropDown--title">관련 <span>사이트</span></h1>
  <ul class="dropDown--menu is--active">
    <li>제로베이스</li>
    <li>W3C</li>
    <li>데이원 컴퍼니</li>
    <li>웹 접근성 연구소</li>
    <li>MDN</li>
  </ul>
</div>
```

1. 기본 마크업 구조 작업 진행
- `<div>` 안에 `<h1>`과 `<ul>`을 넣어 마크업
- 스타일이 필요한 요소에 class 삽입
- transition을 줄 <ul> 요소에 애니메이션을 넣을 거라는 의미의 `is--active` 삽입
  


## 스타일
```css
@import url(./css-reset.css);
```
1. css 기초 스타일 리셋
- [meyerweb css reset](https://meyerweb.com/eric/tools/css/reset/)

```css
.dropDown {
  padding: 12px;
  margin: 20px;
  width: 166px;
  height: 63px;
  background: linear-gradient(180deg, #CCCCCC 0%, #EEEEEE 100%);
  border-radius: 5px;
  border: 1px solid #A3A3A3;
}
```
2. <div> 스타일 적용 (_figma 시안 참고_)
- 배경의 크기와 안쪽의 패딩 삽입
- 배경 그라디언트 색과 radius 등 꾸밈 요소 지정


```css
.dropDown--title {
  font-size: 15px;
  font-weight: 700;
  line-height: 150%;
  width: 69px;
  height: 23px;
}

.dropDown--title span {
  color: #ED552F;
}
```
3. 타이틀 텍스트 스타일 적용
- 기본 스타일 지정
- '스타일' 문구만 묶은 <span> 요소 스타일 지정


```css
.dropDown--menu {
  margin-top: 8px;
  background-color: #FFF;
  border: 1px solid #A3A3A3;
  border-radius: 5px;
  height: 25px;
  width: 165px;
  overflow: hidden;
}

.dropDown--menu li {
  margin-left: 24px;
  padding: 3px 3px 0;
  font-size: 400;
  font-size: 14px;
  line-height: 150%;
}
```
4. 리스트 스타일 지정
- 기본 접혀 있는 스타일로 지정

```css
.dropDown .is--active:hover {
  width: 166px;
  height: 150px;
  line-height: 150%;
}

.dropDown .is--active:hover li {
  margin-top: 5px; 
  transition-property: margin-top;
  transition-duration: 0.45s;
  transition-delay: 0.2s;
}
```
5. transition을 활용한 드롭 다운 메뉴 설정


---
### 결과물
![결과-접힘](./images/스크린샷%202023-06-12%20오전%204.29.02.png)
![결과-펼침](./images/스크린샷%202023-06-12%20오전%204.29.12.png)
