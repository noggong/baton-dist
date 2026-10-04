# Baton 배포본

macOS 데스크탑 앱 **Baton** 의 배포본(dmg · zip)을 두는 곳입니다.
**소스는 여기 없습니다** — 비공개 레포에 있고, 이 레포에는 릴리스만 올라옵니다.

## 받는 법

[Releases](https://github.com/noggong/baton-dist/releases) 에서 최신 버전을 받습니다.

| 파일 | 대상 |
| --- | --- |
| `Baton-<버전>-arm64.dmg` | Apple silicon (M1 이상) |
| `Baton-<버전>.dmg` | Intel |
| `…-mac.zip` | 같은 앱의 zip 본 |

- **서명·공증본**입니다(Developer ID + notarized) — Gatekeeper 경고 없이 열립니다.
- **자동 업데이트는 없습니다.** 새 dmg 로 `Applications` 의 앱을 덮어쓰면 되고,
  데이터(`~/.baton`)는 그대로 남습니다.
- 각 릴리스 노트에 **sha256** 과 **소스 커밋 SHA** 가 적혀 있습니다. 받은 파일이 그 해시와
  같은지 확인하려면:

  ```sh
  shasum -a 256 ~/Downloads/Baton-<버전>-arm64.dmg
  ```

## 워크플로우·에이전트

앱에서 쓸 워크플로우와 에이전트는 **다른 레포**에 있습니다 —
[noggong/baton-catalog](https://github.com/noggong/baton-catalog).
앱의 `실행 › 가져오기 › 카탈로그에서` 로 골라 받습니다.

## 이 레포에 PR 하지 마세요

여기는 릴리스 자산만 두는 자리라 고칠 소스가 없습니다.
워크플로우·에이전트 기여는 [baton-catalog](https://github.com/noggong/baton-catalog) 로,
앱 자체의 문제는 배포본을 받은 경로로 알려 주세요.
