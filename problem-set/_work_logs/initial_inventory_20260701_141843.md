# 초기 인벤토리 — LEET 언어이해 2012–2026 정리·검수

- 작성 시각: 2026-07-01 14:18:43
- 작업 루트: `E:\LEET\lu-project-vlm`
- 작업 브랜치: `main`

## 0-1. 작업 전 git status --short

```
 D converted-files_GPTdraft/2025_LU_improved_outputs.zip
 M "docs_problems/2025_LEET_언어이해_문제지(홀수형).pdf"
?? converted-files_GPTdraft/2025_LU_improved_ouputs.zip
?? converted-files_GPTdraft/review-reports/
```

> 참고: 위 D/M/?? 상태는 작업 시작 시점의 스냅샷이며 본 작업 이전에 이미 존재하던 것이다.
> - `2025_LU_improved_outputs.zip`(정상명)이 삭제(D)되고 `2025_LU_improved_ouputs.zip`(오타명, "outputs"→"ouputs")이 신규(??)로 존재한다.
> - 원본 입력 파일은 수정/이동/삭제하지 않는다. 2025년은 오타 파일명 ZIP을 소스로 사용한다.

## 0-2. 입력 파일 존재 확인

### ZIP (converted-files_GPTdraft) — 15/15 존재
| 연도 | ZIP 파일명 | 비고 |
|---|---|---|
| 2012 | 2012_LU_improved_outputs.zip | |
| 2013 | 2013_LU_improved_outputs.zip | work_report 포함 |
| 2014 | 2014_LU_improved_outputs.zip | |
| 2015 | 2015_LU_improved_outputs.zip | |
| 2016 | 2016_LU_improved_outputs.zip | |
| 2017 | 2017_LU_improved_outputs.zip | |
| 2018 | 2018_LU_improved_outputs.zip | work_report 포함 |
| 2019 | 2019_LU_improved_outputs.zip | |
| 2020 | 2020_LU_improved_outputs.zip | |
| 2021 | 2021_LU_improved_outputs.zip | |
| 2022 | 2022_LU_improved_outputs.zip | |
| 2023 | 2023_LU_improved_outputs.zip | |
| 2024 | 2024_LU_improved_outputs.zip | work_report 포함 |
| 2025 | **2025_LU_improved_ouputs.zip** | ⚠️ 파일명 오타(ouputs), work_report 포함 |
| 2026 | 2026_LU_improved_outputs.zip | |

### PDF (docs_problems) — 15/15 존재
2012~2026 `{연도}_LEET_언어이해_문제지(홀수형).pdf` 전부 확인.

### 검수보고서 (converted-files_GPTdraft/review-reports) — 3개
- `2012-2016_LU_review_report.md`
- `2017-2021_LU_review_report.md`
- `2022-2026_LU_review_report.md`

## 0-3. 도구 가용성
- Python 3.12.1 + PyMuPDF 1.28.0 (fitz) — PDF 렌더링/텍스트 추출
- pdftotext 4.00, pdftoppm 0.86.1, pdfinfo (poppler 0.86.1)
- mutool 없음 (미설치)

## 0-4. ZIP 압축해제 결과 (problem-set/{연도}_files)

모든 ZIP은 wrapper 폴더 없는 평평한 구조. 각 연도 폴더에 `{연도}_LU_problems.md`(주 파일) + 이미지 PNG(+ 일부 work_report.md) 배치 완료.

| 연도 | 주 md | 이미지 수 | 깨진 링크 |
|---|---|---|---|
| 2012 | 2012_LU_problems.md | 1 | 없음 |
| 2013 | 2013_LU_problems.md | 3 | 없음 |
| 2014 | 2014_LU_problems.md | 2 | 없음 |
| 2015 | 2015_LU_problems.md | 1 | 없음 |
| 2016 | 2016_LU_problems.md | 5 | 없음 |
| 2017 | 2017_LU_problems.md | 2 | 없음 |
| 2018 | 2018_LU_problems.md | 2 | 없음 |
| 2019 | 2019_LU_problems.md | 2 | 없음 |
| 2020 | 2020_LU_problems.md | 2 | 없음 |
| 2021 | 2021_LU_problems.md | 1 | 없음 |
| 2022 | 2022_LU_problems.md | 3 | 없음 |
| 2023 | 2023_LU_problems.md | 4 | 없음 |
| 2024 | 2024_LU_problems.md | 1 | 없음 |
| 2025 | 2025_LU_problems.md | 3 | 없음 |
| 2026 | 2026_LU_problems.md | 5 | 없음 |

- 모든 md의 이미지 참조는 `./{파일명}` 상대경로이며 실제 파일과 정상 연결됨(broken link 0건).
- 각 md의 이미지 링크와 폴더 내 이미지 파일이 1:1 대응.

## 0-5. 누락 파일
- 없음. 15개년 ZIP·PDF·주 md 모두 확보.

## 다음 단계
1. 검수보고서 3종을 읽고 연도별 체크리스트 생성 (`_qa_reports/{연도}_review_checklist.md`)
2. 연도별 PDF 대조 및 최소 수정
