# STRUCTURE · t-housing-sample (v0.1.0 · 사진 가득 갤러리형 · 흰 바탕 + 거의 검정 · 주황은 장식만 · 모서리 2px · 배포 예정 t-housing-sample.lgt3232.workers.dev)

```
t-housing-sample/
├─ index.html                 단일 파일 (CSS · JS 인라인)
├─ wrangler.toml              name = t-housing-sample
├─ .assetsignore              img/ · _old/ · 문서 · index_*.html · _deploy 배포 제외
├─ th-jost.woff2              영문 라벨 · 메뉴 (Jost 400–600, 영문만)
├─ th-pretendard.woff2        본문 · 한글 (Pretendard 300–700)
├─ th-logo.svg · th-logo-w.svg  가로 로고(주황 마크 + HOUSING 검정 / 흰색)
├─ th-mark.svg                마크만 (파비콘 원본)
├─ th-hero.webp · th-hero-m.webp  히어로 PC 1200×900 · 모바일 810×1080
├─ th-g01 ~ th-g14.webp       SHOWROOM 갤러리 (g01 · g07 넓은 칸 1200×800 · 나머지 600×800)
├─ favicon.png · og-th.jpg
├─ img/                       다올 제공 원본 + _원문.md (배포 제외 · 레포에 올리지 말 것)
└─ CHANGELOG.md / STRUCTURE.md
```

## 섹션 순서
헤더 → 히어로(사진 풀스크린) → 품목 띠 → `#showroom`(갤러리 화면 끝까지) → `#care`(회색) → `#projects`(어두운 띠) → `#visit` → 푸터(#111) + 모바일 `.quick`.

## 갤러리 배치
- 900 미만 2열 · 이상 4열, 간격 4px. 넓은 칸(`li.w`) 2개는 900 미만 3:2 한 줄 전체, 900 이상은 같은 줄 세로 사진 높이에 맞춤(사진 absolute).
- 순서 = 4열 기준 줄마다 빈칸 0(넓1+세2 / 세2+넓1 / 세4 / 세4), 2열에서도 빈칸 0.

## 버튼 · 링크
- 전화 `tel:0647212279`(메인): 헤더(900 이상) · 히어로 · 오시는 길 · 푸터 · 하단 바
- 네이버 플레이스 `m.place.naver.com/place/2008207089/home`: 히어로 · 푸터 · 하단 바
- 인스타그램 `instagram.com/t.housing_official`: 오시는 길 · 푸터 · 하단 바 · PROJECTS
- 네이버 지도 `map.naver.com/p/entry/place/2008207089` · 블로그 `blog.naver.com/t-housing`

## 주황 쓰는 곳 (다올: 조금만)
로고 마크 · 히어로 라벨 앞 28px 선 · 품목 띠 점 · CARE 번호 옆 18px 선 · PROJECTS 현장명 hover 밑줄. 그 외 금지.

## 모션 (강제 재생 · 다올 방침)
- 히어로 `.intro` 등장 · 섹션 `.reveal`(setInterval) · 앵커 rAF 스크롤(R-25). reduced-motion 분기 없음.

## 폰트 재생성
문구 바꾸면 빠진 글자 검사(LESSONS §26). 한글은 Pretendard만, Jost는 영문만.
