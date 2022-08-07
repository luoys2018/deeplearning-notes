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

![image](https://user-images.githubusercontent.com/45502587/183271552-e6303c81-d622-4a4a-9f4f-6486bfa7ec28.png)

# torch.range()函数
>torch.range(start=0, end, step=1, *, out=None, dtype=None, layout=torch.strided, device=None, requires_grad=False) → Tensor
## 返回值
a 1-D tensor of size $\left\lfloor \frac{\text{end} - \text{start}}{\text{step}} \right\rfloor + 1$ with values from start to end with step step. Step is the gap between two values in the tensor.
$\text{out}_{i+1} = \text{out}_i + \text{step}$.
注意：该函数已弃用。
## 参数

## 代码举例
