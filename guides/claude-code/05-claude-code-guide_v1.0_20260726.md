# 클로드 코드 설치하고 *첫 프로그램 만들기*

**CLAUDE CODE 준비 · 05 CLAUDE CODE — v1.0 · 2026-07-26**

> 명령어 한 줄로 클로드 코드를 설치하고, 로그인한 뒤, 한국어로 말해서 프로그램을 만들어 봅니다.
> 소요 시간 약 10분 · Windows 10 / 11 · 유료 플랜 계정 필요 · 앞의 4개 설치 완료 후

> 📌 화면 그림(목업)이 포함된 버전은 같은 폴더의 **05-claude-code-guide_v1.0_20260726.html** 을 브라우저로 여세요. 명령어는 HTML에서 `복사` 버튼으로 바로 복사할 수 있습니다.

---

## Claude Code 설치 전체 흐름

사전 점검 → 설치 명령 한 줄 → 로그인 → 첫 실행 순서입니다. 설치 마법사 창은 없습니다.

| 순서 | 단계 | 하는 일 |
|:---:|:---|:---|
| 01 | 🔍 사전 점검 | STEP 1 |
| 02 | ⌨️ 설치 명령 | STEP 2–4 |
| 03 | 🔑 로그인 | STEP 5–6 |
| 04 | 💬 첫 대화 | STEP 7–8 |
| 05 | 🛠 점검·활용 | STEP 9–10 |

**필요한 것:** Git · Node.js · VS Code 설치 완료 · Claude 유료 플랜 계정(Pro/Max/Team/Enterprise) · 인터넷 연결  |  무료 플랜은 사용 불가

---

## STEP 1 — 앞의 3개가 잘 설치됐는지 확인  <sub>CLAUDE CODE · 사전 점검</sub>

**목표:** 설치를 시작하기 전에 준비물이 모두 갖춰졌는지 확인합니다.

1. PowerShell을 **새로** 열고 아래 한 줄을 붙여넣은 뒤 Enter.
2. **세 줄이 모두** 버전 숫자로 나오면 준비 완료입니다.
3. 빨간 오류가 보이면 해당 가이드(02·03번)로 돌아가세요.

**한 번에 확인 (세미콜론으로 3개 연결)**

```powershell
git --version; node --version; npm --version
```

> ℹ️ **Node.js가 없어도 됩니다** — 다음 **방법 A(네이티브 설치)**는 Node.js 없이도 동작합니다. 다만 다른 도구를 위해 설치해 두는 편이 좋습니다.

## STEP 2 — 네이티브 설치 — 명령 한 줄  <sub>CLAUDE CODE · 설치 (방법 A · 권장)</sub>

**목표:** Node.js 없이도 동작하고 자동 업데이트되는 권장 방식으로 설치합니다.

1. **PowerShell** 창인지 확인합니다. (`PS C:\…>` 로 시작)
2. 아래 명령을 복사해 붙여넣고 **Enter**. (붙여넣기 = 마우스 오른쪽 클릭)
3. **installed successfully** 가 나올 때까지 1~3분 기다립니다.

**방법 A · 네이티브 설치 (권장)**

```powershell
irm https://claude.ai/install.ps1 | iex
```

> ⚠️ **'irm' 용어가 인식되지 않습니다** — 지금 창이 **CMD(명령 프롬프트)** 입니다. 이 명령은 **PowerShell 전용**입니다. Windows 키 → **powershell** 로 다시 여세요.

> ✅ **왜 이 방법이 권장인가요?** — npm 권한 문제를 피할 수 있고, **업데이트가 자동**으로 이루어집니다.

## STEP 3 — npm 설치 — 방법 A가 막혔을 때  <sub>CLAUDE CODE · 설치 (방법 B)</sub>

**목표:** 네이티브 설치가 막히는 환경에서 npm으로 설치합니다.

1. 아래 npm 명령을 복사해 붙여넣고 Enter. (Node.js가 설치돼 있어야 합니다)
2. 노란 **warn** 메시지는 무시해도 됩니다. 2~4분 기다립니다.
3. 마지막에 **added … packages** 가 나오면 성공입니다.

**방법 B · npm 전역 설치**

```powershell
npm install -g @anthropic-ai/claude-code
```

> ⚠️ **권한 오류(EACCES/EPERM)가 나면** — PowerShell을 **관리자 권한으로 실행**해 재시도하거나 방법 A(네이티브)를 쓰세요.

> ℹ️ **둘 다 설치할 필요 없습니다** — A 또는 B **하나만** 하면 됩니다. 둘 다 하면 버전이 충돌할 수 있습니다.

## STEP 4 — 터미널 새로 열고 **claude --version**  <sub>CLAUDE CODE · 설치 확인</sub>

**목표:** 설치가 정상적으로 끝났는지 확인합니다.

1. 지금 PowerShell 창을 **완전히 닫고 새로** 엽니다.
2. `claude --version` 을 실행해 **2.x.x** 가 나오는지 봅니다.
3. `claude doctor` 를 실행해 ✔ 표시가 모두 초록인지 확인합니다.

**버전 확인**

```powershell
claude --version
```

**전체 진단 (문제가 있을 때)**

```powershell
claude doctor
```

> ⚠️ **"claude 용어가 인식되지 않습니다"** — ① 터미널을 **새로** 열었는지 확인 ② PC 재부팅 ③ 그래도 안 되면 다른 설치 방법(A↔B)으로 재시도.

## STEP 5 — 작업 폴더에서 **claude** 실행  <sub>CLAUDE CODE · 첫 실행</sub>

**목표:** 클로드 코드를 실제로 켭니다. 실행한 폴더가 곧 작업 대상입니다.

1. 작업 폴더를 만들고 그 안으로 이동합니다.
2. **claude** 라고 입력하고 Enter.
3. 처음이면 **테마 선택** 화면이 나옵니다. 화살표로 고르고 Enter.

**① 작업 폴더 만들고 이동**

```powershell
mkdir "$HOME\Desktop\dev\hello-claude" -Force; cd "$HOME\Desktop\dev\hello-claude"
```

**② 클로드 코드 실행**

```powershell
claude
```

> ⚠️ **아무 폴더에서나 켜지 마세요** — 클로드 코드는 **실행한 폴더의 파일을 읽고 고칩니다.** 반드시 작업용 폴더를 만들어 그 안에서 실행하세요.

## STEP 6 — 브라우저로 로그인하기  <sub>CLAUDE CODE · 로그인</sub>

**목표:** Claude 계정과 연결해 사용 준비를 마칩니다.

1. **Claude account with subscription** (구독 계정)을 선택하고 Enter.
2. 브라우저가 자동으로 열립니다. 안 열리면 화면의 **주소를 복사**해 직접 붙여넣습니다.
3. 브라우저에서 **Authorize** 를 누릅니다.
4. 터미널로 돌아오면 **Login successful** 이 뜹니다.

> ⚠️ **유료 플랜이 필요합니다** — Claude Code는 **Pro · Max · Team · Enterprise** 유료 플랜에서 사용합니다. **무료 플랜으로는 로그인해도 사용할 수 없습니다.**

## STEP 7 — 한국어로 말해서 프로그램 만들기  <sub>CLAUDE CODE · 첫 대화</sub>

**목표:** 바이브 코딩을 직접 체험합니다. 코드를 몰라도 한국어로 요청하면 됩니다.

1. `>` 표시 옆에 **한국어로** 원하는 것을 적고 Enter.
2. 클로드가 만들 파일 내용을 미리 보여 줍니다. 내용을 확인합니다.
3. **1. Yes** 를 골라 승인하면 실제로 파일이 만들어집니다.

**첫 요청 예시 (그대로 복사해 붙여넣기)**

```powershell
한국어로 인사하는 간단한 웹페이지를 index.html 로 만들어줘. 버튼을 누르면 오늘 날짜가 표시되게 해줘.
```

> ✅ **승인(Yes)이 안전장치입니다** — 클로드 코드는 파일을 만들거나 고치기 전에 **항상 물어봅니다.** 내용을 보고 Yes를 골라야 실행됩니다.

## STEP 8 — 만들어진 파일 확인하고 열어 보기  <sub>CLAUDE CODE · 결과 확인</sub>

**목표:** 클로드 코드가 실제로 파일을 만들었는지 확인하고 결과를 봅니다.

1. **/exit** 를 입력해 클로드 코드를 빠져나옵니다. (Ctrl+C 두 번도 가능)
2. `dir` 로 **index.html** 이 생겼는지 확인합니다.
3. `start index.html` 로 브라우저에서 열어 봅니다.

**① 파일 목록 확인**

```powershell
dir
```

**② 브라우저로 열어 보기**

```powershell
start index.html
```

> ✅ **이것이 바이브 코딩입니다** — 코드를 한 줄도 쓰지 않고 **한국어 요청만으로** 동작하는 웹페이지를 만들었습니다. 수정도 `claude` 를 다시 켜고 말하면 됩니다.

## STEP 9 — 꼭 알아야 할 슬래시 명령  <sub>CLAUDE CODE · 기본 사용법</sub>

**목표:** 클로드 코드 안에서 쓰는 기본 명령을 익힙니다.

1. 클로드 코드 실행 중에 **/** 를 입력합니다.
2. 명령 목록이 나오면 **↑↓** 로 고르고 **Enter**.
3. 초보자는 오른쪽의 **5개**만 알면 충분합니다.

**대화 새로 시작 (맥락 초기화)**

```powershell
/clear
```

**종료**

```powershell
/exit
```

> ℹ️ **/clear 를 자주 쓰세요** — 주제가 바뀌면 **/clear** 로 정리하세요. 이전 대화가 섞여 엉뚱한 답이 나오는 것을 막습니다. 새 프로젝트를 시작할 때는 **/init**.

## STEP 10 — VS Code 안에서 클로드 코드 쓰기  <sub>CLAUDE CODE · VS Code 연동</sub>

**목표:** 편집기와 터미널을 한 화면에서 함께 써 작업 효율을 높입니다.

1. VS Code에서 작업 폴더를 엽니다. (우클릭 → Code로 열기)
2. **Ctrl + `** 로 아래쪽 터미널을 엽니다.
3. 터미널에 **claude** 를 입력하고 한국어로 요청합니다.
4. 왼쪽 파일 목록에서 결과가 바뀌는 것을 **실시간으로** 확인합니다.

> ✅ **이 조합이 가장 편합니다** — 왼쪽 = 파일 목록·코드, 아래 = 클로드 코드 대화. **바뀌는 내용을 눈으로 확인**하면서 작업할 수 있습니다.

> ℹ️ **VS Code 확장도 있습니다** — 확장 검색에서 **Claude Code** 를 설치하면 사이드 패널에서도 쓸 수 있습니다. 터미널 방식만으로도 충분합니다.

## Claude Code 명령어 모음 (복사해서 사용)

터미널 명령(PowerShell)과 클로드 코드 안에서 쓰는 슬래시 명령을 모았습니다.

### ① 설치 — 방법 A · 네이티브 (권장)

```powershell
irm https://claude.ai/install.ps1 | iex
```

**PowerShell 전용**입니다. CMD에서는 동작하지 않습니다.

### ② 설치 — 방법 B · npm

```powershell
npm install -g @anthropic-ai/claude-code
```

Node.js가 있어야 합니다. A가 막힐 때만 사용하세요.

### ③ 버전 확인

```powershell
claude --version
```

```
→ 2.x.x (Claude Code)
```

설치가 끝났는지 확인하는 명령입니다.

### ④ 전체 진단 (문제 생기면 가장 먼저)

```powershell
claude doctor
```

설치·버전·인증 상태를 한 번에 점검합니다.

### ⑤ 실행 (작업 폴더 안에서)

```powershell
claude
```

실행한 폴더가 곧 작업 대상입니다.

### ⑥ 이전 대화 이어서 실행

```powershell
claude --continue
```

마지막 대화를 그대로 이어 갑니다.

### ⑦ 업데이트

```powershell
claude update
```

네이티브 설치는 보통 자동 업데이트됩니다.

### ⑧ 작업 폴더 만들고 바로 시작 (한 줄)

```powershell
mkdir "$HOME\Desktop\dev\my-app" -Force; cd "$HOME\Desktop\dev\my-app"; claude
```

폴더 생성 → 이동 → 실행을 한 번에 합니다.

### ⑨ 실행 정책 오류가 날 때

```powershell
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

"스크립트를 실행할 수 없으므로" 오류에 사용. 물어보면 **Y**.

### ⑩ 한글이 깨질 때

```powershell
chcp 65001
```

터미널 인코딩을 UTF-8로 바꿉니다.

---

## Claude Code — 문제가 생겼을 때

무엇을 해도 안 되면 `claude doctor` 부터 실행하세요.

| 이런 화면·메시지가 나오면 | 원인 | 이렇게 해결하세요 |
|:---|:---|:---|
| `'irm' 용어가 … 인식되지 않습니다` | 지금 창이 CMD(명령 프롬프트) | `irm` 은 PowerShell 전용 명령입니다. Windows 키 → **powershell** 입력 → **Windows PowerShell** 실행 후 다시 시도하세요. |
| `'claude' 용어가 … 인식되지 않습니다` | PATH 미반영 | ① 터미널 **완전히 닫고 새로 열기** ② PC 재부팅 ③ `claude doctor` ④ 그래도 안 되면 다른 설치 방식(A↔B)으로 재시도. |
| `이 시스템에서 스크립트를 실행할 수 없으므로` | PowerShell 실행 정책 제한 | `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned` 실행 → **Y** 입력 → 터미널 새로 열기. |
| 로그인은 되는데 사용이 막힘 | 무료 플랜 계정 | Claude Code는 **Pro·Max·Team·Enterprise** 유료 플랜이 필요합니다. claude.ai에서 플랜을 확인하세요. 결제 후 `/status` 로 재확인. |
| 브라우저가 안 열려 로그인 불가 | 기본 브라우저 설정·보안 정책 | 터미널에 표시된 `https://claude.ai/oauth/…` 주소를 **드래그해 복사**한 뒤 브라우저 주소창에 직접 붙여넣으세요. |
| `npm ERR! EACCES` 권한 오류 | npm 전역 설치 권한 | 관리자 PowerShell로 재시도하거나, **방법 A(네이티브 설치)**로 바꾸세요. **권한을 강제로 바꾸지 마세요.** |
| 한글이 깨져 보임 | 터미널 인코딩 | PowerShell에서 `chcp 65001` 실행. 또는 **Windows Terminal**(Microsoft Store 무료)을 설치해 사용하면 한글이 깔끔합니다. |
| 엉뚱한 폴더의 파일을 고침 | 잘못된 위치에서 실행 | `/exit` 후 `cd` 로 **작업 폴더로 이동**한 뒤 다시 `claude` 실행. 실행 위치가 곧 작업 범위입니다. |

---

## 전체 설치 완료 — 이제 시작입니다

5개 프로그램이 모두 준비됐습니다. 아래 명령으로 최종 점검하세요.

### ✅ 완료 체크리스트

- [ ] **GitHub 계정을 만들었다** — 아이디·비밀번호·복구 코드 보관
- [ ] **git --version 이 나온다** — 이름·이메일 설정 완료
- [ ] **node --version / npm --version 이 나온다** — LTS 버전
- [ ] **code --version 이 나온다** — VS Code PATH 등록 완료
- [ ] **claude --version 이 나온다** — 2.x.x (Claude Code)
- [ ] **로그인하고 첫 파일을 만들어 봤다** — index.html 생성 성공

### ➡️ 다음 단계 & 참고

- **앞으로의 작업 루틴** — ① 작업 폴더 우클릭 → **Code로 열기** ② `Ctrl + `` 터미널 ③ `claude` ④ 한국어로 요청
- **좋은 요청 쓰는 법** — **무엇을**(기능) · **어떤 파일로** · **어떻게 동작하게** 를 함께 적으면 결과가 훨씬 좋아집니다.
- **주제가 바뀌면 /clear** — 이전 대화가 섞이면 엉뚱한 결과가 나옵니다.
- **문제가 생기면 claude doctor** — 설치·인증·버전을 한 번에 진단합니다.
- **만든 결과를 GitHub에 올리기** — 클로드 코드에게 **"이 폴더를 GitHub에 올려줘"** 라고 말하면 됩니다.

> 최종 점검 (한 줄로 전부) `git --version; node --version; code --version; claude --version`

---

### 📌 출처 (2026-07 기준)

- Claude Code 공식 설치 문서 — https://code.claude.com/docs/en/setup
- Claude Code 빠른 시작 — https://code.claude.com/docs/en/quickstart
- 요금제 안내 — https://www.anthropic.com/pricing

> ※ 본 문서의 브라우저·설치창·터미널 그림은 실제 스크린샷이 아닌 **화면을 재현한 벡터 목업**입니다. 버전에 따라 버튼 위치·문구가 다를 수 있습니다.
