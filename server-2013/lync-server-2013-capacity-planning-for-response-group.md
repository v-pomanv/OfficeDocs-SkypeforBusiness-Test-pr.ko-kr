﻿---
title: 'Lync Server 2013: 응답 그룹 용량 계획'
TOCTitle: 응답 그룹 용량 계획
ms:assetid: a2459a69-1f45-4f2f-bca5-d4f442708e44
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/Gg412754(v=OCS.15)
ms:contentKeyID: 49304581
ms.date: 08/24/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013의 응답 그룹 용량 계획

 

_**마지막으로 수정된 항목:** 2015-03-09_

다음 표에서는 용량 계획 요구 사항에 대한 기본으로 사용할 수 있는 응답 그룹 사용자 모델에 대해 설명합니다.


> [!NOTE]
> 다음 표의 숫자는 모든 응답 그룹 오디오 파일에 대해 16kHz, 모노, 16비트 Wave(.wav) 파일을 사용하고 있다는 가정을 바탕으로 합니다. Windows Media 오디오(.wma) 등과 같은 다른 파일 형식을 사용하는 경우에는 숫자가 달라질 수 있습니다.




> [!IMPORTANT]
> 재해 복구 용량 계획을 위해 한 쌍으로구성된 풀의 각 풀은 두 풀에 있는 모든 응답 그룹의 작업을 처리할 수 있어야 합니다.



### 응답 그룹 사용자 모델

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>메트릭</th>
<th>Enterprise Edition 풀별 (8개의 프런트 엔드 서버 포함)</th>
<th>Standard Edition Server별</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>초당 걸려오는 전화 수</p></td>
<td><p>16</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>IVR 또는 MoH에 연결된 동시 통화 수</p></td>
<td><p>480</p></td>
<td><p>60</p></td>
</tr>
<tr class="odd">
<td><p>동시 익명 세션 수(IM 포함 안 함)</p></td>
<td><p>224</p></td>
<td><p>28</p></td>
</tr>
<tr class="even">
<td><p>동시 익명 세션 수(IM 포함)</p></td>
<td><p>64</p></td>
<td><p>8</p></td>
</tr>
<tr class="odd">
<td><p>활성 에이전트(공식 및 비공식)</p></td>
<td><p>1200</p></td>
<td><p>1200</p></td>
</tr>
<tr class="even">
<td><p>헌트 그룹 수</p></td>
<td><p>400</p></td>
<td><p>400</p></td>
</tr>
<tr class="odd">
<td><p>IVR 그룹 수(음성 인식 사용)</p></td>
<td><p>200</p></td>
<td><p>200</p></td>
</tr>
</tbody>
</table>

