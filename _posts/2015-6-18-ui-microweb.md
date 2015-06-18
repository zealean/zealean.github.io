---
layout: post
title: 微网站
tags: 海鹚UI2.0
---

###microwebsit(微网站)

####微网站首页
微网站首页一般是该医院所有基本信息的入口。包括医院介绍、专家出诊、科室介绍、医生介绍、科室分布、楼群分布、交通指引、联系我们等。

[demo_microwebIndex.html](http://uat.gzhc365.com/html/module/hosinf/html/hospInf.html)

####医院介绍


[demo_hospIntro.html](http://uat.gzhc365.com/html/module/hosinf/html/hospInf.html)


####科室介绍
科室介绍，需要先选择某一个科室，所以，一开始展现给用户的是科室列表页。

[demo_deptList.html](http://uat.gzhc365.com/html/module/hosinf/html/deptList.html)

科室列表一般情况下都是两级，但是也有一级科室的情况。
[demo_deptList2.html](http://uat.gzhc365.com/html/module/hosinf/html/deptList2.html)

科室介绍
[demo_deptInftro.html](http://uat.gzhc365.comejbs/html/module/hosinf/html/deptInftro.html)

####医生介绍
医生介绍，也是需要选择科室，然后再从该科室下的医生列表中选择医生，查看介绍。所以，这里的科室列表是长得和科室介绍的科室列表一样。但是，对应的交易是不一样的。

科室列表 [demo_deptList.html](http://uat.gzhc365.com/html/module/hosinf/html/deptList.html)
 
医生列表 [demo_docList.html](http://uat.gzhc365.com/html/module/hosinf/html/docList.html)

医生介绍 [demo_docInftro.html](http://uat.gzhc365.com/html/module/hosinf/html/docInftro.html)

####专家排班表
专家排班，固定的7天，每天有哪些专家坐班

[demo_expertsScheduling.html](http://uat.gzhc365.com/html/module/hosinf/html/expertsScheduling.html)

####科室分布
科室分布，楼栋——》楼层——》科室

科室分布有好几种形式,待完善

[demo_depFloorDistribution.html](http://uat.gzhc365.com/html/module/hosinf/html/depFloorDistribution.html)

####楼群分布
楼群分布，医院的楼群图。一般情况下都是以图片展示。此页面可以单独写成静态页面。

####来院导航
一般都是用第三方地图uri链接实现。微信服务号这边用腾讯qq地图。支付宝服务窗用高德地图。

[腾讯地图坐标拾取器](http://api.map.soso.com/doc_v2/tooles/picker.html)

**在微信端使用腾讯qq地图**

[URI API 开发文档]( http://lbs.qq.com/uri_v1/guide.html)

   
    pointx：坐标x轴
    pointy：坐标y轴
    level:当前缩放等级
    word:医院名称
    addr:地址
    如有其它特殊要求，请参照API。

    demo:http://map.qq.com/m/place/info/pointx=120.868140&pointy=32.054860&level=16&word=南通市第六人民医院&addr=江苏省南通市港闸区永和路500号?referer=tengxun&ch=wap-map1.0

    http://apis.map.qq.com/uri/v1/search?keyword=惠州中医医院&level=16&region=惠州&referer=tengxun&ch=wap-map1.0

[从微信服务号的查看地理位置进去的链接地址](http://map.qq.com/m/place/info/pointx=113.588764&pointy=24.790812&level=16&word=%E7%B2%A4%E5%8C%97%E4%BA%BA%E6%B0%91%E5%8C%BB%E9%99%A2&addr=%E4%B8%AD%E5%9B%BD%E5%B9%BF%E4%B8%9C%E7%9C%81%E9%9F%B6%E5%85%B3%E5%B8%82%E6%AD%A6%E6%B1%9F%E5%8C%BA%E6%83%A0%E6%B0%91%E5%8D%97%E8%B7%AF151%E5%8F%B7?from=wap-map1.0&referer=weixinmp_profile)


**在支付宝上使用高德地图**

[URI API 开发文档](http://lbs.amap.com/smart/lightmap/guide-2/summary/
)

    demo:
    http://m.amap.com/navi/?dest=111.312205,30.689601&destName=宜昌市中心人民医院&key=ca582245ffab9647fbe7094a29704dd3

    需要编码：
    http://m.amap.com/navi/?dest=111.312205,30.689601&destName=%E5%AE%9C%E6%98%8C%E5%B8%82%E4%B8%AD%E5%BF%83%E4%BA%BA%E6%B0%91%E5%8C%BB%E9%99%A2&key=ca582245ffab9647fbe7094a29704dd3

