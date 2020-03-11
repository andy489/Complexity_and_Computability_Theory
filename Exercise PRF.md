## Примитивно рекурсивни функции 
*02.10.2019г.*

**Твърдение 5.** Следните функции са примитивно рекурсивни:<br>
**а)** <img src="https://latex.codecogs.com/svg.latex?\Large&space;{\;}C_{a}^{n}(x_1,...,x_n)\stackrel{\text{def.}}{\cong}{a},{\;}\forall{\overline{x}\in{\mathbb{N}}},{\;}n\ge{1},{\;}a\in{\mathbb{N}}">;<br><br>
**б)** <img src="https://latex.codecogs.com/svg.latex?{\;}f_1(x,y)=x+y"><br><br>
**в)** <img src="https://latex.codecogs.com/svg.latex?{\;}f_2(x,y)=x.y"><br><br>
**г)** <img src="https://latex.codecogs.com/svg.latex?{\;}f_3(x,y)=x^y"><br><br>
**д)** <img src="https://latex.codecogs.com/svg.latex?{\;}f_4(x,y)=\underbrace{x^{x^{{.^{.^x}}}}}_{y}"><br><br>
**е)** <img src="https://latex.codecogs.com/svg.latex?{\;}f_5(x,y)=\underbrace{x\diamond{x\diamond{...(x\diamond{x})})})}_{y}">, където <img src="https://latex.codecogs.com/svg.latex?\Large&space;x\diamond{y}=f_4(x,y)"><br><br>
**ж)** <img src="https://latex.codecogs.com/svg.latex?{\;}f_6(x,y)=x\stackrel{\text{o}}{-}y">, където <img src="https://latex.codecogs.com/svg.latex?{\;}pred(x)=x\stackrel{\text{o}}{-}1\stackrel{\text{def.}}{=}\begin{cases}x-1,{\;}x\ge{1}\\0,{\;}x=0\end{cases}"> е функция *предшественик*<br><br>
**з)** <img src="https://latex.codecogs.com/svg.latex?sg(x)=\begin{cases}0,{\;}x=0\\1,{\;}>0\end{cases}"><br><br>
**и)** <img src="https://latex.codecogs.com/svg.latex?\overline{sg}(x)=\begin{cases}1,{\;}x=0\\0,{\;}>0\end{cases}"><br><br>
**й)** <img src="https://latex.codecogs.com/svg.latex?min(x,y)"><br><br>
**к)** <img src="https://latex.codecogs.com/svg.latex?max(x,y)"><br><br>

***Док-во***<br><br><br>
**а)**<br> <img src="https://latex.codecogs.com/svg.latex?C_{a}^{n}(x_1,...,x_n)=S\bigg(S\big(...\underbrace{\vartheta{(\underbrace{I_{1}^{n}(x_1,...,x_n)}_{x_1}}}_{0}\big)...\big)\bigg)=a">, където <img src="https://latex.codecogs.com/svg.latex?a"> е фиксирано.<br><br><br>
**б)**<br> <img src="https://latex.codecogs.com/svg.latex?f_1(x,0)=x+0=x=I_{1}^{1}(x)"><br><img src="https://latex.codecogs.com/svg.latex?f_1(x,y+1)=x+(y+1)=\underbrace{(x+y)}+1=f_1(x,y)+1=S(f_1(x,y))">.<br>
Следователно от дефиницията за *примитивно рекурсивна функция*:<br><img src="https://latex.codecogs.com/svg.latex?f(\overline{x},0)=g(\overline{x})"><br><img src="https://latex.codecogs.com/svg.latex?f(\overline{x},y+1)=h(\overline{x},y,f(\overline{x},y))"><br>формално имеме <br> 
<img src="https://latex.codecogs.com/svg.latex?\begin{cases}f_1(x,0)=I_{1}^{1}\\f_1(x,y+1)=S(f_1(x,y))=h(x,f_1(x,y))\end{cases}">,<br> където <img src="https://latex.codecogs.com/svg.latex?\Large&space;h(x,z)=S(z)">. Така достигнахме примитивно рекурсивни (базови) функции от десните страни на равенствата - което искахме. <img src="https://latex.codecogs.com/svg.latex?f_1"> се получава с помощта на *примитивна рекурсия* от базовата примитивно рекурсивни функция <img src="https://latex.codecogs.com/svg.latex?I_{1}^{1}"> и <img src="https://latex.codecogs.com/svg.latex?h">, която също е примитивна рекурсия - следователно и <img src="https://latex.codecogs.com/svg.latex?f_1"> е ПРФ <br><br><br>
 **в)**<br><img src="https://latex.codecogs.com/svg.latex?f_2(x,y)=x.y"><br>
 <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_2(x,0)=x.0=0=\vartheta{(x)}"><br>
 <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_2(x,y+1)=x.(y+1)=x.y+x=f_2(x,y)\underbrace{+}_{PRF}x=h(x,y,f_2(x,y))">,<br>където <img src="https://latex.codecogs.com/svg.latex?h(x,y,z)=x+z">. T.e. <img src="https://latex.codecogs.com/svg.latex?f_2"> се получава с помощта на операцията *примитивна рекурсия* от 0 и събиранетои следователно е *примитивно рекурсивна функция*. (0 е базова ПРФ, а събирането доказахме, че е ПРФ в *а)*)<br><br><br>
 **г)**<br><img src="https://latex.codecogs.com/svg.latex?\f_3(x,y)=x^y"><br>
 <img src="https://latex.codecogs.com/svg.latex?f_3(x,0)=x^0=1=S(\vartheta{x})"><br>
 <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_3(x,y+1)=x^{y+1}=x^y.x=f_3(x,y).x=f_2(x,f_3(x,y))=h(x,y,f_3(x,y))">.<br><br><br>
 **д)**<br><img src="https://latex.codecogs.com/svg.latex?f_4(x,y)=\underbrace{x^{x^{{.^{.^x}}}}}_{y}"> - суперстепенуване.<br><img src="https://latex.codecogs.com/svg.latex?x^{y^z}\stackrel{\text{def.}}{=}x^{(y^z)}"><br>
 <img src="https://latex.codecogs.com/svg.latex?f_4(x,0)=\underbrace{x^{x^{{.^{.^x}}}}}_{0}=1"><br>
 <img src="https://latex.codecogs.com/svg.latex?f_4(x,y+1)=\underbrace{x^{x^{{.^{.^x}}}}}_{y+1}=x^{\underbrace{x^{{.^{.^x}}}}_{y}}=x^{f_4(x,y)}">.<br>
 При <img src="https://latex.codecogs.com/svg.latex?y=0{\;}:{\;}f_4(x,0+1)\stackrel{\text{def.}}{=}x=x^{f_4(x,0)}=x"><br><br><br>
 **e)**<br> *аналогично на д)*<br><br><br>
 **ж)**<br><img src="https://latex.codecogs.com/svg.latex?x\stackrel{\text{o}}{-}y\stackrel{\text{def.}}{=}\begin{cases}x-y,{\;}x\ge{y}\\0,{\;}x<y\end{cases}">.<br>
 <img src="https://latex.codecogs.com/svg.latex?f(x,0)=x-0=x=I_{1}^{1}(x)"><br>
 <img src="https://latex.codecogs.com/svg.latex?f(x,y+1)=x-(y+1)\underbrace{=}_{?}(x-y)-1"><br>
 *Проверка:*<br> 1.) <img src="https://latex.codecogs.com/svg.latex?x>y{\;}(x\ge{y+1})"><br><br>
 *от ляво:* <img src="https://latex.codecogs.com/svg.latex?x\stackrel{\text{o}}{-}(y+1)\stackrel{\text{def.}}{=}x-(y+1)=(x-y)-1=\underbrace{(x\stackrel{\text{o}}{-}y)}_{>0}\stackrel{\text{o}}{-}1"><br>
2.) <img src="https://latex.codecogs.com/svg.latex?x\le{y}{\;}:{\;}x\stackrel{\text{o}}{-}(y+1)=0{\;};{\;}(x\stackrel{\text{o}}{-}y)\stackrel{\text{o}}{-}1=0">.<br>
Функцията предшественик е примитивно рекурсивна, защото: <img src="https://latex.codecogs.com/svg.latex?pred(0)=0{\;};{\;}p(x+1)=(x+1)-1=x+1-1=x=I_{1}^{1}(x)=g(x,pred(x)),{\;}g(x,y)=x"><br><br><br>
**з)**<br><img src="https://latex.codecogs.com/svg.latex?\begin{cases}sg(0)=0\\sg\underbrace{(x+1)}_{>0}=1=S(\vartheta(x))\end{cases}"><br><br>
**и)**<br> <img src="https://latex.codecogs.com/svg.latex?\overline{sg}(x)=1-sg(x)=1\stackrel{\text{o}}{-}sg(\overline{x})"><br><br>
 **й)**<br> <img src="https://latex.codecogs.com/svg.latex?min(x,y)=x\stackrel{\text{o}}{-}(x\stackrel{\text{o}}{-}y)"><br><br>
 **к)**<br> <img src="https://latex.codecogs.com/svg.latex?max(x,y)=x+(y\stackrel{\text{o}}{-}x)"><br>
 *Проверка:*<br> 1.) <img src="https://latex.codecogs.com/svg.latex?x\ge{y}\Rightarrow{x}+(y\stackrel{\text{o}}{-}x)=x+0=x=max(x,0)"><br>2.) <img src="https://latex.codecogs.com/svg.latex?<{y}\Rightarrow{x}+(y\stackrel{\text{o}}{-}x)=x+(y-x)=y=max(0,y)"><br>

**Задача 1.** <br>a) Докажете, че: <img src="https://latex.codecogs.com/svg.latex?f(x_1,...,x_n)=max(x_1,...,x_n)"> е примитивно рекурсивна функция.<br>б) <img src="https://latex.codecogs.com/svg.latex?f(x,y)\stackrel{\text{def.}}{=}max\{g(x,z)|z\le{y}\}"> докажете, че ако <img src="https://latex.codecogs.com/svg.latex?g"> е примитивно рекурсивна функция, то и <img src="https://latex.codecogs.com/svg.latex?\Large&space;f"> е такава.<br><br>
*Док-во:*<br><br>
a)<br> <img src="https://latex.codecogs.com/svg.latex?f(x_1,...,x_n)=max(x_1,max(x_2,max(...x_{n-2}(max(x_{n-1},x_n))...)))">

*Итеративна програма, която симулира примитивна рекурсия за намирането на най-големия от 5 сравними елемента:*
```cpp
#include <iostream>
int max(int x, int y)
{
	return x > y ? x : y;
}
int main()
{
	int a, b; std::cin >> a >> b;

	int result(max(a, b));
	for (size_t i = 0; i < 3; i++)
	{
		int c; std::cin >> c;
		result = max(result, c);
	}
	std::cout << result;
	return 0;
}
```

б)<br> <img src="https://latex.codecogs.com/svg.latex?f(x,0)=max\{g(x,z)|z\le{0}\}=g(x,0)"> <br>
<img src="https://latex.codecogs.com/svg.latex?f(x,y+1)=max\{g(x,0),...,g(x,y)\}"><br><br>
<img src="https://latex.codecogs.com/svg.latex?f(x,y+1)=max(max\{g(x,0),...,g(x,y)\},g(x,y+1))="><br><img src="https://latex.codecogs.com/svg.latex?=max(f(x,y),g(x,y+1))="> <br> 
<img src="https://latex.codecogs.com/svg.latex?\begin{cases}f(x,0)=g(x,0)\\f(x,y+1)=max(f(x,y),g(x,y+1))=h(x,y,f(x,y)),{\;}h(x,y,z)=max(z,g(x,y))\end{cases}">

**Задача 2.** <br> <img src="https://latex.codecogs.com/svg.latex?h(\overline{x})=max\{g(\overline{x},z)|z\le{b}(\overline{x}),{\;}g,b"> - фиксирани функции. Докажете, че ако <img src="https://latex.codecogs.com/svg.latex?g,b"> са примитивно рекурсивни, то и <img src="https://latex.codecogs.com/svg.latex?h"> e примитивно рекурсивна функция.
<img src="https://latex.codecogs.com/svg.latex?\h(\overline{x})=f(\overline{x},b(\overline{x}))">, където <img src="https://latex.codecogs.com/svg.latex?f"> е функцията от *задача 1*.
