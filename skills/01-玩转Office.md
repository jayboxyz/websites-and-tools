[toc]

# Office 操作与技巧

## Word

**Word 教程：**

- [office2010word文档怎样划横线 添加画横线教程](https://jingyan.baidu.com/article/e4d08ffdb6cb040fd2f60d14.html)
- [如何在word2010里面单独设置一页的页眉](https://zhidao.baidu.com/question/560649539.html)
- [怎么让每页的页眉不同](https://jingyan.baidu.com/article/870c6fc3310685b03fe4be0c.html?qq-pf-to=pcqq.group)
- [excel超过12位数字如何下拉递增和保存?](https://www.kafan.cn/edu/81596841.html)
- 



## Excel

**Excel 教程：**

- [Excel表格如何插入日期和时间](https://jingyan.baidu.com/article/49711c616cd716fa441b7c07.html)
- 





## PowerPoint

**PowerPoint 教程：**


- [动画设置――PowerPoint 2007 多媒体课件制作攻略（六）](http://office.wps.cn/officeppt/33940-2013-04-10-18-41-23-8.html)
- 



**官方教程：**

- [使用键盘快捷方式创建 PowerPoint 演示文稿 - PowerPoint](https://support.office.com/zh-cn/article/%E4%BD%BF%E7%94%A8%E9%94%AE%E7%9B%98%E5%BF%AB%E6%8D%B7%E6%96%B9%E5%BC%8F%E5%88%9B%E5%BB%BA-powerpoint-%E6%BC%94%E7%A4%BA%E6%96%87%E7%A8%BF-ebb3d20e-dcd4-444f-a38e-bb5c5ed180f4)
- 



**PPT 键盘快捷方式：**

- [PowerPoint Online 中的键盘快捷方式](https://support.office.com/zh-cn/article/powerpoint-online-%E4%B8%AD%E7%9A%84%E9%94%AE%E7%9B%98%E5%BF%AB%E6%8D%B7%E6%96%B9%E5%BC%8F-fef9c0ea-51f9-4580-a502-ed2736241a07#bkmk_frequentlyused)
- [PPT中的快捷键](https://jingyan.baidu.com/article/ff42efa9d7a2e2c19e220299.html)
- [Microsoft Office PowerPoint 2013最新快捷键大全整理收藏](http://www.ihref.com/read-16311.html)



# 一些问题

## 【Word】Word 图标在任务栏显示异常，如何解决？ 

下面的方法我有使用过，解决了该问题：

来自：<http://www.dn92.com/zhi/v/135171/> 文章【山水阿锐】的回答。

解决方法：

1、首先鼠标右击任务栏空白处，然后取消勾选“锁定任务栏”项；
2、接着打开“开始 - 运行”，然后输入命令：
``` 
cmd /c wmic process where name="explorer.exe" delete&explorer reg delete HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\StuckRects2 /f&taskkill /f /im explorer.exe&explorer
```
然后回车；
3、任务栏移到底部后，这时候再鼠标右击任务栏再锁定任务栏即可。

## 【Word】设置 tab 键为缩进 2 字符？

本人在使用 Office2016 时，发现 tab 键缩进和设置段落“首行缩进2字符”的距离不一样，后面才发现 tab 键默认为缩进 1.75 字符。解决办法是，修改 tab 默认缩进的距离为 2 字符即可。操作如下：

![image](https://user-images.githubusercontent.com/25930007/71429844-b39cbc00-2703-11ea-8457-df5ac78af361.png)

找到“段落/制表位/制表位”修改：

![image](https://user-images.githubusercontent.com/25930007/71429849-b8617000-2703-11ea-8156-44cbc94de025.png)

## word 中如何将参考文献编号上标？

[论文格式#插入参考文献上标_运维_夏普通-CSDN博客](https://blog.csdn.net/qq_34243930/article/details/86523030)

**方法1：** 

把[1]选中以后按一下 `Ctrl+Shitf+ =`，下标的话是 `Ctrl + =`，再按一次可以恢复。

**方法2：**

1、输入相应参考文献的数字比如[1]。
2、选中"[1]",点击右键，选择字体。
3、勾选“上标”，点击确定。

[将论文中的所有参考文献编号批量上标化_kevinhg的博客-CSDN博客](https://blog.csdn.net/kevinhg/article/details/7371290)