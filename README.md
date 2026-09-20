# 탐정 진구지 사부로: 꿈의 끝에서 — 한국어 패치 v0.8.5

Sega Saturn 일본판의 비공식 한국어 패치입니다. 원본 게임은 포함하지 않으며, 아래 SHA-256과 일치하는 원본 BIN이 필요합니다.

**[v0.8.5 패치 다운로드](https://github.com/lf-idonotknow/Jinguuji-Yume-Saturn-Korean-Patch/releases/tag/v0.8.5)**

릴리스의 **Assets**에서 `Jinguuji-Yume-Saturn-Korean-Patch-v0.8.5.zip`을 받으세요. GitHub가 자동으로 표시하는 `Source code (zip)`은 패치가 아닙니다.

## v0.8.5 변경 사항

- 번역을 더 자연스럽고 매끄럽게 다듬었습니다.
- SAROO를 이용한 새턴 실기와 MiSTer에서 동작하도록 호환성 문제를 수정했습니다.

이전 버전의 한글화 내용을 모두 포함한 누적 패치입니다. **v0.8.0 위에 덧씌우지 말고 수정하지 않은 일본판 원본에 적용하세요.**

## 준비물

- 아래 해시와 일치하는 수정하지 않은 일본판 단일 BIN 파일
- 이 패치 ZIP을 압축 해제한 폴더
- [Delta Patcher 공식 다운로드](https://github.com/marco-calautti/DeltaPatcher/releases/latest)
  - Windows 일반 64비트 PC: `windows_bin_x86_64.zip`
  - macOS: `macos11+_bin_universal.zip`(macOS 11 이상)
- 원본 보관 공간 외에 약 3GB 이상의 여유 공간

패치 도구는 별도로 받습니다. 프로그램을 실행할 수 없다면 운영체제에 맞는 파일인지 확인하세요. 보안 기능을 일괄 해제하지 마세요.

## 적용 방법 — 순서대로 따라 하세요

1. 원본 BIN/CUE는 안전한 곳에 보관합니다. **별도의 작업 폴더를 만들고 원본 BIN을 복사**합니다. 이후에는 이 복사본만 선택합니다.
2. 가능하면 아래 방법으로 복사본 BIN의 SHA-256을 확인합니다. 원본 해시와 다르면 적용하지 마세요. 파일 이름만 바꾸어도 판본이 같아지는 것은 아닙니다.
3. Delta Patcher를 실행해 패치 적용 화면을 엽니다.
4. **Original file**에 작업 폴더의 BIN 복사본을 선택합니다. CUE를 선택하는 것이 아닙니다.
5. **XDelta patch**에 동봉한 `Jinguuji-Yume-Saturn-Korean-Patch-v0.8.5.xdelta`를 선택합니다.
6. 설정에서 **Checksum validation**은 켜 둡니다. 여기서는 원본을 따로 보관하고 복사본에 적용하므로 **Backup original file**은 끈 상태로 진행합니다. 이 설정에서는 선택한 복사본이 한글판으로 교체됩니다.
7. **Apply patch**를 누르고 완료될 때까지 기다립니다. 오류가 나면 진행하지 말고 아래 주의사항을 확인하세요.
8. 적용된 BIN의 이름을 아래 이름으로 바꿉니다. `.bin.bin`처럼 확장자가 두 번 붙지 않도록 주의하세요.

   `Tantei_Jinguuji_Saburou-Yume_no_Owari_ni_JAP_KR_DEV.bin`

9. ZIP에 들어 있는 `Tantei_Jinguuji_Saburou-Yume_no_Owari_ni_JAP_KR_DEV.cue`를 같은 폴더에 넣습니다.
10. 아래 적용 후 해시와 일치하는지 확인한 뒤 실행 환경에 맞게 BIN/CUE를 함께 복사합니다. 에뮬레이터나 MiSTer에서 이미지를 선택할 때는 **동봉된 CUE**를 사용합니다. SAROO에서는 게임 폴더에 두 파일을 함께 넣고 게임 목록에서 선택합니다.

최종 폴더에는 다음 두 파일이 함께 있어야 합니다. 이름의 `KR_DEV`는 현재 패치가 사용하는 고정 파일명입니다.

```text
Tantei_Jinguuji_Saburou-Yume_no_Owari_ni_JAP_KR_DEV.bin
Tantei_Jinguuji_Saburou-Yume_no_Owari_ni_JAP_KR_DEV.cue
```

## 원본 및 패치 적용 후 SHA-256

해시는 파일 내용을 확인하는 식별값입니다. 파일 이름과 무관하며, 아래 값과 한 글자라도 다르면 동일한 파일이 아닙니다.

**원본 BIN — 665,719,488바이트**

```text
4c473477677053c2b8026b0e95d005339cd6fe14090c10cf5ddf5dbb6d2e7b4b
```

**패치 적용 후 BIN — 670,080,096바이트**

```text
d12f7d4abb4eec56444eb94efd354b8753d010d40fe61f50501f2d0894e1c956
```

**동봉 CUE — SHA-256**

```text
be1d54edd4e2667ffd6d8f4a526e0876b563fac16aef6b5799be69ade205d48c
```

### 해시 확인 방법

Windows에서는 PowerShell을 열고 다음 명령의 경로를 실제 BIN 위치로 바꿔 실행합니다. 출력된 `Hash`를 비교하세요. 영문 대소문자는 무관합니다.

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath "C:\게임\원본.bin"
```

macOS에서는 터미널에서 다음 명령의 경로를 바꿔 실행합니다. 출력 맨 앞의 긴 문자열을 비교하세요.

```sh
shasum -a 256 "/게임/원본.bin"
```

적용 후에도 같은 방법으로 완성된 BIN을 검사합니다.

## 주의사항과 오류 해결

- **기존 원본 CUE를 사용하지 마세요.** 한글판은 파일 크기와 오디오 트랙 시작 위치가 달라 동봉 CUE가 필요합니다.
- 원본 보관본에 직접 적용하거나, 이전 한글판 위에 다시 적용하지 마세요. 항상 해시가 맞는 원본 복사본에서 시작합니다.
- CHD, ISO, 여러 개로 나뉜 트랙 BIN에는 이 패치를 직접 적용하지 않습니다. 다른 형식을 변환했더라도 BIN의 해시가 지원 원본과 정확히 일치해야 합니다.
- 체크섬 오류가 나면 원본 판본과 해시, ZIP 압축 해제 여부를 확인하세요. **체크섬 검사를 끄거나 강제로 적용하지 마세요.**
- 실행 파일을 찾지 못한다면 BIN과 CUE가 같은 폴더에 있는지, BIN 이름이 위 안내와 정확히 같은지 확인하세요.
- BIN 이름을 임의로 바꿨다면 CUE를 텍스트 편집기로 열어 첫 `FILE "…" BINARY` 줄의 따옴표 안도 실제 BIN 이름과 확장자에 맞게 바꾸세요. `TRACK`, `INDEX`와 시간 값은 바꾸지 마세요. CUE 파일명 자체는 BIN과 같을 필요가 없습니다. CUE를 수정하면 동봉 CUE 해시와는 달라지지만 BIN 해시는 변하지 않습니다.
- 패치 전 또는 다른 버전의 세이브스테이트에는 옛 게임 코드와 그래픽이 남을 수 있습니다. 업데이트 후에는 게임을 완전히 종료하고 새 CUE로 실행하세요. 이상이 있으면 세이브스테이트 대신 게임 내 일반 세이브로 확인하세요.
- 세이브 데이터는 미리 백업하세요. 모든 환경과 세이브의 호환성을 보장하지 않습니다.
- 원본 게임 이미지와 BIOS는 제공하지 않습니다.

## 포함 내용과 검증 범위

현재 누적 한글화 빌드의 대사·메뉴·안내도·선택지 수정, 영상 자막과 잡음 제거 테이프의 한국어 자막을 포함합니다. 스토리상 잡음이 남은 테이프에는 자막을 표시하지 않습니다.

**이 버전은 검수 중인 프리릴리스입니다.** 사용자가 SAROO 새턴 실기와 MiSTer 동작을 확인했으며, 최근 저장·불러오기 후 복귀 정지 수정 이후 정상 작동도 확인했습니다. 모든 문구·루트·펌웨어 환경과 자막 동기까지 검증을 끝낸 최종판을 뜻하지는 않습니다.

원본에 xdelta3 3.1.0으로 패치를 적용해 만든 BIN이 기준 한글판과 크기·SHA-256까지 일치하는 것은 확인했습니다. 이는 패치 적용의 무결성 검증이며, 전체 게임 플레이 완료나 모든 패치 도구·에뮬레이터에서의 실행 검증을 뜻하지 않습니다.

## 오류 제보

[Issues](https://github.com/lf-idonotknow/Jinguuji-Yume-Saturn-Korean-Patch/issues)에 버전, 사용 환경, 루트·장면, 재현 순서, 화면 사진을 남겨 주세요. 원본/적용 후 BIN 해시도 적어 주시면 확인에 도움이 됩니다. 게임 이미지나 BIOS는 첨부하지 마세요.

## 글꼴

[Galmuri](https://github.com/quiple/galmuri) — Copyright (c) 2019–2025 Lee Minseo. SIL Open Font License 1.1. ZIP에 포함된 `LICENSE-Galmuri.txt`를 참조하세요.
