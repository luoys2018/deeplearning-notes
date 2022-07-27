# 确认Cuda安装是否成功  
cuda版本对应表  
https://docs.nvidia.com/cuda/cuda-toolkit-release-notes/index.html#cuda-major-component-versions  

在文件目录'C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.3\extras\demo_suite'中  
运行 **deviceQuery.exe**
![image](https://user-images.githubusercontent.com/45502587/180989339-842bf872-d69c-444f-9c42-bbd86fc0fa6b.png)  

运行随机雾化程序 **Randomfog.exe** 
![image](https://user-images.githubusercontent.com/45502587/180989934-fd41d7e1-edbc-4d3a-b6ce-592f72b466cc.png)  
傅里叶变换模拟程序  
![image](https://user-images.githubusercontent.com/45502587/180990329-a63659a0-1161-472d-ab0b-09a08108a1a3.png)  

# 安装pytorch问题
conda安装环境报错：Solving environment: failed with initial frozen solve.  
一直停在solving environment。  
试了换清华、中科大等国内镜像安装源也不行，后来在“D:\anaconda3\pkgs\”删除安装包，反复安装几次后成功。  

后来搜到到网上这个帖子，还是分析得不错，没有测试。  
[一招解决Conda安装卡在solving environment这一步！](https://blog.csdn.net/qazplm12_3/article/details/108924561?spm=1001.2101.3001.6661.1&utm_medium=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-1-108924561-blog-100582862.pc_relevant_multi_platform_whitelistv2_ad_hc&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-1-108924561-blog-100582862.pc_relevant_multi_platform_whitelistv2_ad_hc&utm_relevant_index=1)  
