# 그림 갤러리

가족·신앙·여정을 주제로 한 그림 12점을 담은 정적 웹 갤러리입니다.
그림을 클릭하면 확대되는 라이트박스 기능과, 인스타그램·유튜브 링크가 포함되어 있습니다.

- Instagram: https://instagram.com/lakesky7_art
- YouTube: https://www.youtube.com/@ForJesus2030

## 폴더 구성 (★ 중요)

```
gallery/
├── index.html
├── images/                      ← 이 폴더 "통째로" 올려야 합니다
│   ├── feed-my-sheep.jpg
│   ├── family-sharing-gospel.jpg
│   ├── tibet-family.gif
│   ├── village-river.jpg
│   ├── mountain-village.jpg
│   ├── mountain-path.jpg
│   ├── children-smiling.jpg
│   ├── family-heart.jpg
│   ├── family-portrait.jpg
│   ├── field-gathering.jpg
│   ├── campfire-family.jpg
│   └── sharing-bread.jpg
└── README.md
```

**지난번에 이미지가 안 보였던 이유는 이미지 파일들이 `images` 폴더 없이
저장소 최상위(루트)에 바로 올라갔기 때문이었어요.** `index.html`은
`images/파일명.jpg` 경로를 찾기 때문에, 반드시 이미지들이 `images`라는
이름의 폴더 안에 들어있어야 합니다.

## 기존 저장소(`skylake-gallery`)를 업데이트하는 방법

기존에 만드신 `korean0217-lang/skylake-gallery` 저장소를 그대로 사용하시면 됩니다.

### 1. 기존 이미지 파일 삭제
저장소 루트에 있는 `feed-my-sheep.jpg`, `family-sharing-gospel.jpg`,
`tibet-family.gif` 3개 파일을 각각 열어서 우측 상단 휴지통 아이콘으로 삭제하세요.
(같은 이름의 이미지가 새 `images` 폴더 안에도 들어있으니 중복해서 남겨둘 필요가 없습니다.)

### 2. 새 파일 업로드
1. 저장소 페이지에서 **Add file → Upload files** 클릭
2. 이 답변과 함께 드린 압축 파일을 풀면 나오는 `index.html`, `README.md`,
   그리고 **`images` 폴더 전체**를 통째로 끌어다 놓으세요.
   - 폴더째로 끌어놓아야 `images/파일.jpg` 구조가 만들어집니다.
   - 이미지 파일 12개를 낱개로 하나씩 올리면 지난번처럼 루트에 바로 올라가서
     다시 깨지니, 꼭 폴더째 드래그하세요.
3. 기존 `index.html`도 새 버전으로 덮어써집니다 (같은 이름이라 자동으로 교체 확인창이 뜹니다).
4. 하단의 **Commit changes** 클릭

### 3. 확인
1~2분 후 `https://korean0217-lang.github.io/skylake-gallery/` 에 접속해서
그림 12점과 하단(그리고 상단)의 Instagram / YouTube 버튼이 잘 보이는지 확인하세요.

## 그림을 더 추가하고 싶다면

1. `images/` 폴더에 새 이미지 파일을 넣습니다 (영문 파일명 권장, 공백·한글 대신 하이픈 사용).
2. `index.html`의 `<main class="gallery" id="gallery">` 안에 아래 블록을 하나 더 복사해서 붙여넣고, 이미지 경로·제목·설명을 바꿔주세요.

```html
<article class="frame" tabindex="0" data-index="12">
  <span class="corner-bl"></span><span class="corner-br"></span>
  <div class="frame-media">
    <img src="images/새그림.jpg" alt="그림 제목" loading="lazy">
  </div>
  <div class="frame-caption">
    <span class="num">13</span>
    <h3>그림 제목</h3>
    <p>한 줄 설명을 적어주세요.</p>
  </div>
</article>
```

`data-index`는 0부터 순서대로 이어지게 해주세요 (13번째 그림이면 12).

## 소셜 링크 주소를 바꾸고 싶다면

`index.html`에서 `instagram.com/lakesky7_art`와
`youtube.com/@ForJesus2030` 문자열을 찾아 원하는 주소로 바꾸면 됩니다.
(상단 한 곳, 하단 한 곳 — 총 2곳에 각각 있습니다.)
