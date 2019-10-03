## Сложност и Изчислимост 02.10.2019 г.

Подходи към формализиране на изчислимостта:
- подход на Тюринг, *1936 г.* - машини на Тюринг
- подход на Клини, *1936 г.* - частично рекурсивни функции

Частични функции: <img src="https://latex.codecogs.com/svg.latex?\Large&space;f(x)=\frac{1}{x};{\;}f(x)=\log_{2}x"> - не са дефинирани върху цялото множество <img src="https://latex.codecogs.com/svg.latex?\Large&space;\mathbb{R}"> на реалните числа.

По-надолу, където споменаваме *функция* ще разбираме <img src="https://latex.codecogs.com/svg.latex?\Large&space;f:\mathbb{N}^n\nrightarrow\mathbb{N}">, където <img src="https://latex.codecogs.com/svg.latex?\Large&space;\mathbb{N}=\{0,1,2,...\}"> (частично рекурсивна функция).

<img src="https://latex.codecogs.com/svg.latex?\Large&space;f(x_1,...,x_n)=f(\overline{x})">.

*Означения:*
- <img src="https://latex.codecogs.com/svg.latex?\Large&space;!f(\overline{x})"> - <img src="https://latex.codecogs.com/svg.latex?\Large&space;f"> е дефинирана в <img src="https://latex.codecogs.com/svg.latex?\Large&space;\overline{x}">
- <img src="https://latex.codecogs.com/svg.latex?\Large&space;\neg{!}f(\overline{x})"> - <img src="https://latex.codecogs.com/svg.latex?\Large&space;f"> няма дефинирана стойност в <img src="https://latex.codecogs.com/svg.latex?\Large&space;\overline{x}">
- <img src="https://latex.codecogs.com/svg.latex?\Large&space;f(\overline{x})\cong{g(\overline{x})}"> - условно равенство <img src="https://latex.codecogs.com/svg.latex?\Large&space;\Leftrightrrow"> и двете функции са дефинирани и имат еднакви стойности:
<img src="https://latex.codecogs.com/svg.latex?\Large&space;!f(\overline{x})\&!g(\overline{x})\&f(\overline{x})=g(\overline{x})"> или едновременно не са дефинирани: <img src="https://latex.codecogs.com/svg.latex?\Large&space;\neg{!}{f(\overline{x})}\&\neg{!}{g(\overline{x})}">  
- <img src="https://latex.codecogs.com/svg.latex?\Large&space;Dom(f)"> - дефиниционна област на <img src="https://latex.codecogs.com/svg.latex?\Large&space;f:{\;}\{\overline{x}|!f(\overline{x})\}"> - множеството на тези <img src="https://latex.codecogs.com/svg.latex?\Large&space;\overline{x}">, за които <img src="https://latex.codecogs.com/svg.latex?\Large&space;f(\overline{x})"> е дефинирана 

Изходни (базисни) примитивно рекурсивни функции:
- <img src="https://latex.codecogs.com/svg.latex?\Large&space;\vartheta{(x)}=0">, за <img src="https://latex.codecogs.com/svg.latex?\Large&space;\forall{x}\in\mathbb{N}">  
- <img src="https://latex.codecogs.com/svg.latex?\Large&space;S{(x)}=x+1">, за <img src="https://latex.codecogs.com/svg.latex?\Large&space;\forall{x}\in\mathbb{N}">  

<img src="https://latex.codecogs.com/svg.latex?\Large&space;I_{k}^n(x_1,...,x_n)=x_k,{\;}\forall{n}\in{\mathbb{N}},{\;}1\le{k}\le{n}"> - проектираща (координатна) функция.

<img src="https://latex.codecogs.com/svg.latex?\Large&space;\overline{f_n}=\{f|f:\mathbb{N}^n\nrightarrow{\mathbb{N}\}"> - <img src="https://latex.codecogs.com/svg.latex?\Large&space;f"> е тотална, ако <img src="https://latex.codecogs.com/svg.latex?\Large&space;Dom(f)=\mathbb{N}^n">.
- композиция <img src="https://latex.codecogs.com/svg.latex?\Large&space;h=f\cdot{g}\Leftrightarrowh(x)\stackrel{\text{def}}{=}g(f(x))">.
- суперпозиция: по дадени <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_1,...,f_k\in\overline{f_n}"> и <img src="https://latex.codecogs.com/svg.latex?\Large&space;g\in{\overline{f_k}}">, дефинираме нов функция <img src="https://latex.codecogs.com/svg.latex?\Large&space;h=g(f_1,...,f_k)\in{\overline{f_n}}"> по следния начин <img src="https://latex.codecogs.com/svg.latex?\Large&space;h(x_1,...,x_n)\stackrel{\text{def}}{=}g(f_1(x_1,...,x_n),...,f_k(x_1,...,x_n))">. 

Примитивна рекурсия:

Пример - <img src="https://latex.codecogs.com/svg.latex?\Large&space;f(x)=1">, ако <img src="https://latex.codecogs.com/svg.latex?\Large&space;x=0">. <img src="https://latex.codecogs.com/svg.latex?\Large&space;f(x)=f(x-1).x">, в противен случай. <img src="https://latex.codecogs.com/svg.latex?\Large&space;f(x)=x!">.

Казваме, че <img src="https://latex.codecogs.com/svg.latex?\Large&space;f"> се дефинира чрез примитивна рекурсия от <img src="https://latex.codecogs.com/svg.latex?\Large&space;g">, ако :
<img src="https://latex.codecogs.com/svg.latex?\Large&space;\begin{cases}f(0)=c\\f(x+1)=g(x,f(x))\end{cases}">.

примера за <img src="https://latex.codecogs.com/svg.latex?\Large&space;x!">: <img src="https://latex.codecogs.com/svg.latex?\Large&space;\begin{cases}f(0)=1\\f(x+1)=(x+1).f(x)\end{cases}">, <img src="https://latex.codecogs.com/svg.latex?\Large&space;c=1,{\;}g(x,y)=(x+1).y">

Нека <img src="https://latex.codecogs.com/svg.latex?\Large&space;g\in{\overline{f_n}},{\;}h\in{\overline{f_{n+2}}},{\;}n\ge{0}"> и <img src="https://latex.codecogs.com/svg.latex?\Large&space;\overline{0}\{0,1,2,...\}"> - константи, са дадени функции и с тяхна помощ дефинираме нова функция <img src="https://latex.codecogs.com/svg.latex?\Large&space;\overline{f_{n+1}}"> по следния начин:
<img src="https://latex.codecogs.com/svg.latex?\Large&space;\ast\begin{cases}f(x_1,...,x_n,0)\cong{g(x_1,...,x_n)\\f(x_1,...,x_n,y+1)\cong{h(x_1,...,x_n,y,f(x_1,...,x_n,y))}\end{cases}">

<img src="https://latex.codecogs.com/svg.latex?\Large&space;\ast"> ще наричаме обща схема на примитивната рекурсия и ще казваме, че <img src="https://latex.codecogs.com/svg.latex?\Large&space;f"> е дефинирана чрез примитивна рекурсия от <img src="https://latex.codecogs.com/svg.latex?\Large&space;g"> и <img src="https://latex.codecogs.com/svg.latex?\Large&space;h">.

*Твърдение 1.* По дадени <img src="https://latex.codecogs.com/svg.latex?\Large&space;f"> и <img src="https://latex.codecogs.com/svg.latex?\Large&space;h{\;}\exists{!}f"> (съществува еднозначно определена функция <img src="https://latex.codecogs.com/svg.latex?\Large&space;f">) удовлетворяваща примитивно рекурсивната схема <img src="https://latex.codecogs.com/svg.latex?\Large&space;\ast">.<br>
*Док-во:* (индукция) Нека <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_1"> и <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_2"> удовлетворяват <img src="https://latex.codecogs.com/svg.latex?\Large&space;\ast">. Ще покажем, че <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_1=f_2">, т.е. <img src="https://latex.codecogs.com/svg.latex?\Large&space;\forall{\overline{x}}{\:}\forall{y}(f_1(\overline{x},y)\cong{f_2(\overline{x},y))">. Фиксираме произволна наредена n-орка <img src="https://latex.codecogs.com/svg.latex?\Large&space;\overline{x}\in\mathbb{N}"> и нека <img src="https://latex.codecogs.com/svg.latex?\Large&space;P(y)\Leftrightarrow{f_1(\overline{x},y)\cong{f_2(\overline{x},y)}}">. 

С индукция по <img src="https://latex.codecogs.com/svg.latex?\Large&space;y"> ще докажем, че <img src="https://latex.codecogs.com/svg.latex?\Large&space;\forall{y}(P(y))">.<br>
*База:* <img src="https://latex.codecogs.com/svg.latex?\Large&space;y=0">: <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_1(\overline{x},y)\stackrel{\text{\ast}}{\cong}g(\overline{x})\Rightarrow{P(0)}"> и <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_2(\overline{x},y)\stackrel{\text{\ast}}{\cong}g(\overline{x})\Rightarrow{P(0)}"> е вярно.<br>
*Индукционна хипотеза:* Нека <img src="https://latex.codecogs.com/svg.latex?\Large&space;P(y)"> е вярно, т.е. <img src="https://latex.codecogs.com/svg.latex?\Large&space;\f_1(\overline{x},y)\cong{f_2(overline{x},y)}">.<br>
*Индукционен преход (стъпка) за <img src="https://latex.codecogs.com/svg.latex?\Large&space;y+1">:* <img src="https://latex.codecogs.com/svg.latex?\Large&space;f_1(\overline{x},y+1)\cong{g(\overline{x},y,f(\overline{x},y))}\stackrel{\text{ind.{\:}hyp.}}{\cong}g(\overline{x},y,f_2(\overline{x},y))\cong{f_2(\overline{x},y+1)}">. С това твърдението е доказано.

Да разгледаме функцията на Маккарти (![McCarthy 91 function](https://en.wikipedia.org/wiki/McCarthy_91_function)). Тя дава ясен пример за това, какво не е примитивна рекурсия.<br> Имаме, че <img src="https://latex.codecogs.com/svg.latex?\Large&space;M(n)=\begin{cases}n-10,{\;}{\;}if{\;}n>100\\M(M(n+11)),{\;}{\;}if{\;}n\le{100}\end{cases}">. Tя дава ясен пример за това как при всяка итерация (навлизане в рекурсията) се отдалечаваме от базовия случай (дъното на рекурсията). В този случай, няма как да знаем дали рекурсията изобщо ще спре някога, за това тя не е примитивна. Въпреки това, в тои случай, тя спира. Например:
 <img src="https://latex.codecogs.com/svg.latex?\Large&space;М(102)=92,{\;}M(103)=93,...">.
 
 От дефиницията за примитивно рекурсивна функция се вижда че ако  <img src="https://latex.codecogs.com/svg.latex?\Large&space;g"> и  <img src="https://latex.codecogs.com/svg.latex?\Large&space;h"> са тотални, то и <img src="https://latex.codecogs.com/svg.latex?\Large&space;f"> - тяхната примитивна рекурсия (функцията, която се получава от тях чрез помощта на операцията примитивна рекурсия) също е тотална.<br>
 *Док-во:* (индукция по  <img src="https://latex.codecogs.com/svg.latex?\Large&space;y">)  <img src="https://latex.codecogs.com/svg.latex?\Large&space;\forall{\overline{x}}\forall{y}!f(\overline{x},y)">, фиксираме  <img src="https://latex.codecogs.com/svg.latex?\Large&space;\overline{x}{\;},{\;}{\;}P(y)\stackrel{\text{def.}}{\cong}!f(\overline{x},y)">.<br>
 *База:*  <img src="https://latex.codecogs.com/svg.latex?\Large&space;y=0{\;}:{\;}f(\overline{x},0)=g(\overline{x})"> - тотална по дефиниция.<br>
 *Индукционна хипотеза:* Нека за някое <img src="https://latex.codecogs.com/svg.latex?\Large&space;y{\;}:{\;}P(y)\stackrel{\text{def.}}{\Leftrightarrow}!f(\overline{x},y)">. Тогава за <img src="https://latex.codecogs.com/svg.latex?\Large&space;y+1{\;}:{\;}f(\overline{x},y+1)\stackrel{\text{*}}{\cong}h(\overline{x},y,f(\overline{x},y))"> - също е дефинирана, защото <img src="https://latex.codecogs.com/svg.latex?\Large&space;f(\overline{x},y)"> е дефинирана от индукционната хипотеза.

