```python
import numpy as np
```

对于所有的ndarray结构来说，里面所有的元素必须是同一类型的，如果不是的话，会自动向下进行转换


```python
tang_list=[1,2,3,4,5]
tang_array=np.array(tang_list)
tang_array
```




    array([1, 2, 3, 4, 5])



查看数组的基本属性


```python
type(tang_array)
```




    numpy.ndarray




```python
tang_array.dtype
```




    dtype('int32')




```python
tang_array.itemsize
```




    4




```python
tang_array.size
```




    5




```python
tang_array.ndim  # 查看是几维的数组
```




    1



填充的操作


```python
tang_array.fill(0)
tang_array
```




    array([0, 0, 0, 0, 0])



索引与切片:与python基础语法一样


```python
tang_list=[1,2,3,4,5]
tang_array=np.array(tang_list)
tang_array
```




    array([1, 2, 3, 4, 5])




```python
tang_array[1:3]
```




    array([2, 3])




```python
tang_array[-2:]
```




    array([4, 5])



矩阵格式（多维的形式）


```python
tang_array=np.array([[1,2,3],[4,5,6],[7,8,9]])
tang_array
```




    array([[1, 2, 3],
           [4, 5, 6],
           [7, 8, 9]])




```python
tang_array.shape
```




    (3, 3)




```python
tang_array.size
```




    9




```python
tang_array[0,0]
```




    1




```python
tang_array[1,1]
```




    5




```python
tang_array[1,1]=10
tang_array
```




    array([[ 1,  2,  3],
           [ 4, 10,  6],
           [ 7,  8,  9]])




```python
tang_array[:,1]
```




    array([ 2, 10,  8])




```python
tang_array2=tang_array
tang_array2
```




    array([[ 1,  2,  3],
           [ 4, 10,  6],
           [ 7,  8,  9]])




```python
tang_array2[1,1]=100
tang_array2
```




    array([[  1,   2,   3],
           [  4, 100,   6],
           [  7,   8,   9]])




```python
tang_array=np.arange(0,100,10)
```


```python
tang_array
```




    array([ 0, 10, 20, 30, 40, 50, 60, 70, 80, 90])




```python
mask=np.array([0,0,0,1,1,1],dtype=bool)
mask
```




    array([False, False, False,  True,  True,  True])



rand为从0-1产生10个随机数


```python
random_array=np.random.rand(10)
random_array
```




    array([0.46914988, 0.49478373, 0.3278713 , 0.09039922, 0.64795466,
           0.70250168, 0.80234121, 0.0245003 , 0.43873498, 0.79327347])




```python
mask=random_array>0.5
mask
```




    array([False, False, False, False,  True,  True,  True, False, False,
            True])




```python
tang_array=np.array([10,20,30,40,50])
tang_array>30
```




    array([False, False, False,  True,  True])



查看tang_array中大于30的位置


```python
np.where(tang_array>30)
```




    (array([3, 4], dtype=int64),)




```python
tang_array[np.where(tang_array>30)]
```




    array([40, 50])




```python
tang_array=np.array([1,2,3,4,5],dtype=np.float32)
tang_array
```




    array([1., 2., 3., 4., 5.], dtype=float32)




```python
tang_array.dtype
```




    dtype('float32')




```python
np.asarray(tang_array)
```
