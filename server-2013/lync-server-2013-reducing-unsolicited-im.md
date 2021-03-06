﻿---
title: 'Lync Server 2013: 원치 않는 메신저 대화 줄이기'
TOCTitle: Lync Server 2013에 대해 원치 않는 메신저 대화 줄이기
ms:assetid: d2998708-e699-4465-a918-e1d9ea4c49c3
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/Dn518335(v=OCS.15)
ms:contentKeyID: 60504744
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013에 대해 원치 않는 메신저 대화 줄이기

 

_**마지막으로 수정된 항목:** 2013-12-05_

지능형 IM 필터 응용 프로그램을 사용하면 사용자 작업에 주는 영향을 최소화하면서 가장 일반적인 형태의 바이러스 공격으로부터 Microsoft Lync Server 2013 배포를 보호할 수 있습니다. 지능형 IM 필터는 다음과 같은 기능을 제공합니다.

  - 향상된 URL 필터링

  - 향상된 파일 전송 필터링

지능형 IM 필터를 사용하면 회사 방화벽 외부의 알 수 없는 끝점에서 보낸 잠재적으로 유해하거나 원치 않는 메신저 대화를 차단하도록 필터를 구성할 수 있습니다. 하이퍼링크를 포함하는 메신저 대화, 특정 확장명의 파일 등 차단할 항목을 결정하는 데 사용할 조건을 지정하여 필터를 구성합니다.

지능형 IM 메시지 필터 응용 프로그램을 배포하기 전에 먼저 메시지가 Lync Server 2013 서버 간에 라우팅될 때 필터링 옵션이 적용되는 방식을 이해해야 합니다. 필터링 옵션이 적용되는 방식은 두 서버가 같은 조직에 있는지 또는 서로 다른 조직에 있는지에 관계없이 동일합니다. 이러한 일관성은 사용자 지정 공지 사항이나 경고 텍스트가 메시지에 삽입되고 서버 간에 전송되는 방식에 적용됩니다.

권장 필터링 옵션은 하이퍼링크가 포함된 메신저 대화는 허용하되 지능형 IM 필터가 링크 앞에 밑줄을 삽입하여 링크를 사용할 수 없도록 설정하는 것입니다. 이 옵션을 선택하는 경우에는 하이퍼링크가 포함된 각 메신저 대화의 첫 부분에 표시되는 사용자에 대한 알림을 직접 작성할 수 있습니다.

하이퍼링크를 수정하지 않고 메신저 대화를 그대로 허용하는 필터링 옵션도 있습니다. 이 옵션을 선택하는 경우에는 각 메시지에 삽입되는 사용자에 대한 경고를 직접 작성할 수 있습니다(권장).

하이퍼링크가 포함된 모든 메신저 대화를 차단할 수도 있습니다. 이 옵션을 선택하는 경우에는 서버에서 사용자에게 경고를 보내며, 이 경고는 직접 작성해야 합니다.

