---
pubDate: "2019-08-01T12:52:00Z"
title: "记一次亿储SSD固态掉盘修复（重新开卡）"
keywords:
  - 分享
description: "这篇文章讲述了作者购买的二手SSD在安装黑苹果过程中出现问题，导致固态硬盘掉盘。作者尝试了一些方法修复，包括拆开硬盘、短接JP1、使用开卡软件等，最终成功修复了固态硬盘。文章提供了所需物料和开卡工具的下载链接。"
draft: "false"
---

<p>老孙在闲鱼淘了一块二手的SSD，本来准备用来安装黑苹果使用。<br />刚开始安装挺顺利，安装的是OSX 12.13.6，分区格式APFS。<br />笔记本没有息屏就上班去了。<br />下班回来一看界面卡死。于是只有强行关机重启。<br />这下问题来了，识别不了硬盘了。<br />百度出的原因就是固态硬盘掉盘。是二三线固态厂商的通病。再次建议大家还是买大厂的产品。<br />有教程说30分钟拯救固态。试了一晚上不行。<br />看了第二种方法就是去开卡量产。<br />摸索了一晚上终于成功了！！！</p><h2>所需物料</h2><p>硬盘盒（USB转接卡） 螺丝刀（拆硬盘用） 开卡软件（文章末尾下载）<br />1 首先把硬盘拆开 拆开硬盘发现主控是慧荣sm 2246XT（其实百度也可以百度到，如果是正品的话……）<br /><img src="https://xy07-1251893119.costj.myqcloud.com/2019/08/01/868332940.jpg" alt="103_2877224_9e544a870ce08b2.jpg" title="103_2877224_9e544a870ce08b2.jpg"><br />图是网上找的，主控型号一般会印在主控芯片上，也就是那个小的。<br />2 短接JP1，PCB上一般会有标注，如果和我的硬盘一样的话就短接最上面两个（懒 没有作图 网图）<br />3 接上硬盘盒 打开开卡软件sm2246XT_MPTool_O1224H<br />4 识别到port1之后 不用短接 <br /><img src="https://xy07-1251893119.costj.myqcloud.com/2019/08/01/3281558957.png" alt="QQ浏览器截图20190801131230.png" title="QQ浏览器截图20190801131230.png"><br />5 此时应该在Parameter里面选择一个合适的flash型号，直接开卡就会成功<br /><img src="https://xy07-1251893119.costj.myqcloud.com/2019/08/01/252432522.png" alt="103_2877224_bd107f5920c8e54.png" title="103_2877224_bd107f5920c8e54.png"></p><p>参考教程链接<a href="http://www.upantool.com/jiaocheng/ssd/2017/10569.html">http://www.upantool.com/jiaocheng/ssd/2017/10569.html</a></p><pre><code>    http://bbs.mydigit.cn/read.php?tid=2367269</code></pre><p>开卡工具下载<a href="https://xy07-1251893119.costj.myqcloud.com/2019/08/01/2111427864.zip">sm2246XT_MPTool_O1224H.zip</a></p><p><img src="https://xy07-1251893119.costj.myqcloud.com/2020/12/21/3940912839.jpg" alt="bg.jpg" title="bg.jpg"></p>