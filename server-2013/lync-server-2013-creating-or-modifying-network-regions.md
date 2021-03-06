﻿---
title: 네트워크 영역 만들기 또는 수정
TOCTitle: 네트워크 영역 만들기 또는 수정
ms:assetid: bd08bb66-5976-4ece-b45c-7de19569f814
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/Gg182579(v=OCS.15)
ms:contentKeyID: 49304874
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 네트워크 영역 만들기 또는 수정

 

_**마지막으로 수정된 항목:** 2012-11-01_

네트워크 지역은 여러 지역의 많은 네트워크 부분을 교차합니다. 모든 네트워크 지역은 중앙 사이트와 연결되어야 합니다. 중앙 사이트는 CAC(통화 허용 제어) 대역폭 정책 서비스가 실행되는 데이터 센터 사이트입니다. 네트워크 지역은 Lync Server 제어판을 사용하여 구성할 수 있습니다. 네트워크 지역에는 오디오 및 비디오 연결에 대해 인터넷을 통한 대체 경로가 허용되는지 여부를 결정하는 설정이 포함됩니다. Lync Server 제어판에서 네트워크 지역을 만들고 수정하거나 삭제할 수 있습니다. 기존 네트워크 지역을 삭제하는 방법에 대한 자세한 내용은 [기존 네트워크 지역 삭제](lync-server-2013-deleting-existing-network-regions.md)를 참조하십시오.

## 네트워크 지역을 만들려면

1.  RTCUniversalServerAdmins 그룹의 구성원(또는 이와 동일한 사용자 권한을 가진 사용자 계정) 또는 CsAdministrator 역할이 할당된 사용자 계정에서 내부 배포된 컴퓨터에 로그온합니다.

2.  브라우저 창을 연 다음 Admin URL을 입력하여 Lync Server 제어판을 엽니다. Lync Server 제어판을 시작하는 데 사용할 수 있는 다양한 방법에 대한 자세한 내용은 [Lync Server 관리 도구 열기](lync-server-2013-open-lync-server-administrative-tools.md)를 참조하세요.

3.  왼쪽 탐색 표시줄에서 **네트워크 구성**을 클릭한 다음 **지역**을 클릭합니다.

4.  **지역** 페이지에서 **새로 만들기**를 클릭합니다.

5.  **새 지역** 페이지의 **이름** 필드에 값을 입력합니다. 이 값은 Microsoft Lync Server 2013 배포 내에서 고유해야 합니다.

6.  **중앙 사이트** 드롭다운 목록에서 이 네트워크 지역에 대한 중앙 사이트를 선택합니다.

7.  **오디오 대체 경로 사용** 확인란은 기본적으로 선택됩니다. 이 필드는 기본 경로에 적절한 대역폭이 없는 경우 대체 경로를 통해 음성 통화를 라우팅할지 여부를 결정하며, 인터넷으로 오프로드를 해제해야 하는 경우에만 이 확인란을 선택 취소합니다. 통화가 인터넷 통화인 경우 대역폭 설정에 관계없이 이 확인란을 선택해야 합니다.

8.  **비디오 대체 경로 사용** 확인란은 기본적으로 선택됩니다. 이 필드는 기본 경로에 적절한 대역폭이 없는 경우 대체 경로를 통해 화상 통화를 라우팅할지 여부를 결정하며, 인터넷으로 오프로드를 해제해야 하는 경우에만 이 확인란을 선택 취소합니다. 통화가 인터넷 통화인 경우 대역폭 설정에 관계없이 이 확인란을 선택해야 합니다.

9.  (선택 사항) **설명** 필드에 값을 입력하여 이름 하나로만 표시될 수 없는 이 지역에 대해 추가 정보를 제공합니다.

10. **커밋**을 클릭합니다.

네트워크 지역을 만드는 데 **연결된 사이트** 표는 사용되지 않습니다. 사이트를 만들거나 수정할 때 사이트와 지역이 연결됩니다. 자세한 내용은 [네트워크 사이트 만들기 또는 수정](lync-server-2013-creating-or-modifying-network-sites.md)을 참조하십시오.

## 네트워크 지역을 수정하려면

1.  RTCUniversalServerAdmins 그룹의 구성원(또는 이와 동일한 사용자 권한을 가진 사용자 계정) 또는 CsAdministrator 역할이 할당된 사용자 계정에서 내부 배포된 컴퓨터에 로그온합니다.

2.  브라우저 창을 연 다음 Admin URL을 입력하여 Lync Server 제어판을 엽니다. Lync Server 제어판을 시작하는 데 사용할 수 있는 다양한 방법에 대한 자세한 내용은 [Lync Server 관리 도구 열기](lync-server-2013-open-lync-server-administrative-tools.md)를 참조하세요.

3.  왼쪽 탐색 표시줄에서 **네트워크 구성**을 클릭한 다음 **지역**을 클릭합니다.

4.  **지역** 페이지에서 수정할 지역을 클릭합니다.

5.  **편집** 메뉴에서 **자세한 정보 표시**를 클릭합니다.

6.  **지역 편집** 페이지에서 오디오 및 비디오 대체 경로를 사용하거나 사용하지 않도록 지정하는 설정을 수정하고 설명을 변경할 수 있습니다(자세한 내용은 이 항목의 이전 섹션인 "네트워크 지역을 만들려면" 섹션 참조).

7.  **커밋**을 클릭합니다.

이 페이지에서 **연결된 사이트**는 수정할 수 없습니다. 연결된 사이트 목록은 참조용으로 제공되므로 지역 설정을 수정할 때는 영향을 받는 사이트를 확인해야 합니다.

## 참고 항목

#### 작업

[기존 네트워크 지역 삭제](lync-server-2013-deleting-existing-network-regions.md)  
[Lync Server 2013에서 CAC에 대한 네트워크 지역 구성](lync-server-2013-configure-network-regions-for-cac.md)  

#### 기타 리소스

[New-CsNetworkRegion](https://docs.microsoft.com/en-us/powershell/module/skype/New-CsNetworkRegion)  
[Set-CsNetworkRegion](https://docs.microsoft.com/en-us/powershell/module/skype/Set-CsNetworkRegion)  
[Remove-CsNetworkRegion](https://docs.microsoft.com/en-us/powershell/module/skype/Remove-CsNetworkRegion)  
[Get-CsNetworkRegion](https://docs.microsoft.com/en-us/powershell/module/skype/Get-CsNetworkRegionLink)

