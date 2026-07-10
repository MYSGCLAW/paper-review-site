# 기술 분석 아카이브

논문 리뷰와 코드 분석 결과를 모아둔 GitHub Pages용 정적 사이트입니다.

## 사이트

- GitHub Pages 저장소: `MYSGCLAW/paper-review-site`
- 메인 페이지: `index.html`
- 논문 리뷰: `papers/`
- 코드 분석: `code-analysis/`
- 정보 수집: `research/`

## 현재 구성

- 논문 리뷰 탭
  - PDF 논문 기반 구조화 분석 보고서
  - 검증 상태가 함께 표시됨
- 코드 분석 탭
  - 프로젝트 단위로 묶인 코드베이스 분석
  - 예: `PJRT`
  - 각 문서는 코드 리딩 순서, 로직 다이어그램, Mermaid 도식을 포함
- 정보 수집 탭
  - 특정 주제에 대한 문서, 링크, 메모를 모아 핵심 요약과 쟁점으로 정리
- 기술 노트 탭
  - 실험, 아이디어, 기타 기술 정리용

## 원본 파이프라인

이 저장소는 생성된 정적 사이트 결과물입니다. 실제 분석 파이프라인은 로컬의 `paper-review` 작업 디렉터리에서 실행됩니다.

주요 입력 경로:

```text
queue/papers/pending/
queue/code-analysis/pending/
queue/research/pending/
references/code-analysis/
references/research/
```

주요 출력 경로:

```text
site/
work/
```

게시 명령:

```bash
cd /home/sam/paper-review
./scripts/publish_site.sh "Update analysis site"
```

코드 분석 전체 실행 후 게시:

```bash
cd /home/sam/paper-review
ANALYSIS_AUTO_PUBLISH=true ./run-analysis-all.sh code-analysis
```
