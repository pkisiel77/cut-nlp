# Wykład 3 (16.05.2021)

## Analiza fleksyjna

Polszczyzna należy do języków o bogatej odmianie wyrazów1. Słownik języ- ka polskiego notujący 200 000 haseł można uznać za obszerny. Hasłom takiego słownika odpowiada jednak kilka milionów różnych realizacji pojawiających się w tekstach. 


Języki syntetyczne – języki, w których formy gramatyczne tworzone są za pomocą afiksów i funkcjonują w charakterze pojedynczego słowa[1]. Należą do nich języki fleksyjne, aglutynacyjne i polisyntetyczne[2]; ich przeciwieństwem są języki analityczne[1].


## Algorytmy tekstowe


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

levenshtein('ala ma kota', 'kot ma alę')

```

https://pypi.org/project/python-Levenshtein/0.12.0/
















