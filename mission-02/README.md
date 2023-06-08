# Mission-02
Position과 Float를 사용하여 로그인 칸 만들기

### 조건
1. 마크업은 로그인(제목)-아이디 레이블과 입력서식-비밀번호 레이블과 입력서식-로그인 버튼-회원가입 및 아이디/비밀번호 찾기 링크 순일 것
2. 이미지 assets 없이 모든 디자인을 CSS로 구현할 것
3. 일부 요소의 배치를 position 속성을 활용할 것
4. 회원 가입, 아이디/비밀번호 찾기 영역은 float을 활영할 것
   

### Stacks 🐈
<div>
  <img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
  <img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white">
</div>

## 마크업
```html
<header class="header">
  <h1 class="loginTitle">로그인</h1>
  <div class="loginArea">
    <form action="https://formspree.io/f/xeqwwbwk" method="POST"
        class="loginForm">
      <fieldset>
        <legend>로그인</legend>
        <div>
          <label for="id" class="idInput__label">아이디</label>
          <input type="text" id="id" required
          class="idInput__input" placeholder="euid@euid.dev" />
        </div>
        <div>
          <label for="password" class="passInput__label">비밀번호</label>
          <input type="text" id="password" required
          class="passInput__input" placeholder="8자리 이상" />
        </div>
        <button type="submit" class="button">로그인</button>
      </fieldset>
    </form>
  </div>
</header>
```

-  기본 마크업 구조 작업 진행

form의 기본적인 구조(fieldset과 legend)와 버튼 태그를 삽입

필요한 요소에 class 속성 부여 (class 이름은 현재 상태를 바로 알 수 있는 것으로 지을 것)


## 스타일
```css
@import url(./../base-css/a11y.css);
@import url(./../base-css/base.css);
```
- 기본적으로 적용돼 있는 스타일을 제거하고 `legend`을 화면에서 숨기기 위해 스타일 적용
- 그 외 class `loginForm`에 배경색과 그림자를 추가
- class `loginTitle`에 글자 색과 크기 등 적용

```css
.loginArea {
  width: 220px;
  height: 106px;
  background: #FFFFFF;
  border-radius: 5px;
  position: relative;
}
```
- 필드셋

