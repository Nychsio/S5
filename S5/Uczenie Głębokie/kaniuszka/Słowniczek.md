
### Warstwa gęsta
- innymi słowy fully connected - graf pełny dwudzielny - każdy neuron z każdym następnym - w odróżnieniu sparse (rzadka)

mówimy o połączeniu **każdego neuronu z warstwy poprzedzającej z każdym neuronem w warstwie bieżącej**

### Funkcja aktywacji 
- funkcja (ważona suma) - przeważnie nieliniowa funkcja, np. relu

#### Relu - funkcja aktywacji - dla x < 0: 0; dla x >= 0: y = x

### MNIST
- jeden z najbardziej basicowych zbiorów danych zawierający cyfry - do klasyfikacji cyfr z napisanych ręcznie


### Float32
(double liczby podwójnej precyzji) / int8 (8-bitów) - format danych liczbowych - (0 czerń, 255 biel) - keras nie lubi intów - 
więc na MNIST przechodzimy z wartości od 0 do 255 do 0 - 1 

nie wiem co tu ktoś próbował pierdolić float 32  - liczby zmienno przecinkowe o max precyzji 32 bitów 


### Entropia krzyżowa 
(cross-entropy) - loss - warto znać wzorek 
metoda na obliczenie KARY, jaką model dostaje za swoją odpowiedź.

$$
L = - \sum_{i=1}^{C} y_i \log(\hat{y}_i)
$$

- $L$: To jest właśnie **końcowa kara** (Loss) dla modelu za jedną odpowiedź.
    
- $\sum$: "Suma". Oznacza, że liczymy coś dla każdej klasy (od kota, przez psa, po konia) i dodajemy wyniki.
    
- $y_i$: To **prawdziwa odpowiedź**. Jest to `1` dla właściwej klasy (np. kota) i `0` dla wszystkich pozostałych.
    
- $\hat{y}_i$: (czyt. "y-hat") To **odpowiedź modelu**. Prawdopodobieństwo, jakie model przypisał danej klasie (np. 70% czyli 0.7).
    
- $\log()$: **Logarytm**. To jest nasz "generator kary". Jeśli model da bardzo małe prawdopodobieństwo prawdziwej klasie (np. `log(0.01)`), logarytm zwróci dużą ujemną liczbę. Minus z przodu wzoru zamienia ją na dużą dodatnią karę.


### Softmax 
- funkcja aktywacji

funkcja aktywacji używana na samym końcu sieci w problemach klasyfikacji, aby zamienić surowe wyniki (logity) w ładny, zrozumiały rozkład prawdopodobieństw, którego suma zawsze wynosi 100%

### Logity / log-odds - logit - log odds - logarytm szans 


### Kompilacja modelu 
- określanie loss, optimizer, opcjonalnie callbacks i metryki 


	### Callbacks
- wywoływania wydarzeń podczas uczenia modelu (early stopping, logowanie danych do serwera)



### Optimizer
Optimizer to algorytm, który na podstawie bieżących błędów modelu (gradientu) decyduje, jak zmienić jego wagi


- **SGD (Stochastic Gradient Descent):** To najprostsza strategia. Zawsze robisz krok o stałej długości, prosto w dół. Działa, ale może być powolna i czasem "utknąć" w małych zagłębieniach terenu.
    
- **Adam (Adaptive Moment Estimation):** To jest "inteligentny turysta". Ma pęd (momentum), więc jeśli schodzi w dół, to nabiera prędkości. Potrafi też dostosować długość kroku – robi większe na stromych zboczach i mniejsze, gdy teren się wypłaszcza blisko dna doliny. Dlatego **Adam** jest najczęściej domyślnym i bardzo skutecznym wyborem.


|           | Funkcja straty (loss)       | Metryki (metrics)            |
| --------- | --------------------------- | ---------------------------- |
| dla kogo  | maszyna                     | człowiek                     |
| cwel      | kierowanie procesem uczenia | ocena końcowej wydajności    |
| wymagania | musi być różniczkowalna     | nie muszą być różniczkowalna |
| przykład  | cross entropy               | acu                          |
|           |                             |                              |
loss fun - do nauki a a metryki do oceny modelu 



dla człowieka

### Odds (szansa) 
- p(1)/1-p(1) = p(1)/p(0) 

### Magic numbers
dane nie ze zmiennej które są w  kodzie działają ale pózniej chuj wiei jak 

