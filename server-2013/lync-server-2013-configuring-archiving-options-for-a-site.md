﻿---
title: 사이트에 대한 보관 옵션 구성
TOCTitle: 사이트에 대한 보관 옵션 구성
ms:assetid: 59b48fd9-d5fc-40b4-abae-e9cf89ee5573
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/JJ204930(v=OCS.15)
ms:contentKeyID: 49303728
ms.date: 08/24/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 사이트에 대한 보관 옵션 구성

 

_**마지막으로 수정된 항목:** 2012-10-09_

이러한 각 사이트에 대해 보관 구성에서 옵션을 만들고 구성하여 특정 사이트에 적용할 보관 옵션을 지정할 수 있습니다. 사이트 구성은 전역 구성을 무시하지만 사이트 구성에 지정된 사이트로만 제한됩니다. 풀 구성은 사이트 구성을 무시합니다.

전역, 사이트 및 풀 구성에 대한 계층을 포함하여 보관 구성의 작동 방법에 대한 자세한 내용은 계획 설명서, 배포 설명서 또는 작업 설명서에서 [Lync Server 2013의 보관 작동 방식](lync-server-2013-how-archiving-works.md)을 참조하십시오.


> [!NOTE]
> 보관을 사용하도록 설정하기 전에 보관 구성에서 모든 적합한 옵션을 지정해야 합니다.




> [!IMPORTANT]
> 보관을 사용하도록 설정하려면 글로벌 수준, 그리고 적절한 경우 사이트 및 사용자 수준에서 내부 및 외부 통신의 보관을 제어하는 보관 정책을 지정해야 합니다. 사용자 수준 정책을 구성하는 경우에는 또한 특정 사용자에게 사용자 정책을 할당해야 합니다. 보관 정책을 만들고 구성하는 방법에 대한 자세한 내용은 작업 설명서에서 <A href="lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md">Lync Server 2013에서 내부 및 외부 통신의 보관 관리</A>를 참조하세요.



## 사이트 수준에서 보관 옵션을 구성하려면

1.  CsArchivingAdministrator 또는 CsAdministrator 역할에 지정된 사용자 계정에서 내부 배포된 컴퓨터에 로그온합니다.

2.  브라우저 창을 열고 관리 URL을 입력하여 Lync Server 2013 제어판을 엽니다. Lync Server 2013 제어판을 시작하기 위해 사용할 수 있는 여러 방법들에 대한 자세한 내용은 [Lync Server 관리 도구 열기](lync-server-2013-open-lync-server-administrative-tools.md)를 참조하십시오.

3.  왼쪽 탐색 모음에서 **모니터링 및 보관**을 클릭하고 **보관 구성**을 클릭합니다.

4.  **보관 구성** 페이지에서 **새로 만들기**를 클릭한 다음 **사이트 구성**을 클릭합니다.

5.  **사이트 선택**에서 보관을 위해 구성할 사이트를 선택합니다.

6.  **새 보관 설정**의 **보관 설정** 드롭다운 목록 상자에서 다음 중 하나를 수행합니다.
    
      - IM(인스턴트 메시징) 세션에 대해서만 보관을 사용하도록 설정하려면 **IM 세션 보관**을 클릭합니다.
    
      - IM 세션 및 회의 모두에 대해 보관을 사용하도록 설정하려면 **IM 및 웹 회의 세션 보관**을 클릭합니다.
    
      - 정책에 대해 보관을 사용하지 않도록 설정하려면 **보관 사용 안 함**을 클릭합니다.

7.  **새 보관 설정**에서도 다음을 수행합니다.
    
      - 보관을 사용할 수 없을 경우 작업을 차단하려면 **보관이 실패할 경우 IM(인스턴트 메시징) 또는 웹 회의 세션 차단** 확인란을 선택합니다.
    
      - Microsoft Exchange Server를 사용해서 보관 데이터를 저장하려면 **Microsoft Exchange 통합** 확인란을 클릭합니다.
    
      - 데이터 삭제를 사용하도록 설정하려면 **보관 데이터 삭제 사용** 확인란을 선택한 후 다음 중 하나를 수행합니다.
        
          - 특정 일수 이후 삭제되도록 설정하려면 **내보낸 보관 데이터 및 최대 기간(일)이 지난 저장된 보관 데이터 삭제**를 클릭한 다음 일수를 지정합니다.
        
          - 내보낸 보관 데이터에 대한 삭제를 제한하려면 **내보낸 보관 데이터만 삭제**를 클릭합니다,

8.  **커밋**을 클릭합니다.

