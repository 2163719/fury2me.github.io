# **来自刚刚入门多智能体系统故障检测算法的小白的分享！**   
# **———基于matlab R2018a**   
## **用到的函数**   
* unifrnd（）：生成连续均匀的随机数，如```R = unifrnd(-1,1,2,1)```，生成一个2行1列的矩阵R，矩阵元素在-1到1之间随机生成。   
* horzcat（）：水平拼接数组（矩阵），要求数组行数相等。如```Fib = horzcat([0;0;0;0],[1;1;1;1])```,将4行1列的矩阵水平拼接成4行2列的矩阵。   
* int8（）：可将数据转化为8位（1字节）带符号的整数。   
* ones（）：创建矩阵元素全是1的矩阵。如```ones（1,2）```，生成1行2列的矩阵，矩阵元素全是1。  
* zeros（）：创建矩阵元素全是0的矩阵。   
* plot（）：matlab绘图中最常用的函数。如```plot(t,R,t,J,'--')```,表示在figure图中绘出两条曲线，自变量都是t，因变量分别是R和J，其中R默认为实线，J默认为虚线“--”。在基本的图中可以添加横纵轴的标签：```xlabel('t'),ylabel('y')```。还可以添加图例：```legend('R','J')```，分别标明两条曲线所代表的的含义。   
综合在一起，
```plot(t,R,t,J,'--'),xlabel('t'),ylabel('y'),legend('R','J')```绘出的图如下所示：      
                   ![figure1](https://github.com/2163719/fury2me.github.io/blob/master/1.png)   
                   
## **递归算法**      
对连续时间方程进行离散化处理后，出现```x(k+1) = x(k)```类似的式子，因此就用到了递归算法，而且```x(k)```还是多维矩阵，给运算增添了难度。一开始运行一直有问题，后来在网上查了递归算法最经典也是最基础的案例——斐波那契数列，这才有了思路。代码如下，其中k是采样次数，因此```x(k)```是要封装成一个自定义的函数的，k需要自己赋值。   
```
if k == 0
    x1 = [0;0;0;0];
else
    Op = [0;0;0;0];
    Fibb = horzcat(Op,zeros(4,k));
    for i=1:1:k
        Fibb(:,i+1) = A*Fibb(:,i)+B;
    end
end
```
其中A、B代表式子中的各个系数矩阵


**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/2163719/fury2me.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

