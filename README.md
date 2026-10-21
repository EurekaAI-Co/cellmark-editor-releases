# Cellmark Editor

A fast, lightweight Markdown editor for Windows that is especially good with tables.

**[Download the latest version](https://github.com/EurekaAI-Co/cellmark-editor-releases/releases/latest)**

This repository only hosts the Windows installers. The source code is not public.

A Korean version of this page is [below](#한국어).

## Features

- **Live editing:** Formatting shows right where you type. Switch at any time to Source or Split view to see the Markdown, or to the publish view for the printed look.
- **Powerful table editing:** Tables with merged cells or multi-row headers are kept intact in [LTEM (LLM-friendly Table-Enhanced Markdown)](https://github.com/hugman/ltem) format. Click a cell to edit it in place. Tables copied from the web, Word or Excel paste in with their merged cells intact.
- **AI table recognition:** Drag over a table in a PDF or HWP document, and it is recognized and brought in as an LTEM table.
- **Only on your PC:** No documents, table images, recognition results or usage data ever leave your PC. AI table recognition also runs on your PC, without any cloud service. Every feature works without the internet.
- **Free:** Free for everyone, for personal use and for work.

The app is available in English and Korean. The license agreement is currently available in Korean only.

## System requirements

- Windows 10 (version 1809 or later) or Windows 11, 64-bit
- About 380 MB of disk space. Table recognition uses about 0.5 GB of extra memory while it runs.
- No graphics card or internet connection is needed.
- Installing requires administrator rights (the app is installed for all users).

## Download

Download `Cellmark-Editor-Setup-<version>.exe` from [Releases](https://github.com/EurekaAI-Co/cellmark-editor-releases/releases/latest). Each release lists the installer's SHA-256 in its notes and in `SHA256SUMS.txt`.

If you cannot download from GitHub, download from our website: <https://eurekax.co/cellmark-editor/releases>

To check that the download is intact, run this in PowerShell and compare the result with the SHA-256 in the release notes:

```powershell
Get-FileHash .\Cellmark-Editor-Setup-<version>.exe -Algorithm SHA256
```

## Install

1. **If "Windows protected your PC" appears, click More info, then Run anyway.**
   Windows shows this for programs it does not know yet. Cellmark Editor is signed with EurekaAI Co., Ltd.'s own (self-signed) certificate, not one from a certificate authority that Windows already trusts, so the publisher shows as "Unknown publisher". If the SHA-256 matches, the file is exactly as we released it.
2. **When asked "Do you want to allow this app to make changes to your device?", click Yes.** The publisher shows as "Unknown" here as well.
3. Read and accept the license agreement, choose an install folder and click **Install**.
4. Start **Cellmark Editor** from the Start menu or the desktop. The license agreement is shown once more the first time you start the app.

### Check the signature (optional)

Right-click the installer and choose **Properties → Digital Signatures**. The signer is **EurekaAI Co., Ltd.** Under **Details → View Certificate → Details**, the **Thumbprint** should match the certificate thumbprint in the release notes.

## Open .md files with Cellmark Editor

Setup registers Cellmark Editor for Markdown (`.md`, `.markdown`) and LTEM (`.lmd`) files. `.lmd` files open in Cellmark Editor right away. Windows does not let an app make itself the default, so if another app already opens `.md` files, choose Cellmark Editor in one of these ways:

- **At the end of setup:** Leave **Also open Markdown (.md) files with Cellmark Editor** checked and click **Finish**. On Windows 11, click **Set default** at the top of the settings page that opens.
- **Open with:** Right-click a `.md` file, choose **Open with → Choose another app**, pick **Cellmark Editor** and click **Always** (Windows 10: check **Always use this app to open .md files** and click **OK**). On Windows 11, click **Show more options** first if you do not see **Open with**.
- **Settings:** On Windows 11, go to **Settings → Apps → Default apps**, click **Cellmark Editor** and choose it for `.md`, `.markdown` and `.lmd`. On Windows 10, go to **Settings → Apps → Default apps → Choose default apps by file type**.

If Cellmark Editor is already running, a file you open is added as a new tab in the same window.

## Updates

- When a new version is out, the app lets you know. Click **New version** in the status bar to download and install it.
- To check for updates, the app only downloads a small file from a fixed address. It sends no information. A downloaded installer runs only after its SHA-256 and signature have been checked.
- Where internet access is blocked, the update check is skipped quietly. You can download a new version from this page and install it over the installed one.
- To turn off the update check, open **ⓘ (About)** in the app and turn off **Check for updates at startup**.

## Uninstall

- **Settings → Apps → Installed apps** (Windows 10: **Apps & features**) → **Cellmark Editor** → **Uninstall**
- Settings, the recent documents list and autosaved text stay in `%APPDATA%\Cellmark Editor`. Delete that folder if you no longer need them.

## For IT administrators

- **Redistribution:** You may distribute the unmodified installer inside your organization, for example through an internal software repository or deployment system, under the terms of the license agreement.
- **Silent install:** From an administrator command prompt, run `Cellmark-Editor-Setup-<version>.exe /S`.
- **Turn off update checks (Group Policy and others):** Set `DisableUpdateCheck` (DWORD) to `1` under `HKLM\SOFTWARE\Policies\EurekaAI\Cellmark Editor`. The app then never connects to check for updates.
- **Default app associations (Group Policy or DISM XML):** The ProgIDs are `CellmarkEditor.Markdown` for `.md` and `.markdown`, and `CellmarkEditor.LTEM` for `.lmd`. The app name is "Cellmark Editor".
- The app does not send documents, table images, recognition results or usage data off the PC. There is no remote error reporting and no usage statistics.

## Contact

Bug reports, feedback, and technology or adoption inquiries: **contact@eurekax.co**. Issues are not used in this repository.
Website: https://eurekax.co

## Trademarks

"Hangul", "Hancom", "HWP" and "HWPX" are registered trademarks of Hancom Inc. Cellmark Editor is not affiliated with, sponsored by, or endorsed by Hancom.

---

## 한국어

이 저장소에는 설치 파일만 있습니다. 소스 코드는 공개하지 않습니다.

Cellmark Editor는 표에 특히 강한, 빠르고 가벼운 Markdown 편집기입니다.

- **라이브 편집:** 쓰는 자리에서 서식이 바로 보입니다. 원문을 보는 소스·나란히 보기와 인쇄 모양을 보는 발행 보기로도 언제든 바꿀 수 있습니다.
- **강력한 표 편집:** 병합한 칸이나 여러 줄 머리글이 있는 표도 [LTEM (LLM-friendly Table-Enhanced Markdown)](https://github.com/hugman/ltem) 형식으로 그대로 담습니다. 표 위에서 칸을 눌러 바로 고칩니다. 웹·워드·엑셀에서 복사한 표도 병합한 칸을 살린 채 붙여 넣을 수 있습니다.
- **AI 표 인식:** PDF·HWP 문서에서 표 영역을 끌어 고르면, 그 표를 인식해 LTEM 표로 옮겨 옵니다.
- **이 PC 안에서만:** 문서, 표 그림, 인식 결과, 사용 정보 등 어떤 정보도 이 PC 밖으로 보내지 않습니다. AI 표 인식도 클라우드를 쓰지 않고 이 PC 안에서 처리합니다. 인터넷이 없어도 모든 기능이 동작합니다.
- **무료:** 개인은 물론 업무용으로도 누구나 무료로 쓸 수 있습니다.

화면은 한국어와 영어를 지원합니다.

### 필요한 것

- Windows 10(1809 이상) 또는 Windows 11, 64비트
- 디스크 약 380MB. 표를 인식할 때 메모리를 약 0.5GB 더 씁니다.
- 그래픽 카드와 인터넷 연결은 필요 없습니다.
- 설치에는 관리자 권한이 필요합니다(모든 사용자용으로 설치됩니다).

### 내려받기

[Releases](https://github.com/EurekaAI-Co/cellmark-editor-releases/releases/latest)에서 `Cellmark-Editor-Setup-<판>.exe`를 받습니다. 릴리스마다 설치 파일의 SHA-256을 본문과 `SHA256SUMS.txt`에 적어 둡니다.

GitHub에서 받을 수 없으면 홈페이지에서 받습니다: <https://eurekax.co/cellmark-editor/releases>

받은 파일이 온전한지 확인하려면, PowerShell에서 아래 명령의 결과가 릴리스 본문의 SHA-256과 같은지 봅니다.

```powershell
Get-FileHash .\Cellmark-Editor-Setup-<판>.exe -Algorithm SHA256
```

### 설치하기

1. **"Windows의 PC 보호" 창이 뜨면 [추가 정보] → [실행]을 누릅니다.**
   Windows가 처음 보는 프로그램이라서 뜨는 경고입니다. Cellmark Editor는 Windows가 미리 알고 있는 인증 기관의 서명 대신 (주)유레카에이아이의 자체 서명을 씁니다. 그래서 게시자가 "알 수 없는 게시자"로 보입니다. SHA-256이 같으면 받은 파일은 배포한 그대로입니다.
2. **"이 앱이 디바이스를 변경할 수 있도록 허용하시겠어요?"에서 [예]를 누릅니다.** 여기서도 게시자는 "알 수 없음"으로 보입니다.
3. 사용권 계약서를 읽고 동의합니다. 설치할 폴더를 고르고 [설치]를 누릅니다.
4. 설치가 끝나면 시작 메뉴나 바탕화면의 **Cellmark Editor**로 실행합니다. 처음 실행할 때 사용권 계약서를 한 번 더 묻습니다.

#### 서명 확인 (선택)

설치 파일을 마우스 오른쪽 단추로 누르고 [속성] → [디지털 서명]을 보면 서명자가 **EurekaAI Co., Ltd.**입니다. [자세히] → [인증서 보기] → [자세히]의 "지문"이 릴리스 본문의 인증서 지문과 같으면 (주)유레카에이아이가 서명한 파일입니다.

### .md 파일을 두 번 눌러 열기

설치하면 Cellmark Editor가 Markdown(`.md`, `.markdown`)과 LTEM(`.lmd`) 문서를 여는 프로그램으로 Windows에 등록됩니다. `.lmd` 파일은 바로 Cellmark Editor로 열립니다. Windows에서는 프로그램이 스스로 기본 앱이 될 수 없으므로, 다른 프로그램이 이미 `.md`를 열고 있다면 아래 방법 가운데 하나로 Cellmark Editor를 고릅니다.

- **설치를 마칠 때:** 마지막 화면의 **[Markdown(.md) 문서도 Cellmark Editor로 열기]**에 표시한 채로 **[마침]**을 누릅니다. Windows 11은 열린 설정 화면 위쪽의 **[기본값으로 설정]**을 누릅니다.
- **연결 프로그램:** `.md` 파일을 마우스 오른쪽 단추로 누르고 **[연결 프로그램] → [다른 앱 선택]**에서 **Cellmark Editor**를 고른 뒤 **[항상]**을 누릅니다(Windows 10: **[항상 이 앱을 사용하여 .md 파일 열기]**에 표시하고 **[확인]**). Windows 11에서 [연결 프로그램]이 안 보이면 먼저 [추가 옵션 표시]를 누릅니다.
- **Windows 설정:** Windows 11은 **설정 → 앱 → 기본 앱**에서 **Cellmark Editor**를 눌러 `.md`, `.markdown`, `.lmd`를 고릅니다. Windows 10은 **설정 → 앱 → 기본 앱 → [파일 형식별 기본 앱 선택]**에서 고릅니다.

Cellmark Editor가 이미 켜져 있으면 연 파일은 켜져 있는 창에 새 탭으로 열립니다.

### 업데이트

- 새 판이 나오면 앱이 알려 줍니다. 상태 막대의 "새 판"을 눌러 받고 설치합니다.
- 앱은 업데이트를 확인할 때 정해진 주소의 작은 파일을 내려받기만 하고, 아무 정보도 보내지 않습니다. 받은 설치 파일은 SHA-256과 서명을 확인한 뒤에만 실행합니다.
- 인터넷이 막힌 곳에서는 업데이트 확인을 조용히 건너뜁니다. 이 페이지에서 새 판을 받아 설치된 판 위에 그대로 설치하면 됩니다.
- 업데이트 확인을 끄려면 앱의 **ⓘ(프로그램 정보)**에서 "시작할 때 새 판 확인"을 끕니다.

### 지우기

- **설정 → 앱 → 설치된 앱**(Windows 10: **앱 및 기능**) → **Cellmark Editor** → **제거**
- 설정과 최근 문서 목록, 자동 저장본은 `%APPDATA%\Cellmark Editor` 폴더에 남습니다. 필요 없으면 지웁니다.

### 기관 전산 담당자께

- **재배포:** 고치지 않은 설치 파일은 기관 내부 저장소나 배포 시스템에 올려 직원 PC에 설치하게 할 수 있습니다. 조건은 사용권 계약서를 따릅니다.
- **무인 설치:** 관리자 권한 명령 창에서 `Cellmark-Editor-Setup-<판>.exe /S`
- **업데이트 확인 끄기(그룹 정책 등):** 레지스트리 `HKLM\SOFTWARE\Policies\EurekaAI\Cellmark Editor`에 `DisableUpdateCheck`(DWORD) = `1`. 그러면 앱이 업데이트를 확인하려고 접속하지 않습니다.
- **기본 앱 일괄 지정(그룹 정책·DISM 기본 앱 연결 XML):** ProgID는 `.md`·`.markdown` → `CellmarkEditor.Markdown`, `.lmd` → `CellmarkEditor.LTEM`입니다(앱 이름 "Cellmark Editor").
- 앱은 문서, 표 그림, 인식 결과, 사용 정보를 PC 밖으로 보내지 않습니다. 원격 오류 보고·사용 통계도 없습니다.

### 문의

버그 제보와 의견, 기술 협력·도입 문의: **contact@eurekax.co**. 이 저장소는 Issues를 쓰지 않습니다.
홈페이지: https://eurekax.co

### 상표

"한글", "한컴", "HWP", "HWPX"는 주식회사 한글과컴퓨터의 등록 상표이며, Cellmark Editor는 한글과컴퓨터와 제휴, 후원, 승인 관계가 없습니다.

---

© 2026 EurekaAI Co., Ltd. All rights reserved.
