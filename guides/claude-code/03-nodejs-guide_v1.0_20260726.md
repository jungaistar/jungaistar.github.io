# Node.js LTS *안정 버전 설치하기*

**CLAUDE CODE 준비 · 03 NODE.JS — v1.0 · 2026-07-26**

> 클로드 코드와 개발 도구를 돌리는 엔진 Node.js를 설치합니다. 화면에서 **딱 한 가지**, 반드시 **LTS**를 고르는 것만 기억하세요.
> 소요 시간 약 7분 · Windows 10 / 11 · 무료 · 관리자 권한 필요 · 초보자 대상

> 📌 화면 그림(목업)이 포함된 버전은 같은 폴더의 **03-nodejs-guide_v1.0_20260726.html** 을 브라우저로 여세요. 명령어는 HTML에서 `복사` 버튼으로 바로 복사할 수 있습니다.

---

## Node.js 설치 전체 흐름

LTS 내려받기 → 설치 마법사(Next 반복) → 터미널 새로 열기 → 확인 순서입니다. 설치 마법사에서 **바꿀 것이 거의 없습니다.**

| 순서 | 단계 | 하는 일 |
|:---:|:---|:---|
| 01 | ⬇️ LTS 내려받기 | STEP 1 |
| 02 | ⚙️ 설치 마법사 | STEP 2–5 |
| 03 | 🔄 새 터미널 | STEP 6 |
| 04 | ✅ 설치 확인 | STEP 7 |
| 05 | 📦 npm 확인 | STEP 8 |

**가장 중요한 한 가지:** 반드시 왼쪽 초록색 LTS(장기 지원) 버전을 고르세요. 오른쪽 Current(최신) 버전은 실험용이라 오류가 잦습니다.

---

## STEP 1 — nodejs.org 에서 **LTS** 고르기  <sub>NODE.JS · 내려받기</sub>

**목표:** 안정 버전(LTS) 설치 파일을 내려받습니다.

1. 주소창에 **nodejs.org** 를 입력해 접속합니다.
2. 왼쪽 초록색 **LTS** 카드를 고릅니다. — **오른쪽 Current 아님**
3. 그 아래 **Windows Installer (.msi)** 를 누릅니다.
4. 화면 아래에서 `node-v24.x.x-x64.msi` 가 받아졌는지 확인합니다.

> ⚠️ **LTS vs Current** — **LTS**는 오래 지원되는 안정 버전, **Current**는 최신 기능 실험 버전입니다. 업무용은 무조건 **LTS**.

> ℹ️ **버전 숫자가 달라도 됩니다** — v24가 아닌 다른 숫자가 보여도 **LTS 라고 적힌 쪽**이면 정상입니다.

## STEP 2 — .msi 파일 실행 → 라이선스 동의  <sub>NODE.JS · 설치 시작</sub>

**목표:** 설치 마법사를 열고 라이선스에 동의합니다.

1. 내려받은 `node-v24.x.x-x64.msi` 를 **더블클릭**하고, UAC 창이 뜨면 **예**.
2. 첫 **Welcome** 화면에서 **Next**.
3. **I accept the terms in the License Agreement** 를 체크합니다.
4. **Next** 를 누릅니다.

> 💬 **.msi 가 뭔가요?** — Windows 표준 설치 파일 형식입니다. **.exe** 와 똑같이 더블클릭하면 됩니다.

## STEP 3 — **Add to PATH** 켜져 있는지 확인  <sub>NODE.JS · 설치 마법사 ★확인</sub>

**목표:** 기본값 그대로 두되, Add to PATH가 설치 대상인지만 눈으로 확인합니다.

1. **Destination Folder** 화면은 그대로 **Next**. (`C:\Program Files\nodejs\`)
2. **Custom Setup** 화면에서 **Add to PATH** 앞에 **💾 디스크 아이콘**이 있는지 확인합니다.
3. 아무것도 바꾸지 말고 **Next** 를 누릅니다.

> ⚠️ **✕ 표시가 있으면 눌러서 바꾸세요** — 항목 앞이 **✕(빨간 X)** 면 제외된 상태입니다. 클릭 → **Will be installed on local hard drive** 를 선택하세요.

> ℹ️ **PATH가 뭔가요?** — "이 프로그램은 어느 창에서든 이름만 부르면 실행된다"고 Windows에 알려 주는 목록입니다. 여기 없으면 `node` 명령이 동작하지 않습니다.

## STEP 4 — Tools for Native Modules → **체크하지 말고 Next**  <sub>NODE.JS · 설치 마법사</sub>

**목표:** 용량이 큰 추가 도구를 건너뛰어 설치 시간을 줄입니다.

1. **Tools for Native Modules** 화면이 나옵니다.
2. **Automatically install the necessary tools…** 체크박스는 **비워 둡니다.**
3. **Next** 를 누릅니다.

> ⚠️ **체크하면 오래 걸립니다** — 체크하면 Python·Visual Studio 빌드 도구까지 자동 설치되어 **10~30분**이 더 걸립니다. 클로드 코드 사용에는 필요 없습니다.

> 💬 **나중에 필요해지면?** — 그때 다시 설치하면 됩니다. 지금은 건너뛰는 것이 정답입니다.

## STEP 5 — **Install** → 잠시 대기 → **Finish**  <sub>NODE.JS · 설치 완료</sub>

**목표:** 실제 설치를 진행하고 마법사를 닫습니다.

1. **Ready to install** 화면에서 **Install** 을 누르고, UAC 창이 뜨면 **예**.
2. 초록색 진행 막대가 끝날 때까지 1~2분 기다립니다.
3. **Completed the Node.js Setup Wizard** 문구를 확인합니다.
4. **Finish** 를 눌러 창을 닫습니다.

> ⚠️ **검은 창이 잠깐 떠도 정상** — 설치 마무리에 명령 창이 깜빡일 수 있습니다. 저절로 닫힐 때까지 두세요.

## STEP 6 — 터미널 새로 열기 (또는 재부팅)  <sub>NODE.JS · 반영</sub>

**목표:** PATH 등록 내용을 시스템에 적용합니다. 이 단계를 건너뛰면 다음 확인이 실패합니다.

1. 열려 있던 **PowerShell·CMD 창을 모두 닫습니다.**
2. **Windows 키** 를 누르고 **powershell** 이라고 입력합니다.
3. 목록에서 **Windows PowerShell** 을 클릭해 실행합니다.

> ⚠️ **가장 흔한 실수** — 설치 **전에** 열어 둔 터미널에는 새 PATH가 반영되지 않습니다. "설치했는데 안 된다"의 90%가 이 경우입니다.

> ✅ **재부팅이 가장 확실** — 시간이 있다면 재부팅하세요. Node.js와 Git 모두 확실히 반영됩니다.

## STEP 7 — **node --version** 으로 확인  <sub>NODE.JS · 설치 확인</sub>

**목표:** Node.js가 정상 설치되었는지 확인합니다.

1. 새로 연 PowerShell에 `node --version` 을 붙여넣고 Enter. (붙여넣기 = 마우스 오른쪽 클릭)
2. `v24.x.x` 처럼 **v로 시작하는 숫자**가 나오면 성공입니다.
3. 이어서 `npm --version` 도 확인합니다.

**Node.js 버전 확인**

```powershell
node --version
```

> 결과 예시: `→ v24.x.x`

**npm 버전 확인**

```powershell
npm --version
```

> 결과 예시: `→ 11.x.x`

> ✅ **두 개 다 나와야 정상** — npm은 Node.js와 함께 설치됩니다. 둘 다 버전이 보이면 완료입니다.

## STEP 8 — npm이 실제로 동작하는지 시험  <sub>NODE.JS · 동작 시험</sub>

**목표:** 클로드 코드를 npm으로 설치할 수 있는 상태인지 미리 점검합니다.

1. `npm config get prefix` 를 실행해 **설치 폴더 경로**가 나오는지 봅니다.
2. `npm ping` 을 실행합니다.
3. **PONG** 이 나오면 인터넷으로 프로그램을 받아올 수 있는 상태입니다.

**① npm 전역 설치 폴더 확인**

```powershell
npm config get prefix
```

**② npm 서버 연결 시험**

```powershell
npm ping
```

> 결과 예시: `→ npm notice PONG`

> ⚠️ **npm ping 이 실패한다면** — 기관 방화벽·프록시 때문입니다. 이 경우 클로드 코드는 **네이티브 설치(irm)** 로 진행하세요.

## Node.js 명령어 모음 (복사해서 사용)

오른쪽 위 **복사** 버튼 → PowerShell에서 **마우스 오른쪽 클릭**으로 붙여넣기 → Enter.

### ① Node.js 버전 확인

```powershell
node --version
```

```
→ v24.x.x
```

**v로 시작하는 숫자**가 보이면 설치 성공입니다.

### ② npm 버전 확인

```powershell
npm --version
```

```
→ 11.x.x
```

Node.js와 함께 설치되는 패키지 관리자입니다.

### ③ 설치 위치 확인 (문제 진단)

```powershell
Get-Command node | Select-Object Source
```

경로가 나오면 설치는 정상, PATH만 점검하면 됩니다.

### ④ npm 전역 폴더 확인

```powershell
npm config get prefix
```

npm으로 설치한 프로그램이 저장되는 위치입니다.

### ⑤ npm 서버 연결 시험

```powershell
npm ping
```

```
→ npm notice PONG
```

실패하면 방화벽·프록시 문제입니다.

### ⑥ npm 캐시 정리 (설치 오류 시)

```powershell
npm cache clean --force
```

설치가 자꾸 실패할 때 한 번 실행한 뒤 재시도하세요.

### ⑦ 실행 정책 확인 (npm 스크립트 오류 시)

```powershell
Get-ExecutionPolicy -Scope CurrentUser
```

`Restricted` 가 나오면 아래 ⑧을 실행하세요.

### ⑧ 실행 정책 완화 (⑦이 Restricted일 때만)

```powershell
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

내 계정에만 적용되는 안전한 설정입니다. 물어보면 **Y** 입력.

---

## Node.js — 문제가 생겼을 때

증상별 해결 순서입니다. 대부분 **새 터미널** 또는 **재부팅** 으로 해결됩니다.

| 이런 화면·메시지가 나오면 | 원인 | 이렇게 해결하세요 |
|:---|:---|:---|
| `'node' 용어가 … 인식되지 않습니다` | 터미널이 PATH를 아직 못 읽음 | ① 터미널을 **모두 닫고 새로 열기** ② **재부팅** ③ `Get-Command node` 로 확인 ④ 없으면 설치 마법사에서 **Add to PATH** 가 제외됐던 것 → 재설치. |
| 설치 도중 멈춘 것처럼 보임 | Native Modules 도구 자동 설치 | STEP 4에서 체크를 **비워야** 합니다. 이미 시작됐다면 끝날 때까지 기다리거나, 설치 취소 후 다시 설치하며 체크를 해제하세요. |
| `npm ERR! code EACCES` / 권한 오류 | 전역 설치 폴더 권한 | ① PowerShell을 **관리자 권한으로 실행** 후 재시도 ② 그래도 안 되면 **npm 방식 대신** 클로드 코드 네이티브 설치(`irm …`)를 사용하세요. |
| `이 시스템에서 스크립트를 실행할 수 없으므로` | PowerShell 실행 정책 Restricted | `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned` 실행 후 **Y** 입력 → 터미널 새로 열기. |
| `npm ERR! network` / ETIMEDOUT | 기관 방화벽·프록시 | ① `npm ping` 으로 확인 ② 사내망이면 전산실에 **registry.npmjs.org 허용** 요청 ③ 임시로 휴대폰 테더링 사용 ④ 클로드 코드는 네이티브 설치로 우회. |
| node 버전이 v18 등 예전 것으로 나옴 | 예전에 설치한 Node가 남아 있음 | **설정 → 앱** 에서 이전 Node.js 제거 → 재부팅 → LTS 다시 설치. 여러 버전이 섞이면 오류가 잦습니다. |
| Current(v26)를 잘못 설치했음 | LTS 대신 최신 버전 선택 | 그대로 써도 대부분 동작하지만, 문제가 생기면 **제어판 → 프로그램 제거** 후 LTS로 다시 설치하세요. |

---

## Node.js 설치 완료 확인

아래가 모두 되면 완료입니다. 다음은 **VS Code 설치**입니다.

### ✅ 완료 체크리스트

- [ ] **LTS 버전을 내려받았다** — 왼쪽 초록색 LTS 카드 (Current 아님)
- [ ] **Add to PATH 가 켜진 채 설치했다** — Custom Setup 화면에서 💾 아이콘 확인
- [ ] **Native Modules 체크는 비워 두었다** — 설치 시간을 크게 줄여 줍니다
- [ ] **설치 후 터미널을 새로 열었다** — 또는 재부팅
- [ ] **node --version 이 v24.x.x 로 나온다** — v로 시작하는 숫자
- [ ] **npm --version 이 정상 출력된다** — 11.x.x 형태

### ➡️ 다음 단계 & 참고

- **④ VS Code 설치 가이드** — 코드를 보고 고칠 편집기를 설치합니다. (**04-vscode-guide**)
- **⑤ Claude Code 설치 가이드** — npm 방식으로 설치할 때 Node.js가 필요합니다.
- **알아 두면 좋은 것** — Node.js를 직접 다룰 일은 거의 없습니다. **클로드 코드가 대신 사용하는 엔진**이라고 생각하세요.
- **업데이트 방법** — 나중에 새 LTS가 나오면 **같은 방식으로 다시 설치**하면 됩니다. 기존 것을 지울 필요 없습니다.

> 최종 확인 명령 `node --version   ·   npm --version`

---

### 📌 출처 (2026-07 기준)

- Node.js 다운로드 — https://nodejs.org/en/download
- Node.js 릴리스 일정(LTS) — https://github.com/nodejs/release#release-schedule

> ※ 본 문서의 브라우저·설치창·터미널 그림은 실제 스크린샷이 아닌 **화면을 재현한 벡터 목업**입니다. 버전에 따라 버튼 위치·문구가 다를 수 있습니다.
