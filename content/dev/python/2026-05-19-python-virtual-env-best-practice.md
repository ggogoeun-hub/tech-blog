---
title: Python 가상환경 베스트 프랙티스
date: 2026-05-19
tags:
  - dev
  - python
draft: false
---

## 왜 가상환경이 필요한가

프로젝트마다 다른 패키지 버전을 사용해야 하므로, 격리된 환경이 필수다.

## 주요 도구 비교

| 도구 | 장점 | 단점 |
|------|------|------|
| `venv` | Python 내장, 가볍다 | 패키지 관리 별도 |
| `conda` | 데이터 사이언스 특화 | 무겁다 |
| `uv` | 매우 빠름, Rust 기반 | 비교적 새로움 |

## uv 추천 워크플로우

```bash
# 프로젝트 초기화
uv init my-project
cd my-project

# 패키지 추가
uv add pandas numpy

# 가상환경 실행
uv run python main.py
```

`uv`는 pip 대비 10-100배 빠른 패키지 설치 속도를 제공한다. 2024년부터 빠르게 생태계를 넓히고 있어, 새 프로젝트에는 `uv`를 기본으로 사용하는 것을 추천한다.
