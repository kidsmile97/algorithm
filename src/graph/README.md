### 图论，详细概念请翻阅相关书籍进行系统学习
+ 无向图
+ 有向图
+ 无权图
+ 有权图
### 简单图（无向无权，没有自环和平行边的图）
+ 用邻接矩阵(Adjacency Matrix)表示节点与节点间的关系
	* 适合表示稠密图(Dense Graph)
	* 邻接矩阵用boolean值来说明是否两个节点有边，不自觉的就把平行边以及有权边给去除了
+ 用邻接表(Adjacency Lists)表示节点与节点之间的关系
	* 适合表示稀疏图(Sparse Graph)，占用内存较少
	* 每一个节点都用一行来表示，行内只存储与自身相连的节点信息，就能大大节约存储空间
+ 遍历图
	* 迭代器实现
		+ 迭代器模式：就是提供一种方法对一个容器对象中的各个元素进行访问，而又不暴露该对象容器的内部细节，一般迭代器模式实现有4个部分组成
			* (1)定义一个迭代器接口
			* (2)实现迭代器接口，实现一个具体的迭代器
			* (3)定义一个容器接口，里面有一个得到迭代器接口的方法
			* (4)实现容器接口，实现一个具体的容器
			* ![迭代器模式简图](./../../source/iteratorMode.png)
		+ 容器一般指的是具有某种数据结构的对象数据集合，一般java中集合框架也称之为容器
		+ 迭代器遍历容器的最大好处就是通过访问逻辑，把容器内部数据暴露出来了，但是不暴露内部结构，避免了用户得到内部数据不小心修改了，导致容器结构出现问题的情况