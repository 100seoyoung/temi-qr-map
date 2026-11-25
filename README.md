# 새빛관 층별 안내도 (테미 QR)

테미 화면에 QR 이미지를 띄우면 → 사용자가 휴대폰으로 스캔 → 이 웹사이트(층별 안내도)가 열립니다.

```
[테미 화면: 네이버 QR 이미지] --스캔--> [휴대폰: https://아이디.github.io/temi-qr-map/]
```

## 폴더 구성

| 파일 | 설명 |
|---|---|
| `index.html` | 휴대폰에서 열리는 안내도 페이지 (1층/2층/3층 탭) |
| `images/1f.png` `2f.png` `3f.png` | 층별 지도 이미지 (직접 넣어야 함) |

## 1. 지도 이미지 넣기

`images` 폴더에 `1f.png`, `2f.png`, `3f.png` 이름으로 지도 이미지를 넣습니다.
파일 이름이 다르면 해당 층에 "이미지를 찾을 수 없습니다" 문구가 뜹니다.

## 2. GitHub Pages에 올리기

1. GitHub에서 새 저장소 `temi-qr-map` 생성 (Public)
2. 이 폴더에서 터미널 실행:
   ```
   git add .
   git commit -m "층별 안내도"
   git remote add origin https://github.com/<아이디>/temi-qr-map.git
   git push -u origin main
   ```
3. 저장소 **Settings → Pages → Branch: main / (root) → Save**
4. 1~2분 뒤 `https://<아이디>.github.io/temi-qr-map/` 접속 확인

## 3. 네이버 QR 만들기

1. [qr.naver.com](https://qr.naver.com) 에서 QR 코드 만들기
2. 연결할 정보에서 **링크로 바로 이동**을 고르고 2번의 GitHub Pages 주소 입력
3. 완성된 QR 이미지 다운로드

네이버 QR은 나중에 연결 주소를 바꿔도 QR 이미지는 그대로 쓸 수 있습니다.

## 4. 테미 화면에 띄우기

다운로드한 QR 이미지를 테미 화면에 띄웁니다.

## 테스트

- **올리기 전 (PC에서):** `index.html`을 더블클릭해 브라우저로 열고, 탭 전환과 지도 표시 확인.
  F12 → 휴대폰 모양 아이콘을 누르면 휴대폰 화면 크기로 볼 수 있습니다.
- **올린 후 (휴대폰에서):** 휴대폰 브라우저로 GitHub Pages 주소 직접 접속.
- **최종:** 테미 화면의 QR을 휴대폰 카메라로 스캔해서 안내도가 열리는지 확인.
  잘 안 읽히면 화면 밝기를 올리고 QR을 크게 띄워보세요.
