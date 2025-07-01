######崔江旗7.1日报
>![img.png](img.png)
通过运行脚本以及conf文件和sql文件生成ods层，然后从hdfs读取出来写到hive里面
> ![img_1.png](img_1.png)
在插入数据之前建立一个名为gmall的数据库，把所有数据存进去
> ![img_2.png](img_2.png)
建立dim层并且在建表前面加上前缀可以吧dim层存放到dim层的数据库里
>如下图所示 ![img_3.png](img_3.png)
dim层为数据的维度层 主要存储的是时间、地点以及一些用户的属性
> ![img_5.png](img_5.png)dim层
>![img_4.png](img_4.png)
建立dwd层并且建立数据表，通过一些sql查询以及需要的字段来查询一些数据
> ![img_6.png](img_6.png)dwd层
> dws层为汇总数据层 把一些主题以及维度对明细数据进行计算为ADS提供预计算的汇总数据，减少重复计算，加速报表查询
> ![img_7.png](img_7.png)dws层
> ADS层为应用数据层 根据业务做一些报表以及一些指标查询
> ![img_8.png](img_8.png)