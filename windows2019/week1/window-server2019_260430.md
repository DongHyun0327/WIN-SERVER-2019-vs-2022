# Windows Server 2019 Study Week 1

> Windows Server 2019 설치, Desktop Mode/Core Mode 비교, 초기 보안 설정 실습 정리 문서입니다.
>
> 이미지가 많은 문서라 이미지가 잘리지 않도록 모든 이미지는 `max-width:100%; height:auto;` 속성을 적용했습니다.

## Windows Server 2019 설치 및 초기 보안설정

**서버 Mode별 설치 과정 및 초기 보안설정은 아래 토글을 눌러서 확인하시면 좋습니다.**

## VMware에 Windows Server 2019 설치
### 가상머신 생성

먼저 마이크로소프트 홈페이지에서 ISO파일을 다운로드 합니다.
[Windows Server 2019 ISO 다운로드](https://www.microsoft.com/ko-kr/evalcenter/download-windows-server-2019)
<p align="center"><img src="attachment:f4319db5-0231-4417-978f-870c583101a6:스크린샷_2026-04-26_125807.png" alt="스크린샷 2026-04-26 125807.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

Typical 유형을 선택합니다.

<p align="center"><img src="attachment:e3e1bf81-2722-4796-958d-b2d6cb5aaf36:스크린샷_2026-04-26_130518.png" alt="스크린샷 2026-04-26 130518.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

ISO 파일이 다운로드가 완료되었을 경우 자신 있으시면 , disc이미지에 넣어서 바로 설치해도 됩니다. ISO 파일이 아직 다운중이시라면, 먼저 가상머신을 생성한 후에 ISO 이미지를 설치해도 됩니다. 저희는 실습 환경을 위해서 ISO파일을 나중에 설치하기로 합니다.

<p align="center"><img src="attachment:a90e2998-fe06-4018-a20c-87415ad84dae:스크린샷_2026-04-29_140025.png" alt="스크린샷 2026-04-29 140025.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

저희가 설치할 운영체제는 Windows Server 2019이기 때문에, 2019 버전을 찾아 선택합니다.

<p align="center"><img src="attachment:bec7284b-7735-4a9f-bff5-cdd3b4fe405f:스크린샷_2026-04-26_130548.png" alt="스크린샷 2026-04-26 130548.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

디스크의 최대 용량은 시스템에서 추천해주는대로 60GB로 설정합니다. 용량이 부족할 경우 설치 단계 혹은 설치 후에도 많은(?) 문제가 발생할 수 있습니다.

그리고 설치 후 가상 디스크를 분할할 것인지 단일 디스크로 사용할 것인지를 물어봅니다.

둘의 차이점은 많은 분들이 이미 아실 겁니다.

- Single file : Windows Server 2019(최대 60GB)를 메인PC에 하나의 단일 파일로 저장

    ⇒ 파일 개수가 적어 관리가 단순함

- Multiple file : 메인 PC에 여러개의 파일로 분할해서 저장

    ⇒ 성능, 기능에 큰 차이는 없으나, 백업, 이동, 압축 등이 자주 일어난다면 multiple file로 저장하는것이 유리

저희 환경에서는 split을 선택, 설치하는것이 좋습니다. 저희는 현업자 마인드를 탑재해야 하니까.

<p align="center"><img src="attachment:ca942e9c-a27e-4b60-a3ae-c914f0ab1728:스크린샷_2026-04-26_130706.png" alt="스크린샷 2026-04-26 130706.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

최종적으로 설정을 확인한 후에 완료(Finish) 버튼을 누릅니다.

<p align="center"><img src="attachment:3d24aa1b-31f5-4e0c-b10e-b4207f04c1cd:스크린샷_2026-04-26_130712.png" alt="스크린샷 2026-04-26 130712.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

설치가 끝난 후에는 창 왼쪽의 CD/DVD(SATA)를 클릭해 아까 설치하지 않은 ISO 파일을 설치하도록 합니다.

<p align="center"><img src="attachment:9f60ed36-d485-4e58-a055-d93d43e2225a:스크린샷_2026-04-29_135916.png" alt="스크린샷 2026-04-29 135916.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

오른쪽 하단에 보이는 use ISO image file 에서 browse을 눌러 ISO 파일을 선택해서 설치합니다.

<p align="center"><img src="attachment:a5331698-cc94-45a0-a46d-72567acadc9d:스크린샷_2026-04-26_130847.png" alt="스크린샷 2026-04-26 130847.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

ISO image 파일이 정상적이라면, 설치가 진행되며 다음과 같은 설정창이 뜨게 됩니다. 여기서 언어와 시간대, 키보드 입력 방식을 선택합니다. 안타깝게도 최초 설정은 영어밖에 안됩니다. 이부분은 설치가 완료된 이후 설정 창에서 변경이 가능하니 너무 아쉬워하지 마세요.

<p align="center"><img src="attachment:32fc1052-a86a-4689-8825-fddc6588a34d:스크린샷_2026-04-26_131154.png" alt="스크린샷 2026-04-26 131154.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

그것보다 중요한것이 시간대와 키보드 입력방식입니다. 저희는 한국에 있고 한국 키보드를 사용하니 그에 맞게 설정해줍니다.

<p align="center"><img src="attachment:b424af23-bd89-48b6-836b-c4eab44233e8:스크린샷_2026-04-26_131650.png" alt="스크린샷 2026-04-26 131650.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

마지막 항목인 키보드 유형에는 4가지 유형이 있는데 선택하기를 힘들어하시는 분들을 위해 간단하게 설명드리자면, 키보드 배열에 따라 다른 유형을 뜻합니다.

저의 친구 Chat-Gpt에게 물어보니, 유형별로 다음과 같은 차이점이 있습니다. 현재 저희의 실습 상황에는 Type1이 적합합니다. 다른 분들은 각자의 환경에 맞는 키보드 유형을 선택하시면 될 것 같습니다.

<p align="center"><img src="attachment:6631cb4c-8b53-4325-9272-9471d2b03283:image.png" alt="image.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

키보드 선택이 끝나면 기본 설정이 끝나고 선택한 설정에 맞게 바로 설치가 가능합니다.

<p align="center"><img src="attachment:092ddd5c-ba3c-4c32-9836-a23ee58ce1aa:스크린샷_2026-04-26_131700.png" alt="스크린샷 2026-04-26 131700.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

## Windows Server 2019 (Desktop Mode)
### Windows Server 2019 Desktop Mode 설치

갑자기 4개의 선택지가 주어집니다. 읽어보시면 Standard 버전 2개, Datacenter 버전 2개가 있습니다. 저희는 일반 환경이니 Standard로 선택을 해야할 것만 같습니다.(설마 Datacenter겠어?)

Standard 버전 2개의 차이는 하나는 Core Mode, Desktop Mode 입니다. 일단은 저희에게 친숙한  Desktop 환경을 선택해서 설치해봅니다.

<p align="center"><img src="attachment:0974ca04-b565-45e8-a2df-c094c3ea8d28:스크린샷_2026-04-26_131816.png" alt="스크린샷 2026-04-26 131816.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:91dedf98-f62c-4ebb-9987-7108bb0c84fc:스크린샷_2026-04-26_131823.png" alt="스크린샷 2026-04-26 131823.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

이용약관 및 주의사항, 라이선스 조건 은 안읽고(X), 꼼꼼히 읽고(O) 다음으로 넘어갑니다.

<p align="center"><img src="attachment:bb7f315b-07df-47ff-9ed0-1018f684509c:스크린샷_2026-04-26_132424.png" alt="스크린샷 2026-04-26 132424.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

또 다시 선택지가 주어집니다. Custom 버전으로 설치합니다. 왜냐하면 Upgrade는 선택해도 안됩니다. 저희는 기존에 설치한 Windows Server 버전이 없기 때문입니다.

<p align="center"><img src="attachment:7cb6c61a-18e4-4179-b61f-15a0cdcf5171:스크린샷_2026-04-26_132537.png" alt="스크린샷 2026-04-26 132537.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:64014d5a-9027-46fd-9083-ea49fc1b6ffc:스크린샷_2026-04-26_132834.png" alt="스크린샷 2026-04-26 132834.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:4a6f5595-7c4f-4198-a3b8-dc998f53d8f0:스크린샷_2026-04-26_132659.png" alt="스크린샷 2026-04-26 132659.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

만약에 기존에 설치된 파일, 파티션으로 나뉘어진 디스크가 있다면 여기 표시됩니다. 첫 설치이기 때문에 넘어가면 됩니다.

<p align="center"><img src="attachment:d9eaf4a8-9889-4615-a4d6-5e229fe0ed2e:스크린샷_2026-04-26_132816.png" alt="스크린샷 2026-04-26 132816.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

기나긴 선택 화면들이 끝나고 드디어 설치에 들어갑니다.

<p align="center"><img src="attachment:8f645869-e204-4b26-a603-c647ecbadd44:스크린샷_2026-04-26_132917.png" alt="스크린샷 2026-04-26 132917.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

이제 본격적인 시작입니다. 생성 후 새 암호를 설정합니다. 우리는 현업자이기 때문에 쉬운비밀번호는 지양해야합니다.

<p align="center"><img src="attachment:0787a471-a412-45f8-a3c9-fee54b5d5b07:스크린샷_2026-04-26_133220.png" alt="스크린샷 2026-04-26 133220.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:cf27ff64-b2b1-48cf-9886-a41a5fdc68cf:스크린샷_2026-04-26_133250.png" alt="스크린샷 2026-04-26 133250.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

성공적으로 로그인했습니다. 이제 남은 과제들이 있습니다.

<p align="center"><img src="attachment:733842d2-b40f-4641-9a0d-162467951bb3:스크린샷_2026-04-26_133311.png" alt="스크린샷 2026-04-26 133311.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

보안 업데이트, 이름변경, 시간동기화 등등이 있습니다. 그전에 현업자들은 Language를 English로 setting 해서 use하지만 저희는 practice가 purpose다 보니 한국어로 변경해보겠습니다.

설정 창으로 들어가 lauguage로 들어가 빠르게 korean을 찾아 다운로드합니다.

<p align="center"><img src="attachment:e1f1d8f2-9cbb-44d6-bf23-0dbb9c7d3060:스크린샷_2026-04-26_133443.png" alt="스크린샷 2026-04-26 133443.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:e4dbc8d2-a54a-49f1-8961-52e58729decf:스크린샷_2026-04-29_145909.png" alt="스크린샷 2026-04-29 145909.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:60cc14d6-7691-4675-a3ed-1dbe05587a29:다운로드.jpg" alt="다운로드.jpg" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

남은 과제들은 다음 항목에서 진행해보겠습니다.

### Windows Server 2019 Desktop Mode 초기 보안설정

설정창으로 이동해 Windows 업데이트로 들어갑니다. 업데이트 파일을 다운 받아 보안성을 강화해줍니다. 업데이트 설치가 끝났다고 해도, 한번 더 확인해서 더 이상 가능한 업데이트가 없을 때 까지 확인해줍니다.

<p align="center"><img src="attachment:a83c3315-5526-47e8-8735-2a971782af89:스크린샷_2026-04-26_143219.png" alt="스크린샷 2026-04-26 143219.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:d5c50651-dc7c-457d-970a-23aaf29f8930:스크린샷_2026-04-26_144641.png" alt="스크린샷 2026-04-26 144641.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

업데이트가 완료되었습니다. 두 번 정도 업데이트하니 업데이트가 완료되었습니다.

<p align="center"><img src="attachment:e243143d-12c5-456b-968b-218f573bb15b:스크린샷_2026-04-26_145831.png" alt="스크린샷 2026-04-26 145831.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

그 후에는 사용자 이름을 변경해줍니다.

<p align="center"><img src="attachment:da53b47b-8857-4cc7-acc5-879993367a01:스크린샷_2026-04-26_150039.png" alt="스크린샷 2026-04-26 150039.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

저희는 Windows Server 2019 스터디라는 의미로 아래와 같이 이름을 변경했습니다.

<p align="center"><img src="attachment:4d7d5349-529d-4077-97c4-8a5ef38918f8:스크린샷_2026-04-26_150111.png" alt="스크린샷 2026-04-26 150111.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

이제 시간대를 설정합니다. 표준 시간대로 들어가서 (UTC +09:00 서울) 항목을 눌러 시간대가 맞는지 확인합니다.

<p align="center"><img src="attachment:f17c9c63-96ee-42a2-8013-ad7975384a46:스크린샷_2026-04-26_150443.png" alt="스크린샷 2026-04-26 150443.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:b8e576ab-fb3e-45de-a1e2-34ab6c0037fa:스크린샷_2026-04-26_150458.png" alt="스크린샷 2026-04-26 150458.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

이제 네트워크 연결이 정상적으로 되어 있는지 확인해볼 차례입니다.

ipconfig를 입력해 ip주소를 확인하고, 우리의 Google public domain(8.8.8.8)에 ping을 보내봅니다. 이상없이 잘 작동합니다.

<p align="center"><img src="attachment:c8b075d1-7389-4927-947b-0b0c0c1de764:스크린샷_2026-04-26_153314.png" alt="스크린샷 2026-04-26 153314.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:65a09472-8c45-49db-8147-f9002b68ac81:스크린샷_2026-04-26_153432.png" alt="스크린샷 2026-04-26 153432.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

다음으로는 불필요한 서비스 비활성화가 남았습니다. 우리의 친구 Chat-Gpt에게 불필요한 활성화 서비스 목록을 확인하는 방법을 물어봅니다. 친절하게 명령어를 알려줍니다.

> 💡

명령어

*현재상태 저장

`mkdir C:\Audit`

*서비스 전체목록 저장

`wmic service get Name,DisplayName,State,StartMode > C:\Audit\desktop_services_all_before.txt`

*자동시작 서비스 저장

`wmic service where "StartMode='Auto'" get Name,DisplayName,State,StartMode > C:\Audit\desktop_services_auto_before.txt`

*cmd 화면에 목록 출력

`wmic service where "StartMode='Auto'" get Name,DisplayName,State,StartMode`

아래와 같이 목록이 출력됩니다. 목록 중에 굳이 필요없는 서비스들이 보입니다.

<p align="center"><img src="attachment:54ff3134-8ab9-43f9-b003-1690f97a6e32:스크린샷_2026-04-29_164652.png" alt="스크린샷 2026-04-29 164652.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:8bbf9ada-f660-4748-8bac-b61a7fe62196:스크린샷_2026-04-29_164704.png" alt="스크린샷 2026-04-29 164704.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

PrintSpooler = 프린트 사용 시, 프린트 드라이버를 확인하고 다운로드 받는 프로그램입니다. 현재 프린트를 사용할 계획이 없기 때문에 비활성화해도 될 것 같습니다.

MapsBroker = Downloaded Maps Manager로 오프라인 지도 앱의 데이터 접근을 관리하는 서비스입니다. 서버에서 지도를 사용할 일이 없을 것 같으니 비활성화해도 될 것 같습니다.

> 💡

비활성화 명령어

*MapsBroker 비활성화

`sc config mapsbroker start= disabled`

*PrintSpooler

`sc config spooler start= disabled`

*비활성화 확인

`sc qc mapsbroker`

`sc qc spooler`

아래와 같이 불필요한 서비스를 비활성화 했습니다.

<p align="center"><img src="attachment:0e89cf21-4692-4312-b78a-87b30fae8910:스크린샷_2026-04-29_172348.png" alt="스크린샷 2026-04-29 172348.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

협업에서는 CMD 보다 Powershell 을 더 많이 사용한다.

관리자 이름 변경

<p align="center"><img src="attachment:dd60f128-4dd5-4d46-a56b-b67ed3084dae:image.png" alt="image.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

CMD 와 Powershell 의 차이점

| 구분 | CMD | PowerShell |
| --- | --- | --- |
| 등장 시기 | 오래됨 | 비교적 최신 |
| 기본 목적 | 명령 실행 | 시스템 관리/자동화 |
| 데이터 처리 | 텍스트 | 객체 |
| 자동화 | `.bat`, `.cmd` | `.ps1` |
| 명령어 형태 | 짧은 명령어 | 동사-명사 구조 |
| 서버 관리 | 제한적 | 강력함 |
| 학습 난이도 | 쉬움 | 처음엔 조금 어려움 |
| 실무 중요도 | 기본기 | 필수에 가까움 |

GUI환경에서는 `services.msc` 을 통해 확인할 수 있습니다.

<p align="center"><img src="attachment:4261b285-5505-4a83-a58d-c9c0ee64f7fa:스크린샷_2026-04-29_174330.png" alt="스크린샷 2026-04-29 174330.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

입력 후에는 더블클릭해서 시작 유형을 선택할 수 있습니다.

<p align="center"><img src="attachment:f5d25155-eadf-416e-a590-5b20a7b8f52b:스크린샷_2026-04-29_174801.png" alt="스크린샷 2026-04-29 174801.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

여기까지 Windows Server 2019 Study 1주차 - Desktop Mode 설치 및 초기 보안설정

에 대해 진행해보았습니다.

## Windows Server 2019 (Core Mode)
### Windows Server 2019 Core 설치

Windows Server 2019(Core Mode)를 설치해봅니다. Core Mode는 CMD환경에서 실습이 진행됩니다.

<p align="center"><img src="attachment:0e32ab82-fd53-4ce6-bb2a-fa1c835f25f7:스크린샷_2026-04-26_140242.png" alt="스크린샷 2026-04-26 140242.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

### Windows Server 2019 Core Mode 초기 설정

설치가 완료되면 Core Mode에서는 아래와 같이 CMD창이 뜨게 됩니다. 초기에 새로운 비밀번호를 입력해서 비밀번호를 설정해줍니다. Desktop Mode와 같이 복잡한 비밀번호를 설정해줍니다. 저희는 역시 현업자 마인드를 탑재해야하니까.

<p align="center"><img src="attachment:e57da9b8-8fd3-4cb7-a12c-1bc86784af23:스크린샷_2026-04-26_140524.png" alt="스크린샷 2026-04-26 140524.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:0806462c-6cc8-4bb5-bd71-8173c40d34c0:스크린샷_2026-04-26_141905.png" alt="스크린샷 2026-04-26 141905.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:36294bad-a627-4d98-8f64-fc7457c24d66:스크린샷_2026-04-26_141920.png" alt="스크린샷 2026-04-26 141920.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

초기 보안 설정은 CMD 창에서 sconfig를 입력해 설정화면으로 들어갑니다.

<p align="center"><img src="attachment:5ac9d5f8-e52f-4ccf-ac0a-fbf27224c9f1:스크린샷_2026-04-29_153608.png" alt="스크린샷 2026-04-29 153608.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

뭔가 잘못된것만 같은 블루스크린의 Sever Configuration 화면이 뜹니다. 저희가 변경해야할 부분들입니다. 먼저 업데이트부터 확인해줍니다.

<p align="center"><img src="attachment:ce170414-0e06-49b0-82e0-07f4e3c2c754:스크린샷_2026-04-26_142133.png" alt="스크린샷 2026-04-26 142133.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

5번을 눌러 업데이트를 자동으로 할지, 다운로드만 할지, 수동으로 할지를 선택합니다. 업데이트를 저는 수동으로 선택했습니다.

<p align="center"><img src="attachment:8eb817d8-8b6b-4943-9376-51406c1a667a:스크린샷_2026-04-26_144030.png" alt="스크린샷 2026-04-26 144030.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

6번을 누르게 되면, 업데이트를 다운로드하고, 설치를 할 수 있습니다. 설치 가능한 업데이트가 있는지 검색하고, 아래와 같이 설치할 업데이트 목록이 뜨게 됩니다.

<p align="center"><img src="attachment:25408495-8993-4e8e-bf31-9ab780b5b3cd:스크린샷_2026-04-26_144132.png" alt="스크린샷 2026-04-26 144132.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:c37f22af-9f48-4b4f-8c3a-da3937b4f2b7:스크린샷_2026-04-26_144338.png" alt="스크린샷 2026-04-26 144338.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:1d4ff6c8-722b-412c-ab92-e384e404f4c3:스크린샷_2026-04-26_144655.png" alt="스크린샷 2026-04-26 144655.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:35efcef7-56c9-4bc0-8963-530b662be751:스크린샷_2026-04-26_144705.png" alt="스크린샷 2026-04-26 144705.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:f29a14ec-2a63-406b-a22c-d8825c22e0e6:스크린샷_2026-04-26_145553.png" alt="스크린샷 2026-04-26 145553.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

이번엔 이름을 변경합니다. 아래에 2번을 눌러 이름을 변경해줍니다. Desktop 모드와 동일하게 Study-Win2019Server로 변경합니다.

<p align="center"><img src="attachment:6bb1c157-d9b7-4d4e-998e-b4c203f70916:스크린샷_2026-04-29_161440.png" alt="스크린샷 2026-04-29 161440.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

변경 시 재부팅을 하면, 아래와 같이 이름이 바뀌어 있습니다.

<p align="center"><img src="attachment:93843f68-c11d-4aa2-9386-fffd755a96c6:스크린샷_2026-04-29_161455.png" alt="스크린샷 2026-04-29 161455.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

<p align="center"><img src="attachment:73482756-b28c-4080-b867-665d87c8eebb:스크린샷_2026-04-26_150319.png" alt="스크린샷 2026-04-26 150319.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

다음으로는 표준 시간대 설정입니다. 9번을 눌러 시간대를 확인합니다. 이상 없으면, 표준시간대도 설정이 완료되었습니다.

<p align="center"><img src="attachment:5653dd3c-386b-4bbb-a336-b4376c3115a1:스크린샷_2026-04-26_150345.png" alt="스크린샷 2026-04-26 150345.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

다음으로는 네트워크 연결이 정상적으로 되는지 확인해봅니다. 15번을 눌러 CMD창을 나갑니다. ipconfig /all을 눌러 확인해봅니다. 아래와 같이 Hostname과 IPv4주소, Gateway 주소를 확인해봅니다. 이름이 잘변경되어 있습니다.

<p align="center"><img src="attachment:c49b53d5-3d6d-4ee6-aa04-c5ca5c9ab87f:스크린샷_2026-04-26_153213.png" alt="스크린샷 2026-04-26 153213.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

Core Mode에서도 우리의 Google public domain에 ping을 보내봅니다. 이상없이 잘 작동합니다.

<p align="center"><img src="attachment:992ca8ec-a5db-4bcc-9eeb-2922cf217fcd:스크린샷_2026-04-26_153440.png" alt="스크린샷 2026-04-26 153440.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

불필요한 서비스 비활성화에는 판단 기준이 필요합니다. 판단 기준은 아래와 같습니다.

1. 서버의 역할과 그에 맞는 서비스 인가?
2. 기본 설치 서비스인가? 추가 설치된 서비스인가?
3. 현재 실행 중인가?
4. 종료 시 원격접속/로그/네트워크/업데이트/보안기능에 피해가 가는가?
5. 끄기 전 상태 기록했는가?

> 💡

**CMD 명령어**

*기록폴더 생성

**`mkdir C:\Audit`**

*전체 서비스 목록 확인 및 저장 명령어

**`wmic service get Name,DisplayName,State,StartMode > C:\Audit\services_all_before.txt`**

*자동시작 서비스 확인 명령어

**`wmic service where "StartMode='Auto'" get Name,DisplayName,State,StartMode`**

sc query를 통해 확인한 현재 실행중인 ‘자동시작’ 프로그램

<p align="center"><img src="attachment:2a5d1730-5c3f-47d0-a173-99bb6171afbd:스크린샷_2026-04-28_205540.png" alt="스크린샷 2026-04-28 205540.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

실행중인 전체 프로그램

<p align="center"><img src="attachment:c1056593-1cfa-4363-bdc1-ba0d3a1aff5e:스크린샷_2026-04-28_205445.png" alt="스크린샷 2026-04-28 205445.png" style="max-width:100%; height:auto; display:block; margin: 0 auto;"></p>

*빨간색 : 건드리지 말아야할 프로그램 (→제거 혹은 비활성화 시 서버가 망가질 가능성이 높은 프로그램)

*노란색 : 보안정책 이나 필요성을 확인해야하는 검토 대상 프로그램

⇒ 사실 현재 실행중인 프로그램들은 종료, 비활성화가 거의 필요없는 최소한의 프로그램

검토대상 프로그램 명령어

> 💡

`sc query RemoteRegistry >> C:\Audit\service_review_targets.txt`

`sc query DiagTrack >> C:\Audit\service_review_targets.txt`

`sc query MSDTC >> C:\Audit\service_review_targets.txt`

`sc query SysMain >> C:\Audit\service_review_targets.txt`

`sc query UALSVC >> C:\Audit\service_review_targets.txt`

사실 core 모드에서는 비활성화 할 프로그램이 많지 않습니다. 불필요한 GUI 서비스를 거의 설치하지 않기 때문입니다.

여기까지 Windows Server 2019 Study 1주차 - Core Mode 설치 및 초기 보안설정

에 대해 진행해보았습니다.

요약

- Desktop Mode는 저희가 익숙한 GUI환경입니다.
- Core Mode는 CMD 환경입니다.
- Core Mode는 불필요한 프로그램을 거의 설치하지 않고 핵심적인 프로그램들만 설치합니다.

## 서버 엔지니어의 역할

서버 엔지니어의 역할에 대한 정의는 **서버가 안정적으로, 안전하게 운영되도록 하는 사람**입니다.

> 💡

**서버 엔지니어의 역할**

구축 : Windows Server, Linux 설치, 가상머신 생성, 스토리지 구성, 네트워크 설정, 도메인 가입 등

운영 : 계정 관리, 권한 관리, 서비스 상태 및 성능 확인, 로그 확인, 백업 확인, 장애 대응 등

보안 : 불필요 서비스 제거, 방화벽 정책 관리, 관리자 계정/일반 계정 및 패스워드 등 보안 정책, 이벤트 로그 감사, 취약점 조치, 보안 업데이트 적용, 백신/EDR 상태 확인

자동화 : PowerShell 사용, 배치 스크립트 작성, 그룹 정책, 원격 관리 등

## Study 1주차 결과요약

- Windows Server의 Desktop Mode와 Core Mode를 모두 설치해보고, 기본적인 설정을 진행해보았습니다.
- 각 Mode의 환경에서 보안 설정을 진행해보았고, CMD 환경과 GUI 환경의 차이점을 확인했습니다.
- 전체 서비스 목록을 확인하고 불필요한 서비스 목록을 확인, 비활성화 단계도 실습 했습니다.