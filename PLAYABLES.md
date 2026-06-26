# Toss 플레이어블 광고 PoC — 소재 인덱스

> 광고주 미팅 / 토스 PoC 검증용 단일 HTML 모음.
> Base URL: `https://mod157.github.io/playables/`
>
> 각 링크를 모바일 (또는 좁은 폭) 브라우저에서 열면 320×480 광고 영역으로 확인 가능. 노션에서는 `/embed` 블록으로 붙여넣어도 됩니다.

업데이트: 2026-06-26

---

## 1. 인터랙티브 (재작업본)

| 소재 | 미리보기 URL |
|---|---|
| 연애시뮬 분기 엔드카드 | https://mod157.github.io/playables/magent_branching_endcard.html |
| 스크래치 복권 엔드카드 | https://mod157.github.io/playables/magent_scratch_endcard.html |

선택지 / 긁기 같은 단순 인터랙션. 광고주 톤 들어오면 카피·색만 갈아끼우면 됨.

## 2. 일반 플레이어블

| 소재 | 미리보기 URL | 비고 |
|---|---|---|
| 블록 블라스트 shape match (PDF 1번 톤, 신규) | https://mod157.github.io/playables/magent_block_blast_shape_match.html | 분홍 + Block Blast 게임 룩. 실루엣에 블록 드래그. |
| 단어 빈칸 채우기 (재작업본) | https://mod157.github.io/playables/magent_word_completion_game.html | 글자 드래그, 3개 단어 클리어. |
| 테트리스 shape match 보라 톤 (기존) | https://mod157.github.io/playables/magent_shape_match.html | MAGENT 보라 톤 1차본. |
| 블록 블라스트 라인 클리어 (기존) | https://mod157.github.io/playables/magent_block_blast.html | 1차본. |
| 3매치 (기존) | https://mod157.github.io/playables/magent_match3.html | 1차본. |
| 2048 머지 — 스와이프형 (기존) | https://mod157.github.io/playables/magent_merge_2048.html | 보너스 카테고리. |

## 3. 엔드카드 (1차 결과물 — PoC 비추천)

| 소재 | 미리보기 URL | 비고 |
|---|---|---|
| 럭키 드로우 (3장 카드 뽑기) | https://mod157.github.io/playables/magent_lucky_draw_endcard.html | AI 티 남아 있음. 톤 재작업 필요. |
| 미스터리 박스 (3개 보물상자) | https://mod157.github.io/playables/magent_mystery_box_endcard.html | AI 티 남아 있음. 톤 재작업 필요. |

## 4. 외부 config 주입 빌드 예시

`build.js + configs/<example>.json` 결과물. 광고주별 카피/색/이미지/URL만 갈아끼우면 새 소재가 5초 안에 빌드된다는 걸 보여주는 샘플.

| 소재 | 미리보기 URL |
|---|---|
| 분기 엔드카드 — 빌드 예시 | https://mod157.github.io/playables/built_branching_example.html |
| 스크래치 — 빌드 예시 | https://mod157.github.io/playables/built_scratch_example.html |
| 단어 게임 — 빌드 예시 | https://mod157.github.io/playables/built_word_completion_example.html |

## 5. 3D & 완전 커스텀 플레이어블

**아직 0건.** PoC 3유형 중 차별화 포인트로 가장 중요한 카테고리지만 비어 있음. 광고주 확정 후 우선순위로 진행 예정.

---

## PoC 스펙 요약

- 광고주 3개사 × 2건 = **6건** (게임/논게임 카테고리 균형)
- 제작 유형 3종: **인터랙티브 / 일반 플레이어블 / 3D·완전 커스텀**
- 기간: **2026-06-30 ~ 2026-08-31** (2개월)
- 공통 규약: `mraid.open()` 우선 + `clickTag` 파라미터 지원, 외부 네트워크 요청 없음, 단일 HTML 50KB 이하

## 공유 / 임베드 팁

- 노션에서는 URL 줄 끝에서 `Esc` → "Embed" 선택 시 iframe으로 노션 안에서 바로 플레이 가능. 단, 모바일 사이즈 영역으로 좁혀져야 의도된 비주얼이 보임.
- 브라우저 DevTools 모바일 뷰(320×480, 360×640, 390×844 등)로 보면 실제 광고 환경에 가장 가까움.
- `?clickTag=https://광고주랜딩` 식 파라미터를 URL에 추가하면 CTA 클릭 시 그 URL로 이동. 광고망 테스트에서 동일 방식으로 동작.
