# 그림 갤러리

가족·신앙·여정을 주제로 한 그림 3점을 담은 정적 웹 갤러리입니다.
그림을 클릭하면 확대되는 라이트박스 기능이 포함되어 있습니다.

## 폴더 구성

```
gallery/
├── index.html          ← 갤러리 페이지 (그대로 두세요)
├── images/
│   ├── feed-my-sheep.jpg
│   ├── family-sharing-gospel.jpg
│   └── tibet-family.gif
└── README.md
```

## GitHub Pages로 배포하는 방법

### 1. GitHub에 새 저장소(Repository) 만들기
1. [github.com](https://github.com)에 로그인 후 우측 상단 **+** → **New repository** 클릭
2. Repository name을 정하세요 (예: `my-gallery`)
3. **Public**으로 설정 (GitHub Pages 무료 사용을 위해 필요)
4. **Create repository** 클릭

### 2. 파일 업로드
가장 쉬운 방법 — 웹 브라우저에서 바로 업로드:
1. 새로 만든 저장소 페이지에서 **Add file → Upload files** 클릭
2. `index.html`, `README.md`, 그리고 `images` 폴더 전체를 끌어다 놓기(drag & drop)
3. 하단의 **Commit changes** 클릭

> 터미널을 쓰신다면 다음 명령으로도 가능합니다.
> ```bash
> cd gallery
> git init
> git add .
> git commit -m "그림 갤러리 첫 배포"
> git branch -M main
> git remote add origin https://github.com/사용자명/저장소명.git
> git push -u origin main
> ```

### 3. GitHub Pages 활성화
1. 저장소 페이지에서 **Settings** 탭 클릭
2. 왼쪽 메뉴에서 **Pages** 클릭
3. **Source**를 **Deploy from a branch**로 설정
4. **Branch**를 `main` / `(root)`로 선택 후 **Save**
5. 1~2분 정도 기다리면 상단에 사이트 주소가 표시됩니다:
   `https://사용자명.github.io/저장소명/`

이제 이 주소를 누구에게나 공유할 수 있습니다.

## 그림을 더 추가하고 싶다면

1. `images/` 폴더에 새 이미지 파일을 넣습니다 (영문 파일명 권장).
2. `index.html`의 `<main class="gallery" id="gallery">` 안에 아래 블록을 하나 더 복사해서 붙여넣고, 이미지 경로와 제목·설명을 바꿔주세요.

```html
<article class="frame" tabindex="0" data-index="3">
  <span class="corner-bl"></span><span class="corner-br"></span>
  <div class="frame-media">
    <img src="images/새그림.jpg" alt="그림 제목" loading="lazy">
  </div>
  <div class="frame-caption">
    <span class="num">04</span>
    <h3>그림 제목</h3>
    <p>한 줄 설명을 적어주세요.</p>
  </div>
</article>
```

`data-index` 번호는 순서대로 0, 1, 2, 3 … 으로 이어지게 해주시면 됩니다.
