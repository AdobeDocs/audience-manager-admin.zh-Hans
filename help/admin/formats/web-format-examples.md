---
description: 一些常用HTTP宏组合的示例。
seo-description: 一些常用HTTP宏组合的示例。
seo-title: HTTP 格式宏示例
title: HTTP 格式宏示例
uuid: a81a2e2a-de7e-4b6a-8771-fcfa0dc74570
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 17%

---


# HTTP 格式宏示例{#http-format-macro-examples}

一些常用[!DNL HTTP]宏组合的示例。

有关宏的列表及其定义，请参见[HTTP格式宏](../formats/web-formats.md)。

<table id="table_D5FAC5D056ED49D79FA883197EF8F42E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 宏示例 </th> 
   <th colname="col2" class="entry"> Output Format（输出格式） </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;TRAITALIAS_LIST; separator=","&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|count:&lt;NUM_USERS&gt;|users:[&lt;USER_LIST:{user|&lt;user.aamUuid&gt;:&lt;user.dpUuid&gt;}; separator=", "&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>"pid_alias|count:2|users:[uuid1:dpuuid1, uuid2:dpuuid2]"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;USER_AGENT&gt;|&lt;IP&gt;|&lt;TIMESTAMP&gt;|&lt;RANDOM&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>"Firefox|255.255.255.255|1395758143|42341"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;USER_LIST:{u|&lt;u.userAgent&gt;|&lt;u.ip&gt;|&lt;u.timestamp&gt;|&lt;u.random&gt;}; separator=", "&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>"Firefox|255.255.255.255|1395758143|42341"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;DP_UUIDS.1&gt; AND &lt;DP_UUIDS.2&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>dpuuid1 AND dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>users:[&lt;USER_LIST:{user|&lt;user.dpUuids.1&gt; AND &lt;user.dpUuids.2&gt;}; separator=", "&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>users:[dpuuid1 AND dpuuid2]</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_known_string=loremlipsum&amp;segid=&lt;TRAITALIAS_LIST; separator=","&gt;&amp;test_dpuuid_1000=&lt;DP_UUIDS.1000&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_known_string=loremlipsum&amp;segid=trait_1,trait_2&amp;test_dpuuid_1000=dpuuid_1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_dpuuids=&lt;DP_UUIDS.(DPID)&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_dpuuids=dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>"&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;TRAITALIAS_LIST; separator=","&gt;|&lt;REMOVED_TRAITALIAS_LIST; separator=","&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2|trait_3,trait_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>
       {"Users":&nbsp;[&lt;USER_LIST:{user|&lt;OPEN_BRACKET&gt; 
      &nbsp;&nbsp;&nbsp;"AAM_UUID":&nbsp;"&lt;user.aamUuid&gt;", 
      &nbsp;&nbsp;&nbsp;"DataPartner_UUID":&nbsp;"&lt;user.dpUuid&gt;", 
      &nbsp;&nbsp;&nbsp;"Segments":&nbsp;[&lt;user.segments:{seg|&lt;OPEN_BRACKET&gt;"Segment":&nbsp;"&lt;seg.traitAlias&gt;"&lt;CLOSE_BRACKET&gt;};&nbsp;separator=","&gt;] 
      &nbsp;&nbsp;&nbsp;"Removed_Segments":&nbsp;[&lt;user.removedSegments:{rseg|&lt;OPEN_BRACKET&gt;"Segment":&nbsp;"&lt;rseg.traitAlias&gt;"&lt;CLOSE_BRACKET&gt;};&nbsp;separator=","&gt;] 
      &nbsp;&nbsp;&nbsp;&lt;CLOSE_BRACKET&gt;};&nbsp;separator=","&gt;]} 
     </code> </p> </td> 
   <td colname="col2"> <p> 
     <code>
       {&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;"Users":[&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"AAM_UUID":"uuid1", 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"DataPartner_UUID":"dpuuid1", 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segments":[&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segment":"alias1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}, 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segment":"alias2" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;], 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Removed_Segments":[&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segment":"alias3" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}, 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segment":"alias4" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;] 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} 
      &nbsp;&nbsp;&nbsp;] 
      } 
     </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>
       {"Users":&nbsp;[&lt;USER_LIST:{user|&lt;OPEN_BRACKET&gt; 
      &nbsp;&nbsp;&nbsp;"AAM_UUID":&nbsp;"&lt;user.aamUuid&gt;", 
      &nbsp;&nbsp;&nbsp;"DataPartner_UUID":&nbsp;"&lt;user.dpUuid&gt;", 
      &nbsp;&nbsp;&nbsp;"Segments":&nbsp;[&lt;user.segments:{seg|&lt;OPEN_BRACKET&gt;"Segment":&nbsp;"&lt;seg.traitAlias&gt;","Status":&nbsp;"&lt;seg.status&gt;"&lt;CLOSE_BRACKET&gt;};&nbsp;separator=","&gt;] 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;CLOSE_BRACKET&gt;};&nbsp;separator=","&gt;]} 
     </code> </p> </td> 
   <td colname="col2"> <p> 
     <code>
       {&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;"Users":[&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"AAM_UUID":"uuid1", 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"DataPartner_UUID":"dpuuid1", 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segments":[&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segment":"alias1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Status":"1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}, 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segment":"alias2" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Status":"0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;] 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} 
      &nbsp;&nbsp;&nbsp;] 
      } 
     </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;SEGMENTS:{seg|&lt;seg.traitAlias&gt;}; separator=\",\"&gt;|&lt;REMOVED_SEGMENTS:{seg|&lt;seg.traitAlias&gt;}; separator=\",\"&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2|trait_3,trait_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;if(user.segments &amp;&amp; user.removedSegments)&gt;&lt;COMMA&gt;&lt;endif&gt;</code> </p> </td> 
   <td colname="col2"> <p>如果字段<code>segments</code>和<code>removedSegments</code>不为空，则打印逗号。 当为区段和删除的区段连接POST时，此条件可用于列表请求。 </p> </td> 
  </tr> 
 </tbody> 
</table>
