# munroni-mode

[English](README.md)

[Claude Code](https://claude.com/claude-code)용 작업 방식 스킬입니다. Claude에게 이렇게 일하라고 알려 줍니다.

- 첫 줄에 답부터, 쉬운 말로 씁니다.
- 맡은 일은 중간에 묻지 않고 끝까지 합니다. 되돌리기 어려운 일(커밋, 푸시, 배포, 파일 삭제, 바깥으로 나가는 메일)만 먼저 묻습니다.
- 시킨 것만 합니다. 시키지 않은 칸, 버튼, 파일을 덧붙이지 않습니다.
- 검증은 테스트, 타입 검사, 린트로 하고 결과를 지어내지 않습니다.
- 만든 파일과 시안은 경로만 주지 않고 직접 열어 줍니다.
- 화면은 장식 없이 단순하게, 구조는 보이게 만듭니다.
- 글은 AI 말투 없이 씁니다.

## 판

| 스킬 | 규칙 언어 |
|---|---|
| `munroni-mode` | 영어(기본) |
| `munroni-mode-ko` | 한국어 |

두 판의 규칙은 같습니다. 어느 판을 써도 답은 사용자가 쓰는 언어로 합니다.

## 구성

```
skills/munroni-mode/
├─ SKILL.md                  답변, 자율성, 위임, 검증, 진행 방식, 코드, 메모
└─ references/
   ├─ ui-defaults.md         화면과 시안을 만들기 전에 읽음
   └─ writing.md             문서, 발표 자료, 바깥 글, 다른 세션 프롬프트를 쓰기 전에 읽음
```

## 설치

플러그인으로 설치:

```
/plugin marketplace add ruddbs273-hue/munroni-mode
/plugin install munroni@munroni
```

설치한 뒤 `/munroni:munroni-mode-ko`(영어판은 `/munroni:munroni-mode`)를 칩니다.

복사해서 설치할 수도 있습니다. `skills/munroni-mode-ko`(또는 `skills/munroni-mode`) 폴더를 `~/.claude/skills/` 아래에 넣고 `/munroni-mode-ko`를 칩니다.

## 참고

- 명령을 쳐야만 켜집니다(`disable-model-invocation: true`). Claude가 알아서 불러오지 않습니다.
- 한 사람의 취향입니다. 포크해서 규칙을 고치고 이름을 바꿔 자기 것으로 쓰면 됩니다.

## 라이선스

[MIT](LICENSE)
