

![image-20200930164415135](./yarn_img/image-20200930164415135.png)



![image-20200930163812448](./yarn_img/image-20200930163812448.png)



-------

Yarn在MR中的作用：

http://www.sxtbz.com/down/9464.html

NodeManager 和DataNode是一对一的关系。下面 App Master 相当于原来的JobTracker的**调度**的模块。

JobTracker 原来**资源管理**的功能被 ResourceManager 实现了。

ResourceManager 为任务分配 Container 跑服务。

整体上多这么一个客户端就会多一套   App Master  和 Container 。 

HA 如何保障的：   App Master 在一个节点上挂掉之后，ResourceManager会在其他的节点上重启一个  App Master 。

![image-20200930183229034](./yarn_img/image-20200930183229034.png)

RM 也可以做HA， 使用 zk 协调。



Cgroup可以限制系统的资源的使用情况。

![image-20200930184350122](./yarn_img/image-20200930184350122.png)





