# torch.arange() 函数
![pytorch doc url](https://pytorch.org/docs/stable/generated/torch.arange.html#torch-arange)
>  **torch.arange** (start=0, end, step=1, *, out=None, dtype=None, layout=torch.strided, device=None, requires_grad=False) → Tensor
## 返回值
Returns a 1-D tensor of size $\left\lceil \frac{\text{end} - \text{start}}{\text{step}} \right\rceil$ with values from the interval [start, end) taken with common difference step beginning from start.
## 参数
--start (Number) – the starting value for the set of points. Default: 0.
--end (Number) – the ending value for the set of points
-- step (Number) – the gap between each pair of adjacent points. Default: 1.
