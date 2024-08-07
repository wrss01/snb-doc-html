# SageMath数学软件
SageMath 是一个免费的、开源的数学软件系统，采用GPL协议。它整合了许多开源Python包，采用Python语言编写，但也支持其他语言。它的目标是创造一个可变的开源软件以替代Matlab、Magma、Maple 和 Mathematica。

为使大家方便的了解、学习并使用SageMath，我们的SmartNoteBook通过引入SageMath引擎并细致地对兼容性做了优化和完善，充分利用NoteBook的特性，不仅减少大量复杂的安装和配置，而且做到可以让用户即开即用。

# SageMath数学引擎的安装配置
SmartNotebook默认的部署镜像内没有内置SageMath语言计算引擎，需要Node环境中进行安装SageMath和SageMath的kernel包。



# 创建SageMath的notebook及示例代码


在`新建NoteBook`对话框中"选择计算引擎(Kernel)类型"为"Sagemath"的选项。

输入`NoteBook标题`并选择对应的环境，最后点击提交。

![图 0](../images/b0d3df55f45e4e16cb710adc72a87b55d9930ed875d02925fdcb4c96db515d49.png)  


> [!warning|style:flat]
> 成功创建NoteBook后，用户无法在不同的kernel语言类型之间切换。


接下来我们进入NoteBook后直接创建Code单元格，便可以编写并执行Sage代码了。



比如：当我们对整数`20221208` 进行素数因子分解 ，新建一个Code单元格 ，输入以下代码并点击执行：

```
factor(20221208)
```

执行结果：

![picture 2](../images/factor%E5%87%BD%E6%95%B0.png)  


# 算术(SageMath as a Calculator)

这里我们介绍介绍一下如何像图形计算器一样使用 SageMath 的一些算术和函数命令。

## 基本算术

基础的算术运算符为加 + 、减 -、乘 * 、除 / 、指数 ^
数字前面的符号-表示它是负数。

```
print('1+1=',1+1)
print('103-101=',103-101)
print('7*9=',7*9)
print('7337/11=',7337/11)
print('11/4=',11/4)
print('2^5=',2^5)
print('-11+9=',-11+9)
-6
```

SageMath 遵守标准的操作顺序， 即PEMDAS (parenthesis, exponents, multiplication, division, addition, subtraction): 括号、指数、乘法、除法、加法、 减法。

```
print(2*4^2+1)
print((2*4)^2+1)
print(2*4^(2+1))
print(-3^2)
print((-3)^2)
```


当两个整数相除时，有一个微妙之处：SageMath将返回分数或其十进制近似值。与大多数图形计算器不同，SageMath将尝试尽可能精确，除非另有说明，否则将返回分数。

```
print(11/4)
print(11/4.0)
print(11/4.)
print(11.0/4)
print(11/4*1.)
```

## 整数除法和因式分解

有时当我们使用除法时，除法运算符不会给我们所有想要的信息。比如，我们不仅想知道约化分数是多少，甚至想知道它的十进制近似值，或者想知道唯一商和余数是多少。我们可以使用运算符// 来计算商，使用运算符 % 用于余数。使用 divmod(）函数来同时计算获得商和余数。

```
print( 14 // 4)
print( 14 % 4)
print( divmod(14,4))
```

我们知道当两个整数是否能整除，可以采用A/B余数是0，说明可以整除，但SageMath 整数有一个内置的方法可以专门用来检查一个整数是否整除另一个整数。

```
print(3.divides(15))
print(5.divides(17))
```

与divides方法相关的还有一个方法divisors()，此方法可以返回指定整数的所有正除数的列表。

```
print(12.divisors())
101.divisors()
```

我们知道当整数的除数只是1和它本身时，这个数字是素数。为了检查一个数字在SageMath中是否是素数，我们可使用方法is_prime()

```
print(153.is_prime())
(2^19-1).is_prime()
```

factor()可计算整数的素因数分解

```
print(62.factor())
63.factor()
```

有兴趣简单地知道哪些素数除以整数，我们可以使用prime_divisors() 或 prime_factors()方法。

```
print(24.prime_divisors())
print(24.prime_factors())
print(63.prime_factors())
print(63.prime_divisors())
```

求最大公约数和最小公倍数。

最大公约数（GCD）是所有这些公约数中最大的一个。

最小公倍数（LCM）是两个整数相除的最小整数。

```
print( gcd(14,63))
print( gcd(15,19))
print(lcm(4,5))
lcm(14,21)
```

## 标准函数和常量

SageMath几乎包含了人们在学习数学时遇到的所有标准函数。接下来我们将介绍一些最常用的函数：maximum、minimum、 floor、ceiling、trigonometric、exponential、logarithm 函数。我们还将看到许多标准的数学常数，如欧拉常数(e）、π 和黄金比例（ ϕ ）。

```
# max 最大值
print(max(1,5,8))
# min 最小值
print(min(1/2,1/3))
# abs 绝对值
print(abs(-10))
# floor 向下取整 
print(floor(2.1))
# ceil 向上取整
print(ceil(2.1))
```

当使用floor、ceil 时要特别小心，注意计算精度问题

```
 print(floor(1/(2.1-2)))
 print(1/(2.1-2))
```


sqrt()该命令/函数计算实数的平方根。正如我们之前在分数中看到的那样，如果我们想要十进制近似值，我们可以通过给出一个十进制数作为输入来获得它。

```
print(sqrt(3))
print( sqrt(3.0))
```

为了计算其他根，我们使用有理指数。SageMath可以计算任何有理数指数幂(SageMath can compute any rational power)。如果指数或基数是小数，则输出将是小数。

```
print( 3^(1/2) )
print( (3.0)^(1/2) )
print( 8^(1/2) )
print( 8^(1/3) )
```

SageMath 还支持所有标准三角函数，例如：正弦sin()和余弦 cos()

```
print( sin(1) )
print( sin(1.0) )
print( cos(3/2) )
print( cos(3/2.0) )
```

在SageMath内，我们完全处理的是π，而不是一些数字近似。但是，我们可以使用以下方法调用数值近似：pi.n()

```
print(pi.n())
print(sin(pi))
print(sin(pi.n()))
```


我们看到，当使用符号时，SageMath 返回确切的结果。但是，当我们使用近似值时，我们会得到一个近似值。是 的10^{-16}简写，数字应为零，但近似值引入了错误。以下是使用符号、精确 π 与数值近似的几个示例:

```
print( sin(pi/6))
print( sin(pi.n()/6))
print( sin(pi/4))
print(sin(pi.n()/4))
```

继续我们的主题，有一些鲜为人知的特殊角度，可以巧妙地简化正弦或余弦的值。

```
print( sin(pi/10)) 
print( cos(pi/5) )
print( sin(5*pi/12) )
```

其他三角函数、反三角函数和双曲函数也可用

```
print( arctan(1.0) )
print( sinh(9.0))
```

SageMath内与 π 类似，它有一个内置的数字符号常数e，即自然对数的底数。

```
print(e)
print(e.n())
```

我们使用命令:ln(x)、log(x)、log(x,b)，幂基e可以使用函数和通过将符号常数提高到指定幂来完成。

```
print(  ln(e) )
print(  log(e) )
print(  log(e^2) )
print(  log(10) )
print(  log(10.0) )
print(  log(100,10) )
print(  exp(2) )
print(  exp(2.0) )
print(  exp(log(pi)) )
print(  e^(log(2)) )
```

# SageMath的高级运算

## 关于符号计算和数值计算

我们需要先了解符号计算和数值计算的区别。

符号计算（也称为符号化计算）是一种使用符号和数学公式来解决问题的方法。它利用符号和公式来表示数学概念，而不是使用数字。符号计算通常用于解决复杂的数学问题，因为它可以更好地表示数学概念，更容易理解。

例如，使用符号计算解决微积分问题时，可以使用符号表示微积分的概念，而不是使用数字。符号计算可以帮助我们更好地理解数学概念，并使用数学公式来解决问题。

符号计算可以使用专门的符号计算软件或编程语言，例如 Mathematica、Maple 和 SymPy等。这些软件可以帮助用户表示数学概念，并使用符号计算来解决问题。

数值计算是使用数字来解决问题的方法。它通常用于解决某些无法使用符号计算直接解决的问题。数值计算通常使用的科学计算软件有 Matlab、Octave 或 Python 的 NumPy 库。这些软件提供了大量的数值计算工具和函数，可以帮助用户解决各种数学问题。

总结：符号计算使用符号和数学公式来表示数学概念，而数值计算使用数字来解决问题。另外，符号计算通常用于解决复杂的数学问题，而数值计算则常用于解决无法使用符号计算直接解决的数学问题。

## 求解方程和不等式

在SageMath里，方程和不等式使用运算符 ==、>=、<=等符号来定义，且可返回True 或False ，如果方程或不等式中有变量，将只返回方程或不等式。

```
print(9==9)
print(9<=10)
3*x - 10 == 5
```

为了求解方程或不等式，我们可以使用命令solve()。

我们先来解决只有x一个变量的情况。我们知道方程可能有多个解的情况。当有多个解时，SageMath 会以列表的形式返回找到的所有解。

```
var('x')
print( solve(3*x - 2 == 5,x))
print( solve( 2*x -5 == 1, x))
print( solve( 2*x - 5 >= 17,x))
print( solve( 3*x -2 > 5, x))
solve(2*x^2 - x + 1 == 0, x)
```

```
print( solve( x^2 + x  == 6, x))
solve( exp(x) == -1, x)
```

solve()尝试不使用浮点数来表示方程的解，它将以符号的形式返回：

```
print(solve( sin(x) == x, x))
print(solve( exp(x) - x == 0 , x))
print( solve( cos(x) - sin(x) == 0 , x))
sage: solve( cos(x) - exp(x) == 0 , x)
```

如果想得到解的数字近似值，我们可以使用命令find_root()。

```
print(find_root(sin(x) == x, -pi/2 , pi/2))
find_root(sin(x) == cos(x), pi, 3*pi/2)
```

## 声明多个变量

前面的内容，我们求解了方程中仅有一个变量的情况，并且我们总是使用x作为变量名，此时SageMath 会创建一个符号变量 x用于求解方程。如果要求解多元方程，我们就需要使用其他的符号变量，此时我们必须要先使用var()命令声明它。符号变量的名称可以是字母，也可以是字母和数字的组合。

注意：变量名称不能包含空格，例如“square root”不是有效的变量名称，而“square_root”可以。另外，如果在声明符号变量之前使用它将导致 NameError。

```
sage: y,z,t = var("y z t")
sage: phi, theta, rho = var("phi theta rho")
sage: x1, x2 = var("x1 x2")
```

取消声明一个符号变量使用命令restore()，就像上面定义变量一样。

```
sage: restore('phi')
```

## 求解具有多个变量的方程

我们也可以用命令solve()求解线性方程组，前提是方程组中所有符号变量都已声明。另外，方程组必须以列表形式输入，最后跟符号变量。结果也是以列表的形式输出。当然，方程组可能是唯一解，也可能有无限多个解，或者压根没有解：

```
print(solve( [3*x - y == 2, -2*x -y == 1 ], x,y))
print(solve( [  2*x + y == -1 , -4*x - 2*y == 2],x,y) )
sage: solve( [  2*x - y == -1 , 2*x - y == 2],x,y)
```

```
sage: solve([ 2*x + 3*y + 5*z == 1, 4*x + 6*y + 10*z == 2, 6*x + 9*y + 15*z == 3], x,y,z)
```

solve()对于大型方程组来说可能非常慢。对于这种情况，最好的办法是使用线性代数函数求解多个变量不等式，但这可能会导致表达式求解变的非常复杂，因为它们定义的区域很复杂。

在下面的示例中，SageMath 求出的解是一个列表，其中包含线的交点，接下来是两条射线，最后是两条射线之间的区域：

```
print(solve([ x-y >=2, x+y <=3], x,y))
solve([ 2*x-y< 4, x+y>5, x-y<6], x,y)
```

## 微积分(Calculus)

SageMath有许多命令可用于研究微分和积分，接下来我们一起熟悉一些这方面的函数使用。

```
var('g h')
f(x) = x*exp(x)
print(f)
g(x) = (x^2)*cos(2*x)
print( g)
h(x) = (x^2 + x - 2)/(x-4)
print(h)
```

SageMath 用x |–>来告诉你，返回的表达式实际上是一个函数，而不仅仅是一个数字或字符串。这意味着我们可以像您期望任何函数一样计算这些表达式。

```
print( f(1) )
print( g(2*pi) )
print( h(-1))
```

定义以上这些函数后，我们将研究如何使用 SageMath 来计算这些函数的极限。

## 极限(Limits)
$$x \rightarrow 1$$ 的极限 $$f(x) = xe^{x}$$是在SageMath中通过在SageMath中输入以下命令来计算的：

```
limit(f, x=1)
```

我们可以对g(x)评估在x=2处的极限，$$g(x) = x^{2} \cos(2x)$$    $$x \rightarrow 2$$:


```
limit(g, x=2)
```

h(x)在x=4 处有一个不连续性，我们查看x趋近于4时h(x)的极限：

```
limit(h, x = 4)
```

下面这个h(x)的图表说明为什么我们在使用计算机代数系统时必须要小心一点。

![图 4](../images/hx%E7%9A%84%E5%9B%BE%E5%BD%A2.png)  


我们得到的x=4是一个垂直渐近线，其函数趋向于正无穷大。当x大于4时，当x趋近于4时，h(x)趋近于正无穷大；反之当x从负轴方向趋近于4时，h(x)趋近于负无穷大。我们可以使用 SageMath 提供的dir参数来确认方向。

```
print( limit(h, x=4, dir="right") )
sage: limit(h, x=4, dir="left")
```

## 导数(Derivatives)

接下来我们要做的是使用 SageMath 来计算我们之前定义的函数的导数。例如，要计算 $$f^{\prime}(x)$$、 $$g^{\prime}(x)$$、$$h^{\prime}(x)$$ 我们将使用该命令。

```
fp  =  derivative(f,x)
print(fp)
gp =  derivative(g, x)
print(gp)
hp  = derivative(h,x)
print( hp)
```

第一个参数是您要微分的函数，第二个参数是您想要微分的变量，例如：

```
y = var('y')
print( derivative(f,y))
print( derivative(g,y))
derivative(h,y)
```

计算导数函数后，我们可以使用solve()命令找到临界点：

```
print(fp(10))
print(gp(pi/2))
print(hp(10))
solve( fp(x) == 0, x)
```

在点$$\left(x, f\left(x\right)\right)$$处构造与我们的函数相切的线是一项重要的计算，在 SageMath 中很容易完成。例如，以下命令将计算与点$$\left(0,f(0)\right)$$相$$f(x)$$切的直线。

```
T_f = fp(0)*( x - 0 ) + f(0)
T_f
```

## 积分(Integrals)

SageMath具有计算许多常见函数的定积分和不定积分的功能。我们将从计算我们之前定义的每个函数的不定积分（也称为反导数）开始。这将通过使用具有类似于integral() 的参数的命令来完成。

```
integral(f,x)
```

## 定积分

```
integral(f, x,0,1)
```

在上述每种情况下，SageMath 都会返回一个函数作为其结果。这些函数中的每一个都是一个常量函数，这就是我们所期望的。如前所述，SageMath 将返回保留最高精度的表达式，除非被告知，否则不会使用小数。告诉 SageMath 需要近似的一种快速方法是用数值近似命令n()来包装命令。

```
print( n(integral(f, x,0,1)))
print(n(integral(g, x,0,1)))
n(integral(h, x,0,1))
```

## 泰勒级数扩展(Taylor Series Expansion)

SageMath的另一个有趣的功能是可以计算围绕一个点的泰勒级数展开。首先，我们展示如何在 0 周围展开，也称为麦克劳林级数。让我们举一个函数的例子 $$g(x) = \cos(x)$$。

```
g = cos(x); 
print(g)
g_taylor = g.taylor(x,0,3)
g_taylor
```

```
f = exp(x^3)*sin(x-5);
print( f)
f_taylor = f.taylor(x,2,3);
print(f_taylor)
```

现在，这种计算的结果可能有点难以可视化，因此，SageMath的另一个有趣功能是可以以Latex格式打印结果，这对眼睛来说要好得多。

```
print(f_taylor._latex_())
```

打印输出：

```
\frac{1}{6} \, {\left(x - 2\right)}^{3} {\left(467 \, \cos\left(3\right) - 2130 \, \sin\left(3\right)\right)} e^{8} + \frac{1}{2} \, {\left(x - 2\right)}^{2} {\left(24 \, \cos\left(3\right) - 155 \, \sin\left(3\right)\right)} e^{8} + {\left(x - 2\right)} {\left(\cos\left(3\right) - 12 \, \sin\left(3\right)\right)} e^{8} - e^{8} \sin\left(3\right)
```

我们可以把上面的Latex格式放到SNB的MarkDown代码块来执行会看到：
$$\frac{1}{6} \, {\left(x - 2\right)}^{3} {\left(467 \, \cos\left(3\right) - 2130 \, \sin\left(3\right)\right)} e^{8} + \frac{1}{2} \, {\left(x - 2\right)}^{2} {\left(24 \, \cos\left(3\right) - 155 \, \sin\left(3\right)\right)} e^{8} + {\left(x - 2\right)} {\left(\cos\left(3\right) - 12 \, \sin\left(3\right)\right)} e^{8} - e^{8} \sin\left(3\right)$$


## 统计学(Statistics)

SageMath提供的基本描述性统计函数的使用。为了演示它们的用法，我们将首先生成一个从 0 到 100 的整数伪随机列表。我们来计算平均值、中位数、众数、方差和标准差。

```
data = [  int(random()*(100-0) + 0)  for i in [ 1 .. 20 ] ]
print(mean(data))
print(median(data))
print(mode(data))
print(variance(data))
print(std(data))
print(moving_average(data,4))
print(moving_average(data,10))
print(moving_average(data,20))
```


# SageMath的可视化

SageMath是一个强大的开源数学软件，具有非常广泛的数学可视化功能。它可以生成2-D以及3-D图形，甚至可以制作动画图。

而且除SageMath本身包含了大量的可视化工具外，同时SageMath与Python的紧密结合，也使得它可以运用Python中与可视化和图形有关的一系列库。这些广泛的数学工具和功能可以帮助您通过图形和动画的形式来理解数学概念和模型。

具体来说，SageMath提供了以下可视化功能：

* 图形绘制：SageMath可以绘制多种数学函数，如曲线、曲面、等高线等。

* 动画制作：SageMath可以制作动画，通过动画来展示数学模型的变化过程。

* 交互式可视化：SageMath可以创建交互式可视化，允许用户通过拖拽、缩放等操作来探索数学模型。

* 图像处理：SageMath可以处理图像，包括对图像进行缩放、旋转、剪裁等操作。

* 图形和动画的导出：SageMath可以将图形和动画导出为多种格式，如PNG、SVG、GIF等，方便您在其他软件或文档中使用。

总的来说，SageMath的可视化功能非常强大，能够帮助您更直观地理解数学概念和模型。

## 函数可视化的理论

- **一元函数**是一种特殊的函数，其中函数的输入和输出都是单个变量。一元函数的形式通常是 y=f(x)，其中 x 是输入变量，y 是输出变量。例如，函数 y=x^2+1 就是一个一元函数，其中 x 是输入变量，y 是输出变量。

- **隐函数**是由隐式方程所隐含定义的函数。设F（x,y）是某个定义域上的函数。如果存在定义域上的子集D，使得对每个x属于D，存在相应的y满足F(x,y)=0，则称方程确定了一个隐函数。记为y=y(x)。 显函数是用y=f(x)来表示的函数，显函数是相对于隐函数来说的。

- **参数方程**是一种特殊的方程，其中函数的一个变量是参数。例如，x=t^2+1 和 y=t+2 可以联立起来得到参数方程：
  x=t^2+1
  y=t+2
  在这个参数方程中，t 是参数。我们可以用不同的值来替换 t，然后求出对应的 x 和 y 值。参数方程常用于描述曲线或曲面，因为它可以用一组方程来描述多维几何图形。

对应以几类函数的定义，我们需要先了解SageMath中三个绘图函数plot()、implicit_plot()以及parametric_plot()

plot函数是SageMath中的一个常用函数，用于绘制一元函数的图像。这意味着，如果你想绘制一个函数y=f(x)的图像，你可以使用plot函数。例如：

```
sage: var('x')
x
sage: f(x) = x^2
sage: plot(f, (x,-2,2))
```

这将在平面直角坐标系中绘制出函数y=x^2的图像。

相比之下，implicit_plot函数用于绘制二元函数的图像。这意味着，如果你想绘制一个函数f(x,y)=0的图像，你可以使用implicit_plot函数。例如：

```
sage: var('x,y')
(x, y)
sage: f(x,y) = x^2 + y^2 - 1
sage: implicit_plot(f, (x,-2,2), (y,-2,2))
```

这将在平面直角坐标系中绘制出函数f(x,y)=0的图像。

最后，parametric_plot函数用于绘制参数方程的图像。这意味着，如果你想绘制由两个一元函数x=f(t)和y=g(t)定义的曲线，你可以使用parametric_plot函数。例如

```
sage: var('t')
t
sage: f(t) = cos(t)
sage: g(t) = sin(t)
sage: parametric_plot((f, g), (t,0,2*pi))
```

这将在平面直角坐标系中绘制出由x=cos(t)和y=sin(t)定义的圆。

## 2D图形

SageMath提供了广泛的二维绘图功能，它的底层渲染是使用matplotlib库完成的。

它可以支持以下图形图元函数：

- `arrow()` - an arrow from a min point to a max point.

- `circle()` - a circle with given radius

- `ellipse()` - an ellipse with given radii and angle

- `arc() `- an arc of a circle or an ellipse
  
- `disk()` - a filled disk (i.e. a sector or wedge of a circle)
  
- `line()` - a line determined by a sequence of points (this need not be straight!)

- `point()` - a point

- `text()` - some text

- `polygon()` - a filled polygon
  
支持以下绘图打印功能：
  
- `plot()` - plot of a function or other Sage object (e.g., elliptic curve).
  
- `parametric_plot()`
  
- `implicit_plot()`
  
- `polar_plot()`
  
- `region_plot()`
  
- `list_plot()`
  
- `scatter_plot()`
  
- `bar_chart()`
  
- `contour_plot()`
  
- `density_plot()`
  
- `plot_vector_field()`
  
- `plot_slope_field()`
  
- `matrix_plot()`
  
- `complex_plot()`
  
- `graphics_array()`
  
- `multi_graphics()`
  
支持以下日志打印功能：
  
- `plot_loglog()`
  
- `plot_semilogx()` and `plot_semilogy()`
  
- `list_plot_loglog()`
  
- `list_plot_semilogx()` and `list_plot_semilogy()`
  
包括以下各种图形功能：
  
- `Graphics()`
  
- `is_Graphics()`
  
- `hue()`


> [!Tip]
> 在每个函数名后面输入`?`，可以获得该函数的帮助和示例。

## 3D图形

Sage广泛支持3D图形，从基本形状到隐式和参数化绘图。支持以下图形功能：

- `plot3d()` - plot a 3d function

- `parametric_plot3d()` - a parametric three-dimensional space curve or surface

- `revolution_plot3d()` - a plot of a revolved curve

- `plot_vector_field3d()` - a plot of a 3d vector field

- `implicit_plot3d()` - a plot of an isosurface of a function

- `list_plot3d()`- a 3-dimensional plot of a surface defined by a list of points in 3-dimensional space

- `list_plot3d_matrix()` - a 3-dimensional plot of a surface defined by a matrix defining points in 3-dimensional space

- `list_plot3d_array_of_arrays()`- A 3-dimensional plot of a surface defined by a list of lists defining points in 3-dimensional space

- `list_plot3d_tuples()` - a 3-dimensional plot of a surface defined by a list of points in 3-dimensional space

支持以下基本形状：

- `Box` - a box given its three magnitudes

- `Cone` - a cone, with base in the xy-plane pointing up the z-axis

- `Cylinder` - a cylinder, with base in the xy-plane pointing up the z-axis

- `Line` - a 3d line joining a sequence of points

- `Sphere` - a sphere centered at the origin

- `Text` - a text label attached to a point in 3d space

- `Torus` - a 3d torus

- `Point` - a position in 3d, represented by a sphere of fixed size

支持以下基本形状的绘图功能：

- `ColorCube()` - a cube with given size and sides with given colors

- `LineSegment()` - a line segment, which is drawn as a cylinder from start to end with given radius

- `line3d()` - a 3d line joining a sequence of points

- `arrow3d()` - a 3d arrow

- `point3d()` - a point or list of points in 3d space

- `bezier3d()` - a 3d bezier path

- `frame3d()`- a frame in 3d

- `frame_labels()` - labels for a given frame in 3d

- `polygon3d()` - draw a polygon in 3d

- `polygons3d()` - draw the union of several polygons in 3d

- `ruler()` - draw a ruler in 3d, with major and minor ticks

- `ruler_frame()` - draw a frame made of 3d rulers, with major and minor ticks

- `sphere()` - plot of a sphere given center and radius

- `text3d()` - 3d text

Sage还支持以下：

- `tetrahedron()`

- `cube()`

- `octahedron()`

- `dodecahedron()`

- `icosahedron()`

支持不同的查看器: 基于web的交互式查看器，默认使用Three.js JavaScript library, Jmol以及Tachyon ray tracer. 通过添加关键字参数来调用查看器，如viewer='threejs' ('jmol'或者 'tachyon') 并使用命令show（）显示任何三维图形。

- `Tachyon` - create a scene the can be rendered using the Tachyon ray tracer

- `Axis_aligned_box` - box with axis-aligned edges with the given min and max coordinates

- `Cylinder` - an infinite cylinder

- `FCylinder` - a finite cylinder

- `FractalLandscape`- axis-aligned fractal landscape

- `Light` - represents lighting objects

- `ParametricPlot` - parametric plot routines

- `Plane`- an infinite plane

- `Ring` - an annulus of zero thickness

- `Sphere`- a sphere

- `TachyonSmoothTriangle` - a triangle along with a normal vector, which is used for smoothing

- `TachyonTriangle` - basic triangle class

- `TachyonTriangleFactory` - class to produce triangles of various rendering types

- `Texfunc` - creates a texture function

- `Texture` - stores texture information

- `tostr()` - converts vector information to a space-separated string

## 动画

我们知道动画是由一系列图形对象（或其他可迭代的对象）渲染生成的。通过对每个输入对象调用save_image方法，创建一系列PNG文件来生成图像。然后使用不同的工具将它们组合成各种目标格式。其中，ImageMagick的转换程序可用于生成动画GIF文件。FFmpeg（带有命令行程序FFmpeg）提供了对各种视频格式的支持，但也是生成动画GIF的另一种方法。对于支持APNG的浏览器，APNG可以用作另一种替代方案，并且无需任何额外的依赖。

例如：

使用ImageMagick生成动画

```
x = SR.var("x")
sines = [plot(c*sin(x), (-2*pi,2*pi), color=Color(c,0,0), ymin=-1, ymax=1) for c in sxrange(0,1,.2)]
a = animate(sines)
a         # optional -- ImageMagick
# Animation with 5 frames
a.show()  # optional -- ImageMagick
```

使用FFmpeg:
```
f = tmp_filename(ext='.gif')
a.save(filename=f, use_ffmpeg=True) # optional -- ffmpeg
```

生成APNG:
```
a.apng()  # long time
```

3D动画:
Animations of 3d objects:

```
s,t = SR.var("s,t")
def sphere_and_plane(x):
    return sphere((0,0,0),1,color='red',opacity=.5)+parametric_plot3d([t,x,s],(s,-1,1),(t,-1,1),color='green',opacity=.7)
sp = animate([sphere_and_plane(x) for x in sxrange(-1,1,.3)])
sp[0]      # first frame
# Graphics3d Object
sp[-1]     # last frame
# Graphics3d Object
sp.show()  # optional -- ImageMagick
(x,y,z) = SR.var("x,y,z")

def frame(t):
    return implicit_plot3d((x^2 + y^2 + z^2), (x, -2, 2), (y, -2, 2), (z, -2, 2), plot_points=60, contour=[1,3,5], region=lambda x,y,z: x<=t or y>=t or z<=t)
a = animate([frame(t) for t in srange(.01,1.5,.2)])
a[0]       # long time
# Graphics3d Object
a.show()   # optional -- ImageMagick   # long time
```

## 常用的绘图命令

* plot()：当需要绘制基本的图形时，我们可以使用plot命令。

```
f(x) = sin(x)
p = plot(f(x), (x, -pi/2, pi/2))
p.show()
```

默认情况下创建的绘图会非常简单，接下来我们可以通过增加一些配置绘图属性来进行装饰。比如添加轴标签axes_labels并使我们的绘制线color 为紫色：

```
p = plot(f(x), (x,-pi/2, pi/2), axes_labels=['x','sin(x)'], color='purple')
p.show()
```

其中，color选项可以接受多种形式，比如字符串颜色指定（'purple', 'green', 'red', 'black'等)）、RGB 三元组（如 （255，10，1）或 HTML 样式的十六进制三元组（如 #ff00aa）。

我们还可以通过使用 linestyle和 thickness选项更改线条的样式，比如实线、虚线以及粗细线：

```
p = plot(f(x), (x,-pi/2, pi/2), linestyle='--', thickness=3)
p.show()
```

那如果需要需要绘制多条线怎么办？我们可以通过将图直接“相加”来在同一轴上显示两个函数的图形。

```
f(x) = sin(x)
g(x) = cos(x)
p = plot(f(x),(x,-pi/2,pi/2), color='black')
q = plot(g(x), (x,-pi/2, pi/2), color='red')
r = p + q
r.show()
```

* parametric_plot()：我们可以使用parametric_plot命令来处理参数图。比如画一个半径为 3 的简单圆。

```
t = var('t')
sage: p = parametric_plot( [3*cos(t), 3*sin(t)], (t, 0, 2*pi) )
sage: p.show()
```

* polar_plot()：使用该命令polar_plot完成极坐标图。

```
sage: theta = var("theta")
sage: r(theta) = sin(4*theta)
sage: p = polar_plot((r(theta)), (theta, 0, 2*pi) )
sage: p.show()
```

* plot3d()、implicit_plot3d()：生成 3D 绘图

```
var('x,y,z')
g=golden_ratio;r =4.77
p = 2-(cos(x+g*y)+cos(x-g*y)+cos(y+g*z)+  cos(y-g*z)+cos(z-g*x)+cos(z+g*x))
show(
    implicit_plot3d(p,(x,-r,r),(y,-r,r),(z,-r,r),plot_points=30,color='orange',mesh=1,opacity=.7),spin=1,
    figsize=[8,16],dpi=300
  )
```

```
var('x y z')
F = (x^2+9/4*y^2+z^2-1)^3 - x^2*z^3 - 9/(80)*y^2*z^3
r = 1.5
show(
    implicit_plot3d(F, (x,-r,r), (y,-r,r), (z,-r,r),plot_points=30,color='red',mesh=0,opacity=.7),spin=1,
    figsize=[8,16],dpi=300
  )
```

## 优美案例

以上我们介绍了SageMath绘图的基础知识，那接下来让我们一起欣赏一些用SageMath绘制的比较有趣的图形，感受一下“函数之美”。

* 高斯函数

高斯函数是一种常用的数学函数，通常用来描述物理系统中的扩散过程。它的一般形式为：


<center> $$ f(x)=ae^{-(x-b)^2/{2c^2}} $$ </center>

其中 a、b 与 c 为实数常数 ，且a > 0

高斯函数的图形在形状上像一个倒悬着的钟。参数a指高斯曲线的峰值，b为其对应的横坐标，c即标准差（有时也叫高斯RMS宽值），它控制着“钟”的宽度。

高斯函数在许多领域都有广泛应用，如信号处理、机器学习等。

我们只需要四行代码：

```
a=var("x,a,b,c")
f(x,a,b,c)=a*e^(-(x-b)^2/(2*c^2))
p=plot(f(x,5,2,-0.5),(-10,10), ymin=-10, ymax=10)
p.show()
```

接着我们通过控制参数并使用animate让高斯函数“动起来”，也只需要四行代码：

```
sines = [plot(f(x,a,b,c), (-10,10), color=Color(c,0,0), ymin=-10, ymax=10) for a,b,c in 
zip(sxrange(1,10,1),sxrange(-10,10,2),sxrange(-1,0,0.1))]
a = animate(sines)
a.show()
```

* 笛卡尔心形函数

传说，当年52岁的笛卡尔邂逅了18岁的瑞典公主克里斯汀。笛卡尔在给克里斯汀寄出第十三封信后就气绝身亡了，这第十三封信内容只有短短的一个公式：r=a(1-sinθ）。

公主看到后，立即明了恋人的意图，她马上着手把方程的图形画出来，看到图形，她开心极了，她知道恋人仍然爱着她，原来方程的图形是一颗心的形状。这也就是着名的“心形线”。r=a(1-sinθ）是它在极坐标下的方程表达式：

```
theta = var("theta")
a = 2
r(theta) =  a*(1-sin(theta)) 
p = polar_plot((r(theta)), (theta, 0, 2*pi) ,color = 'red')
p.show()
```

* 摆线的参数方程

摆线是指一个圆在一条定直线上滚动时，圆周上一个定点的轨迹，又称圆滚线、旋轮线。

摆线最早出现可见于公元 1501 年出版的 C·鲍威尔的一本书中。在17世纪，大批卓越的数学家（如伽利略，帕斯卡，托里拆利，笛卡儿，费尔马， 伍任，瓦里斯，惠更斯，约翰·伯努利，莱布尼兹，牛顿等等）热心于研究这一曲线的性质。17 世纪是人们对数学力学和数学运动学爱好的年代，这能解释人们为什么对摆线怀有强烈的兴趣。通常，摆线的参数方程可以表示为：

<center> $$ x = a*cos(ωt+φ) $$ </center>

<center> $$ y = b*sin(ωt+φ) $$ </center>

<br>
其中，a 和 b 是摆线的振幅，ω 是摆线的角速度，t 是时间，φ 是初始相位。

这个方程可以用来描述摆线的位置随时间的变化情况。通过改变 a、b、ω 和 φ 的值，可以得到不同的摆线运动轨迹。

```
t = var('t')
a_values = [a for a in sxrange(0,10,1)]
a_values.extend([a for a in sxrange(10,-10,-1)])
sines = [
  parametric_plot( [a*t-sin(a*t), 1-cos(a*t)], (t, 0, 1) )+
  implicit_plot((x-a)^2+(y-1)^2 == 1, (x,-12,12),(y,-1,3),color='red')
  for a in a_values]
a = animate(sines)
a.show()
```

* 绘制经典函数 x * sin(1/x)

我们在学高等数学的极限一章时应该对f(x)=x * sin(1/x)颇有印象。用SageMath来画一下，可以清楚的看到当x趋近于0时候，f(x)也将无限趋近于0。

```
p = plot(x * sin(1/x), x, -2, 2, plot_points=500)
show(p)
```

* 玫瑰曲线方程

基本的极坐标玫瑰方程为：

<center> $$ ρ=a*cos(nθ) $$ </center>

```
t = var('t')
n = 20/19
g1 = polar_plot(1+2*cos(n*t),(t,0,n*36*pi),plot_points=5000)
g2 = polar_plot(1+1/3*cos(n*t),(t,0,n*36*pi),plot_points=5000)
g1+g2
```

* 画两个3D圆锥体

```
x,y,z=var('x y z')
Lx,Ly,Lz=12,12,12
def get_circular_cone(l=8,r=5,cl='red'):
    h=sqrt(l^2-r^2)
    r0=abs((z/h)*r)
    return implicit_plot3d(
        x^2+y^2==r0^2,
        (x,-Lx,Lx),(y,-Ly,Ly),(z,-Lz,Lz),
        plot_points=50,smooth=True,
        color=cl
    )
p0=get_circular_cone()
show(p0)
```

* 转动的筷子曲线

```
puntos = [(0,0),(0,1),(1,3),(2,1)]
K = len(puntos)
var('x y')
coefs = matrix(QQ, K, 6)
for j in range(K):
    x0, y0 = puntos[j]
    coefs[j,:] = vector([x0^2, y0^2, x0*y0, x0, y0, 1])
    
K = coefs.right_kernel()
v1 = K.basis()[0]
v2 = K.basis()[1]
graficas = []
for t in srange(0,2*pi,0.3):
    c1, c2 = sin(t), cos(t)
    a,b,c,d,e,f = c1*v1 + c2*v2
    curva = a*x^2 + b*y^2 + c*x*y + d*x + e*y + f
    graficas.append( point2d(puntos,color=(1,0,0),pointsize=30) + 
                     implicit_plot(curva,(x,-1,4),(y,-1,4)) )
a = animate(graficas)
a.show(delay=10)
```

* 画一只2D蝴蝶

```
def butterfly2d():
    g = Graphics()
    x1, y1 = 0, 0
    from math import sin, cos, exp, pi
    for theta in srange( 0, 10*pi, 0.01 ):
        r = exp(cos(theta)) - 2*cos(4*theta) + sin(theta/12)^5
        x = r * cos(theta)  
        y = r * sin(theta)
        xx = x*6 + 25       
        yy = y*6 + 25
        if theta != 0:
            l = line( [(x1, y1), (xx, yy)], rgbcolor=hue(theta/7 + 4) )
            g = g + l
            x1, y1 = xx, yy
    g.show(dpi=100, axes=False)
butterfly2d()
```

* 画3D蝴蝶

```
def butterfly3d():
    g = point3d((0,0,0))
    x1, y1 = 0, 0
    from math import sin, cos, exp, pi
    for theta in srange( 0, 10*pi, 0.05):
        r = exp(cos(theta)) - 2*cos(4*theta) + sin(theta/12)^5
        x = r * cos(theta)  
        y = r * sin(theta)
        xx = x*6 + 25     
        yy = y*6 + 25
        if theta != 0:
            l = line3d( [(x1, y1, theta), (xx, yy, theta)],
            rgbcolor=hue(theta/7 + 4) )
            g = g + l
            x1, y1 = xx, yy
    g.show(dpi=100, axes=False)
butterfly3d()
```

# SageMath的帮助系统

- Help帮助：使用 “？”

当我们需要准确了解某个函数或命令的作用以及如何使用它，我们可以使用 “？”来调用内置的帮助系统。例如：

```
lcm?
```

- 查看源代码：使用“??”

有些喜欢研究源码的同学想看看 SageMath 中某个命令的源码，您只需键入您感兴趣的命令，然后键入“??”。

例如，查看factor()的源代码：

```
factor??
```

![图 3](../images/%E6%9F%A5%E7%9C%8B%E6%BA%90%E4%BB%A3%E7%A0%81.png)  



# 更多

受限于篇幅，我们以上只介绍了SageMath的小部分内容，其中提供的代码希望大家能够借助SmartNoteBook去亲自实践并查看输出的信息，探索和领悟SageMath和数学的魅力！

如果您想了解更多关于SageMath的知识和用例，可以参考[SDSU Sage Tutorial](https://mosullivan.sdsu.edu/Teaching/sdsu-sage-tutorial) 以及[SageMath Documentation](https://doc.sagemath.org/)
