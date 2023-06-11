# Mission-02
Position과 Float를 사용하여 로그인 칸 만들기

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