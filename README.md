# Tikker Community Preview

가상 시세로 차트를 탐색하고, 선을 그리고, 나만의 작업 공간을 저장하는
Flutter 차트 앱입니다. Apache-2.0 오픈소스 공개용으로 분리한 버전입니다.

**실제 시세·거래·AI 분석은 제공하지 않습니다.** 가격은 임의 단위이며
투자 판단에 사용할 수 없습니다. 개인용 Tikker와 저장 공간이 분리됩니다.

## 기능

- 가상 종목 4개와 단계별 시세 재생
- 분·일·주·월·년 차트, SMA 및 보조 지표
- 다중 차트, 확대/축소, 이동, 비교
- 추세선과 도형, 색·굵기·선 종류·좌표 편집, 잠금·숨김
- 선과 배치의 로컬 저장, 라이선스 표시

## 실행

Flutter stable 3.41.9 기준. 정확한 검증 버전은 docs/VERIFICATION.md를 확인하세요.

```sh
flutter pub get
flutter run -d chrome
# 또는
flutter run -d macos
```

백엔드, Docker, API 키가 필요하지 않습니다.

## 검증과 홈페이지 빌드

```sh
flutter analyze
flutter test
python3 scripts/audit_public.py
python3 scripts/build_site.py
python3 -m http.server 4318 --directory dist/site --bind 127.0.0.1
```

홈페이지 `/`에서 체험판 `/demo/`와 소스 ZIP을 이용할 수 있습니다.
GitHub: https://github.com/mardien-vosse/tikker-community
배포 완료 여부와 검증 범위는 docs/VERIFICATION.md에 기록합니다.

## 배포 범위

macOS는 독립 실행 빌드를 만들 수 있지만 Developer ID 서명·공증·다른 Mac
검증이 완료되기 전까지 일반 이용자용 다운로드를 게시하지 않습니다.
Windows·모바일·실제 시세 연결은 추후 범위입니다.

[개인정보](docs/PRIVACY.md) · [배포 절차](docs/RELEASE.md) ·
[기여 안내](CONTRIBUTING.md) · [라이선스](LICENSE)
