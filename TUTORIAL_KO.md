# Megalo Image Generator Pro v1.43 초보자 튜토리얼

## 내려받기와 설치

GitHub **Releases**에서 `Megalo_Pro_v1.43_GitHub_Free_protected_20260724.zip`을 받습니다. GitHub가 자동 생성하는 소스 코드 ZIP은 설치 파일이 아닙니다.

ZIP을 완전히 풀고 `chrome://extensions`에서 **개발자 모드**를 켠 뒤 `ko_KR/extension`을 로드합니다.

## Cloud Run 백엔드 업데이트

v1.43에는 신규 Gemini 엔진이 들어갔으므로 v1.42에서 업데이트하는 사용자는 포함된 v1.43 재배포 스크립트로 Cloud Run 백엔드를 다시 배포해야 합니다.

1. `SCENE 장면 생성`을 엽니다.
2. `Vertex / 백엔드 설정`을 펼칩니다.
3. Project ID를 입력합니다.
4. 자동 재배포 스크립트를 생성하고 복사합니다.
5. Google Cloud Shell에서 실행합니다.
6. 출력된 Cloud Run 주소를 같은 슬롯의 Backend URL에 입력합니다.

## v1.43 엔진

- 기본 이미지: `gemini-3.1-flash-image`
- 고품질 이미지: `gemini-3-pro-image`
- 저비용 1K 이미지: `gemini-3.1-flash-lite-image`
- 기본 텍스트: `gemini-3.6-flash`
- 경량 텍스트 대체: `gemini-3.5-flash-lite`

종료된 Preview 이미지 모델은 제거되며, 구형 Preview 선택은 자동 이전됩니다. Flash Lite Image는 1K만 지원합니다.

## 기존 프리셋과 캐릭터 설정 복원

v1.43에서는 예전 프리셋, 캐릭터 파일, 폴더 백업, 암호화 백업을 불러와도 현재 입력된 Backend URL 슬롯 1~10이 덮어써지지 않습니다. 캐릭터·장면·레퍼런스·Project ID·생성 옵션은 정상 복원됩니다.

## 첫 시험

레퍼런스 1장, 장면 1개, 출력 1장으로 시험하세요. Flash Lite Image는 1K를 선택해야 합니다.

## 오류 해결

- **404 모델 없음:** v1.43 백엔드를 재배포하고 모델 위치를 확인합니다.
- **403 권한 오류:** Vertex AI API, IAM, 모델 권한, Project ID를 확인합니다.
- **429 할당량 오류:** 동시 생성, 재시도, 배치 크기를 줄입니다.
- **Failed to fetch:** Backend URL과 Cloud Run 상태를 확인합니다.
