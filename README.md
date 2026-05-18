# Portfolio

순수 HTML/CSS로 만든 한 장짜리 포트폴리오 템플릿. 빌드 도구 없이 `index.html` 한 파일만 수정하면 됩니다.

## 실행

```sh
python3 -m http.server 8000
```

브라우저에서 http://localhost:8000 접속.

## 수정 가이드

모든 콘텐츠는 `index.html`에 있습니다. 아래 위치를 찾아 값을 바꿔주세요.

### 1. 페이지 메타 정보

`<head>` 안:

- `<title>` — 브라우저 탭에 표시되는 제목
- `<meta name="description">` — 검색엔진/공유 미리보기에 노출되는 설명

### 2. 프로필 (자기소개 영역, `<section class="about">`)

- **아바타**
  - 이니셜만 쓰려면: `<div class="avatar">CH</div>` 의 `CH` 를 원하는 글자로 변경
  - 사진을 쓰려면: 해당 `<div>` 를 다음으로 교체
    ```html
    <img class="avatar" src="profile.jpg" alt="이름" />
    ```
    그리고 같은 폴더에 `profile.jpg` 파일을 둡니다.
- **이름** — `<h1 class="name">` 안의 텍스트
- **직함** — `<p class="title">` 안의 텍스트 (예: `Software Engineer`, `학생`, `디자이너` 등)
- **소개 문장** — `<p class="tagline">` 안의 텍스트. 한두 줄 자기소개

### 3. 연락처 버튼 (`<div class="contacts">`)

각 `<a>` 의 `href` 를 본인 정보로 변경:

- 이메일 버튼: `href="mailto:이메일주소"` 형태로 — `mailto:` 접두사는 그대로 두고 이메일만 변경
- GitHub 버튼: `href` 를 본인 GitHub 프로필 URL로
- LinkedIn 버튼: `href` 를 본인 LinkedIn 프로필 URL로

버튼을 추가하고 싶다면 `<a class="contact-btn secondary">…</a>` 블록을 복사해서 붙여넣고, 안의 텍스트와 `href` 만 바꾸면 됩니다. 빼고 싶은 버튼은 해당 `<a>` 블록을 통째로 지우면 됩니다.

### 4. 프로젝트 목록 (`<section>` 안 `<div class="projects">`)

각 프로젝트는 다음 구조입니다:

```html
<a class="project" href="프로젝트_URL">
  <p class="project-title">
    프로젝트 이름
    <span class="project-meta">연도나 태그</span>   <!-- 선택, 빼도 됨 -->
  </p>
  <p class="project-desc">
    한 줄 설명.
  </p>
</a>
```

- `href` → 프로젝트로 연결할 URL. 아직 링크가 없다면 `#` 으로 두면 됩니다
- `project-title` → 프로젝트 이름
- `project-meta` → 우측에 표시되는 작은 라벨 (연도, 상태 등). 필요 없으면 `<span>` 째로 삭제
- `project-desc` → 한두 줄 설명

프로젝트를 추가하려면 위 `<a class="project">` 블록을 통째로 복사해 붙여넣으면 됩니다. 빼려면 해당 블록을 통째로 지우면 됩니다.

### 5. 푸터

페이지 가장 아래 `<footer>` 안의 연도와 이름을 본인 정보로 바꿔주세요.
