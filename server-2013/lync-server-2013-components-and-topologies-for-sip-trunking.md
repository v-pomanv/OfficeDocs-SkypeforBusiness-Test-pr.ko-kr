﻿---
title: 'Lync Server 2013: SIP 트렁크에 대한 구성 요소 및 토폴로지'
TOCTitle: SIP 트렁크에 대한 구성 요소 및 토폴로지
ms:assetid: 8ed9a9d0-517e-4f36-a131-22cdafa257fa
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/Gg398720(v=OCS.15)
ms:contentKeyID: 49304350
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013의 SIP 트렁크에 대한 구성 요소 및 토폴로지

 

_**마지막으로 수정된 항목:** 2012-09-21_

다음 그림에서는 Lync Server의 SIP 트렁크 토폴로지를 보여 줍니다.

**SIP 트렁크 토폴로지**

![SIP 트렁크 토폴로지](images/Gg398720.669fb55d-7c81-4e21-9421-fabc43d6e064(OCS.15).jpg "SIP 트렁크 토폴로지")

다이어그램에 나온 것처럼 엔터프라이즈 네트워크 및 PSTN(공중 전화망) 서비스 공급자 간의 연결에 IP VPN(가상 사설망)이 사용됩니다. 이 사설망의 목적은 IP 연결을 제공하고 보안을 향상시키며 선택적으로 QoS(서비스 품질) 보증을 얻는 것입니다. VPN의 특성으로 인해 SIP 신호 트래픽을 위한 TLS(Transport Layer Security)나 미디어 트래픽을 위한 SRTP(실시간 전송 프로토콜)를 사용할 필요가 없습니다. 따라서 엔터프라이즈와 서비스 공급자 간의 연결은 SIP를 위한 일반 TCP 연결 및 IP VPN을 통해 터널링되는 미디어를 위한 UDP를 통한 일반 RTP(실시간 전송 프로토콜)로 구성됩니다. 이때 VPN 라우터 간 모든 방화벽에서는 VPN 라우터가 통신할 수 있도록 포트를 열어 놓아야 하고 VPN 라우터의 외부 에지에 대한 IP 주소는 공개적으로 라우팅 가능한 주소여야 합니다.


> [!IMPORTANT]
> 장애 조치(failover)를 비롯한 고가용성에 대한 지원의 제공 여부를 서비스 공급자에 확인하십시오. 제공하는 경우 해당 설정 절차를 확인해야 합니다. 예를 들어 각 중재 서버에 대해 하나의 IP 주소 및 하나의 SIP 트렁크만 구성해야 합니까? 아니면 각 중재 서버에 대해 여러 SIP 트렁크를 구성해야 합니까?<BR>여러 중앙 사이트가 있는 경우 서비스 공급자가 다른 중앙 사이트로/에서 연결을 사용하도록 설정할 수 있는지 문의하십시오.




> [!NOTE]
> SIP 트렁크의 경우 독립 실행형 중재 서버를 배포하는 것이 좋습니다. 자세한 내용은 배포 설명서의 <A href="lync-server-2013-deploying-mediation-servers-and-defining-peers.md">Lync Server 2013에서 중재 서버 배포 및 피어 정의</A>를 참조하십시오.



## SIP 트렁크에 대해 중재 서버 보호

보안을 위해 두 VPN 라우터 간의 각 연결에 대해 VLAN(가상 LAN)을 설치해야 합니다. VLAN의 실제 설치 프로세스는 라우터 제조업체별로 다릅니다. 자세한 내용은 라우터 공급업체에 문의하십시오.

다음 지침을 따르는 것이 좋습니다.

  - 경계 네트워크(DMZ, 완충 지역 및 스크린된 서브넷이라고도 함)에 있는 중재 서버와 VPN 라우터 간에 VLAN(가상 LAN)을 설치합니다.

  - 라우터에서 VLAN으로 브로드캐스트나 멀티캐스트 패킷이 전송되는 것을 허용하지 않습니다.

  - 라우터에서 중재 서버가 아닌 다른 곳으로 트래픽을 라우팅하는 모든 라우팅 규칙을 차단합니다.

VPN 서버를 사용하는 경우 다음 지침을 따르는 것이 좋습니다.

  - VPN 서버와 중재 서버 간에 VLAN을 설치합니다.

  - VPN 서버에서 VLAN으로 브로드캐스트나 멀티캐스트 패킷이 전송되는 것을 허용하지 않습니다.

  - VPN 서버 트래픽을 중재 서버가 아닌 다른 곳으로 라우팅하는 모든 라우팅 규칙을 차단합니다.

  - GRE(Generic Routing Encapsulation)를 사용하여 VPN의 데이터를 암호화합니다.
