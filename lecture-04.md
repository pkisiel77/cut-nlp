## Dzielenie danych tekstowych na porcje (chunks)

W celu dalszej analizy dane tekstowe zwykle trzeba podzielić na części. Ten proces jest nazywany fragmentacją.
Jest to często używane w analizie tekstu.
Warunki, które są używane do podzielenia tekstu na fragmenty, mogą się różnić w zależności od problemu.
To nie to samo, co tokenizacja, w której tekst jest również dzielony na części.

Podczas dzielenia na fragmenty nie stosujemy się do żadnych ograniczeń, z wyjątkiem faktu, że fragmenty wyjściowe muszą mieć znaczenie.

Kiedy mamy do czynienia z dużymi dokumentami tekstowymi, ważne staje się podzielenie tekstu na fragmenty, aby wydobyć znaczące informacje.

W tej sekcji zobaczymy, jak podzielić tekst wejściowy na kilka części.


```py
import numpy as np
from nltk.corpus import brown

# Split the input text into chunks, where
# each chunk contains N words
def chunker(input_data, N):
    input_words = input_data.split(' ')


```



