# Git 설치하고 _처음 실행하기_

**CLAUDE CODE 준비 · 02 GIT — v1.0 · 2026-07-26**

> 내 컴퓨터와 GitHub를 연결해 주는 프로그램 Git을 설치합니다. 설치 창이 많아 보이지만 실제로 **신경 쓸 화면은 단 3개**입니다.
> 소요 시간 약 10분 · Windows 10 / 11 · 무료 · 관리자 권한 필요 · 초보자 대상

> 📌 화면 그림(목업)이 포함된 버전은 같은 폴더의 **02-git-guide_v1.0_20260726.html** 을 브라우저로 여세요. 명령어는 HTML에서 `복사` 버튼으로 바로 복사할 수 있습니다.

---

## Git 설치 전체 흐름

내려받기 → 설치 마법사(중요 화면 3개) → 설치 확인 → 최초 설정 순서입니다.

| 순서 | 단계           | 하는 일  |
| :--: | :------------- | :------- |
|  01  | ⬇️ 내려받기    | STEP 1–2 |
|  02  | ⚙️ 설치 마법사 | STEP 3–7 |
|  03  | ✅ 설치 확인   | STEP 8–9 |
|  04  | 🪪 최초 설정   | STEP 10  |
|  05  | 🚀 실행해 보기 | STEP 11  |

**꼭 기억할 3개 화면:** ① 기본 편집기 → Visual Studio Code ② 기본 브랜치 이름 → main ③ PATH 설정 → 가운데(권장) 항목 | 나머지는 전부 Next

---

## STEP 1 — git-scm.com 에서 설치 파일 받기 <sub>GIT · 내려받기</sub>

**목표:** Git 설치 파일(.exe)을 내 컴퓨터에 내려받습니다.

1. 주소창에 **git-scm.com/download/win** 을 입력하고 Enter.
2. **Click here to download** 를 누릅니다. (몇 초 뒤 자동 시작되기도 합니다)
3. 화면 아래 다운로드 표시에서 `Git-2.5x.x-64-bit.exe` 를 확인합니다.

**주소 (복사해서 주소창에 붙여넣기)**

```powershell
https://git-scm.com/download/win
```

> ℹ️ **32비트? 64비트?** — 요즘 PC는 거의 **64-bit** 입니다. 사이트가 알아서 골라 주므로 큰 버튼을 누르면 됩니다.

## STEP 2 — 내려받은 파일 실행 (보안 경고 통과) <sub>GIT · 설치 시작</sub>

**목표:** 설치 파일을 실행하고 Windows 보안 경고를 정상적으로 넘깁니다.

1. "이 앱이 디바이스를 변경하도록 허용하시겠어요?" 창이 뜨면 **예(Y)** 를 누릅니다.
2. 파란 **Windows의 PC 보호** 화면이 뜨면 **추가 정보** 를 누릅니다.
3. 나타난 **실행** 버튼을 누릅니다.

> ⚠️ **이 경고는 정상입니다** — Git은 전 세계에서 쓰는 공식 프로그램입니다. 다만 **반드시 git-scm.com 에서 직접 받은 파일**일 때만 실행하세요.

> ℹ️ **관리자 권한이 막혀 있다면** — 기관 PC에서 "관리자에게 문의" 메시지가 나오면 전산 담당 부서에 **Git for Windows 설치 승인**을 요청하세요.

## STEP 3 — 라이선스 · 설치 위치 · 구성요소 → 모두 **Next** <sub>GIT · 설치 마법사 (1/5)</sub>

**목표:** 앞쪽 화면은 손대지 않고 그대로 넘어갑니다. 화면 제목이 달라도 Next만 누르면 됩니다.

1. 구성요소 목록은 **기본 체크 그대로** 둡니다. 아무것도 바꾸지 마세요.
2. **Next** 를 누릅니다.
3. 같은 방식으로 **License → 설치 폴더 → 구성요소 → 시작 메뉴** 4개 화면을 Next로 넘깁니다.

> 💬 **겁먹지 마세요** — 이 4개 화면은 **아무것도 바꾸지 않습니다.** Next 버튼만 4번 누르면 됩니다.

> ℹ️ **설치 위치는 그대로** — `C:\Program Files\Git` 이 기본값입니다. 바꾸면 나중에 문제가 생길 수 있으니 그대로 두세요.

## STEP 4 — 기본 편집기 → **Use Visual Studio Code** <sub>GIT · 설치 마법사 (2/5) ★중요</sub>

**목표:** Git이 메모를 띄울 때 쓸 편집기를 VS Code로 지정합니다.

1. **Choosing the default editor used by Git** 화면에서 **드롭다운(▾)** 을 클릭합니다.
2. 목록에서 **Use Visual Studio Code as Git's default editor** 를 선택합니다.
3. 선택된 내용이 위 칸에 표시되는지 확인합니다.
4. **Next** 를 누릅니다.

> ⚠️ **기본값(Vim)은 피하세요** — 기본값 **Vim** 은 마우스가 안 통하고 종료 방법도 어려워 초보자가 크게 당황합니다. 반드시 바꾸세요.

> ℹ️ **VS Code가 아직 없다면** — 나중에 설치해도 됩니다. **Use Notepad as Git's default editor** 를 골라도 무방합니다.

## STEP 5 — 기본 브랜치 이름 → **main** <sub>GIT · 설치 마법사 (3/5) ★중요</sub>

**목표:** GitHub와 이름을 맞추기 위해 기본 브랜치를 main으로 바꿉니다.

1. 아래쪽 **Override the default branch name…** 를 선택합니다.
2. 입력칸에 **main** 이 들어 있는지 확인합니다. (비어 있으면 직접 입력)
3. 위쪽 **Let Git decide** 가 선택 해제되었는지 확인합니다.
4. **Next** 를 누릅니다.

> ℹ️ **브랜치가 뭔가요?** — 작업 갈래의 이름입니다. 지금은 **기본 폴더 이름** 정도로 생각하세요. GitHub가 `main` 을 쓰므로 맞춰 두면 헷갈리지 않습니다.

> 💬 **지나쳤어도 괜찮아요** — 나중에 명령 한 줄로 바꿀 수 있습니다: `git config --global init.defaultBranch main`

## STEP 6 — PATH 설정 → **가운데(Recommended)** <sub>GIT · 설치 마법사 (4/5) ★가장 중요</sub>

**목표:** 어느 창에서나 git 명령을 쓸 수 있도록 등록합니다. 이 화면만 틀리면 나중에 "git을 찾을 수 없다" 오류가 납니다.

1. 세 개 중 **가운데** 항목(Git from the command line and also from 3rd-party software)을 선택합니다.
2. 괄호 안에 **(Recommended)** 라고 적혀 있는지 확인합니다.
3. **Next** 를 누릅니다.

> ⚠️ **맨 위를 고르면 안 됩니다** — 맨 위(Git Bash only)를 고르면 PowerShell에서 `git` 이 동작하지 않아 **클로드 코드가 Git을 못 찾습니다.**

> ✅ **기본값이 이미 가운데입니다** — 대부분 처음부터 가운데가 선택되어 있습니다. **확인만** 하고 Next를 누르세요.

## STEP 7 — 나머지는 전부 Next → **Install** → **Finish** <sub>GIT · 설치 마법사 (5/5)</sub>

**목표:** 남은 화면은 기본값 그대로 두고 설치를 끝냅니다.

1. SSH · HTTPS · 줄바꿈 · 터미널 · git pull · 자격 증명 관리자 화면 → 모두 **Next** → **Install**.
2. 완료 화면이 나오면 **Launch Git Bash** 등 체크를 **모두 해제**합니다.
3. **Finish** 를 눌러 창을 닫습니다.

> 💬 **몇 번 더 눌러야 하나요?** — 보통 **Next 6~7번 → Install → Finish** 입니다. 화면 제목이 달라도 그냥 Next를 누르면 됩니다.

> ✅ **설치 완료 신호** — "Completing the Git Setup Wizard" 문구가 보이면 끝입니다.

## STEP 8 — PowerShell 열고 **git --version** <sub>GIT · 설치 확인</sub>

**목표:** Git이 제대로 설치되었는지 명령 한 줄로 확인합니다.

1. 키보드 **Windows 키** → **powershell** 입력 → **Windows PowerShell** 실행. (설치 전에 열어 둔 창은 닫으세요)
2. 아래 명령을 복사해 붙여넣고 **Enter**. (터미널 붙여넣기는 **마우스 오른쪽 클릭**)
3. **git version …** 이 나오면 설치 성공입니다.

**버전 확인**

```powershell
git --version
```

> 결과 예시: `→ git version 2.5x.x.windows.1`

> ⚠️ **오류가 나면 새 창을 여세요** — PATH 설정은 **새로 연 창부터** 적용됩니다.

## STEP 9 — 오류가 났을 때 확인하는 법 <sub>GIT · 설치 확인</sub>

**목표:** "git이 인식되지 않습니다" 오류의 원인을 스스로 찾아 해결합니다.

1. **빨간 오류**가 나면 먼저 PowerShell을 완전히 닫고 새로 엽니다.
2. 그래도 오류면 아래 **설치 경로 확인** 명령을 실행합니다.
3. 경로가 나오면 PATH 문제, 아무것도 안 나오면 설치가 안 된 것입니다.

**① Git이 어디 설치됐는지 확인**

```powershell
Get-Command git | Select-Object Source
```

**② 경로로 직접 실행해 보기**

```powershell
& "C:\Program Files\Git\cmd\git.exe" --version
```

> ⚠️ **②는 되는데 ①이 안 된다면** — PATH 등록 문제입니다. **Git을 다시 설치**하면서 STEP 6에서 **가운데 항목**을 선택하세요.

## STEP 10 — 이름 · 이메일 등록 (딱 한 번만) <sub>GIT · 최초 설정</sub>

**목표:** 누가 작업했는지 기록되도록 이름과 이메일을 등록합니다. 컴퓨터당 한 번만 하면 됩니다.

1. **이름**과 **이메일** 명령을 한 줄씩 붙여넣고 Enter. (따옴표 안은 본인 것으로 수정)
2. `git config --global --list` 를 실행합니다.
3. **user.name** · **user.email** 이 보이면 저장 완료입니다.

**① 이름 등록 (본인 이름으로 수정)**

```powershell
git config --global user.name "Hong Gildong"
```

**② 이메일 등록 (GitHub 가입 메일)**

```powershell
git config --global user.email "hufs.staff@gmail.com"
```

> ℹ️ **이메일은 가입 메일과 같게** — GitHub 가입 메일과 같아야 **내 작업으로 인식**됩니다. 이름은 영문 권장.

## STEP 11 — GitHub 저장소를 내 컴퓨터로 가져오기 <sub>GIT · 실행해 보기</sub>

**목표:** 앞 가이드에서 만든 저장소를 실제로 내려받아 Git이 동작하는지 확인합니다.

1. 작업 폴더를 만들고 그 안으로 이동합니다.
2. **git clone** 뒤에 내 저장소 주소를 붙여 실행합니다.
3. `dir` 로 폴더가 생겼는지 확인합니다.

**① 작업 폴더 만들고 이동**

```powershell
mkdir "$HOME\Desktop\dev" -Force; cd "$HOME\Desktop\dev"
```

**② 저장소 내려받기 (주소는 본인 것으로)**

```powershell
git clone https://github.com/hufs-hong/my-first-app.git
```

> ✅ **처음 한 번은 로그인 창이 뜹니다** — **Sign in with your browser** 를 눌러 GitHub에 로그인하면 이후로는 자동 처리됩니다.

## Git 명령어 모음 (복사해서 사용)

오른쪽 위 **복사** 버튼을 누른 뒤, PowerShell에서 **마우스 오른쪽 클릭**으로 붙여넣고 Enter.

### ① 설치 확인

```powershell
git --version
```

```
→ git version 2.5x.x.windows.1
```

이 줄이 나오면 설치 성공입니다.

### ② 이름 등록 (본인 이름으로 수정)

```powershell
git config --global user.name "Hong Gildong"
```

컴퓨터당 한 번만 실행하면 됩니다.

### ③ 이메일 등록 (GitHub 가입 메일)

```powershell
git config --global user.email "hufs.staff@gmail.com"
```

GitHub 가입 메일과 **동일하게** 맞추세요.

### ④ 설정 전체 확인

```powershell
git config --global --list
```

이름·이메일이 제대로 저장됐는지 확인합니다.

### ⑤ 기본 브랜치를 main으로 (설치 때 놓쳤다면)

```powershell
git config --global init.defaultBranch main
```

STEP 5를 지나쳤을 때 이 명령으로 보완합니다.

### ⑥ 저장소 내려받기

```powershell
git clone https://github.com/hufs-hong/my-first-app.git
```

주소는 GitHub의 **<> Code → HTTPS** 에서 복사한 것으로 바꾸세요.

### ⑦ 현재 상태 보기 (저장소 폴더 안에서)

```powershell
git status
```

무엇이 바뀌었는지 알려 줍니다. 가장 자주 쓰는 명령입니다.

### ⑧ Git 설치 위치 확인 (문제 진단용)

```powershell
Get-Command git | Select-Object Source
```

경로가 나오면 설치는 정상, PATH만 확인하면 됩니다.

### ⑨ 기본 편집기를 VS Code로 (설치 때 놓쳤다면)

```powershell
git config --global core.editor "code --wait"
```

Vim 화면에 갇히는 일을 예방합니다.

### ⑩ 한글 파일명 깨짐 해결

```powershell
git config --global core.quotepath false
```

한글 파일 이름이 숫자 코드로 보일 때 실행하세요.

---

## Git — 문제가 생겼을 때

증상별 해결 순서입니다. 대부분 **터미널 새로 열기** 로 해결됩니다.

| 이런 화면·메시지가 나오면            | 원인                            | 이렇게 해결하세요                                                                                                                           |
| :----------------------------------- | :------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------ |
| `'git' 용어가 … 인식되지 않습니다`   | PATH 미적용 또는 설치 옵션 오류 | ① PowerShell을 **완전히 닫고 새로 열기** ② PC 재부팅 ③ `Get-Command git` 로 확인 ④ 그래도 없으면 **재설치 후 STEP 6에서 가운데 항목** 선택. |
| 설치 파일 실행 시 파란 경고 화면     | SmartScreen 보호                | **추가 정보 → 실행** 순서로 클릭. git-scm.com 에서 직접 받은 파일이면 안전합니다.                                                           |
| "관리자에게 문의하세요" 로 설치 불가 | 기관 PC 권한 제한               | 전산 담당 부서에 **Git for Windows 설치 승인** 요청. 임시로는 **Portable 버전**(git-scm.com → Portable)으로 사용 가능.                      |
| clone 할 때 아이디/비밀번호를 물어봄 | GitHub는 비밀번호 로그인을 폐지 | **Sign in with your browser** 를 눌러 브라우저로 로그인하세요. 비밀번호를 직접 입력하면 실패합니다. 한 번 성공하면 자동 저장됩니다.         |
| `fatal: repository not found`        | 주소 오타 또는 비공개 저장소    | GitHub 저장소 화면의 **<> Code → HTTPS** 에서 주소를 다시 복사하세요. Private 저장소는 **로그인한 계정에 권한**이 있어야 합니다.            |
| 검은 편집기가 떠서 빠져나올 수 없음  | 기본 편집기가 Vim으로 설정됨    | 키보드로 **Esc** → **:q!** → **Enter** 입력해 탈출. 이후 `git config --global core.editor "code --wait"` 실행해 VS Code로 변경.             |
| 한글 파일명이 깨져 보임              | 기본 인코딩 설정                | `git config --global core.quotepath false` 를 실행하면 한글 파일명이 정상 표시됩니다.                                                       |

---

## Git 설치 완료 확인

아래가 모두 되면 Git 준비 완료입니다. 다음은 **Node.js LTS 설치**입니다.

### ✅ 완료 체크리스트

- [ ] **git --version 이 정상 출력된다** — git version 2.5x.x.windows.1
- [ ] **설치 중 PATH를 가운데(권장)로 선택했다** — PowerShell에서 git이 동작하는 것이 그 증거
- [ ] **기본 편집기를 VS Code로 지정했다** — Vim 탈출 소동을 예방합니다
- [ ] **기본 브랜치가 main 이다** — git config --global --list 로 확인
- [ ] **이름·이메일을 등록했다** — user.name / user.email
- [ ] **git clone 을 한 번 성공했다** — 브라우저 로그인 1회 완료

### ➡️ 다음 단계 & 참고

- **③ Node.js LTS 설치 가이드** — 클로드 코드가 사용하는 실행 엔진입니다. (**03-nodejs-guide**)
- **④ VS Code 설치 가이드** — Git 설치 때 지정한 편집기를 실제로 설치합니다.
- **⑤ Claude Code 설치 가이드** — 마지막 단계입니다.
- **자주 쓰는 3개만 기억** — `git status` · `git clone` · `git --version` — 나머지는 클로드 코드가 대신 해 줍니다.

> 최종 확인 명령 `git --version`

---

### 📌 출처 (2026-07 기준)

- Git for Windows 다운로드 — https://git-scm.com/download/win
- Git 최초 설정 공식 문서 — https://git-scm.com/book/ko/v2/시작하기-Git-최초-설정

> ※ 본 문서의 브라우저·설치창·터미널 그림은 실제 스크린샷이 아닌 **화면을 재현한 벡터 목업**입니다. 버전에 따라 버튼 위치·문구가 다를 수 있습니다.
