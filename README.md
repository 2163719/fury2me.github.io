# **来自刚刚入门多智能体系统故障检测算法的小白的分享！**   
# **———基于matlab R2018a**   
## **用到的函数**   
* unifrnd（）：生成连续均匀的随机数，如R = unifrnd(-1,1,2,1)，生成一个2行1列的矩阵R，矩阵元素在-1到1之间随机生成。   
* horzcat（）：水平拼接数组（矩阵），要求数组行数相等。如Fib = horzcat([0;0;0;0],[1;1;1;1]),将4行1列的矩阵水平拼接成4行2列的矩阵。   
* int8（）：可将数据转化为8位（1字节）带符号的整数。   
* ones（）：创建矩阵元素全是1的矩阵。如ones（1,2），生成1行2列的矩阵，矩阵元素全是1。  
* zeros（）：创建矩阵元素全是0的矩阵。   
* plot（）：matlab绘图中最常用的函数。如plot(t,R,t,J,'--'),表示在figure图中绘出两条曲线，自变量都是t，因变量分别是R和J，其中R默认为实线，J默认为虚线“--”。在基本的图中可以添加横纵轴的标签：xlabel('t'),ylabel('y')。还可以添加图例：legend('R','J')，分别标明两条曲线所代表的的含义。   
综合在一起，
plot(t,R,t,J,'--'),xlabel('t'),ylabel('y'),legend('R','J')绘出的图如下所示：      
![figure1](https://github.com/2163719/fury2me.github.io/blob/master/1.png)

## **递归算法**   

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/2163719/fury2me.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
