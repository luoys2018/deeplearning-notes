# 张量的基本概念
 张量是一个多维数组。更正式地说，一个 N 阶张量是 N 个向量空间元素的张量积，每个向量空间都有自己的坐标系。  
 张量的阶数（the order of a tensor）也称为维数（dimensions）、模态（modes）、或方式（ways）。  
 一阶张量是一个矢量，二阶张量是一个矩阵，三阶或更高阶的张量叫做高阶张量。  
 定义 From https://blog.csdn.net/AIMZZY/article/details/106528350   
 
 # 张量的数据类型  
 见 https://pytorch.org/docs/stable/tensors.html
 # 张量创建的方式  
 ## 1.通过 torch.tensor()和torch.Tensor()创建  
 ```python
 a = torch.tensor(4)  
 print(a)              # 输出:tensor(4) 
 anp = np.asarray([4])
 a = torch.tensor(anp) 
 print(a)              # 输出：tensor([4], dtype=torch.int32)
 
 b = torch.Tensor(2)   # 定义一个指定形状的张量
 print(b)
 b = torch.Tensor(1,2)
 print(b)
 b = torch.Tensor([2]) # 定义一个指定内容的张量
 print(b)
 print( torch.numel(b))
 b = torch.Tensor([1,2]) # 定义一个指定内容的张量
 print(b)
 ```
 ![image](https://user-images.githubusercontent.com/45502587/181870453-1c7a4c48-dbef-47fc-bb72-2d195cbd7350.png)  

 ## 2.通过pytorch内置函数创建  
 torch.ones()  # 指定形状、元素值均为1的张量数组  
 torch.zeros()  # 指定形状、元素值均为0的张量数组  
 torch.ones_like()  # 生成与目标张量形状相同、元素值均为1的张量数组  
 torch.zeros_like()  # 生成与目标张量形状相同、元素值均为0的张量数组  
 torch.randn()  # 生成指定形状的随机数张量数组  
 torch.eye()   # 生成对角矩阵的张量  
 torch.full()  # 生成元素值均为1的矩阵的张量  
 
 ```python
shape = (2,3,)
rand_tensor = torch.rand(shape)
ones_tensor = torch.ones(shape)
zeros_tensor = torch.zeros(shape)

print(f"Random Tensor: \n {rand_tensor} \n")
print(f"Ones Tensor: \n {ones_tensor} \n")
print(f"Zeros Tensor: \n {zeros_tensor}")
```
![image](https://user-images.githubusercontent.com/45502587/181871238-c0174785-631a-4b1c-9817-ff7c5b6e8bc7.png)  

 
 ## 3.通过已知张量创建形状相同的张量  
 ## 4.通过已知张量创建形状不同但数据类型相同的张量  
 
 
