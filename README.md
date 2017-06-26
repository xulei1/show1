# show1
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">

<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>河北中学</title>
<link href="{CSS_PATH}/HBschool/content.css" rel="stylesheet" type="text/css" />
<!-- 引入文件 -->
<script type="text/javascript" src="{JS_PATH}/jquery.min.js"></script>

</head>

<body>
	<div id="mybody">
    	<div id="top">
        	<div class="menu">
            	<ul>
                <li>网站首页</li><!--没有任何效果只获取后边的是11个不需要动态获取-->
                     {pc:content 
                    <!-- 获取出来 -->
                   action="category"
                   catid="0" 
                   order="listorder ASC"
                   num="11"
                   siteid="$siteid"}

                   <!-- 显示出来$v代表11条数据 -->

                    {loop $data $v}
                        <!--这里面是找一对li写出结构-->
                        <li><a href="{$v['url']}">{$v['catname']}</a></li>
                        <!--在数据库中category中找到栏目名称对应的内容-->
                            

                    {/loop}{/pc}
                	<!-- <li>网站首页</li>
                    <li><a href="list.html">学校概况</a></li>
                    <li><a href="#">规章制度</a></li>
                    <li><a href="#">德育网</a></li>
                    <li><a href="#">教研网</a></li>
                    <li><a href="#">名师风采</a></li>
                    <li><a href="#">高考专栏</a></li>
                    <li><a href="#">图书馆</a></li>
                    <li><a href="#">校友会</a></li>
                    <li><a href="#">河中论坛</a></li>
                    <li><a href="#">查询系统</a></li>
                    <li><a href="#" class="specil">东校区</a></li>     -->                
                </ul>
            </div>           
        </div>
      <div id="dh">
            	<h1><a href="index.html">河北中学首页</a> - <a href="list.html">学校概况</a> - <a href="#">校园文化</a></h1>
            	<div id="search">
            <input name="search" type="text" class="search_text" /><input name="searchbut" type="button" class="search_but" value=" " />
            </div>
          </div>
        <div id="left">
        	<div id="hot">
            	<h2></h2>
                <ul>
			<!-- 推荐热点在后台没有设置栏目等没办法动态实现 -->
                	<li><a href="#">我校举行五四表彰大会暨成人仪式</a></li> 
					<li><a href="#">河北中学4月份家长开放日公告</a> </li>
					<li><a href="#">教育处组织学生收看《2013年中小学… </a></li>
					<li><a href="#">高一年级励志踏青活动花絮 </a></li>
					<li><a href="#">我校组织高一年级励志踏青活动</a></li>
					<li><a href="#">我校举行五四表彰大会暨成人仪式</a></li> 
					<li><a href="#">河北中学4月份家长开放日公告</a></li> 
					<li><a href="#">教育处组织学生收看《2013年中小学…</a></li>
                </ul>
            </div>
          	<div id="pic">
          		<h1></h1>
	           	<div id="colee" >
					<div id="colee1">
                    <!-- 内容模块 -->
                    {pc:content 
                    action="position" 
                    <!-- 没有catid不是某一个栏目所以不写这个 -->
                    posid="2" num="2" order="listorder DESC"}
                     {loop $data $v}<p> <img src="{$v['thumb']}" width="200" height="150" />{$v['title']}</p>{/loop}
                    {/pc}
                   
					<!-- <p> <img src="{IMG_PATH}/HBschool/pic.gif" width="200" height="150" />2010-2011年度先进单位</p>
					<p> <img src="{IMG_PATH}/HBschool/pic.gif" width="200" height="150" />2010-2011年度先进单位</p>
					<p> <img src="{IMG_PATH}/HBschool/pic.gif" width="200" height="150" />2010-2011年度先进单位</p>
					<p> <img src="{IMG_PATH}/HBschool/pic.gif" width="200" height="150" />2010-2011年度先进单位</p>
					<p> <img src="{IMG_PATH}/HBschool/pic.gif" width="200" height="150" />2010-2011年度先进单位</p>
					<p> <img src="{IMG_PATH}/HBschool/pic.gif" width="200" height="150" />2010-2011年度先进单位</p> -->
				</div>
				<div id="colee2"></div>
			</div>
        </div>
    </div>
    <div id="right">
        <h1>{$title}</h1>
        <h2>作者：{$username}&nbsp;&nbsp;&nbsp;&nbsp;    图片来源：本站原创&nbsp;&nbsp;&nbsp;&nbsp;     点击数： <span id="hits"></span>&nbsp;&nbsp;&nbsp;&nbsp;     更新时间：{$updatetime}</h2>
            <!-- <p>2013年4月14日，教育处和高一年级组共同组织了高一年级及高二实验部学生“励志踏青”活动。</p>
    		<p>此次“励志踏青”活动，行程约30多华里，历时5个小时。同学们从学校大门南行，左转至燕赵大街直行经历史文化街出南城门过子龙大桥，在南桥头右转进入汊河湿地公园景区，然后向西自由活动到神农庄园停车场集合，沿107国道北行至镇远路右转，到承德街左转北行，经恒山西路返回学校。</p>
    		<p><img src="{IMG_PATH}/HBschool/newspic.jpg" width="550px" height="380px"></p>
    		<p>同学们在此次活动中展现出学校和班级的良好精神风貌。一路上，校旗班旗迎风招展，队伍整齐，每个人脸上都洋溢着青春的笑容。沿途和景区，随处都可以看到同学们捡拾垃圾的身影，互帮互助的身影。在景区，同学们尽情地拥抱大自然，呼吸着自由的空气，和好朋友合影留念。此次活动使同学们在徒步远行中砥砺了意志品质，于集体踏青时领略了湖光水色。</p>
    		<p>此次活动经教育处和高一年级组缜密筹划、精心组织，全体班主任和随队老师的通力配合，在校医校车有利的后勤保障下，获得圆满成功！！</p> -->
            {$content}
        <div class="next"><span class="font_next">上一篇：</span><a href="{$previous_page['url']}">{$previous_page['title']}</a><span class="font_next">下一篇：</span><a href="{$next_page['url']}">{$next_page['title']}</a></div>
      </div>
 
    </div>
	<div id="foot">	  
 	Copyright © 2008－2013 http://www.***.com All Rights Reserved   网站备案：冀ICP备00000000号
	</div>
</body>
<script language="JavaScript" src="{APP_PATH}api.php?op=count&id={$id}&modelid={$modelid}"></script>
</html>
Contact GitHub API Training Shop Blog About
© 2017 GitHub, Inc. Terms Privacy Security Status Help
