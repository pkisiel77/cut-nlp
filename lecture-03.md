# Wykład 3 (16.05.2021)

## HTML

## PDF

## WORD (open xml)

## Przygotowanie tekstu do dlaszej obróbki

![image](https://user-images.githubusercontent.com/26519123/119262826-e7bc2b00-bbdc-11eb-8f22-142658400fd3.png)

## Tokenization

```py
sentence = "The capital of Poland is Warsaw"
sentence.split()

['The', 'capital', 'of', 'Poland', 'is', 'Warsaw']
```
### Issues with tokenization

## Different types of tokenizers

### Regular expressions

### Regular expressions-based tokenizers

### Treebank tokenizer

### TweetTokenizer

## Understanding word normalization

### Stemming

#### Over-stemming and under-stemming

## Lemmatization

### WordNet lemmatizer

### Spacy lemmatizer

## Stopword removal

### Case folding

## N-grams







## Algorytmy tekstowe

### Wyszukaj 

### Porównaj

https://pypi.org/project/textdistance/

#### Levenshtein

https://pypi.org/project/python-Levenshtein/0.12.0/

[wikipedia](https://pl.wikipedia.org/wiki/Odleg%C5%82o%C5%9B%C4%87_Levenshteina)

[algorytm](http://www.algorytm.org/przetwarzanie-tekstu/odleglosc-levenshteina-odleglosc-edycyjna.html)

[kod](https://stackabuse.com/levenshtein-distance-and-text-similarity-in-python/)

```py
import numpy as np

def levenshtein(seq1, seq2):
    size_x = len(seq1) + 1
    size_y = len(seq2) + 1
    matrix = np.zeros ((size_x, size_y))
    for x in xrange(size_x):
        matrix [x, 0] = x
    for y in xrange(size_y):
        matrix [0, y] = y

    for x in range(1, size_x):
        for y in range(1, size_y):
            if seq1[x-1] == seq2[y-1]:
                matrix [x,y] = min(
                    matrix[x-1, y] + 1,
                    matrix[x-1, y-1],
                    matrix[x, y-1] + 1
                )
            else:
                matrix [x,y] = min(
                    matrix[x-1,y] + 1,
                    matrix[x-1,y-1] + 1,
                    matrix[x,y-1] + 1
                )
    print (matrix)
    return (matrix[size_x - 1, size_y - 1])

levenshtein('ala ma kota', 'ola ma psa')
```
```
[[ 0.  1.  2.  3.  4.  5.  6.  7.  8.  9. 10.]
 [ 1.  1.  2.  2.  3.  4.  5.  6.  7.  8.  9.]
 [ 2.  2.  1.  2.  3.  4.  5.  6.  7.  8.  9.]
 [ 3.  3.  2.  1.  2.  3.  4.  5.  6.  7.  8.]
 [ 4.  4.  3.  2.  1.  2.  3.  4.  5.  6.  7.]
 [ 5.  5.  4.  3.  2.  1.  2.  3.  4.  5.  6.]
 [ 6.  6.  5.  4.  3.  2.  1.  2.  3.  4.  5.]
 [ 7.  7.  6.  5.  4.  3.  2.  1.  2.  3.  4.]
 [ 8.  8.  7.  6.  5.  4.  3.  2.  2.  3.  4.]
 [ 9.  8.  8.  7.  6.  5.  4.  3.  3.  3.  4.]
 [10.  9.  9.  8.  7.  6.  5.  4.  4.  4.  4.]
 [11. 10. 10.  9.  8.  7.  6.  5.  5.  5.  4.]]

4.0
```

## Literatura





















