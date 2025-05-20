# web-test

## main home 디자인 보고 따라 만들기

<img width="1440" alt="Image" src="https://github.com/user-attachments/assets/f0748415-02ac-4866-9dab-fe46ee3a8cd1" />
 <img width="1440" alt="Image" src="https://github.com/user-attachments/assets/8deef4ea-1449-4529-835b-2e5ecc976520" />

## HTML 기본 템플릿 분석

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  
</body>
</html> 
```

* <code> \<!DOCTYPE html> </code> : 이 문서가 HTML5 문서임을 선언합니다. 브라우저에게 이 페이지를 HTML5 표준에 따라 렌더링하라고 알려줌
  * 없는 경우에는 호한 모드로 작동할 수 있고 CSS, js 해석에 문제가 생길수도 있다.
* <code> \<html lang="en"> </code>: html 문서의 루투 요소로서 전체 문서의 시작과 끝을 감싼다. lang="en"은 문서의 언어가 영어임을 명시한다.
* <code> \<head> </code>: 메타데이터 저장
* <code> \<meta charset="UTF-8"></code>: 문자 인코딩 설정
  * 없는 경우 한글/특수문자 깨짐
* <code> \<meta name="viewport"> </code>: 반응형 레이아웃 설정
* <code> \<title> </code>: 브라우저 탭 제목
* <code> \<body> </code>: 사용자 컨텐츠 영역

## HTML 기본 태그 정리

## ✅ 1. 문서 구조 및 시맨틱 태그

| 태그 | 설명 | 역할 | 없으면? |
|------|------|------|---------|
| `<header>` | 문서나 섹션의 머리말 | 로고, 네비게이션 포함 | 구조 이해 어려움 (접근성 문제) |
| `<nav>` | 네비게이션 영역 | 메뉴, 링크 모음 | SEO/스크린리더에서 의미 약화 |
| `<main>` | 문서의 주요 콘텐츠 | 페이지 핵심 내용 | 의미 구조 모호 |
| `<section>` | 콘텐츠 영역 구분 | 기사, 블록 나눔 | 의미 없는 div 남발 유발 |
| `<article>` | 독립적 콘텐츠 | 블로그 글, 뉴스 등 | SEO, 시맨틱 구조 약화 |
| `<aside>` | 보조 정보 | 사이드바, 광고 등 | 의미 불명확 |
| `<footer>` | 하단 정보 | 저작권, 연락처 등 | 구조화 부족 |

---

## ✅ 2. 텍스트 관련 태그

| 태그 | 설명 | 예시 |
|------|------|------|
| `<h1>` ~ `<h6>` | 제목 태그 | `<h1>제목</h1>` |
| `<p>` | 단락 | `<p>본문</p>` |
| `<br>` | 줄 바꿈 | `<br>` |
| `<hr>` | 수평선 | `<hr>` |
| `<strong>` | 강조 (굵게) | `<strong>중요</strong>` |
| `<em>` | 강조 (기울임) | `<em>강조</em>` |
| `<span>` | 인라인 그룹화 | `<span>강조</span>` |
| `<div>` | 블록 그룹화 (의미 없음) | `<div>영역</div>` |

---

## ✅ 3. 링크 & 미디어

| 태그 | 설명 | 예시 |
|------|------|------|
| `<a href="">` | 하이퍼링크 | `<a href="https://example.com">링크</a>` |
| `<img src="" alt="">` | 이미지 | `<img src="image.jpg" alt="설명">` |
| `<video>` | 비디오 삽입 | `<video controls src="video.mp4"></video>` |
| `<audio>` | 오디오 삽입 | `<audio controls src="sound.mp3"></audio>` |
| `<iframe>` | 다른 웹페이지 삽입 | `<iframe src="https://example.com"></iframe>` |

---

## ✅ 4. 목록 관련

| 태그 | 설명 | 예시 |
|------|------|------|
| `<ul>` | 순서 없는 목록 | `<ul><li>항목</li></ul>` |
| `<ol>` | 순서 있는 목록 | `<ol><li>1단계</li></ol>` |
| `<li>` | 목록 항목 | `<li>내용</li>` |

---

## ✅ 5. 입력 & 폼 관련

| 태그 | 설명 | 예시 |
|------|------|------|
| `<form>` | 입력 폼 전체 | `<form action="/submit"></form>` |
| `<input>` | 텍스트, 체크박스 등 입력 | `<input type="text">` |
| `<label>` | 입력 설명 | `<label for="id">이름</label>` |
| `<textarea>` | 여러 줄 입력 | `<textarea></textarea>` |
| `<button>` | 버튼 | `<button>전송</button>` |
| `<select>` / `<option>` | 드롭다운 메뉴 | `<select><option>선택</option></select>` |

---

## ✅ 6. 스크립트 및 리소스

| 태그 | 설명 | 예시 |
|------|------|------|
| `<script>` | JavaScript 코드 포함 | `<script src="app.js"></script>` |
| `<link>` | 외부 CSS 연결 | `<link rel="stylesheet" href="style.css">` |
| `<style>` | 내부 CSS 작성 | `<style>p { color: red; }</style>` |

---

## ✅ 7. 표 관련

| 태그 | 설명 | 예시 |
|------|------|------|
| `<table>` | 테이블 전체 | `<table></table>` |
| `<tr>` | 행(Row) | `<tr><td>내용</td></tr>` |
| `<td>` | 데이터 셀 | `<td>데이터</td>` |
| `<th>` | 제목 셀 | `<th>제목</th>` |
| `<thead>` / `<tbody>` / `<tfoot>` | 테이블 구조 나누기 | `<thead><tr></tr></thead>` |

---

## 🧠 시맨틱 태그 vs 비시맨틱 태그

| 종류 | 설명 | 예시 |
|------|------|------|
| 시맨틱 태그 | 의미 있는 구조 표현 | `<article>`, `<nav>`, `<main>` |
| 비시맨틱 태그 | 의미 없이 구조만 표현 | `<div>`, `<span>` |

---

