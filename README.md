# style-transform  
## neural style  
https://github.com/jcjohnson/neural-style 
这部分代码其实就是单图片的全局优化过程，也就是每次输入一张content图片矩阵A，一张style图片矩阵B，以及一个与A同等大小矩阵C(矩阵内容可以都为0.0001)，之后将这三个矩阵输入VGG网络中，分别计算对应的loss，然后根据loss去优化矩阵C，使得C与A内容相近，C与B风格相近，如此循环，直至到达停止条件为止。其中VGG的权重是不变的，真正变化的只有C。
