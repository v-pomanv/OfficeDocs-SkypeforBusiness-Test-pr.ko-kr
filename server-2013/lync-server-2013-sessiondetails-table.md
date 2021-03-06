﻿---
title: 'Lync Server 2013: SessionDetails 테이블'
TOCTitle: SessionDetails 테이블
ms:assetid: 783d2508-e31f-4b54-be0c-63aa5ec21c04
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/Gg398589(v=OCS.15)
ms:contentKeyID: 49304096
ms.date: 08/24/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013의 SessionDetails 테이블

 

_**마지막으로 수정된 항목:** 2015-03-09_

각 레코드는 VoIP-VoIP 전화 통화, 두 사용자 간 IM 세션 또는 기타 유형의 세션일 수 있는 하나의 피어 투 피어 세션을 나타냅니다. [Lync Server 2013의 Media 테이블](lync-server-2013-media-table.md)과의 테이블 조인을 수행하면 이 세션에 관련된 각 미디어의 세부 정보를 찾을 수 있습니다.

IsUser1IntegratedWithDeskPhone 및 IsUser2IntegratedWithDeskPhone 필드는 Microsoft Lync Server 2013에 사용된 SessionDetails 테이블에서 삭제되었습니다.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>열</th>
<th>데이터 형식</th>
<th>키/인덱스</th>
<th>세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>SessionIdTime</strong></p></td>
<td><p>datetime</p></td>
<td><p>기본, 외래</p></td>
<td><p>세션 요청 시간입니다. <strong>SessionIdSeq</strong> 와 함께 세션을 고유하게 식별하기 위해 사용됩니다. 자세한 내용은 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013의 Dialogs 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="even">
<td><p><strong>SessionIdSeq</strong></p></td>
<td><p>int</p></td>
<td><p>기본, 외래</p></td>
<td><p>세션을 식별하기 위한 ID 번호입니다. <strong>SessionIdTime</strong> 과 함께 세션을 고유하게 식별하기 위해 사용됩니다. 자세한 내용은 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013의 Dialogs 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CorrelationId</strong></p></td>
<td><p>uniqueidentifier</p></td>
<td><p></p></td>
<td><p>여러 세션의 관계를 지정하기 위한 GUID입니다.</p></td>
</tr>
<tr class="even">
<td><p><strong>ReplaceDialogIdTime</strong></p></td>
<td><p>datetime</p></td>
<td><p>외래</p></td>
<td><p>현재 세션으로 교체된 대화를 식별하기 위한 ID 번호입니다. 자세한 내용은 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013의 Dialogs 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ReplaceDialogIdSeq</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>세션을 식별하기 위한 ID 번호입니다. <strong>ReplacesDialogIdTime</strong> 과 함께 이 세션으로 교체된 세션을 고유하게 식별하기 위해 사용됩니다. 자세한 내용은 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013의 Dialogs 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="even">
<td><p><strong>User1Id</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>세션에 포함된 한 사용자의 ID입니다. 자세한 내용은 <a href="lync-server-2013-users-table.md">Lync Server 2013의 Users 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="odd">
<td><p><strong>User2Id</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>세션에 포함된 다른 사용자의 ID입니다. 자세한 내용은 <a href="lync-server-2013-users-table.md">Lync Server 2013의 Users 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="even">
<td><p><strong>User1EndpointId</strong></p></td>
<td><p>uniqueIdentifier</p></td>
<td><p></p></td>
<td><p>세션의 첫 번째 사용자가 사용한 끝점을 식별하는 GUID입니다.</p>
<p>이 필드는 Microsoft Lync Server 2013에 새로 도입되었습니다.</p></td>
</tr>
<tr class="odd">
<td><p><strong>User2EndpointId</strong></p></td>
<td><p>uniqueIdentifier</p></td>
<td><p></p></td>
<td><p>세션의 두 번째 사용자가 사용한 끝점을 식별하는 GUID입니다.</p>
<p>이 필드는 Microsoft Lync Server 2013에 새로 도입되었습니다.</p></td>
</tr>
<tr class="even">
<td><p><strong>TargetUserId</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>SIP 요청에서 원래의 대상 사용자 URI입니다. 자세한 내용은 <a href="lync-server-2013-users-table.md">Lync Server 2013의 Users 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SessionStartedById</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>세션을 시작한 사용자의 ID입니다. 자세한 내용은 <a href="lync-server-2013-users-table.md">Lync Server 2013의 Users 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="even">
<td><p><strong>OnBehalfOfId</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>발신자가 역할을 대신 수행하고 있는 원래 사용자의 ID를 나타냅니다. 자세한 내용은 <a href="lync-server-2013-users-table.md">Lync Server 2013의 Users 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ReferredById</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>통화를 참조한 사용자의 ID입니다. 자세한 내용은 <a href="lync-server-2013-users-table.md">Lync Server 2013의 Users 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="even">
<td><p><strong>ServerId</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>이 세션에 사용된 프런트 엔드 서버의 ID입니다. <a href="lync-server-2013-servers-table.md">Lync Server 2013의 Servers 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="odd">
<td><p><strong>PoolId</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>세션이 캡처된 풀의 ID입니다. 자세한 내용은 <a href="lync-server-2013-pools-table.md">Lync Server 2013의 Pools 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="even">
<td><p><strong>ContentTypeID</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>세션에 사용된 콘텐츠 형식입니다. 자세한 내용은 <a href="lync-server-2013-contenttypes-table.md">Lync Server 2013의 ContentTypes 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="odd">
<td><p><strong>User1ClientVerId</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>User1이 사용한 클라이언트 버전입니다. 자세한 내용은 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013의 ClientVersions 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="even">
<td><p><strong>User2ClientVerId</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>User2가 사용한 클라이언트 버전입니다. 자세한 내용은 <a href="lync-server-2013-clientversions-table.md">Lync Server 2013의 ClientVersions 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="odd">
<td><p><strong>User1EdgeServerid</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>User1이 사용한 에지 서버입니다. 자세한 내용은 <a href="lync-server-2013-edgeservers-table.md">Lync Server 2013의 EdgeServers 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="even">
<td><p><strong>User2EdgeServerid</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>User2가 사용한 에지 서버입니다. 자세한 내용은 <a href="lync-server-2013-edgeservers-table.md">Lync Server 2013의 EdgeServers 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IsUser1Internal</strong></p></td>
<td><p>bit</p></td>
<td><p></p></td>
<td><p>User1이 내부로부터 로그온되었는지 여부입니다.</p></td>
</tr>
<tr class="even">
<td><p><strong>IsUser2Internal</strong></p></td>
<td><p>bit</p></td>
<td><p></p></td>
<td><p>User2가 내부로부터 로그온되었는지 여부입니다.</p></td>
</tr>
<tr class="odd">
<td><p><strong>InviteTime</strong></p></td>
<td><p>datetime</p></td>
<td><p></p></td>
<td><p>첫 번째 INVITE 요청의 시간입니다. 이 필드는 일반적으로 세션의 초기 INVITE 메시지로부터 생성된 데이터로 채워집니다. INVITE 메시지가 없으면 필드에 첫 번째 관련 SIP 메시지(BYE, CANCEL, MESSAGE, or INFO)의 날짜 및 시간이 채워집니다.</p></td>
</tr>
<tr class="even">
<td><p><strong>ResponseTime</strong></p></td>
<td><p>datetime</p></td>
<td><p></p></td>
<td><p>첫 번째 INVITE 메시지에 대한 응답 시간입니다. 이 필드는 일반적으로 세션에서 초기 INVITE 메시지로부터 생성된 데이터로 채워집니다. INVITE 메시지가 없으면 첫 번째 관련 SIP 메시지(BYE, CANCEL, MESSAGE 또는 INFO)의 날짜 및 시간이 필드에 채워집니다.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ResponseCode</strong></p></td>
<td><p>int</p></td>
<td><p></p></td>
<td><p>세션 초대에 대한 SIP 응답 코드입니다. 이 필드는 일반적으로 세션의 초기 INVITE 메시지로 채워집니다. INVITE 메시지가 없으면 첫 번째 관련 SIP 메시지(BYE, CANCEL, MESSAGE 또는 INFO)의 날짜 및 시간으로 채워집니다.</p></td>
</tr>
<tr class="even">
<td><p><strong>DiagnosticId</strong></p></td>
<td><p>int</p></td>
<td><p></p></td>
<td><p>SIP 헤더에서 캡처된 진단 ID입니다.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CallPriority</strong></p></td>
<td><p>int</p></td>
<td><p>외래</p></td>
<td><p>통화 우선 순위입니다. 자세한 내용은 <a href="lync-server-2013-callpriorities-table.md">Lync Server 2013의 CallPriorities 테이블</a>을 참조하십시오.</p></td>
</tr>
<tr class="even">
<td><p><strong>User1MessageCount</strong></p></td>
<td><p>int</p></td>
<td><p></p></td>
<td><p>세션 중 User1이 보낸 메시지 수입니다.</p></td>
</tr>
<tr class="odd">
<td><p><strong>User2MessageCount</strong></p></td>
<td><p>int</p></td>
<td><p></p></td>
<td><p>세션 중 User2가 보낸 메시지 수입니다.</p></td>
</tr>
<tr class="even">
<td><p><strong>SessionEndTime</strong></p></td>
<td><p>datetime</p></td>
<td><p></p></td>
<td><p>세션 종료 시 시간입니다.</p></td>
</tr>
<tr class="odd">
<td><p><strong>MediaTypes</strong></p></td>
<td><p>int</p></td>
<td><p></p></td>
<td><p>이 세션의 미디어 유형을 나타내는 비트 집합입니다. 다음 유형의 정의가 나열됩니다.</p>
<h3 id="section-1"> </h3>
<div>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>IM</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>FILE_TRANSFER</p></td>
<td><p>2</p></td>
</tr>
<tr class="odd">
<td><p>REMOTE_ASSISTANCE</p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p>APP_SHARING</p></td>
<td><p>8</p></td>
</tr>
<tr class="odd">
<td><p>AUDIO</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>VIDEO</p></td>
<td><p>32</p></td>
</tr>
<tr class="odd">
<td><p>APP_INVITE</p></td>
<td><p>64</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><strong>User1Flag</strong></p></td>
<td><p>smallint</p></td>
<td><p></p></td>
<td><p>User1 특성을 나타내는 비트 집합입니다. 다음 특성 정의가 나열됩니다.</p>
<ul>
<li><p>0x01 - 데스크톱 전화와 통합됨</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>User2Flag</strong></p></td>
<td><p>smallint</p></td>
<td><p></p></td>
<td><p>User2 특성을 나타내는 비트 집합입니다. 다음 특성 정의가 나열됩니다.</p>
<ul>
<li><p>0x01 - 데스크톱 전화와 통합됨</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>CallFlag</strong></p></td>
<td><p>smallint</p></td>
<td><p></p></td>
<td><p>통화 특성을 나타내는 비트 집합입니다. 다음 특성 정의가 나열됩니다.</p>
<ul>
<li><p>0x01 - 재시도된 세션</p></li>
<li><p>0x02 - 응답 그룹을 대신하여 에이전트가 시작한 통화</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Processed</strong></p></td>
<td><p>bit</p></td>
<td><p></p></td>
<td><p>모니터링 서비스의 내부 사용 용도</p>
<p>이 필드는 Microsoft Lync Server 2013에 새로 도입되었습니다.</p></td>
</tr>
</tbody>
</table>


\* 대부분의 경우 SessionIdSeq는 1을 해당 값으로 사용합니다. 여러 세션이 정확히 동시에 시작될 경우 한 세션에 대한 SessionIdSeq가 1이 되고 다른 세션에 대해서는 2, 3, 4의 순서로 지정됩니다.

