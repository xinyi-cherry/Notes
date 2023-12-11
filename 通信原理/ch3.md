# 第三章 随机过程

## 正态分布

高斯随机变量在任意时刻上的取值是一个正态分布的随机变量，一维概率密度函数为：
$$ f(x)=\frac{1}{\sqrt{2\pi}\sigma}\exp(-\frac{(x-a)^2}{2\sigma^2}) $$
其中 $ a $ 为均值, $ \sigma^2 $ 为方差

正态分布函数
$$ F(x)=P(\xi\leq x) $$
可用误差函数表示
$$ F(x) = \frac12+\frac{1}{2}erf(\frac{x-a}{\sqrt2\sigma}) $$
其中
$$ erf(x) = \frac{2}{\sqrt\pi}\int^x_0e^{-t^2}dt $$
互补误差函数
$$ erfc(x) = 1-erf(x) $$
$$ F(x) =  1-\frac12erfc(\frac{x-a}{\sqrt{2}\sigma}) $$
当 $ x>2 $ 时
$$ erfc(x)\approx\frac{1}{x\sqrt{\pi}}e^{-x^2} $$
Q函数
$$ Q(x) = \frac{1}{\sqrt{2\pi}}\int^\infty_xe^{-t^2/2} $$
即正态分布概率密度函数从 $ x $到无穷的积分,因此可以得到
$$ F(x)=1-Q(\frac{x-a}{\sigma}) $$ 

## 瑞利分布

当一个随机二维向量的两个分量呈独立同方差的正态分布时,向量的模呈瑞利分布.

$$ f(x;\sigma) = \frac{x}{\sigma^2}e^{-x^2/2\sigma^2},x\geq0 $$

## 莱斯分布

$$ f(x|v,\sigma)=\frac{x}{\sigma^2}\exp(\frac{-(x^2+v^2)}{2\sigma^2})I_0(\frac{xv}{\sigma^2}) $$

其中 $ I_0(z) $ 是修正的第一类零阶贝塞尔函数,当 $ v=0 $ 时莱斯分布退化为瑞利分布.

## 随机过程

一维分布函数
$$ F_1(x_1,t_1) = P[\xi(t_1)\leq x_1] $$

一维概率密度函数

$$ f_1(x_1,t_1) = \frac{\partial F_1(x_1,t_1)}{\partial x_1} $$

随机过程存在均值和方差

$$ a(t)=E[\xi(t)] = \int^\infty_{-\infty} xf_1(x,t)dx $$

$$ \sigma^2(t)=D[\xi(t)] = E\{[\xi(t)-a(t)]^2\} = \int^\infty_{-\infty}x^2f_1(x,t)dx - [a(t)]^2 $$

即均方值减去均值平方
