# CatalpaJudge

向服务器端上传代码，在服务器端运行后返回结果的一个程序。<br>
开发ing……

## 1、设计目的

在进行社团的Python教学时，发现限于条件会出现可能在学生机上无法安装足量的库或是插件的情况。所以我们希望通过这个程序可以降低教学对设备的需求。

## 2、实现

1. 学生上传Python源代码
2. 服务器接收到代码后将代码保存，使用os.popen运行程序
3. 将程序的打印部分返回给学生

## 3、具体任务

1. 服务器程序的编写
2. 提交程序的运行和结果的获取——周子皓
3. 使用一定的方法限制运行人数

对于任务3，我有两个想法：

- 使用队列，先提交的先运行先返回，后提交的排队等待，在等待时可以重新提交以更新代码，不需重新排队
- 提交一份源码就直接运行，无需等待，设置同时运行的最大数量

前者适合教师机的配置低或者是对于运行时间有要求的源码，后者适合教师配置高的且运行时间较短的源码，最好是可以进行选择，可以两个人各完成一部分。<br>
如果有人领取了该项任务，请在该项任务后面加上自己的名字。为了锻炼自己的编程能力，建议选择自己不擅长的方面。

## 4、程序结构

        CatalpaJudge/
                .git/
                .idea/
                templates/
                static/
                app.py(服务器端)
                work.py(提交程序的运行)
                queue.py(队列方式限制人数)
                nolimit.py(非队列方式限制人数)

## 5、其他

时间仓促，如有错误请指正。

 