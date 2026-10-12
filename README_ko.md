<p align="center"><img src="videodownloadiyagi.png" width="128" alt="VideoDownloadIyagi"></p>

# VideoDownloadIyagi (비디오다운로드이야기)

브라우저에서 재생되는 영상을 찾아 **PC 에 저장**합니다.

**브라우저 확장**이 영상을 찾고, PC 에 설치하는 **VideoDownloadIyagi 엔진**이 받습니다.
브라우저 안에서 받지 않으므로 큰 영상도 빠르고, 브라우저를 닫아도 다운로드가 계속됩니다.

[English](README.md) · [한국어](README_ko.md)

<p align="center"><img src="popup.png" width="420" alt="확장 팝업"></p>

## 왜 VideoDownloadIyagi 인가

- **보고 있는 영상에서 클릭 한 번.** 재생하고, 도구 모음 아이콘을 누르고, 화질을 고르면 끝. 링크 복사도, m3u8 파일 찾기도 필요 없습니다.
- **큰 영상도 빠르게.** HLS 는 조각 6개를 동시에, 큰 파일은 4갈래로 나눠 받습니다.
- **끊겨도 이어서.** 멈추거나 네트워크가 끊겨도 받던 곳부터 계속합니다.
- **브라우저를 닫아도 계속.** 엔진이 브라우저 탭이 아니라 트레이에서 돕니다.
- **깔끔한 MP4/MKV.** 영상과 음성을 재인코딩 없이 합쳐 화질 손실이 없습니다.
- **개인정보 안전.** 쿠키는 받는 동안 메모리에만 있고, 아무것도 내 PC 밖으로 나가지 않습니다.

---

## ✨ 주요 기능

* **자동 감지** — 페이지가 재생하는 HLS(m3u8)·MP4·WebM 등을 네트워크에서 바로 찾아 도구 모음 배지로 표시
* **화질·음성 선택** — HLS 의 여러 화질(1080p·720p…)과 음성 트랙 중에서 고르기
* **빠른 다운로드** — HLS 조각 6개 동시, 큰 파일은 4갈래로 나눠 동시에
* **이어받기** — 끊기거나 일시정지해도 받은 데까지 이어서
* **무손실 합치기** — 영상·음성을 재인코딩 없이 MP4 / MKV 로 (FFmpeg 필요)
* **AES-128 HLS** — 표준 암호화 스트림 지원
* **로그인 유지** — 브라우저가 쓰던 쿠키·헤더로 받고, 만료되면 확장에서 새로 받아 이어감
* **트레이 상주 엔진** — 작업 목록·진행률·완료 알림, 브라우저를 닫아도 계속
* **지원 시스템** — Windows 10/11 · Ubuntu · Fedora · Arch · 그 밖의 리눅스
* **지원 브라우저** — Chrome · Edge · Chromium · Brave · Vivaldi (Firefox 준비 중)

## 📥 설치

### 1. 엔진

[**Releases**](https://github.com/iyagicom/VideoDownloadIyagi/releases/latest) 에서 내 시스템에 맞는 파일을 받습니다.

| 시스템 | 파일 |
|---|---|
| Windows 10/11 (64비트) | `videodownloadiyagi-v<버전>-windows-x64-setup.exe` (설치) 또는 `…-windows-x64.zip` (압축 풀어 바로 실행) |
| Ubuntu 24.04 | `videodownloadiyagi_<버전>.ubuntu24.04_amd64.deb` |
| Ubuntu 26.04 | `videodownloadiyagi_<버전>.ubuntu26.04_amd64.deb` |
| Fedora | `videodownloadiyagi-<버전>-1.x86_64.rpm` |
| Arch | `videodownloadiyagi-<버전>-1-x86_64.pkg.tar.zst` |
| 그 밖의 리눅스 | `.AppImage` 또는 `.zip` |

```bash
sudo apt install ./videodownloadiyagi_*ubuntu26.04_amd64.deb
```

Windows 설치 파일·deb·rpm·pkg.tar.zst 는 설치만 하면 브라우저에 연결됩니다(Windows 는 관리자 권한 없이 사용자 단위 설치). AppImage·zip 은 **한 번 실행**하면 스스로 연결합니다.
영상·음성을 합치려면 `ffmpeg` 이 필요합니다 — Windows 판에는 들어 있고, 리눅스는 `sudo apt install ffmpeg`. 없으면 트랙을 따로 저장합니다.

### 2. 브라우저 확장

크롬 웹 스토어 등록 전까지는 압축 해제 확장으로 설치합니다.

1. Releases 의 `videodownloadiyagi-extension-<버전>.zip` 을 받아 압축을 풉니다
   (Windows 는 설치 폴더의 `extension`, deb·rpm·zst 는 `/usr/share/videodownloadiyagi/extension` 에 이미 있습니다)
2. 주소창에 `chrome://extensions` (Edge 는 `edge://extensions`) → 오른쪽 위 **개발자 모드** 켜기
3. **압축해제된 확장 프로그램을 로드합니다** → 그 폴더 선택
4. 영상을 재생하고 도구 모음의 아이콘을 눌러 **엔진 연결됨** 이 보이면 끝

## ⚠️ 받을 수 없는 것 및 법적 한계 (필독)

* **DRM 및 암호화 우회 불가:** DRM(Widevine, PlayReady, FairPlay)으로 보호된 콘텐츠는 절대 지원하지 않습니다. 본 소프트웨어는 디지털 저작권 관리 시스템을 우회, 해킹 또는 복호화하는 기능을 일절 포함하고 있지 않습니다.
* **특정 사이트 표적 타겟팅 없음:** 본 프로그램은 특정 스트리밍 제공사나 플랫폼을 표적으로 삼아 취약점을 악용하지 않습니다. 브라우저의 기본 네트워크 트래픽에 이미 공개적으로 노출되어 있는 표준 미암호화 HLS(m3u8) 또는 MP4 스트림만 안전하게 저장하는 범용 네트워크 트래픽 분석 도구입니다.
* **사용자 책임 명시:** 전 세계에는 수천 개 이상의 지역별/국가별 스트리밍 제공사가 존재하며, 개발자가 모든 사이트의 이용 약관을 일일이 확인하는 것은 불가능합니다. 콘텐츠 제공업체의 이용 약관, 지역 법률 및 지식재산권 준수에 대한 책임은 전적으로 서비스를 이용하는 '사용자'에게 있습니다. 본 프로그램은 오직 개인적이고 합법적인 용도로만 사용해 주십시오.


## 🔒 개인정보

쿠키·로그인 정보는 다운로드하는 동안 엔진 메모리에만 두고 파일이나 기록에 남기지 않습니다.
확장과 엔진은 같은 PC 안에서만 통신하며(외부 서버 없음), 로컬 네트워크 포트도 열지 않습니다.
