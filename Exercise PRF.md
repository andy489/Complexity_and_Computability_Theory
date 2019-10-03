## Примитивно рекурсивни функции 
*02.10.2019г.*

**Твърдение 5.** Следните функции са примитивно рекурсивни:<br>
**а)** <img src="https://latex.codecogs.com/svg.latex?\Large&space;{\;}C_{a}^{n}(x_1,...,x_n)\stackrel{\text{def.}}{\cong}{a},{\;}\forall{\overline{x}\in{\mathbb{N}}},{\;}n\ge{1},{\;}a\in{\mathbb{N}}">;<br><br>
**б)** <img src="https://latex.codecogs.com/svg.latex?\Large&space;{\;}f_1(x,y)=x+y"><br><br>
**в)** <img src="https://latex.codecogs.com/svg.latex?\Large&space;{\;}f_2(x,y)=x.y"><br><br>
**г)** <img src="https://latex.codecogs.com/svg.latex?\Large&space;{\;}f_3(x,y)=x^y"><br><br>
**д)** <img src="https://latex.codecogs.com/svg.latex?\Large&space;{\;}f_4(x,y)=\underbrace{x^{x^{{.^{.^x}}}}}_{y}"><br><br>
**е)** <img src="https://latex.codecogs.com/svg.latex?\Large&space;{\;}f_5(x,y)=\underbrace{x\diamond{x\diamond{...(x\diamond{x})})})}_{y}">, където <img src="https://latex.codecogs.com/svg.latex?\Large&space;x\diamond{y}=f_4(x,y)"><br><br>
**ж)** <img src="https://latex.codecogs.com/svg.latex?\Large&space;{\;}f_6(x,y)=x\stackrel{\text{o}}{-}y">, където <img src="https://latex.codecogs.com/svg.latex?\Large&space;{\;}pred(x)=x\stackrel{\text{o}}{-}1\stackrel{\text{def.}}{=}\begin{cases}x-1,{\;}x\ge{1}\\0,{\;}x=0\end{cases}"> е функция *предшественик*<br>

***Док-во***<br><br><br>
**а)**<br> <img src="https://latex.codecogs.com/svg.latex?\Large&space;C_{a}^{n}(x_1,...,x_n)=S\bigg(S\big(...\underbrace{\vartheta{(\underbrace{I_{1}^{n}(x_1,...,x_n)}_{x_1}}}_{0}\big)...\big)\bigg)=a">, където <img src="https://latex.codecogs.com/svg.latex?\Large&space;a"> е фиксирано.<br><br><br>
**б)**<br> <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_1(x,0)=x+0=x=I_{1}^{1}(x)"><br><img src="https://latex.codecogs.com/svg.latex?\Large&space;f_1(x,y+1)=x+(y+1)=\underbrace{(x+y)}+1=f_1(x,y)+1=S(f_1(x,y))">.<br>
Следователно от дефиницията за *примитивно рекурсивна функция*:<br><img src="https://latex.codecogs.com/svg.latex?\Large&space;f(\overline{x},0)=g(\overline{x})"><br><img src="https://latex.codecogs.com/svg.latex?\Large&space;f(\overline{x},y+1)=h(\overline{x},y,f(\overline{x},y))"><br>формално имеме <br> 
<img src="https://latex.codecogs.com/svg.latex?\Large&space;\begin{cases}f_1(x,0)=I_{1}^{1}\\f_1(x,y+1)=S(f_1(x,y))=h(x,f_1(x,y))\end{cases}">,<br> където <img src="https://latex.codecogs.com/svg.latex?\Large&space;h(x,z)=S(z)">. Така достигнахме примитивно рекурсивни (базови) функции от десните страни на равенствата - което искахме. <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_1"> се получава с помощта на *примитивна рекурсия* от базовата примитивно рекурсивни функция <img src="https://latex.codecogs.com/svg.latex?\Large&space;I_{1}^{1}"> и <img src="https://latex.codecogs.com/svg.latex?\Large&space;h">, която също е примитивна рекурсия - следователно и <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_1"> е ПРФ <br><br><br>
 **в)**<br><img src="https://latex.codecogs.com/svg.latex?\Large&space;f_2(x,y)=x.y"><br>
 <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_2(x,0)=x.0=0=\vartheta{(x)}"><br>
 <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_2(x,y+1)=x.(y+1)=x.y+x=f_2(x,y)\underbrace{+}_{PRF}x=h(x,y,f_2(x,y))">,<br>където <img src="https://latex.codecogs.com/svg.latex?\Large&space;h(x,y,z)=x+z">. T.e. <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_2"> се получава с помощта на операцията *примитивна рекурсия* от 0 и събиранетои следователно е *примитивно рекурсивна функция*. (0 е базова ПРФ, а събирането доказахме, че е ПРФ в *а)*)
 
