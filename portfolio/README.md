# 윤동현 포트폴리오

기획부터 촬영, 편집, AI 워크플로우까지 — 영상 제작자 윤동현의 포트폴리오 사이트입니다.

## 폴더 구조

```
index.html              사이트 전체(HTML·CSS·JavaScript가 이 파일 하나에 있음)
assets/
  works/01/             작품 1: video.mp4, thumbnail.jpg, proposal.pdf
  works/02/             작품 2: video.mp4, thumbnail.jpg, proposal.pdf
  process/              Process 사진: planning.jpg, editing.jpg, ai.jpg
  icons/                About > 소프트웨어 아이콘
```

## 수정 방법

- 문구·사진·영상 주소는 `index.html`의 `B. 내용 수정` 부분에서 바꿉니다.
- 새 작품은 `assets/works/03/`처럼 같은 형식으로 폴더를 만들고 `index.html`의 3번째 작품 칸에 주소를 넣습니다.
- 빌드 과정이 없습니다. 파일을 저장하고 브라우저에서 `index.html`을 열면 바로 확인됩니다.

## 참고

- 작품 영상은 웹용으로 압축되어 있습니다(1080p, H.264, 약 4~5Mbps, 빠른 재생 시작 옵션 적용). GitHub는 100MB가 넘는 파일을 올릴 수 없으니 새 영상도 같은 방식으로 압축해서 넣으세요.
  `ffmpeg -i 원본.mp4 -c:v libx264 -preset slow -crf 21 -maxrate 7M -bufsize 14M -profile:v high -pix_fmt yuv420p -c:a aac -b:a 160k -movflags +faststart video.mp4`
- `assets/icons/claude-code.svg`는 직접 그린 아이콘이며, 나머지 아이콘은 각 서비스의 공개 아이콘입니다.
