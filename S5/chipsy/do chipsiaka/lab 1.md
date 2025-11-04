[[numpy]] 

fetch_20newsgroups - funkcja z biblioteki scikit-learn 
pobiera klasyczny zbiór danych z 20k postami z grup dyskusyjnych 

re - moduł pythona do wyrażeń reguralnych 

nltk- natural langugage toolkit 
jedna z najstarszych i najważniejszych bibliotek do NLP w pythonie 

World_tokenize - funkcja z nltk do tokenizacji czyli dzielenia słowan a tokeny 


``` python 
nltk.download("punkt")

```

do world tokenize potrzebne są dodatkowe zasoby pozwalaja dzielić zdania na słowa radząc sobie ze skrótami np DR

- **Pobieranie danych**: Pobieramy zbiór `20newsgroups` dwukrotnie, dzieląc go na dwie części:
    
    - `subset='train'`: **Zbiór treningowy** – na tych danych będziemy "uczyć" nasz przyszły model.
        
    - `subset='test'`: **Zbiór testowy** – na tych danych sprawdzimy, jak dobrze model sobie radzi z tekstami, których nigdy wcześniej nie widział.
        
- **Usuwanie "śmieci"**: Parametr `remove` jest bardzo ważny. Mówi on funkcji, aby usunęła z tekstów nagłówki, stopki i cytowane fragmenty. Dlaczego? Ponieważ często zawierają one informacje, które mogłyby "oszukać" model (np. nazwa grupy dyskusyjnej w nagłówku). Chcemy, aby model uczył się na podstawie treści samego posta, a nie metadanych.

