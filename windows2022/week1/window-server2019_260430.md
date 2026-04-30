# Windows Server 2022 설치 실습 정리

> 이미지가 잘리지 않도록 모든 스크린샷은 HTML `<img>` 태그로 삽입했고, `max-width:100%; height:auto;` 옵션을 적용했습니다.

---

비밀이지만 공개해보겠습니다… 초안1..

스터디 정식 보고서를 쓰기 전 여러분에게 윈도우 서버 설치를 소개하고자 ~ 이렇게 찾아왔습니다...

잘 알려드리고 싶지만 저는 '비'전공자라 부족한 점이 많습니다.

정정하고 싶은 내용이 있다면 댓글로 알려주시거나 직접 찾아와서 알려주시면 감사하겠습니다~!

함께 성장해요 ! ! 함성 !!!!!!!!!!

<p align="center">
  <img src="https://storep-phinf.pstatic.net/ogq_5eedbcd06ab59/original_10.png?type=p100_100" alt="ogq_5eedbcd06ab59-10" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>

안녕하세요. 윈도우 스터디를 시작했습니다.

정신 차리고 보니 내가 윈도우 마스터?가 될 수 있을까 기대가 됩니다.^^

저(안지명)와 송규석군은 서버 2022 하주한님과 김동현님은 서버 2019를 담당해서 각각의 서버가 어떻게 다른지 특징을 살펴볼 예정입니다.

오늘은 1주차 !

윈도우 서버 2022 설치부터 해보겠습니다.

데스크탑 환경과 CLI 환경 두 가지로 진행했습니다.

아래 사진들을 따라와주시면 되겠습니당.

그럼 시작해보겠습니다!

<p align="center">
  <img src="https://storep-phinf.pstatic.net/ogq_5ebebeedf0c9a/original_1.png?type=p100_100" alt="ogq_5ebebeedf0c9a-1" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>

먼저 iso파일이 필요한데요..

[Windows Server 2022 ISO 다운로드](https://www.microsoft.com/ko-kr/evalcenter/download-windows-server-2022)

**Windows Server 2022 | Microsoft Evaluation Center**

Windows Server 2022는 고급 다중 레이어 보안, Azure와 함께 하이브리드 기능, 유연한 응용 프로그램 플랫폼을 도입합니다.

www.microsoft.com

이곳에 들어가면 ISO를 다운받을 수 있습니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfNjcg/MDAxNzc3MjU2MzkzNzMx.zl-tP1vNkRCFA3UEoDAgk0b4J_LAjXmzHWExjJ3OzOUg.SPVsN2spAFSd5Qh4kSRqqmS2eCY7UnsQZnBg2jN0J-gg.PNG/iso%EB%8B%A4%EC%9A%B4.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


iso 설치파일 다운로드하세요~

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMTQ2/MDAxNzc3MjU1ODgyODMx.CRvOz_Os1W9ixDya3kb53PsXf8UYAmX4tAJLjUthGGUg.FEYR1UlT6YCJeI7figP9ZSr8F2FRC4EMaSUoyzMLzgsg.PNG/newfil-1.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


새로운 VM을 생성합니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjg1/MDAxNzc3MjU1ODg5NTE1.0T0bvQeW0oAEjN9JR0Lx3QczzLzQ5NLTaWtyKHJelmgg.D22qUR9Kuyf0l2MQv55dSDfJxYb29KjiCShizc7L83og.PNG/%EC%84%A4%EC%B9%98%EC%8B%9C%EC%9E%91-2.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


지금은 추천하는대로 진행합니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMTky/MDAxNzc3MjU1ODkzMjQ3.pQZSW80vNNcdDkwIRgzK2SLlJcKpRaqzYUw88fThdxIg.kjwkpN-PtHR-U8RJHCO8tMmYXEhL12xzx_ICeSXyHqQg.PNG/%EB%82%98%EC%A4%91%EC%97%90%EC%84%A4%EC%B9%98-3.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


OS는 나중에 설치하시면 됩니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMTk2/MDAxNzc3MjU1ODk4MTIw.UY8Pbft2c6s-LWQrCWsH_MOhL2qWQYnDf7jI7qJPslAg.ndJsce2ft2DtcNtFsVbNrUvRyziP2yGK05brIhGTnrwg.PNG/%EB%A7%88%EC%86%8C%EC%84%A0%ED%83%9D-4.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


Microsoft Windows를 선택하고, Windows Server 2022를 골라주세요.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjI0/MDAxNzc3MjU1OTA0MDI2.9dLffTEVA9tYG_jcDWASlstD-hRfgiblT8jsHhFc5Aog.e3n-VTj4dCrYX7tZuuYPQPtqUJ-Af_znY249OLWJEWEg.PNG/%EB%A9%80%ED%8B%B0%ED%94%8C%ED%8C%8C%EC%9D%BC%EC%84%A0%ED%83%9D-5.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


지금은 디스크를 분할하는 선택지를 택했습니다.

저희는 여기서 두 선택지의 차이가 궁금했습니다.

먼저 **단일 파일 (Single File)은**

하나의 거대한 덩어리로 존재할 때 데이터의 연속성이 확보되어 읽기/쓰기 효율이 극대화됩니다. 성능과 안정성을 중시할 때 선택합니다.

**분할 파일 (Split Files)은**

실험적인 환경이나 개발 서버를 관리하는 엔지니어에게 유리합니다. 백업과 유연성을 중요시할 때 선택합니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMTY5/MDAxNzc3MjgwOTE0Nzc1.yYCNuW7ar-Dw7tGzQmbDLtPnaJok57QShz-rvk0PEUMg.lM18p2YuNjBU3Rb3hUo1yrZ2dcJ_zZKwY_mwvNav26Ag.PNG/image.png?type=w1600" alt="image.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


표시된 부분을 클릭합니다

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjgy/MDAxNzc3MjU1OTExMzg4.mHhwlzEskXsnyllS0GS2UfCLYGjz5vu36QUZvKMWMJIg.s8ICQ-UyJn9vA6qyVdr3FCJX_YTJXEwx3Sez0Sq-RqUg.PNG/iso%EC%84%A4%EC%A0%95-6.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


세팅창이 나타나면 CD/DVD (SATA)를 클릭하고 표시된 부분에 직전에 받은 ISO파일을 넣어줍니다.

그 후에 OK와 finish를 눌러주고, VM실행을 눌러줍니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjUy/MDAxNzc3MjU1OTIxNDgy.bjtO_X5k_BAar7RKy0Bp6BjpVjFqKkVT7TI7beN9t30g.3WZrYSmSm6w2SCRIWQkYfpaBR7aUDJM3GF8fDBNgapIg.PNG/korean-7.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


짜란

Time and currency format을 Korean(Korea)으로 선택합니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjUx/MDAxNzc3MjU1OTI0NTQy.J19KIDvhxaY_GmB43uAH5DNl0xJK6nPK2Wjdy7cAHTUg.bGicn28w_7F_hcOmNCQSnKDrPegrsxDg8E0Wim99f4Yg.PNG/installnow-8.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


Install now click plz^^

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjQ5/MDAxNzc3MjU1OTMwNzMx.cKAEf9hZGQE7cDHBH_3aLvPD-TyavqfEbILHjwGLuKog.t0anrRy-n29Z32nCe7RhMAmA9MjuTASTxn1I4bllrmYg.PNG/desktop%ED%99%98%EA%B2%BD%EC%84%A4%EC%A0%95-9.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


두 번째인 Desktop Experience 를 선택해줍니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfOCAg/MDAxNzc3MjgxMjMxODk5.dwO6GH1WGPGSur9EK6nE119n3bgwtY2IJPTTSITC-jkg.pFdEvUjOD8MIgePoLkHP7BQnyEqOZOk9DiNuEQ_0mzEg.PNG/SE-871345b7-a09b-4a66-9499-18a5efdad5a8.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


화살표 체크박스를 클릭해주세요. 그래야 넘어갑니다.~

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMTgz/MDAxNzc3MjU1OTQwNjkz.DGrZNtuYu0Cbdi_5Xhw5Jm4oqSu6ggZbq3sjInbbnNkg.8_PMX6-XNnetZoEmElfYDnq0_PuaaT7_2ZWeFg9-mlAg.PNG/%EC%BB%A4%EC%8A%A4%ED%85%80%EB%AA%A8%EB%93%9C_%EC%84%A4%EC%A0%95-11.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


Custom을 선택해줍니다....

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjY1/MDAxNzc3MjU1OTQyODQz.xn0FYwG94GBCL5JfBPVtDcA85pRLhoeOEwTqsv0j4A4g.cE7dYyfvx_g67jW7PD4HIMsNWIz0PcZHS5F1yxS5ZpAg.PNG/custom%EC%84%A4%EB%AA%85-11-1.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


두 타입의 차이점은 위와 같습니다..

Upgrade타입은 데이터를 보존하며 버전만 올리는 설정입니다. 따라서 기존에 OS설치가 돼있지 않다면 진행되지 않는데,  저희는 OS설치가 되어있지 않은 환경이므로 Custom으로 진행하였습니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjE1/MDAxNzc3MjU1OTQ1OTE4.mljQ_VXf8gClUTh3lg9hK0tpKTjHt93NA_pAYTnmToIg.RZyw8Pnv8aOBHGKsfiWU5WaIA9ko_LBGFgyzEtfVjL0g.PNG/os%EC%84%A4%EC%B9%98%EC%9C%84%EC%B9%98-12.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


next를 눌러줍니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfODgg/MDAxNzc3MjU1OTQ3OTgz.eYp32OI2O4n5aoDV7wgg1Nr_DrnpdfMscEwFnXvGDUEg.9ZcnH1cc-SvBK24yfVIvAUuTLeoUzcYHOGHz4ofAmN4g.PNG/os%EC%84%A4%EC%B9%98%EC%A4%91-13.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


그럼 설치중 ~~

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfODIg/MDAxNzc3MjU1OTU0NTAx.VinWYIvYgwb2s4c-cdDP4CO0e9qDD5-WN715O9PeyxUg.QXg0qpVsmVIjRNRtozBisSLI6tYqcUBJ-sP3SEZcCW4g.PNG/%EC%95%8C%EC%95%84%EC%84%9Crestart-14.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


restart 중

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfNDAg/MDAxNzc3MjU1OTU5ODEx.HN2yRLxkkA3yePZDXi47pBh064xf8zDCNJSoY5pj6IQg.wvL6VWlC8vxLmWGWbBxGa0XA6cMm3DwG23ouMt7CdXQg.PNG/password%EC%84%A4%EC%A0%95-15.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


비밀번호는 비밀입니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMTE4/MDAxNzc3MjQ5MTk4OTYy.Jy0LlZSoPHW0BRynT4lkN5ktei7M3nxl4VaBLlbf8Icg.3YX01c5SQsug_fD1xmPYhZw-oY89IkXyabF1ZLnWHFYg.PNG/%EC%9C%88%EB%8F%84%EC%9A%B02022%EC%84%9C%EB%B2%84%EB%8C%80%EC%8B%9C%EB%B3%B4%EB%93%9C-1.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


설치 후 첫 화면 'Dashboard'

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjE2/MDAxNzc3MjQ5NDM4OTc3.TyUrqssmzMjL_04JCIfCY3JZMdCXDgqn2dm9akQ727Ag.GibuMFrrRk179uSCb4B_Ln2bN06aRVLE9izvsyq0Tg0g.PNG/SE-7b234c63-1de0-47ed-8573-7b5a128a8906.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


언어 설정

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjYz/MDAxNzc3MjQ5NDkwMzAy.K7QQkQBFCFrJ-24L6tNy9oM2BiovlTzz6ato1HSBMmog.eeSEJTwMyjZKpHG7RYU22cCw1qlf3nky8VJHQQ8Q9isg.PNG/SE-1fd478e9-4628-4ca7-935a-11030bfc4bcb.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


Korean의 Options선택

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMzAw/MDAxNzc3MjQ5MjI1OTc1.toT2jsc_SpQLkO1PMfFZA-l3ghlsNJaDiE5r3nBTckUg.3UZ3g6WK_QWdaNffg5g-TfP4r9EEEfoCC_CzC7sHIcwg.PNG/%EC%A0%84%EB%B6%80%EB%8B%A4%EB%B0%9B%EC%95%84%EC%A3%BC%EC%84%B8%EC%9A%94-4.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


전부 다 download눌러주세요

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjc0/MDAxNzc3MjQ5MjMwMDAx.mLVzxqN9KJkQ9V_W8CGrRCtueKTARDXYAhbTL_pUe_Yg.PtDenEeHaOOLfueUPGnUkBPy3waI5Iw1rGEYmVApajkg.PNG/%EB%8B%A4%EC%9A%B4%EC%99%84%EB%A3%8C-5.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


다운로드 완료!

**Basic Typing이 다운로드 할 때는 있었는데 다운로드 후엔 사라졌습니다. 그게 뭘까요?**

Basic typing은 윈도우에서 특정 언어를 키보드로 치고 읽는 데 필요한 가장 핵심적인 데이터 파일입니다.

**그렇다면 !!!!!!!! 왜 목록에서 사라졌을까요?**

윈도우 설정 화면의 특성상, '다운로드 중'일 때는 진행 상황을 보여주기 위해 각각의 구성 요소(기본 입력, 필기, 음성 등)를 개별적으로 나열합니다.

하지만 '설치 완료' 후에는 화면을 깔끔하게 정리하기 위해 다음과 같이 합쳐집니다.

**Language pack installed:** 이 문구 안에 'Basic typing' 기능이 포함됩니다. 한국어를 읽고 쓰는 데 필요한 가장 핵심적인 기능이라 언어팩 설치 시 세트로 묶여서 표시되는 것이죠.

**Handwriting installed:** 필기 인식 기능은 별도로 표시되기도 합니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMTAy/MDAxNzc3MjQ5ODgyNjE0.8EB9QDgQpEnyhChzWigagxok6EwwxRr-2B_4XkiydEEg.O6IP-Ak8VDyEMtYfXv_ltdK8pqdtR5zQan6KGRSHIKQg.PNG/SE-be16216f-df85-47f5-bd8c-8a73a618fd23.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


sign out now를 눌러줍니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMTg1/MDAxNzc3MjQ5MjU3Nzc1.FuqfSdWH8CKqwxVAMhw2Cnj1ceCbet8hN8Q7OfnDJccg.iGZSmsFXMdN8QGLi5QP7QaXNQCTg5NsXQH-p3ncjjGkg.PNG/%ED%99%94%EB%A9%B4%EC%84%A4%EC%A0%95%ED%95%98%EB%8A%94%EB%B2%95-8.png?type=w1600" alt="image" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


위 사진들과 다른 점은 .. 사이드 검은 공간이 사라졌습니다.

다음 차례는 주차별 상세 커리큘럼.. 에서 sconfig(코어모드)를 실행해보겠습니다.

**sconfig**는 'Server Configuration'의 약자로,

윈도우 서버 특히 GUI가 에서 복잡한 명령어 대신 **번호 선택 방식**으로 서버의 핵심 설정을 할 수 있게 도와주는 **텍스트 기반 설정 도구**입니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfNSAg/MDAxNzc3MjgzMjMyNDM1.z8SuLcvuFWFwFWloiK0mNb7g7SWtHrxjjRZ72z7ODCYg.glGnozFEgJ_GPalBmxs-1cUI28ofzGQBuATjYWoJ3aUg.PNG/sconfig%EC%9E%85%EB%A0%A5-1.png?type=w1600" alt="sconfig입력-1.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


이제 1주차에 해야 할 일 'sconfig'를 터미널 켜서 타닥타닥,,,,

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjY5/MDAxNzc3MjgzMjc2Njc5.TGWSt0la1qdveoshSixQpnotxmDBmLwjsxMGcqZT-8Eg.9vq76frUQMrOBmJI4ylhQ-FImcjYnl97kgk57IpSCSAg.PNG/%EC%BD%94%EC%96%B4%EB%AA%A8%EB%93%9C-2.png?type=w1600" alt="코어모드-2.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


여기선 해당하는 번호를 입력해 설정값을 변경할 수 있습니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMTc2/MDAxNzc3MjgzMzA5Nzk1.y6F_FEtj-fY2V31nNP4HB99iln9ebweVRipcDhC7wF8g.jsNXcHEDXsLsgFcrtZpK3FiDuRgCjcIyncrDGNdbz-og.PNG/2%EB%B2%88_%EC%BB%B4%ED%93%A8%ED%84%B0%EC%9D%B4%EB%A6%84_%EC%84%A4_%EC%A0%95-4.png?type=w1600" alt="2번_컴퓨터이름_설_정-4.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


다음은 Computer name설정을 위해 2번을 눌러보겠습니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfNjQg/MDAxNzc3MjgzMzE0OTA0.Avta2Zqc6h7v2vr2uJzhqmllJJ-85-5vSddmOE3y5Ygg.D9-vHjli2koCGUaYK5ZT1h7QSo7xEzg59txjik_VMsMg.PNG/%EC%BB%B4%ED%93%A8%ED%84%B0%EC%9D%B4%EB%A6%84_%EC%84%A4%EC%A0%95_-5.png?type=w1600" alt="컴퓨터이름_설정_-5.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


이름을 지정해주고나니

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMTM4/MDAxNzc3MjgzMzE5MzM0.wOmJ5veu3kOGgreoG8XIuc0tEFU8l9c6MzN3aj2gOIwg.Hq2JUQ5X_r7hEVuN-vxmvRGk3NHzYkdWA-cbfA9vcxcg.PNG/%EC%9D%B4%EB%A6%84%EC%84%A4%EC%A0%95%EC%99%84%EB%A3%8C_-6.png?type=w1600" alt="이름설정완료_-6.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


대문자로 변경된다는 것을 알게 되었습니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjEw/MDAxNzc3MjgzMzIzNjgx.YiC9Akf_8AtxMgqCoU-r6F3t1lAcqdQiDIFcBSlp2DMg.vmBwoC4cY1d7A89JIJHGaqZKgsk9wmaGyfu4ycf6WBwg.PNG/9%EB%B2%88_%EB%82%A0%EC%A7%9C_%EB%B0%8F_%EC%8B%9C%EA%B0%84_%EB%B3%80%EA%B2%BD_-7.png?type=w1600" alt="9번_날짜_및_시간_변경_-7.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


다음은 9번을 눌러보겠습니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMTQ5/MDAxNzc3MjgzMzMwNDg2.XZHqpWCbj-N2Xd1sBKX2A2jwVtx2vprEOM-UJCfSZDQg.zy-axr03JFQIaP4m8zqJ9Tde42qyVTeg7XVp9beheQYg.PNG/%EC%8B%9C%EA%B0%84_%EB%B0%8F_%EB%82%A0%EC%A7%9C_%EB%B3%80%EA%B2%BD_%EC%99%84%EB%A3%8C_-8.png?type=w1600" alt="시간_및_날짜_변경_완료_-8.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


바로 날짜 및 시간이 뜹니다. 우리는 한국에서 살고 있으니 표준 시간대를 '서울'로 지정해줍니다.

CLI는 그럼 어떻게 될까요?

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjE5/MDAxNzc3MjgyNTQwMTE3.EJDvmbtt-2WBs1YqIN86gYrgV7D8ttF3QvZSJCxoo_4g.TagMY7opmBbjaJn9KO4FYiEKo1nITigmlWJlzWEZ4Owg.PNG/SE-7acb18cb-2a1f-402d-a4cd-495946ca9cce.png?type=w1600" alt="서버코어_선택_-1.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


CLI를 적용하려면 맨 위를 선택해줍니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjM2/MDAxNzc3MjgzMTE0NjU5.Awnl_-X06I57LdqaF62rIUL-rA4xDb2k9FIuVQ3vtS4g.dd0ysqF8KO16EbbXGORjpD9CCHw0IgDFedF0SluN_Esg.PNG/%EC%84%A4%EC%B9%98_%EC%A4%91-2.png?type=w1600" alt="설치_중-2.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


설치과정은 똑같습니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMTcz/MDAxNzc3MjgzMTI0MzE5.-q4-BRUiPzSw38qq0vSFSv3GdLPZJylvqi22FaJu1Fog.1MH1U6jKOPzL7eEbPdMCKbB_U_9fu_uOFqxvzBQ8TzUg.PNG/%EC%8B%9C%EC%9E%91_-3.png?type=w1600" alt="시작_-3.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


로그인 하기 전 비밀번호를 바꾸라는 창이 뜹니다.

그렇다면 왜 .. 뜨는 걸까 ?

지금 사용 중인 윈도우 서버 버전이 **Server Core(서버 코어)** 버전이라서 그렇습니다. 우리가 흔히 쓰는 윈도우처럼 예쁜 바탕화면이나 시작 버튼 대신, 이렇게 검은색 창(CLI)에서 텍스트로만 설정하는 방식입니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjQ2/MDAxNzc3MjgzMTg3ODg1.elU3OZ55IVsEbpqQG2978h2rAefNlVYN8Enj-sXYm4Ig.TXdWyNwRlGtbMwDVViaUFxF52cJxcRX7SBJbVFmQN9sg.PNG/%EC%B4%88%EA%B8%B0_%EB%B9%84%EB%B0%80%EB%B2%88%ED%98%B8_%EC%84%A4%EC%A0%95_-4.png?type=w1600" alt="초기_비밀번호_설정_-4.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


그렇게 비밀번호를 지정해주고

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMjUx/MDAxNzc3MjgzMTkxMjg2.42IOESqPYH5K26lBWUu2WyLRSjMzVorH_5Wy0gUdaPIg.aeO4pq41bajMFfAtBjSxdPh9aQ1TeYX4f2jSUzKnZjEg.PNG/%EB%B3%80%EA%B2%BD_%EC%99%84%EB%A3%8C_-5.png?type=w1600" alt="변경_완료_-5.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


비밀번호가 변경되었다고 나옵니다.

<p align="center">
  <img src="https://cafeptthumb-phinf.pstatic.net/MjAyNjA0MjdfMTI4/MDAxNzc3MjgzMjA0MDQ1.TUq_WTH1K5gw9pDT1ld0YgWu-hvIbkvQRRXm3DGVuIog.bb-3nI74EKrDGR8OMADAix9JTQQA_wd99CglkXCCHXUg.PNG/cli_%EC%8B%9C%EC%9E%91%ED%99%94%EB%A9%B4_sconfig_-6.png?type=w1600" alt="cli_시작화면_sconfig_-6.png" style="max-width:100%; width:100%; height:auto; display:block;" />
</p>


desktop버전에서는 직접 마우스로 터미널을 클릭한 다음 sconfig를 타이핑했다면 서버코어에선 비밀번호를 입력한 후 바로 화면이 뜨는 걸 알 수 있습니다.
