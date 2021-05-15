# 记录一下学习python中用到的一些函数方法

## axis取值：

python中axis=0时：沿着行的垂直往下，axis=1时：沿着列的方向水平延伸。

## 函数‘argmin’的用法

```python
numpy.argmin(a, axis=None, out=None)
#给出axis方向最小值的下标
#a : Input array.
#axis : 默认将输入数组展平。否则，按照axis方向
#out : 可选
#返回的是：下标组成的数组。shape与输入数组a去掉axis的维度相同
```

## 深复制与浅复制

    深复制，即将被复制对象完全再复制一遍作为独立的新个体单独存在。
    所以改变原有被复制对象不会对已经复制出来的新对象产生影响。
    而浅复制并不会产生一个独立的对象单独存在，他只是将原有的数据块打上一个新标签，
    所以当其中一个标签被改变的时候，数据块就会发生变化，
    另一个标签也会随之改变。这就和我们寻常意义上的复制有所不同了。
## pandas.head()函数

在用Pandas读取数据之后，我们往往想要观察一下数据读取是否准确，调用此函数表示只读取前五行的数据。

## pandas.tile()函数

函数格式tile(A,reps)：

A和reps都是array_like

A的类型众多，几乎所有类型都可以：array, list, tuple, dict, matrix以及基本数据类型int, string, float以及bool类型。

reps的类型也很多，可以是tuple，list, dict, array, int, bool.但不可以是float, string, matrix类型。

实例：

```python
>>> a=[[1,2,3],[5,4]]
>>> tile(a,[2,3])
array([[[1, 2, 3], [5, 4], [1, 2, 3], [5, 4], [1, 2, 3], [5, 4]],
       [[1, 2, 3], [5, 4], [1, 2, 3], [5, 4], [1, 2, 3], [5, 4]]])
```

## np.cov(a.T)函数

**<u>需要对变量转置</u>**

## np.argsort(x,axis)函数

返回的是数组值从小到大的索引值