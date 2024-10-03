# 개요

**MyStreamLiveMedia 대시보드**는 방송 송출 및 시청을 위한 통합 관리 플랫폼입니다. 사용자는 대시보드를 활용해 실시간으로 채널을 생성하고, 설정을 조정하며, 모니터링할 수 있습니다.

<br>

## 주요 기능

- **채널 생성 및 관리**: 사용자는 쉽게 새로운 라이브 채널을 생성하고, 기존 채널의 정보를 수정할 수 있습니다.
- **Configuration 설정**: 대시보드의 설정 옵션을 통해 채널 수, 암호화, VOD 및 트랜스코딩 프로필을 세부적으로 조정할 수 있습니다.
- **Viewers 관리**: 방송의 최대 시청자 수를 조정하고 시청자 수를 표시할 수 있습니다.
- **S3 설정**: 저장된 파일을 송출하고 파일을 관리할 수 있습니다.
- **보안 및 인증 관리**: 방송 접근에 필요한 인증 정보를 설정하고, API로 요청할 수 있습니다.

<br>

## 역할별 이용 권한

MyStreamLiveMedia 대시보드 이용 권한 및 권한별 수행할 수 있는 작업은 다음과 같습니다.

| 권한 | 프로젝트 | 채널 |
| :--: | :--: | :--: |
| 관리자 | 프로젝트 생성<br>프로젝트 삭제<br>프로젝트 정보 변경<br>프로젝트 멤버 추가 및 삭제 | 채널 생성<br>채널 모든 정보 변경 |
| 운영자 | 프로젝트 생성<br>프로젝트 정보 변경<br>프로젝트 멤버 추가 및 삭제| 채널 기본 정보 변경<br>채널 상세 정보 변경 |
| 개발자 | 프로젝트 정보 변경 | 채널 상세 정보 변경<br>채널 상세 정보 조회 |
| 게스트 | 프로젝트 조회 | 채널 정보 조회 |

<br>

# MyStreamLiveMedia 채널

방송 송출 및 시청을 위한 채널 정보를 입력합니다.

<br>

## MyStreamLiveMedia 채널 생성하기

MyStreamLiveMedia 채널 생성하는 방법은 다음과 같습니다.

1. 프로젝트 선택하기 
    헤더에서 마이스트림 채널을 생성하려는 프로젝트를 선택합니다. 
    * 미디어라이브 서비스는 프로젝트 단위로 관리됩니다.

2. 채널 생성하기
    왼쪽 내비게이션 바에서 **[Create]** 버튼을 클릭하면, 라이브 채널 생성을 위한 입력 모달이 나타납니다. 
    - 처음 설정하는 라이브 서비스는 알파 버전부터 시작합니다.

3. 생성 정보 입력하기(기본 정보 + Configuration)
    입력 모달에 MyStreamLiveMedia 기본 정보를 입력하고, 총 4개의 탭으로 구성된 라이브 환경 설정을 완료한 후 저장합니다. 입력한 라이브 정보는 임시 저장됩니다. 

    | **참고** <br>저장 후에는 동영상 미리보기 정보를 추가로 설정할 수 있습니다. |
    | --- |

4. 정보 저장하기
    확인한 정보를 최종적으로 저장하면 MyStreamLiveMedia 설정이 완료됩니다. 저장된 내역은 히스토리에 기록되며, **채널 상세 정보** 페이지 하단에서 변경 정보의 버전을 비교하여 확인할 수 있습니다.

5. 정보 저장하기
    확인한 정보를 최종적으로 저장하면 MyStreamLiveMedia 설정이 완료됩니다. 저장된 내역은 히스토리에 기록되며, **채널 상세 정보** 페이지 하단에서 변경 정보의 버전을 비교하여 확인할 수 있습니다.

<br>

## MyStreamLiveMedia 채널 정보 수정

저장된 채널의 정보는 언제든지 수정할 수 있습니다. 기본 정보는 히스토리에 기록되지 않지만, Configuration 정보는 진행 상황이 히스토리에 기록됩니다.

> **참고**
<br>채널의 정보 중 몇몇 값은 환경 설정상 수정할 수 없습니다.

### 기본 정보 및 Configuration 수정하기

1. 상세 정보 화면에서 각 섹션 우측 상단의 **[Edit]** 버튼을 클릭해 변경할 내용을 입력합니다.
2. **[Save]** 버튼을 누르면 바로 배포됩니다. 

## Channel and input details 설정하기

> Volume

동시 방송 횟수에 따라 필요한 채널 수가 확정되었다면 **Channels** 메뉴를 선택하고 채널 규모를 입력합니다.
- 채널은 최대 50개까지 입력할 수 있습니다.

> **안내** 
<br> 30개 이상의 채널이 필요하다면, 운영 3개월 전 medialive_help@media.com을 통해 먼저 상담 후 입력하시기 바랍니다. 상담하지 않은 경우, 생성 요청이 실패할 수 있습니다.

> Encrypt HLS content

 Encrypt HLS를 활성화하면, HLS 사양에 따라 콘텐츠가 암호화되어 시청자에게 전달됩니다. 이 기능을 설정하면 암호화 정보를 제공해야 합니다.

>  VOD

방송 후 방송을 저장해서 VOD로 제공할 수 있습니다. VOD 사용 여부와 VOD 저장 기간을 설정합니다. 
- 최대 10일까지 설정 가능합니다.

> 트랜스코딩 프로필

영상을 트랜스코딩할 프로필을 설정합니다.

| 설정 항목 | 설명 | 기본값 |
| :--: | :--: | :--: |
| Input stream 설정 | 입력 영상에 적용할 프로필을 설정합니다. | 1080p HD / HEVC / 20Mbps |
| Output stream 설정 | 출력 영상에 적용할 프로필을 설정합니다. | 1080p HD / 720p HD / 480 SD |


![트랜스코딩 프로필 설정](https://drive.google.com/uc?id=1aI-N4P18LxMALL32w_oyyvgo2vVvFr5C)

<br>

# Viewers 설정

Viewers는 방송의 스트리밍 시청 인원 수를 설정합니다.

<br>

> Max viewers

라이브 스트리밍을 볼 수 있는 최대 인원을 설정합니다. 

> **참고**
<br> 3000명이 넘는 인원을 설정하고 싶다면, 상담을 요청하시기 바랍니다.


> Viewer count

**Private mode**와 **Public mode** 중에서 선택하여 시청자 수가 보이게 하거나 안 보이게 할 수 있습니다. 

- Private mode인 경우 스트리머만 숫자를 볼 수 있습니다.

> Viewer count type

실시간 시청자 수 또는 총 시청자 수 중 어떤 정보를 플레이어에 표시할 지 설정할 수 있습니다.

> Report

방송을 신고할 수 있는 기능 사용 여부를 결정할 수 있습니다. MyMonitoringSystem과 연계해 신고된 방송 정보를 확인할 수 있습니다. 

<br>

<aside>
참고. 연계를 위해 MyMonitoringSystem에 생성한 프로젝트 ID와 대상 국가를 설정해야 합니다. 국가 목록에서 신고 기능을 반영할 국가를 고르거나 표준 국가 코드를 참고하여 직접 입력할 수 있습니다. 
- 국가 코드: 2자
</aside>

<aside>

주의. 채널 저장 후엔 MyMonnitoringSystem 정보 수정할 수 없습니다. 수정이 필요한 경우, 고객 센터로 문의 바랍니다.

</aside>

<br>

# S3 설정

S3에 저장된 파일을 MediaLive 서비스는 유튜브로 송출할 수 있습니다.

<br>

## S3와 연계하기

MediaLive 서비스 S3와 연계하려면 이 옵션을 활성화합니다. 활성화하면 아래의 추가 옵션들을 설정할 수 있습니다.

> 추가 옵션 설정

- 송출 허용 파일의 종류 설정
- Player mode 설정

| 설정 항목 | 설명 |
| :--: | :--: | :--: |
| Landscape mode 설정 | - 활성화: 플레이어에서 시청자가 Landscape mode와 Portrait mode를 선택하여 시청할 수 있습니다. <br> - 비활성화: 세로 이미지는 세로 모드에서만 시청할 수 있습니다. |
| Viewer count shown 설정 | 실시간 시청자 수 또는 총 시청자 수 중 어떤 정보를 플레이어에 표시할 지 설정할 수 있습니다. |



# Authentication

**Authentication** 메뉴에서는 보안을 위해 접근에 필요한 인증 정보를 관리하고 설정할 수 있습니다.

<br>

## Use authentication 설정

API 접근에 필요한 인증 설정할 수 있습니다.

<br>

## API URL

API URL을 입력합니다. 

```jsx
https://console.mystreamlivemedia.com/api/v1/configuration/{projectId}/{channelId}
```

MyStreamLiveMedia 서비스 설정을 API를 통해 확인하고 가져올 수 있습니다. 설정 이름은 대시보드 이름과 동일합니다.

 `{projectId}`: 특정 프로젝트의 고유 ID

 `{channelId}`: 특정 채널의 고유 ID

<br>

## Headers

- Header를 추가하려면 **[Add]** 버튼을 클릭하여 입력합니다.
- Header 입력 시 대소문자를 구분해서 입력해야 합니다.

<br>

> API 설정 예시

인증 및 설정 정보를 포함한 API 요청 예시입니다.

```json
{
  "authentication": {
    "use": true,
    "apiurl": "https://api.example.com/v1/auth/login",
    "headers": [
      "Authorization",
      "Content-Type",
      "x-security-token"
    ]
  },
  "viewer": {
    "max": 3,000,
    "count": "private",
    "viewercounttype": "SHARED",
    "report": {
      "mmsProjectId": "A1B2C3",
      "country": "ko"
    }
  },
  "s3": {
    "use": "true",
    "type": [
      "MP4",
      "AVI",
      "M4V"
    ],
    "lanscape": true
  },
  "info: {
    "projectId": "sample123",
    "volume": 10,
    "vod": {
      "use": false
    }
  }
}
```