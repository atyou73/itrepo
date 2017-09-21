+++
title = "성능테스트 도구 비교(오픈소스)"
tags = [
    "loadtest",
    "test",
    "loadrunner",
    "jmeter",
]
date = "2017-09-21"
categories = [
    "Development",
    "loadtest",
]
description = "loadtest"
+++

<head><style>

td, th {
    padding: 8px;
}
td {
    background-color: #ffffff;
    border: 1px solid #dddddd;
}
th {
    text-align: center;
    background-color: #dddddd;
    border: 1px solid #ffffff;
}
</style></head>

<table>

<tbody>

<tr>
<th>SW</th>  <th width="50%">기능</th>  <th width="39%">특징</th> <th>비고</th>
</tr>

<tr>
<td >
<a href="http://jmeter.apache.org/">JMeter</a>
</td>

<td >
*   java 기반 오픈소스.<br/>
*   GUI/non-GUI Mode 지원.<br/>
*   분산테스트 지원(<a href="http://odysseymoon.tistory.com/51">URL</a>)<br/>
*   bamboo 지원 (<a href="https://www.blazemeter.com/blog/ow-run-jmeter-continuous-integration-environment-bamboo">연동방법</a>) <br/>
*   Thread 기반으로 동시성에 제한이 있음.<br/>

</td>
<td >
*   여러 프로토콜/플러그인 지원<br/>
*   로드러너와 많이 <a href="https://comparisons.financesonline.com/apache-jmeter-vs-hp-loadrunner">비교됨</a><br/>
*   jenkins 연동됨.<br/>
*   <a href="https://www.blazemeter.com/">BlazeMeter</a>나 <a href="https://https://flood.io/">Flood.io</a>에서 활용하여 서비스 제공.
</td><td > </td>
</tr>

<tr>
<td ><a href="https://naver.github.io/ngrinder/">nGrinder</a></td>

<td >
*   <a href="http://grinder.sourceforge.net/">Grinder</a>를 naver에서 확장시킴.<br/>
*   GUI 제공 (스크립트는 groovy나 jython코딩으로)<br/>
*   Thread 기반으로 동시성에 제한이 있음.<br/>
*   분산테스트 지원(<a href="https://github.com/naver/ngrinder/wiki/Architecture">참고 </a>)<br/>
</td>

<td  >
*   계정관리 기능이 존재함. <br/>
*   <strong>계정별 테스트 스케쥴 및 이력 조회기능 제공.</strong><br/>
*   현재는 활발한 commit이 없음.<br/>
</td>
<td > </td>
</tr>


<tr>
<td ><a href="http://gatling.io/">Gatling</a></td> 

<td >
*   Akka와 Netty기반의 Scala로 개발됨.<br/>
*   GUI 없으며 시나리오 (<a href="https://en.wikipedia.org/wiki/Domain-specific_language">DSL</a>) 로 작성<br/>
*   분산테스트 미지원. 반면 높은 성능 보장.<br/>
*   분산지원하는 <a href="https://github.com/Abiy/distGatling">distGatling</a>프로젝트 존재.
</td>

<td  >
*   <strong>Event와 Async IO기반으로 높은 성능 제공.(<a href="https://blog.flood.io/stress-testing-jmeter-and-gatling/">비교</a>)</strong></br>
*   JMeter와 비견되는 요즘 신흥강자(<a href="https://octoperf.com/blog/2015/06/08/jmeter-vs-gatling/">비교</a>)</br>
*   jenkins 콜라보하여 테스트 가능 (<a href="https://summit.atlassian.com/archives/2014/massive-teams/jira-performance-testing-in-pictures?_ga=1.230245596.1327854792.1491190096">Atlassian 자료</a>)</br>
</td>

<td ><a href="https://www.youtube.com/watch?v=fqP6PTUdtkY">간단동영상</a> </td>
</tr>

<tr>
<td  >Tsung</td>
<td  >
*   Erlang으로 개발된 툴.</br>
*   HTTP뿐만 아니라 다양한 프로토콜 제공.</br>
*   GUI 제공하지 않음.</br>
</td>

<td  >
*   동시성 지향 언어인 Erlang이 가지고 있는 장점으로  
    성능과 확장성에 이점이 존재</br>
</td><td > </td>
</tr>

<tr>
<td  >Vegeta</td>

<td  >
*   Go 언어로 개발된 HTTP 부하 테스트 툴(GUI x)
</td>

<td  >
*   초당 일정한 속도로 부하 발생 지속적으로 발생시킴.
</td><td > </td>

</tr>

<tr>
<td  >Goad</td>
<td  >
*   AWS Lambda를 이용한 분산 성능 테스트
</td>

<td  >
*   AWS의 이점과 AWS Lambda를 최대 활용함
</td><td > </td>
</tr>

<tr>
<td  >Apache Bench</td>

<td  >
*   HTTP 웹 서버의 성능 측정을 위해 사용됨.
</td>

<td  >
*   간단히 테스트해 보기 좋은 툴
</td><td > </td>
</tr>
</tbody>
</table>

cf) 오픈소스 테스팅 : 성능테스트와 더불어 다양한 오픈 소스 테스트 툴에 대한 소개 사이트 <a href="http://www.opensourcetesting.org/category/performance">비교</a> 

