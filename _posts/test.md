## STM32 No Target connected 原因及解决方案

### 产生原因

1.STlink供电不稳定
2.PA13、PA14引脚配置为输出模式了，这两个引脚不能作为SWD的信号线进行程序的下载调试
3.晶振系统不起振
4.VDDA 未供电

### 解决方案

1.STM32 ST-LINK Utility擦除整个芯片
2.BOOT0引脚拉高使用ISP下载模式
3.按reset，再点击download，再松开reset。原理就是在程序运行到SWD引脚占用之前，把新的程序烧录进去

### 参考

- https://blog.csdn.net/u011638597/article/details/82964891?utm_medium=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-1.control&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-1.control
- https://blog.csdn.net/qq_22555959/article/details/89000716?utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-1.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-1.control
- https://blog.csdn.net/qq_35661436/article/details/79629573?utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-1.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-1.control
- https://blog.csdn.net/kangweijian/article/details/107564868

