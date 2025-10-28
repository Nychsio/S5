Przypomnienie z algebry liniowej 

1. Scaralr  = liczba np 5  , $\pi$ , itd
	1. temperatura,wzorst 

2. Wektor a = (3,5,1) a nalezy do Rrzeczywistych 
	1. szereg czasowy
	2. 

3.  Macierz  $$ A = \begin{bmatrix} 3 & 5 & 1 \\ 5 & 4 & 8 \\ 1 & 10 & 12 \end{bmatrix} A \in \mathbb{R} \space \mathbb{R}^{3 \times 3}$$
	1. obrazek ( czarno biały)
	2. spektogram

		 #### Na macierzach możemy
		 1. Transpozycja
			 1. $$(A^T)_{ij} = A_{ji}$$
			 diagonala zostaje to sama ale elementy poza przekontną się zmnienaiją 
		 2. Dodawanie (odejmowanie)
			 $A+B=C$ $dimA=dinB$ czyli musza byc tej samego rozmiaru (o tych samych wymiarach )
		 3. mnożenie
				 $A\times B = C$ 
				 $C_{i j }\sum_k A_{i k } B_{i k}$
		 4. mnożenie przez skalar 
			 1. $C=\alpha A$ 
					to nie jest zwykłe mnożenie w np
					bo zwykłae mnożenie tdaje nam mnożenie hadamard czyli element po leemencie  
		 5. Macierz jednostkowa 
					 $JX=X$ działa jak jedynka  w mnożeniu  
		 6. Macierz odwrotna 
						$AA^{-1} =J$
			 1. jest to bardzo trudne dla komputera im wyższy wymiar tym większa ilość opreacja 
			 2. jest szczególnie przydatna bo układ linowy za pomocą macierzy .......
			 3. liczy się ją 
					 1. $A ^{-1} = \frac{1}{A}=\begin{bmatrix} M_{1 1} & M{1 2} & {...} \\  &  &  \\  &  & M_{N N} \end{bmatrix}$
				
		 7. Normy
		 8. norma $L^P$ $||x||_p = (\sum_i x^p_i)^\frac{1}{p}$
		 
		 9. $L^2=\sqrt{X^2_1+X^2_2+X^2_3+...+X^2_n}$
		 w deep learningu głównie się używa $L^1$ $i $L^2$

		normy muszą spełniać założenia 
		musi być tak zdefiniowana że spełnia nierówność tójkątną 
		$f(x+y)=<f(x)+f(y)$
		do czego się stosuje normy ? 
		do określenia podobieństwa wektorów 
		norma jest celem uczenia 
		optymalizujemy norme 

2 rzecz reguralyzacja wartstw 
możemy sobie dodwać elementy reguralyzacyjne do każdej warstwy w sieci neuronowej żeby pomagać jej odpowiednio się uczyć 
z reguralyzacja chodzi o to że uczy się nam jeden neruon ttylko żeby reprezntacja danych była rozłożona 
żeby nie było że jeden neuron ma wage 10 a reszta ma 0

Wartości własne macierzy 

rozkładanie macierzy to jedna z metod robienia sys rekomendacyjnych 

każdą liczbe nie będącą liczbe pierwszą możemy rozłożyć 
np 12 =3x2x2

tak samo można macierz i do tego służy zagadnienie wartości włąsnych macierzy 


$Av=\lambda \times v$
wystarczy znaleśc wektory własne i wartości własne i liczymy odwrotność tego 

$A= V deg(\lambda) V ^{-1}$

$A=  \begin{bmatrix}  4 & 1 \\ 2 & 3 \end{bmatrix}$

$det(A-J X)=0$
 $\begin{bmatrix}  4-x& 1 \\ 2 & 3-x \end{bmatrix}=(4-x)(3-x)$
$\Delta=4y-40=9$
$\sqrt{\Delta}=3$
$\lambda_1=2 \space \lambda_5$

$\begin{bmatrix}  2 & 1 \\ 2 & 1 \end{bmatrix}\begin{bmatrix}   x_1 \\ 2 x_2 \end{bmatrix}=\begin{bmatrix}  0 \\ 0 \end{bmatrix}=2x_1+x_2=0$

$x_1= \frac{1}{2}$
$x_2 = 1$
$\begin{bmatrix}  -1 & 1 \\ 2 & -2 \end{bmatrix}\begin{bmatrix}   x_1 \\ 2 x_2 \end{bmatrix}=\begin{bmatrix}  0 \\ 0 \end{bmatrix}=x_1=x_2$


### macierz prostokątna $m\times n$
 SVD - singural value decomposition
 za pomocą tego tworzy się systemy rekomendacyjne 
 $A \in R^{n\times m }$
 możemy rozłożyć na 
 $U \space D \ V ^T$
 gdzie U  jest $n\times n$
 D jest $n\times m$
 V jest $m \times m$


czy da się macierz odwrotną dla prostokątnej 

Da ! ale ? jest to przybliżone 

jest to macierz odwrotna Moor'a - Pennrose'a

$$A^+ = \lim_{\delta \to 0^+} (A^\dagger A + \delta^2 I)^{-1} A^\dagger$$
W praktyce stosuje się SVD gdyż obliczeniowo opłaca się bardziej 


$A^T=V D^+ U^T$

V mamy z svd U mamy transponowane D jest macierzą diagonalną w SVD 



Konwolucja - złożenie na sibie dwóch funkcji 
$$(f * g)(t) = \int_{-\infty}^{\infty} f(t - \tau) g(\tau) \, d\tau$$
mamy macierz $C_{m n}=(a\times h)_{mn}=\sum h_{jk} * a_{mj}$  

$A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix}$
$H = \begin{bmatrix} 0 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & 0 & 1 \end{bmatrix}$

$c = \begin{bmatrix} 1 & 2 & 4 & 2 & 3\\ 4& 6& 12 & 8 &6  \\ 8 & 14  & 25 &16&12\\  4& 12 &18&14&6 \\  4&  12&16&8&9  \end{bmatrix}$

te jądra h się uczy

4. tensory
ma on $n\times {m}\times {r}$ wymiarów 
$$ \begin{align*} \text{Warstwa 1 (k=1):} \quad T_{ij1} &= \begin{pmatrix} 5 & 1 \\ 8 & 3 \end{pmatrix} \\ \\ \text{Warstwa 2 (k=2):} \quad T_{ij2} &= \begin{pmatrix} 0 & -2 \\ 4 & 7 \end{pmatrix} \\ \\ \text{Warstwa 3 (k=3):} \quad T_{ij3} &= \begin{pmatrix} 6 & 9 \\ 11 & -5 \end{pmatrix} \end{align*} $$


$T \in \mathbb{R}^{n\times m \times r}$

	1.kolorowy obrazek (R,G,B)
	2.przetwarzanie języka sekwenecje słów
	3.
	 

powszechnie w deep lerningu tylko do 4 rzędu 




### do przestudiowania w domu
transformacja furiera 
przechodzimy z reprezentacji szeregu czasowego ro reprezentecji  częstowlliwości


Elementy statystyki i teori informacji 
