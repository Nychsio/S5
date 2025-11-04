**Warstwa gęsta** - innymi słowy fully connected - graf pełny dwudzielny - każdy neuron z każdym następnym - w odróżnieniu sparse (rzadka)


**Funkcja aktywacji** - funkcja (ważona suma) - przeważnie nieliniowa funkcja, np. relu

**Relu** - funkcja aktywacji - dla x < 0: 0; dla x >= 0: y = x

**MNIST** - jeden z najbardziej basicowych zbiorów danych zawierający cyfry - do klasyfikacji cyfr z napisanych ręcznie

**Float32** (double liczby podwójnej precyzji) / int8 (8-bitów) - format danych liczbowych - (0 czerń, 255 biel) - keras nie lubi intów - 
więc na MNIST przechodzimy z wartości od 0 do 255 do 0 - 1 
Entropia krzyżowa (cross-entropy) - loss - warto znać wzorek 

**Softmax** - funkcja aktywacji

**Logity** / log-odds - logit - log odds - logarytm szans 
Kompilacja modelu - określanie loss, optimizer, opcjonalnie callbacks i metryki 

**Callbacks** - wywoływania wydarzeń podczas uczenia modelu (early stopping, logowanie danych do serwera)
Funkcja straty (loss)

**Optimizer**
**Metryki** (metrics)
**Odds** (szansa) - p(1)/1-p(1) = p(1)/p(0) 

**Magic** **numbers** - trzeba znać kontekst, żeby rozumieć o co chodzi - wstawianie dziwnych liczb niezrozumiałych w kod - błąd projektowy
