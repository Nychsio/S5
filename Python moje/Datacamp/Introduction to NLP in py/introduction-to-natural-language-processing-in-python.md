
biblioteka RE

```py
import re
re.match("abc','abcdef')
```
dopasowuje wzorzec do ciągu znaków 
wzorzec pierwszy argument i ciąg jako drugi

możemy używać specjalnych wzorców 

\w+ - słowo 
\d - cyfra
\s - spacja
`+ **` - greedy match
\S - wszystko co nie spacja 
`[a-z]`  - gtrupowanie

`split` rodziela stringa
`findall` znajduje wszystkie
`serch` szuka paternu
`match` znajduje całego stringa lub substringa bazując na paternie


```python
# Write a pattern to match sentence endings: sentence_endings

sentence_endings = r"[.?!]"

  

# Split my_string on sentence endings and print the result

print(re.split(sentence_endings, my_string))

  

# Find all capitalized words in my_string and print the result

capitalized_words = r"[A-Z]\w+"

print(re.findall(capitalized_words, my_string))

  

# Split my_string on spaces and print the result

spaces = r"\s+"

print(re.split(my_string, spaces))

  

# Find all digits in my_string and print the result

digits = r"\d+"

print(re.findall(digits, my_string))
```


## Tokenizacja

biblioteka nltk


### Tokenizery nltk

sent_tokenize - dzieli dokument na sentencje

`regexp_tokenize` - dzieli stringa lub tokument bazujac na paternie wyrażeń reguralnych

`TweetTokenizer` - spcejalna klasa dla tweetów pozwala na odzielenie hasztagów wspomnień i wykrzykniki


### re.serch() vs re.match()


`re.match('abc','abcde')


`re.serch('abc','abcde')`

na poczaku jak jest wzorzec to zwrócą identyczne 


`re.serch('cd','abcde')`
`re.match('cd','abcde')`
jak szukamy paternu co nie jest na początku uzywac serch


- **`sent_tokenize`**: Dzieli tekst na **listę zdań**.
    
    - Wejście: "Cześć. Jak się masz?"
        
    - Wyjście: `['Cześć.', 'Jak się masz?']`
        
- **`word_tokenize`**: Dzieli (zazwyczaj) zdanie na **listę słów i znaków interpunkcyjnych** (tokenów).
    
    - Wejście: "Cześć."
        
    - Wyjście: `['Cześć', '.']`
        

`sent_tokenize` to "wyższy poziom" (segmentacja na zdania), a `word_tokenize` to "niższy poziom" (segmentacja na słowa).![[Pasted image 20251029001551.png]]