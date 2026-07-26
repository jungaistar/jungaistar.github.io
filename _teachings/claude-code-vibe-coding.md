---
layout: course
title: 클로드 코드로 시작하는 바이브 코딩 — 행정직원 실무 과정
description: 코딩을 전혀 몰라도 한국어로 말해서 업무용 프로그램을 만드는 과정입니다. GitHub·Git·Node.js·VS Code·Claude Code 5개 프로그램 설치부터 첫 프로그램 제작까지, 화면을 보며 그대로 따라 합니다.
instructor: 정동엽 (직업미래연구소 소장)
year: 2026
term: 하반기
location: 한국외국어대학교
time: 4시간 (설치 1시간 + 실습 3시간)
course_id: claude-code-vibe-coding
schedule:
  - week: 1
    date: 1교시
    topic: 왜 지금 바이브 코딩인가
    description: AI가 바꾸는 사무 업무의 지형, 행정 업무에서 자동화할 수 있는 일과 없는 일 구분하기.
    materials:
      - name: 전체 가이드 목차
        url: /guides/claude-code/

  - week: 2
    date: 2교시
    topic: 개발 환경 준비 — 5개 프로그램 설치
    description: GitHub 가입부터 Claude Code 설치까지. 화면 그림의 주황색 번호를 따라 그대로 진행합니다. 모든 명령어는 복사 버튼으로 붙여넣습니다.
    materials:
      - name: ① GitHub 가입 & 저장소 만들기
        url: /guides/claude-code/01-github-guide_v1.0_20260726.html
      - name: ② Git 설치 & 사용 시작
        url: /guides/claude-code/02-git-guide_v1.0_20260726.html
      - name: ③ Node.js LTS 설치
        url: /guides/claude-code/03-nodejs-guide_v1.0_20260726.html
      - name: ④ VS Code 설치 & 실행
        url: /guides/claude-code/04-vscode-guide_v1.0_20260726.html
      - name: ⑤ Claude Code 설치 & 실행
        url: /guides/claude-code/05-claude-code-guide_v1.0_20260726.html

  - week: 3
    date: 3교시
    topic: 첫 프로그램 만들기 — 한국어로 요청하기
    description: 작업 폴더를 만들고 claude 를 실행해 웹페이지 한 장을 만들어 봅니다. 승인(Yes) 절차와 수정 요청 방법을 익힙니다.
    materials:
      - name: ⑤ Claude Code 가이드 (STEP 7–9)
        url: /guides/claude-code/05-claude-code-guide_v1.0_20260726.html

  - week: 4
    date: 4교시
    topic: 업무에 적용하기 & 스스로 문제 해결하기
    description: 반복 문서 작업 자동화 사례, 좋은 요청문 쓰는 법, 오류가 났을 때 각 가이드의 문제 해결표로 스스로 해결하는 방법.
    materials:
      - name: 문제 해결 모음 (각 가이드 뒤쪽)
        url: /guides/claude-code/
---

## 과정 소개

**"코딩을 배우는 과정이 아닙니다. 코딩을 시키는 과정입니다."**

행정 업무를 하며 "이거 자동화하면 좋겠는데" 싶었던 일들을, 프로그래밍 언어 대신 **한국어 문장**으로 요청해서 해결하는 방법을 배웁니다. 참가자는 코드를 한 줄도 직접 쓰지 않습니다.

## 실습 가이드 (온라인)

강의에 사용하는 설치 가이드는 아래에서 언제든 다시 볼 수 있습니다. 화면을 재현한 그림 위에 **주황색 번호**가 표시되어 있고, 오른쪽 실행 순서의 번호와 1:1로 대응합니다.

<div class="row justify-content-sm-center my-4">
  <div class="col-sm-10">
    <a href="/guides/claude-code/" class="btn btn-primary btn-lg w-100 py-3">
      📚 클로드 코드 설치 따라하기 — 5단계 가이드 열기
    </a>
  </div>
</div>

| 순서 | 가이드 | 소요 | 핵심 포인트 |
|:---:|:---|:---:|:---|
| ① | [GitHub 가입 & 저장소 만들기](/guides/claude-code/01-github-guide_v1.0_20260726.html) | 약 10분 | 설치 없음(웹 가입) · 2단계 인증 필수 |
| ② | [Git 설치 & 사용 시작](/guides/claude-code/02-git-guide_v1.0_20260726.html) | 약 10분 | 설치 중 확인할 화면은 단 3개 |
| ③ | [Node.js LTS 설치](/guides/claude-code/03-nodejs-guide_v1.0_20260726.html) | 약 7분 | 반드시 **LTS** 선택 (Current 아님) |
| ④ | [VS Code 설치 & 실행](/guides/claude-code/04-vscode-guide_v1.0_20260726.html) | 약 8분 | "PATH에 추가" 체크 확인 |
| ⑤ | [Claude Code 설치 & 실행](/guides/claude-code/05-claude-code-guide_v1.0_20260726.html) | 약 10분 | 명령 한 줄로 설치 · 유료 플랜 필요 |

> 각 가이드에는 **명령어 복사 버튼**과 **문제 해결표**가 들어 있습니다. 강의 중 막히면 해당 가이드 뒤쪽의 문제 해결 슬라이드를 먼저 확인하세요.

## 학습 목표

- AI 코딩 도구가 무엇을 대신해 주고 무엇을 대신해 주지 못하는지 판단할 수 있다
- 개발 환경 5종을 스스로 설치하고, 설치 오류를 가이드를 보며 혼자 해결할 수 있다
- 원하는 결과를 **구체적인 한국어 문장**으로 요청할 수 있다
- 만들어진 결과를 확인하고 수정을 요청하는 반복 과정을 수행할 수 있다
- 업무 중 반복 작업을 발견하고 자동화 후보로 정리할 수 있다

## 수강 대상

- 코딩 경험이 전혀 없는 **대학·공공기관 행정직원**
- 엑셀·한글 반복 작업에 시간을 많이 쓰는 실무자
- AI 도구를 업무에 적용해 보고 싶은 사무직

## 준비물

| 구분 | 내용 |
|:---|:---|
| 장비 | Windows 10 / 11 노트북 (관리자 권한 권장) |
| 계정 | 본인 이메일 · 스마트폰(2단계 인증용) |
| 필수 | **Claude 유료 플랜 계정**(Pro·Max 등) — 무료 플랜은 Claude Code 사용 불가 |
| 비용 | 설치하는 프로그램 5종은 모두 무료 |

## 진행 방식

- 강사 시연 → 참가자 실습 → 개별 확인의 3단 반복
- 설치 단계마다 **버전 확인 명령**으로 성공 여부를 즉시 점검
- 뒤처지는 참가자는 온라인 가이드의 해당 번호로 바로 복귀

## 기대 효과

- 반복 문서 작업의 자동화 후보를 스스로 식별
- 외주·전산 의뢰 없이 간단한 업무 도구를 직접 제작
- AI 시대에 필요한 **디지털 문해력(AI 리터러시)** 확보
