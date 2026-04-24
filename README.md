# YOUANDUS Pre-Order 2026 Landing

현대백화점 팝업 사전예약 랜딩페이지.

---

## 📁 폴더 구조

```
youandus-landing/
├── index.html        ← 메인 페이지
├── .nojekyll         ← GitHub Pages용 (건드리지 마세요)
├── README.md         ← 이 파일
└── images/           ← 제품 이미지 폴더 (아래 파일명으로 넣으세요)
```

---

## 🚀 GitHub Pages 배포 방법

### 1. 새 저장소 만들기
1. GitHub.com 로그인 → 우측 상단 **+** → **New repository**
2. Repository name: `youandus-landing` (원하는 이름)
3. **Public** 선택 (Private은 Pro 계정만 Pages 가능)
4. **Create repository** 클릭

### 2. 파일 업로드
**옵션 A — 웹에서 드래그앤드롭 (가장 쉬움)**
1. 만든 저장소 페이지에서 **"uploading an existing file"** 클릭
2. 이 폴더(`youandus-landing`)의 **내용물 전체**를 드래그
3. 하단 **Commit changes** 클릭

**옵션 B — 터미널에서 Git 푸시**
```bash
cd /Users/ojungmin/마케팅/youandus-landing
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/youandus-landing.git
git push -u origin main
```

### 3. GitHub Pages 활성화
1. 저장소 페이지 → 상단 **Settings**
2. 좌측 메뉴 **Pages** 클릭
3. **Source**: `Deploy from a branch` 선택
4. **Branch**: `main` / `/ (root)` 선택 → **Save**
5. 1~2분 후 상단에 URL 표시됨:
   `https://YOUR_USERNAME.github.io/youandus-landing/`

---

## 🖼 이미지 교체 가이드

`images/` 폴더에 아래 파일명으로 넣고, `index.html`에서 해당 URL을 교체하세요.

| 파일명 (권장) | 사이즈 | 용도 |
|---|---|---|
| `hero-bg.jpg` | 2000×1200 | Hero 배경 |
| `og-image.jpg` | 1200×630 | SNS 공유 썸네일 |
| `trusted-paltrow.jpg` | 800×1000 | 기네스 펠트로 / Romby |
| `trusted-residence.jpg` | 800×1000 | 르엘·어퍼하우스 |
| `trusted-heritage.jpg` | 800×1000 | Porro 헤리티지 |
| `product-romby.jpg` | 900×675 | Romby Chair |
| `product-materic.jpg` | 900×675 | Materic Oval Table |
| `product-pascal.jpg` | 900×675 | Pascal Table |
| `product-voyage.jpg` | 900×675 | Voyage Chair |
| `product-gap.jpg` | 900×675 | Gap Shelf |
| `product-lovely.jpg` | 900×675 | Lovely Day Sofa |

### 교체 방법

`index.html` 에서 **Ctrl/Cmd+F** 로 `unsplash.com` 검색 → 모두 아래와 같이 변경:

```html
<!-- 변경 전 -->
<div class="hero" style="... url('https://images.unsplash.com/photo-XXX') ...">

<!-- 변경 후 -->
<div class="hero" style="... url('./images/hero-bg.jpg') ...">
```

---

## ✏️ 텍스트/링크 수정 가이드

`index.html` 에서 아래 키워드로 검색하면 수정할 곳을 바로 찾을 수 있습니다.

| 검색어 | 수정 대상 |
|---|---|
| `[IMG:` | 이미지 교체 위치 (11곳) |
| `[LINK:` | 카톡·전화·SNS 링크 (5곳) |
| `[TEXT:` | 팝업 기간·가격·주소 |
| `[TALLY:` | 탈리 폼 ID 교체 |
| `YOUR_FORM_ID` | 탈리 폼 실제 ID |

---

## 📋 탈리(Tally) 폼 연결

1. [tally.so](https://tally.so) 가입 → 새 폼 만들기
2. 추천 필드:
   - 성함 (Short text, 필수)
   - 연락처 (Phone, 필수)
   - 관심 제품 (Dropdown)
   - 희망 상담 방식 (Multiple choice: 카톡/전화/방문)
   - 문의 내용 (Long text)
3. **Share** → **Embed** → **HTML** 탭 → 코드 복사
4. `index.html` 에서 `YOUR_FORM_ID` 를 실제 ID로 교체
5. Tally 대시보드에서 **Slack/이메일 알림** 설정

---

## 📊 Google Analytics 연결

`index.html` 하단 주석 블록에서 `G-XXXXXXX` 를 실제 GA4 측정 ID로 교체 후, 주석 해제해서 `</head>` 직전으로 옮겨주세요.

---

## 🌐 커스텀 도메인 연결 (선택)

GitHub Pages에서 `youandus.co.kr/pre-order` 같은 커스텀 URL 사용하려면:

1. Settings → Pages → **Custom domain** 입력
2. 도메인 업체에서 DNS 설정:
   - `CNAME` 레코드: `YOUR_USERNAME.github.io`
3. Pages 설정에서 **Enforce HTTPS** 체크

---

## ✅ 배포 전 최종 체크

- [ ] 이미지 11장 교체 완료
- [ ] 가격·기간·주소 텍스트 교체
- [ ] 카카오톡 채널 URL 확인
- [ ] 전화번호·이메일 확인
- [ ] Tally 폼 ID 교체
- [ ] GA4 측정 ID 삽입
- [ ] 모바일 뷰 확인 (크롬 개발자도구 → 모바일)
- [ ] 카운트다운 종료일 정확한지 확인
- [ ] OG 이미지 SNS 공유 테스트

---

## 📞 문의

유앤어스 · marketing@youandus.co.kr · 02-547-8009
