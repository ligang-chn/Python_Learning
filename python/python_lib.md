## Python库

#### 1  SciPy

​		![1558594067592](assets/1558594067592.png)

​		SciPy中的数据结构：

		- ndarray（n维数组）
		- Series（变长字典）
		- DataFrame（数据框）



​	**NumPy**：

​	![1558594292661](assets/1558594292661.png)

​	**SciPy核心库**：

​	![1558594380381](assets/1558594380381.png)

​	例如：

```
import numpy as np
from scipy import linalg
arr=np.array([[1,2],[3,4]])
linalg.det(arr)
```



​	**Matplotlib**:

​	![1558594548038](assets/1558594548038.png)

​	**pandas**:

​	![1558594602367](assets/1558594602367.png)



------------------

#### 2  ndarray

​		![1558596700994](assets/1558596700994.png)

​		![1558597152069](assets/1558597152069.png)

​	![1558597209018](assets/1558597209018.png)

​	![1558597291782](assets/1558597291782.png)

​	![1558597463836](assets/1558597463836.png)

​	**ndarray的操作**：

- .shape用来查看维度；
- .reshape用来改变维度。
- .resize也可以改变维度；注意上面的reshape不能改变原数组的维度，但是resize可以。
- .vstack()实现垂直方向上拼接；
- .hstack()实现水平方向上拼接。



​	**ndarray的运算**：

​	![1558598111348](assets/1558598111348.png)

​	利用基本数组统计方法：

​	![1558598207614](assets/1558598207614.png)

​	![1558598238625](assets/1558598238625.png)	



​	**ndarray的ufunc函数**：

​	![1558598326980](assets/1558598326980.png)

​	

------------------------------

#### 3  变长字典Series

​		有序、定长的字典。

​		**基本特征**：

  - 类似一维数组的对象

  - 由数据和索引组成

    ​	![1558599024633](assets/1558599024633.png)

    第一列是索引，索引可以自定义：

    ​	![1558599090532](assets/1558599090532.png)

    可以查看索引和数据：

    ​	![1558599125515](assets/1558599125515.png)



​		**Series的数据对齐**：

​		![1558599241112](assets/1558599241112.png)

​		没有找到的数据，显示NaN表示Not a Number。

​		**重要功能1**：在算术运算中自动对齐不同索引的数据；

​		![1558599551347](assets/1558599551347.png)

​		**重要功能2**：Series对象本身及其索引均有一个name属性；

​							Series的name属性与其他重要功能关系密切。

​		![1558599709018](assets/1558599709018.png)



------

#### 4  DataFrame

​		**基本特征**：

		- 一个表格型的数据结构
		- 含有一组有序的列（类似于index）
		- 大致可看成共享同一个index的Series集合



​		例如：

​		![1558599905615](assets/1558599905615.png)

​		DataFrame的索引和值：

​		![1558599953487](assets/1558599953487.png)



​		**DataFrame的基本操作**：

​		**1）取DataFrame对象的列和行可获得Series**

​		![1558600128490](assets/1558600128490.png)

​		**2）DataFrame对象的修改和删除**

​		![1558600218275](assets/1558600218275.png)



​		**DataFrame的统计功能**：

​		![1558600325389](assets/1558600325389.png)

​		注意：这里输出的是字符串。



------------

#### 5  NLTK语料库

```python
import nltk
nltk.download()
```

​		弹出下载界面：

​		![1558658512896](assets/1558658512896.png)

```python
from nltk.corpus import gutenberg
import nltk
print(gutenberg.fileids())
texts=gutenberg.words('austen-emma.txt')
print(texts)
```



```python
#对数据进行添加列字段名，索引序号更改
import pandas as pd
qutoesdf=pd.read_csv(r'C:\Users\ligang\Desktop\2.csv')
#print(qutoesdf)
qutoesdf1=qutoesdf.iloc[:50,:2]
#print(qutoesdf1)
cols=['longitude','latitude']
qutoesdf1.columns=cols
#print(qutoesdf1)
qutoesdf1.index=range(1,len(qutoesdf1)+1)
print(qutoesdf1)
```















