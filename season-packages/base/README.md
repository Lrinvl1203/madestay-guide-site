# Season Packages

숙소 웹가이드의 기존 정보 구조를 유지하면서 시즌별 hero, 추천 카드, AI 질문 chip, 배경 효과를 교체하기 위한 패키지 구조입니다.

## 적용 원칙

1. 체크인, 와이파이, 쓰레기, 가전 사용법은 기존 정보와 가독성을 유지합니다.
2. 시즌 장식은 hero와 seasonal picks 영역에 제한합니다.
3. `prefers-reduced-motion` 사용자는 particle/fog/snow animation을 끕니다.
4. 새로운 시즌은 `tokens.css` + `seasonal-content.json` + `DESIGN-season-*.md`를 추가합니다.

## PoC

`guide-seasonal-event.html`에서 Christmas/Halloween toggle로 두 테마를 비교합니다.
