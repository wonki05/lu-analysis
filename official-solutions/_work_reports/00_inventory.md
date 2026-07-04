# 00. 인벤토리 조사 보고서

작성일: 2026-07-04
작업 루트: `E:\LEET\lu-project-vlm`

## 도구 환경

- Python 3.12 + PyMuPDF(fitz) 1.28.0 사용 가능 → PDF 페이지 렌더링에 사용.
- `pdftoppm`(TeXLive) 존재. ImageMagick(magick) 없음.
- PDF 대조는 PyMuPDF 렌더링 이미지를 기준으로 수행.

## 입력 파일 확인

- 입력 초안 폴더: `converted-solutions_GPTdraft`
- 검수보고서 폴더: `converted-solutions_GPTdraft\review-reports` (5개 파일 모두 존재)
- 원본 PDF 폴더: `docs_solutions` (2012~2026 15개 모두 존재)

## 연도별 인벤토리

| 연도 | 초안 형태 | PDF 쪽수 | 문항 heading | `정답 :` 행 수 | 이미지 링크 | 비고 |
|---|---|---|---|---|---|---|
| 2012 | ZIP(package) | 81 | 01~33 (33개) | 0 | 2 (23_01, 23_02) | 33번 도중 종료(PDF 자체 불완전), 정답 행 전무 |
| 2013 | MD | 80 | 01~35 (35개) | 0 | 0 | 정답 행 전무 |
| 2014 | MD | 155 | 01~35 (35개) | 35 | 0 | PDF 76쪽~는 2013 자료 중복 |
| 2015 | MD | 78 | 01~35 (35개) | 35 | 0 | |
| 2016 | MD | 84 | 01~35 (35개) | 35 | 0 | |
| 2017 | MD | 85 | 01~35 (35개) | 35 | 0 | |
| 2018 | MD | 74 | 01~35 (35개) | 35 | 0 | |
| 2019 | MD | 64 | 01~30 (30개) | 30 | 0 | 문항유형 라벨 누락 지적 |
| 2020 | MD | 72 | 01~30 (30개) | 30 | 0 | 문항유형/내용영역 라벨 누락 지적 |
| 2021 | MD | 66 | 01~30 (30개) | 0 | 0 | 정답 행 전무 |
| 2022 | MD | 74 | 01~30 (30개) | 30 | 0 | |
| 2023 | MD | 80 | 01~30 (30개) | 0 | 0 | 정답 행 전무 + OCR 잔재 다수 |
| 2024 | MD | 86 | 01~30 (30개) | 0 | 0 | 정답 행 전무 + OCR 깨짐 |
| 2025 | MD | 82 | 01~30 (30개) | 30 | 0 | |
| 2026 | ZIP(package) | 74 | 01~30 (30개) | 30 | 2 (06_01, 06_02) | 어미 누락 2건, 06번 이미지 캡션 |

## ZIP 내부 파일 목록

- `2012_LU_official+solutions_package.zip`
  - `2012_LU_official+solutions.md`
  - `2012_LU_solution_images_23_01.png`
  - `2012_LU_solution_images_23_02.png`
- `2026_LU_official+solutions_package.zip`
  - `2026_LU_official+solutions.md`
  - `2026_LU_solution_images_06_01.png`
  - `2026_LU_solution_images_06_02.png`
  - `2026_LU_official+solutions_report.md` (생성 보고서 → 최종 폴더에 복사하지 않음)

## 이미지 링크 상태

- 2012, 2026 모두 초안 Markdown이 `./파일명.png` 상대경로 사용. 같은 폴더 배치로 링크 정상.
- 깨진 이미지 링크: 조사 시점 기준 없음(모든 링크 대상 파일이 ZIP에 포함).

## 출력 폴더 생성 결과

`official-solutions` 아래 15개 연도 폴더 생성 완료:
`2012_solution_files` ~ `2026_solution_files`. 각 폴더에 `[연도]_LU_official+solutions.md`와 필요한 이미지 배치 완료.

## 정답 행 보완이 필요한 연도

- 2012(33문항, PDF 불완전으로 33 후반부·34·35 제외), 2013(35), 2021(30), 2023(30), 2024(30).

## ZIP과 외부 MD 동시 존재 여부

- 2012, 2026은 ZIP만 존재(외부 MD 없음) → ZIP 기준.
- 그 외 연도는 외부 MD만 존재 → MD 기준.
- ZIP과 외부 MD가 동시에 존재하는 연도는 없음.
