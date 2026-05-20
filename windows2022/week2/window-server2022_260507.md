# 윈도우 (2022) 스터디 2주차

안녕하세요.

윈도우 스터디 시간이 돌아왔습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTUy/MDAxNzc4MDQ0MzAzMjY1.1oKdqswyEutlqS6JOUJ6vz6l1Cwj6W7i_2o72heGL7Yg.R7J5IrHedeJIo1DTAdIHwoXt-T28CDCYbKeMd7Vnrdgg.PNG/image.png?type=w1600)

학습목표! (들 중 하나!)

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTgg/MDAxNzc4MDQyODY5MzUw.8pfeYVgbv0mKdhHK3XC90WiUQJuT1_w1fP5YNTEFcEsg.KJXjG-niYYshJ8X0lkvm9qk2moVheG14_HpISI4LCbIg.PNG/win%2Br_%EB%88%84%EB%A5%B4%EA%B3%A0_ncpa.cpl_%EC%9E%85%EB%A0%A5-1.png?type=w1600)

고정 ip설정하기 위한 시작

Win + R 누른 다음 ncpa.cpl 입력하면

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjQ1/MDAxNzc4MDQyODkyMzYx.kUEw43cllq1FlkknR5d_jE15E0bvO5w4XiESWHI2PY8g.fAlBAtafjH4SBxA2P32x4xtnvV1n-aPBMMjUkBHTvyAg.PNG/%EC%96%B4%EB%8C%91%ED%84%B0_%EC%84%A0%ED%83%9D_%ED%9B%84_%EC%98%A4%EB%A5%B8%EC%AA%BD_%ED%81%B4%EB%A6%AD%2C_%EC%86%8D%EC%84%B1_-2.png?type=w1600)

신기하죠? 이 창이 뜹니다.

사실 다른 방법도 있습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDdfMjcx/MDAxNzc4MTE5NjAzMjY0.Zjy6uXHN2yho-qmVGkxFMycomnN2cESbst4OtlmNWuUg.blHZZXYuw6sXHkm2_X1yicDwkBrDxftdhJtsgPuVTzkg.PNG/image.png?type=w1600)

지구본 모양 클릭합니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDdfMTYg/MDAxNzc4MTE5NjQ2MzAz.tIijG9XJX3Tbs5gBUmJ4asVImFxLWQxTsV6UYm7XPtIg.B9Cc2lJBc-MruVjVdmZAHsOeaQLjhUMZMXSlc0TjRVsg.PNG/image.png?type=w1600)

네트워크 및 인터넷 설정 열기를 누릅니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDdfNzkg/MDAxNzc4MTE5Njc4MTM4.fsXAajJyccOrz6LdHVB-3GZsmliX1NS1EO81PB7668cg.pLkoeOauUFHiJPWyc2mBA9BYdOAkINSreEvs1JLME64g.PNG/image.png?type=w1600)

이더넷을 클릭한 뒤 '어댑터 옵션 변경'을 누릅니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDdfMTQ0/MDAxNzc4MTE5NzA5NzMw.Lm4IJBQqLBSXOmBKKbd9r4NBFy3Y7AIxXBPJ5dlhpfcg.XeaP2qeMRLyopzAPY__VMlYaRXWnpBSJjIDW2KNflmwg.PNG/image.png?type=w1600)

여기부턴 위와 동일합니다.

그럼 일단 고정 ip설정을 위해 이더넷0의 ipv4를 바꿔보겠습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjE5/MDAxNzc4MDQyOTEwMjEy.xnfzSI3L91uyN4arl467csaG7p124ya-0peoZ04HHQcg.CkgiH5rXG5t14tWysCKEouv3iMRYLstfCrC6ptilNn0g.PNG/%EC%86%8D%EC%84%B1%ED%81%B4%EB%A6%AD-3.png?type=w1600)

IPv4를 찾아 속성을 누릅니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfNTIg/MDAxNzc4MDQyOTE0NzY4.hWYLOQkI3qYID_5k9y4rIYdHYl71mUo47EL_jDxYntEg.0O8_tr13lORVw6Ix960Fj_ma_ODknB1BpgOR6fYPRb4g.PNG/ip%EC%84%A4%EC%A0%95%28%EC%88%98%EB%8F%99%29-4.png?type=w1600)

처음엔 자동으로 ip주소 받기가 되어있습니다.

우리가 배운 DHCP(자동할당) 입니다.

바꾸기 전 현재 ip를 확인해보겠습니다.

터미널 창을 열고 ipconfig를 입력해줍니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTQ0/MDAxNzc4MDQyOTIwMjcx.GmelhRFEBpBNNN4Cg_u5VFuLxWQnYFHKKcP-Kbq1Uxwg.p4aKm8ClK9J2tUd0oVzW7kifaSiQ4eAVPR4G_Z8OEIAg.PNG/ipconfiggateway%EC%95%8C%EC%95%84%EB%B3%B4%EC%9E%90-5.png?type=w1600)

192.168.100.139네요.

ip주소 말고 게이트웨이 칸도 비어있는데

기본 게이트웨이는 어떻게 입력해야할지 몰라서 찾아보았습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfNjAg/MDAxNzc4MDQyOTM0ODU3.k8NOmamFW1kGvlddIIbC1v1ZO73jSw9omgiQtyCtPRQg.pvKjqRAjG-yBOMhdhJ3u4Ewa9ZLaaMRu5RHb6hIuZ54g.PNG/%EA%B2%8C%EC%9D%B4%ED%8A%B8%EC%9B%A8%EC%9D%B4%EA%B0%80_2%EC%9D%B8%EC%9D%B4%EC%9C%A0-6.png?type=w1600)

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTQw/MDAxNzc4MDQyOTM5MjIz.RVHXmZKpJhtJgS8nJifs3sBrvUTgyaXwRCX62B88ejwg.p_Ao_313h27G17colSbAHdQjt5ONKSfoAYiOxMVnZL8g.PNG/%EA%B2%8C%EC%9D%B4%ED%8A%B8%EC%9B%A8%EC%9D%B4_2%EC%9D%B8%EC%9D%B4%EC%9C%A0%282%29-7.png?type=w1600)

게이트웨이를 확인해보니 .1이 아니라 .2로 끝나는 걸 확인할 수 있는데요.

.1은 왜 안되는건지 또 .3은 안되는지 물어보니까

vm환경이기 때문에 192.168.100.2를 써야 인터넷이 된다고 합니다!

![](https://storep-phinf.pstatic.net/ogq_5eedbcd06ab59/original_21.png?type=p50_50)

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTI5/MDAxNzc4MDQyOTcyNTg4.M00maCbG93jtBOAwX6PVJQlPeiXnsDzryjL0kCqd07Eg.miw4XtE0B_1g_nrqHtKGGC0T-nkYKBh50aOKnl9bhfAg.PNG/ip%EC%84%A4%EC%A0%95_%EB%81%9D-8.png?type=w1600)

그럼 이제 진짜로 192.168.100.200으로 변경해보겠습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDhfMTEw/MDAxNzc4MTk5MTQyNzM0.UF-Y-QwhejeGT0dwK04pvd2SUyjCeP1pwarrUIC6BkQg.5zV72RM2z423JITxLPUYqk9DhkABhM0zWSW_ORnJx9Ag.PNG/200%EC%9C%BC%EB%A1%9C%EB%B3%80%EA%B2%BD.png?type=w1600)

잘 변경되었습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfNTIg/MDAxNzc4MDQ0NDIzMTU2.X3pxt9xE6LHlhurznt0fjl_ORQ4A4j9id8Tf42OwWpYg.9w6mPxIgJ5vmnp4chEnD-oNqrnpz9PLkFQwapr78Dhcg.PNG/image.png?type=w1600)

다음 순서로 불필요한 포트를 식별해보겠습니다.

근데 저는 불필요한 포트에 대해서 잘 모릅니다.

그래서 검색을 해봤습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjM2/MDAxNzc4MDQzMDIxMzgx.gtnemYpPPOYRvYGWJkQbhbuzvJ4v_Uc7FAXbp5yILxQg.EoSSWShG9VWAVF65RL8mbshSt9yGEGWGSXPUFjBfU8cg.PNG/%EC%9E%98%EC%95%8C%EB%A0%A4%EC%A7%84_%EC%9C%84%ED%97%98_%ED%8F%AC%ED%8A%B8-15.png?type=w1600)

잘 알려진 위험 포트입니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDdfMTYy/MDAxNzc4MTI2MzE4Nzk5.awltppmPsQnsK7jKBhQA_K95XsmrRAb2hMRQsi9rZf0g.o41vr8IxjXbIFKTKapvLqjGTEkP2QNm9r_-9hrrXZn0g.PNG/image.png?type=w1600)

화면에서도 확인할 수 있는 포트입니다.

옵션 ano의 의미를 아시나요?

알려드릴게요!

ano는 All/ Numeric/ Owning process, 세 옵션을 합친 것으로

- a(All) : 연결된 모든 소켓을 표시
- n(Numeric) : 주소와 포트번호를 이름이 아닌 숫자로 표시
- o(Owning process) : 해당 연결을 소유하고 있는 프로세스 ID를 표시

입니다.

다음 순서는 ipconfig와 ipconfig /all 을 비교해보겠습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDdfMjU0/MDAxNzc4MTE3Nzg2NDU2.JnbEdq5Hxbme1F34V49S2t79dK__W4IT0RFIs9uiUJUg.0bGVH0dxHbkG2aN0wodb9j_6Ypafmvt_r8lu6OzNjGwg.PNG/image.png?type=w1600)

ipconfig, ipconfig /all cmd에 입력

/all 이 붙으면 ip주소 뿐만 아니라 네트워크 어댑터의 대한 모든 세부 정보(기본 정보, MAC 등)를 확인할 수 있습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfODEg/MDAxNzc4MDQzMTczMjc4.WJW2bQ8K8WDwZX63PYlWekLaFatxPY7pE73M4WdygnEg.ORpvzUM3IOtSoEZKauxjZhnnuaDpp92X4zUXRFWhnyMg.PNG/%EB%8F%99%ED%98%84%EB%8B%98IP%EB%A1%9C_PING%EB%B3%B4%EB%82%B4%EB%B3%B4%EA%B8%B0-3.png?type=w1600)

동현님 ip로 ping보내기

근데 ping이 안 됩니다. 또 시작이네요.

ping이 안되는건 방화벽 문제예요. 무조건이라고 할 수 있을까요?

일단 먼저 대답해드릴게요.

아니요.

무조건이라는건 없어요.

가장 흔한 이유는 방화벽 문제라고 합니다.

윈도우 서버는 기본적으로 보안을 위해서 외부에서 들어오는 ICMP 패킷을 차단하도록 설정되어 있습니다.

당연히 ICMP 패킷을 사용하는 ping도 차단된 겁니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTU0/MDAxNzc4MDQ0Njc1MDAw.sSImIHiSV_snZvSM-MOkHptWoT8rXcTam7Qw4CuROfog.6_PlbyyV24lO0wu9_SLzipo4gc-ps5W5586paOweddwg.PNG/image.png?type=w1600)

그 외에도 이런 원인들이 있습니다.

동현님 같은 경우엔 방화벽 내리니 바로 됐습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjc0/MDAxNzc4MDQzMTc4MjAx.dsFhEHPoqJjea0XdLBWzeEM5uTWuqy6f6kHWz4wvmJwg.zKA7pUznt4rPa68DrtQy0P-eDohsuIF4m_9QQwe9OmEg.PNG/%EA%B9%80%EB%8F%99%ED%98%84%EB%8B%98_%EB%B0%A9%ED%99%94%EB%B2%BD_%ED%95%B4%EC%A0%9C_-4.png?type=w1600)

동현님 방화벽 해제

tracert도 해줍니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTIg/MDAxNzc4MDQzMjI5NjIw.bZBIoneuCRr51NaC_UU_hYcX7mVpRzwX-EJKx-hBk-Ig.wpxli5X0SAdv5PEgUt-afrsJzk2C9pHqPWk8Ti_kwZMg.PNG/%EB%8F%99%ED%98%84%EB%8B%98%EC%9D%B4%EB%A6%84%EC%A7%80%EC%A0%95%EC%A0%84_-5.png?type=w1600)

동현님 컴퓨터 이름 지정 전

WIN-C9... 였는데

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTY0/MDAxNzc4MDQzMjQzMzM3.jHaMetHfzIl7KjyEjJ45sx9WOjAeqWFRLvd0Z7l11psg.iTWW1jr8vwglxgqogdg9dPqgLCLH97PPpIlu2XFGDfgg.PNG/%EA%B9%80%EB%8F%99%ED%98%84%EB%8B%98_%EC%9D%B4%EB%A6%84%EC%A7%80%EC%A0%95_kdh_-6.png?type=w1600)

이름 지정 후

깔끔하게 KDH 으로 바꿔주셨네요.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMzYg/MDAxNzc4MDQzMjUzMjMy.DbMR9LQHLorCqSdgTPE6RsC5ArFVt4sD4y2-3z3eKJIg.Hibqy-x3fgxDwZjaTf4dW26x-VFTHs5VhA9ThYwIuQsg.PNG/%EC%A3%BC%ED%95%9C%EB%8B%98_%EC%9D%B4%EB%A6%84%EC%84%A4%EC%A0%95_%ED%9B%84_%EC%9E%98%EB%9C%B8_-7.png?type=w1600)

주한님 컴퓨터 이름 변경

주한님 컴퓨터 이름도 2019서버로 바꿔주셨습니다.

화면을 보면 알 수 있듯이 홉 수가 하나밖에 없는 걸 확인할 수 있습니다.

저희 반 안에서는 같은 네트워크 대역을 공유하기 때문입니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDdfMjA5/MDAxNzc4MTI2ODUyNzM4.f-xjqzz-0jLz7MQnALmxVFdPO4yiBjtRYfI5Z0ZpkPog._GFU9YoivFjMg-sdLFhdR5m1XqEwfwui7Q9SXCVooogg.PNG/image.png?type=w1600)

위 이유도 참고하면 좋을 것 같습니다.

**nslookup**도 입력해보기

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjMz/MDAxNzc4MDQzMjYxNzc5.rA4ZvJBg-bti9s64HcAObWDUxyA_SuJRK3Y01HJJKsgg.h6uY9c6xA-t8cnRTwXhS0mDQa-2rfXIU8ubKNDZVIwQg.PNG/nslookup%ED%95%98%EB%8A%94%EC%9D%B4%EC%9C%A0-8.png?type=w1600)

nslookup google.com과 naver.com

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDdfMTAz/MDAxNzc4MTIwMjY4NTY4.FadLCwsKi1V4XdFhtxEIHwRZ3-_FlVCyGhFHjP2AJkQg.snajuASzNTDff12RfZSYRHIknBAHWxShPvb336Eho_Yg.PNG/image.png?type=w1600)

DNS 서버에 8.8.8.8까지 입력 안하면 Unknown이 뜹니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjA3/MDAxNzc4MDQyOTg3NTY4.TwqwXW2fRyV_K1nmgLlwQp3v_Ebp7J_ZvtC1AfRFWnkg.58O7TPuJQp5uXbZMnsLSySjKzh_z4YUDr1PpgW3VyBog.PNG/dns_%EC%84%A4%EC%A0%95_-11.png?type=w1600)

그럼 DNS 서버 주소도 입력해줍니다.

참고로 보조 DNS서버도 ㅈㅁㄴㅇ의 추천을 받았습니다.

잘 모르는 부분이라 더 찾아보고 내용 추가하겠습니다!

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfNzYg/MDAxNzc4MDQyOTkxODQy.qylnkbf_VSgIjVZ6JFxoxkRXMjt2fY9pJO_0S8Xlvpgg.MBT0W0W69jkWNjth-fnD5t0AXix2uxXhsqexqItErqsg.PNG/%EB%96%B4%EC%96%B4%EC%9A%94_-12.png?type=w1600)

이젠 8.8.8.8을 입력 안 해도 서버 정보가 나옵니다.

근데 다들 잘 nslookup아시나요?

리눅스마스터 공부하면서 보긴했지만 .. ~

일단 전 잘 몰라서 찾아봤습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjcz/MDAxNzc4MDQzMjY4MDI4.LHATGEX2vkM-Yr1zhrR8dWlbxbPYebuGFbjnsP8Q0VAg.IOx1Ws9JEomM3MAD6AU_HytJ-hof24F0v-CvPM31dPYg.PNG/nslookup%EC%93%B0%EB%8A%94%EC%9D%B4%EC%9C%A0-9.png?type=w1600)

도메인 이름으로 ip 알아내는 명령어가 nslookup입니다.

이제 여기부터 진짜 재미있는 거 할 거예요. 기대해도 좋습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTUg/MDAxNzc4MDQzMzkyODE4.7nxs2b8EU9j7LDV_3CZ1ylv1mM_YiPSSKlYw-TvekKkg.p6o9sohOyofnTokBZW4xCQLworvakNG_jWFA_ABKM9Qg.PNG/image.png?type=w1600)

Test-NetConnection

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjIz/MDAxNzc4MDQzNDA1ODM5.HY4dCa4vcVMgpw14cFAzetzU0HsykaPEbRqN1JgsIl0g.VPzPYYGq7-qzXiMIlh6gel5zCujRSvMzkWejwItyhM0g.PNG/%EC%B2%AB_%EB%AA%85%EB%A0%B9_cmd%EC%97%90%EC%84%9C_%EC%95%88_%EB%90%A8-1.png?type=w1600)

영어로 안 된다고 하네요.

왜 안 되냐!하고 보니 위에 분명히 powershell 기반 포트 연결 테스트라고 되어있는데 그냥 cmd에 했었네요^^

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjkg/MDAxNzc4MDQzNDEzODc4.6XnDyrKLElYMzHrE1OZUxMIMKEzXfktwvg-taM4vVT0g.g0D90dN4BnaiY1G1nW8CP73su_zCJ4WGYy-vI5gqA6Eg.PNG/%EC%9D%B8%ED%84%B0%EB%84%B7_%EC%84%B8%EA%B3%84%EC%97%90_%ED%8C%8C%EC%9B%8C%EC%89%98_%EB%93%B1%EC%9E%A5%EC%9D%B4%EB%9D%BC..-2.png?type=w1600)

powershell을 입력하면 입장 가능! PS가 붙은 걸 알 수 있습니당.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTI2/MDAxNzc4MDQzNDQyMDMy.6gIuldV1_KPGgwIAI6YooptR1q9C7vdz9iDsUFXGcMUg.xY45b8evewJUaM8UZvTyexTMVI8_eh4uG4JcNyxhipEg.PNG/%EB%8C%80%EC%96%B4%EC%9E%85%EB%8B%88%EB%8B%A4_TNC_%EC%9E%85%EB%A0%A5_%EC%8B%9C_%EB%93%B1%EC%9E%A5-3.png?type=w1600)

저 파란 창 갑자기 떴다가 사라졌습니다. 로딩이라고 보면 될 것 같습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMzUg/MDAxNzc4MDQzNDY2ODQy.iKhyHf_TKBTHTfFaH0ULddPGAxfABfkK5_FSR9l5lPQg.4zrEKARiCc2VRYRMyH5KTbxAg3NVV5RK_4uQSD8wcLIg.PNG/%EB%8C%80%EC%96%B4_%EB%8B%A4%EC%9D%8C%EC%97%90_%EB%9C%A8%EB%8A%94_%ED%95%B4_-4.png?type=w1600)

밑에 다양한 정보가 뜨는 걸 확인할 수 있습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfNDAg/MDAxNzc4MDQzNDcxNDc2.2N-hQ5ZgA5TXoKAhdDelMMUVHP4XdnfuMwgLcjFV4nMg.JVza37xziAP-cJHRwikOOneq8JSZKmrtsIpyS3pmoAMg.PNG/%EC%84%A4%EB%AA%85_4.1.png?type=w1600)

밑 정보의 의미를 검색해봤습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTY2/MDAxNzc4MDQzNDgxOTcz.DwMy-PiFHsHRIoT3TAuy9fvSYe5xbO_QJ-M22sx740og.a4bkOAy19X-Pf6O9cwtHLEvymjKXeH9wib62yivWVewg.PNG/%ED%8C%8C%EC%9B%8C%EC%89%98_%EB%91%90_%EB%B2%88%EC%A7%B8_%EB%AA%85%EB%A0%B9%EC%96%B4_%EC%8B%A4%ED%96%89-5.png?type=w1600)

Get-NetAdapter도 입력해줍니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfOTYg/MDAxNzc4MDQzNDg3ODcx.g-7PaKDy_p1mo5XLV1miNLbV5-DDG6AFgbRimm0kpvAg.ojhVW6r3kmwwBrRsrOREA6DgBQLkhMfECvMCsSGSr1Ig.PNG/%EA%B7%B8%EC%97%90_%EB%8C%80%ED%95%9C_%EC%84%A4%EB%AA%85_-5.1.png?type=w1600)

이 친구의 밑 정보도 의미를 검색해봤습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTYz/MDAxNzc4MDQzNDg5OTcx.AEeZMc_OraV_F4RjPHwo5pcd-SIRec1I920VYq8u53Ug.pVaxFLbXicHNpDa9Cg4IwXwZ8wouEDt5Y08XU7NszEIg.PNG/%ED%99%9C%EC%84%B1%ED%99%94_%EB%90%98%EC%96%B4%EC%9E%88%EB%8A%94%EC%A7%80_%ED%99%95%EC%9D%B8_enable-PSremoting_-6.png?type=w1600)

WinRM(Windows Remote Management) 서비스를 시작했습니다.

Status: Running이라고 뜨죠? 이제 이 서버는 원격 조종을 받을 준비가 완벽히 끝났다는 뜻입니다.

여기부터가 진짜 재미있어요 다들 해보셨으면 좋겠어요.

하는 법 설명도 가능합니다. (송규석이)

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfOTUg/MDAxNzc4MDQzNTcxMDkw.e2AgIOvGI8GOb4719DaePBrMfgIEX3vNTMvSImfp4Ocg.Mf1NBDe7n0U1_QdWYzkgHczgDjBXBVuTNavysMVsjy0g.PNG/%EC%A3%BC%ED%95%9C%EB%8B%98_%EC%9B%90%EA%B2%A9_%EC%A0%91%EC%86%8D_%EC%84%B1%EA%B3%B5-0.png?type=w1600)

Enter-PSSession으로 들어갈건데 targetIP와 cred 변수를 지정해줍니다.

![](https://storep-phinf.pstatic.net/ogq_5ebebeedf0c9a/original_10.png?type=p50_50)

변수를 지정하지 않고 직접 입력해서 연결하려고 했으나 오류가 계속 발생해서 찾아보니,

변수 지정 후 들어가라고 하네요. 정확한 이유는 다시 한 번 알아보겠습니다.

아무튼 주한님 서버에 접속 성공ㅎ

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjY0/MDAxNzc4MDQ4NzY2MDUy.BJ1hF5pskfjV-L-9XMqsNXdl5qTR3qYYj9EOGNK2uM8g.GucV-px6Ymx72lb5MUOcyPvgGK7wAuANYPSRX9TuJo8g.PNG/image.png?type=w1600)

set-netfirewallprofile true, false(방화벽을 켰다, 껐다!)

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfNjkg/MDAxNzc4MDQzNTgyMDgy.k6npwuMqyyZQYEbvcIAYj4rFsTkEusSmzMHyX8g4XWAg.yY-LwIJw2SUCyPfh1iH1CiMTzKe3ysDtDvskV2ogG4wg.PNG/%EC%A3%BC%ED%95%9C%ED%98%95%EB%8B%98_%EB%B0%A9%ED%99%94%EB%A9%B1_off-3.png?type=w1600)

주한님 실제 화면입니다. 방화벽 끄기

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjcg/MDAxNzc4MDQzNTg5MzEw.4eknPCuPcLo88cW03pI3ZroI4bzoYnM2NMZ_FS_kHgUg.2nZhbwQZksIBTroV6vJBXFM4QipDqoePvYjY9DR1NaEg.PNG/%EB%B0%A9%ED%99%94%EB%B2%BD_on_-4.png?type=w1600)

방화벽 켜기 도 가능 !! 정말 신기합니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjMg/MDAxNzc4MDQzNTk0MDEz.3I2Qd7Ww5EpoJ3q3zOH1jEI3NG5Scd2_5BYiN_5f5JAg.owjWNhoQzxR9c2EfH4ypDBw2YtlUmW9CH0VBP0qygBYg.PNG/%EC%99%95%EC%9D%B4%EB%90%98%EC%97%88%EC%9D%8C-5.png?type=w1600)

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMzUg/MDAxNzc4MDQzNTk5NTA1.A1HUhuHq7rqlbEHvuz9C752eUF10130zKPCCWmbekNcg.XJWfsAIXTmFIy-ktDAmlVLUHr7FL0lKm9OJAXBkT5cYg.PNG/%EC%9B%90%EA%B2%A9%EC%A0%91%EC%86%8D%EC%9D%84_%EC%A2%85%EB%A3%8C_%ED%9B%84_%EB%8B%A4%EC%8B%9C_%EB%93%A4%EC%96%B4%EA%B0%80%EB%A0%A4%EA%B3%A0_%ED%95%98%EB%8B%88%EA%B9%8C_%EB%B3%80%EC%88%98_%EC%A7%80%EC%A0%95_%EB%8B%A4%EC%8B%9C%ED%95%A8_%28%EC%9B%90%EC%A2%85%EB%8B%A4%EB%93%A4%ED%95%98%EB%B3%80%EB%8B%A4%29-6.png?type=w1600)

이번엔 동현님 한테 접속할건데

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfOTUg/MDAxNzc4MDQzNjAyNzc3.Z-3l3IuZ77EVqWv8o9lfgDv-pUPjsIGiPrLd4A653xUg.W8Xkp1WFoNP4AgZARsY-bybR1lJgkD9acSkpii88050g.PNG/%EC%9B%90%EC%A2%85%EB%8B%A4%EB%93%A4%ED%95%98%EB%B3%80%EB%8B%A4_%EC%84%A4%EB%AA%85_-7.png?type=w1600)

파워쉘을 껐다가 켜면 변수 지정을 꼭 다시 해야합니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTYy/MDAxNzc4MDQzNjA3NzM4.IJSC8z5e3Gj71nTkEM2UW1cD5Yi2szzwreB4XRaBv30g.EOSIrCJGjYobao9jbnxUEtklSccrcRZcoor8rqmHLDwg.PNG/%EC%A0%91%EC%86%8D%ED%95%98%EC%A7%80_%EC%95%8A%EA%B3%A0_%EB%AA%85%EB%A0%B9%EC%96%B4_%EC%8B%A4%ED%96%89-8.png?type=w1600)

리눅스의 touch 명령어가 윈도우에선 ni(new-item)입니다.

위 사진을 보면 exit로 분명 동현님 서버에서 나왔습니다.

invoke-command... 를 입력하여 동현님 몰래 동현님 서버에서 hiroo 파일 만들었습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjUx/MDAxNzc4MDQ5NTIyNjUx.IObP178YLguOCQOeTnvIMeoNCog4w_t1UBp5iaNwio4g.2go6pOnO8pmwLyrs_G_x1jJPkD8aQ718W3pqrpuYfe4g.PNG/%EC%9D%B4%EB%AF%B8%EC%A7%80.png?type=w1600)

동현님 서버에서 실제로 캡쳐한 화면입니다. (방심은 금물!)

Room mind is gold water!

invoke-command에 대해 더 알아보자면

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfOTEg/MDAxNzc4MDQ1Mzc3MjA4.mBlT24kl2Bj8DHIIkBh0BRmjoUoRf06ZfQFnu8yh8A8g.6_mZ3FrK2KUvw56xfRwLt9vMsMDHu_R6jtKDeAzIny4g.PNG/image.png?type=w1600)

한마디로 원격조종 리모컨의 역할을 한다고 볼 수 있습니다.

다음 순서는 실행 중인 서비스 목록을 확인해보겠습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfNzQg/MDAxNzc4MDQzNzAzMzkw.PdRwcc0sDcEtnQVcZY5Dy0STmu0-oJ_BkpGZwT0Kf9og.JlQ4-uThMQWVe1yOnhdqGXC_wTA_Silt7TaBSAAPjewg.PNG/image.png?type=w1600)

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjMx/MDAxNzc4MDQzNzA3MjY2.0onr8RAFXCA5s2gb_5e9_tV4x4txo2a0DnOrsAXzcF4g._rtJv3f41qUe_2mTQVWZLvIQRe09BRDvGYdixr1Litwg.PNG/%EC%9B%90%EA%B2%A9%EC%9C%BC%EB%A1%9C_%EC%84%9C%EB%B9%84%EC%8A%A4%EB%AA%A9%EB%A1%9D%EC%9C%BC%EB%A1%9C_%ED%99%95%EC%9D%B8-1.png?type=w1600)

물론 우리 서버 말고 동현님 서버에서 실행중인 서비스요 ^^. 조심하세요.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMyAg/MDAxNzc4MDQzNzEwNjM5.GEY-YrfgJwmgdXkaljV4O3EXIj4kMsDkDST7YAQGTf0g.BuGAW3CEGA2DPX2m3Z2B-JT_rNyNOhU8_pFyQvodLqkg.PNG/spooler_%EC%97%AC%EA%B8%B0_%EC%9E%88%EC%96%B4%EC%9A%94_-2.png?type=w1600)

잠깐만.......!! 왜 그 많은 서비스 중 spooler를 건드렸을까요?

이유는 아래와 같습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfNTkg/MDAxNzc4MDQzNzkyNTI4.xuGUdjCw_t4p5Z_GYp-MFtnxQc7e4zXXUlNZIwH3H1Yg.yczPAFzR6lKRQUIg0H1UJww7VkFsiWCcsr_v0J2bKvQg.PNG/image.png?type=w1600)

꺼도 괜찮기 때문이죠.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjA3/MDAxNzc4MDQzNzE0NDg5.l_7FjPkfnaIZX1TRpLb1NWQmWSn58KQCGaHwrZ5hs2gg.d4vRLm9cLyIn6BvZrZsENyQ0v9AIXbFAdWnCD8yp3M8g.PNG/spooler_%EB%81%84%EA%B3%A0_%EB%AA%A9%EB%A1%9D_%ED%99%95%EC%9D%B8%ED%95%B4%EB%B3%B4%EB%8B%88.._-3.png?type=w1600)

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMTIy/MDAxNzc4MDQzNzE3Mjc2.wL4mKcvxsIAM20tXSjfUUNkfu9fDWAVMv8dKxt0kv1sg._HplI1W2wP_765eJHG8mSUMwSfkPAlN5b1XASrJERXAg.PNG/spooler_%EC%97%AC%EA%B8%B0_%EC%97%86%EC%96%B4%EC%9A%94_-4.png?type=w1600)

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjEx/MDAxNzc4MDQzNzE5NTI5.oRwLzjNyL57yg6A0ZNFtUUAxxbcxZsywT4itzUUfGs4g.GcTQSEoyTYMMK_HI3uZRNtSbl9WXRf_DACJLz1lyCbwg.PNG/spooler_%EB%8B%A4%EC%8B%9C_%EC%BC%9C%EA%B3%A0_%EB%AA%A9%EB%A1%9D_%ED%99%95%EC%9D%B8-5.png?type=w1600)

다시 서비스를 재가동했습니다.

![](https://cafeptthumb-phinf.pstatic.net/MjAyNjA1MDZfMjc5/MDAxNzc4MDQzNzIxOTU1.pb9qNZffsyDRqEGSNN-34lVPI0ipx66rizVNcywjD04g.Vy5RfpYpws1JH1fVIit72Qid2x0sMJwY1KDnNPON_-gg.PNG/spooler_%EB%8B%A4%EC%8B%9C_%EC%97%AC%EA%B8%B0_%EC%9E%88%EC%96%B4%EC%9A%94_-6.png?type=w1600)

동현님은 자신의 서비스가 껐다 켜졌는지 모를 겁니다..

이렇게 윈도우 서버에서 ip를 설정하고 다른 서버에 원격으로 접속하는 시간을 가져봤습니다.

송규석 : 사실 이번 시간에 많은 시련과 고난이 있었습니다. 명령어 치면 안 된다고 하고, 알아보면 무슨 의미인지 모르겠고..

그래도 그만큼 재미 있었던 시간이었습니다. 이번 보고서 만큼은 다른 분들도 시간 되실 때 한 번쯤은 따라하셨으면

좋겠습니다. 저희(송규석)에게 물어보시면 얼마든지 도와드리겠습니다!

긴 글 읽어주셔서 감사합니당

![](https://storep-phinf.pstatic.net/ogq_5ebebeedf0c9a/original_24.png?type=p50_50)