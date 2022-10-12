# work
第二次结对编程作业
===
环境搭建
----
>本次编程使用go语言，需搭建go开发环境，可自行寻找教程进行配置 <br/>

运行代码
----
> 在git clone完该仓库之后运行call.go生成五个txt文件以及一个exe应用程序，每个文件对应相应课程的学生名单以及签到情况，可多次运行exe程序，对每个课程进行随机点名，在生成的文件上进行修改，将用于输入的文件作为输出文件输出<br>
> 生成文件：<br>
> ![img](https://img-community.csdnimg.cn/images/09bad7bb1bb14fe195065973151d3015.png "#left")
 
运行结果
----
![img](https://img-community.csdnimg.cn/images/35c341ed73c04c879537ef8043953a8d.png "#left")


算法
----
![img](https://img-community.csdnimg.cn/images/7c7e0ee55aa74a74878497b8402a95ba.png "#left")<br>
>初始时所有的学生的权重都为0，都可能被点名，为了快速筛选，第一次点45名学生，之后以一定比率下降，下降至每次八人，每一次被点到并且逃课了权重值+16，否则权重值-6，每次点名优先点权重最高的学生，需要进行排序，由于80%概率逃课，对于一个80%逃课的学生来说连续到三次的概率是非常低的，即三次点错抵消增加的权重值，可以快速筛选出来经常逃课的学生<br>
若以上无法运行，可使用https://github.com/zhizhi-0416/call该库中的文件
