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

<img src="https://latex.codecogs.com/svg.latex?\Large&space;\overline{f_n}=\{f|f:\mathbb{N}^n\nrightarrow{\mathbb{N}\}"> - <img src="https://latex.codecogs.com/svg.latex?\Large&space;f"> е тотална, ако <img src="https://latex.codecogs.com/svg.latex?\Large&space;Dom(f)=\mathbb{N}^n">
