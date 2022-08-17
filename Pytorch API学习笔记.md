# torch.arange() 函数
![pytorch doc url](https://pytorch.org/docs/stable/generated/torch.arange.html#torch-arange)
>  **torch.arange** (start=0, end, step=1, *, out=None, dtype=None, layout=torch.strided, device=None, requires_grad=False) → Tensor
## 返回值
Returns a 1-D tensor of size $\left\lceil \frac{\text{end} - \text{start}}{\text{step}} \right\rceil$ with values from the interval **[start, end)** taken with common difference step beginning from start.
## 参数
--**start (Number)** – the starting value for the set of points. Default: 0.  
--**end (Number)**– the ending value for the set of points  
-- **step (Number)** – the gap between each pair of adjacent points. Default: 1.  

## 代码举例
```python  
torch.arange(5)
torch.arange(1, 4)
torch.arange(1, 2.5, 0.5)
```
## 代码运行结果  
![image](https://user-images.githubusercontent.com/45502587/183271552-e6303c81-d622-4a4a-9f4f-6486bfa7ec28.png)

# torch.range()函数
>torch.range(start=0, end, step=1, *, out=None, dtype=None, layout=torch.strided, device=None, requires_grad=False) → Tensor
## 返回值
a 1-D tensor of size $\left\lfloor \frac{\text{end} - \text{start}}{\text{step}} \right\rfloor + 1$ with values from start to end with step step. Step is the gap between two values in the tensor.
$\text{out}_{i+1} = \text{out}_i + \text{step}$.  
注意：该函数已弃用。
## 参数
-- **start (float)** – the starting value for the set of points. Default: 0.  
-- **end (float)** – the ending value for the set of points.  
-- **step (float)** – the gap between each pair of adjacent points. Default: 1.  
## 代码举例
```python
a1 = torch.range(1, 4)
print("a1: ",a1)
print("a1's data type: ", a1.dtype)
a2 = torch.range(1, 4, 0.5)
print("a2:", a2)
print("a2's data type： ", a2.dtype)
```
## 代码运行结果  
![image](https://user-images.githubusercontent.com/45502587/183281864-0baa5a28-70ee-48d9-b7d6-f5d6265e0d0f.png)  

# torch.reshape() 函数
torch.reshape(input, shape) → Tensor  

## 返回值 
Returns a tensor with the same data and number of elements as input, but with the specified shape. When possible, the returned tensor will be a view of input. Otherwise, it will be a copy. Contiguous inputs and inputs with compatible strides can be reshaped without copying, but you should not depend on the copying vs. viewing behavior.  
返回与输入数据和元素数量一样的tensor，但形状不同。shape中的单个维数值可以为-1，其最后的维数由其他维数和元素数量计算得到，如果无法整除则会报错。  
## 参数  
## 代码举例  
```python
a = torch.arange(4.)
print(a)
b = torch.reshape(a, (2, 2))
print(b)
c = torch.tensor([[0, 1, 4], [2, 3, 6]])
print(torch.reshape(c, (3,2)))
print(torch.reshape(c, (-1,)))
print(torch.reshape(c, (-1,2)))
print(torch.reshape(c, (2,-1)))
```
## 代码运行结果
```python
tensor([0., 1., 2., 3.])
tensor([[0., 1.],
        [2., 3.]])
tensor([[0, 1],
        [4, 2],
        [3, 6]])
tensor([0, 1, 4, 2, 3, 6])
tensor([[0, 1],
        [4, 2],
        [3, 6]])
tensor([[0, 1, 4],
        [2, 3, 6]])
```
## see also
numpy.reshape() (https://www.w3resource.com/numpy/manipulation/reshape.php)
