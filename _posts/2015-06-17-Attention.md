--
layout:post
title:前端开发须注意
tags:总结与分享
---
#####开发过程中必须边做边记录！

   **要保存好新增及修改文件的路径及sql，还有可根据个人习惯记录更具体的信息。因为我们做的每个需求最终都是要投产上线的。切忌临投产了，才开始担心自己是不是有落文件。**
   
#####申请投产

  1. 申请投产时请尽可能的详细描述投产说明，比如
  
          a)有sql需要更新的的就要说明：更新完sql之后要重启参数服务
          
          b)如果修改生产上已有的文件，请在投产包中加上文件对比报告
     
     
  2. 投产环境
  
      投产环境有三个：
      微信服务号和微信服务窗是同一个用户hwcadm，所以是同一个环境
      
          
      

#####新建目录文件不能太过于随意
现在很多目录都存在很大的冗余。虽然有现成的可以借鉴，但是只是借鉴，不能看都不看就把现有的文件直接copy过来。这样造成很大冗余同事也会造成后期维护成本增加。


#####css文件、js文件、images的引入标准：

   用hh标签，这个hh在解析的时候会在文件后面加个随机参数，可以避免css、js、images文件修改之后不生效。
   
	<link href="<hh:css value='/h006/css/style.css'/>" media="all" type="text/css" rel="stylesheet">
	<script type="text/javascript" src="<hh:script value='/h001/js/validator.js'/>" charset="UTF-8"></script>
	<img src="<hh:image value="${ETF.HIS_IMG}"/>" />

js文件，为了避免乱码，js文件本身设为UTF_8编码，然后在引用的时候加上charset申明

	<script type="text/javascript" src="<hh:script value='/h001/js/validator.js'/>" charset="UTF-8"></script>
   
   
#####jsp中的每个交易请求参数中必须加HIS_CD和viewcode
HIS_CD的值从session中取

    微信中取的是${sessionScope.HIS_INF.HIS_CD}
    支付宝中取的是${sessionScope.ZFB_HIS_INF.HIS_CD}

请求参数中的`viewcode`的值**必须**与ptstpageconfig表中的viewcode相对应。


#####上线之前要对更新影响范围做评估。
已上线的医院，有新需求或有优化和修复，必须要在测试环境测试了没有问题才上线。上线之前要对更新影响范围做评估。

#####微信支付的页面，在页面后面加上  showwxpaytitle=1,会出现“微信安全支付”的标题


#####jsp中的注释规范

    jsp中的注释必须用
   
    <%--注释说明--%>


#####前端页面配置

[前端页面配置说明](https://www.evernote.com/l/AIREKFlE79pASZ_i25IqHEpZsJT-tZtkF10)

#####后台管理网站



