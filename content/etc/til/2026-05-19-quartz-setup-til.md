---
title: "TIL: Quartz v4로 블로그 만들기"
date: 2026-05-19
tags:
  - til
  - quartz
  - blog
draft: false
---

## 오늘 배운 것

Quartz v4로 기술 블로그를 셋업했다.

### 핵심 포인트

- Quartz는 옵시디언 마크다운을 그대로 정적 사이트로 변환해준다
- `quartz.config.ts`에서 테마, 폰트, 색상 등을 설정
- `quartz.layout.ts`에서 사이드바, 본문, 컴포넌트 배치를 커스터마이징
- 폴더 구조가 곧 카테고리 → Explorer에서 자동으로 네비게이션 생성

### 유용한 명령어

```bash
npx quartz build --serve   # 로컬 미리보기
npx quartz sync             # GitHub에 배포
```
