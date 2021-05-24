## Stopwords

Słowa które nie dodają zbyt wiele do znaczenia samego zdania. Można je bezpiecznie zignorować bez zmiany znaczenia zdania.
Stopwords nie wpływa na znaczenie zdania. Na tym etapie w zdaniu zostawiamy tylko i wyłączenie słowa które mają znaczenie.

```
Stop lista (ang. stop word) – lista słów odrzucanych przez wyszukiwarki internetowe w celu zredukowania wielkości zbiorów.

Są to słowa o małym znaczeniu (spójniki: i, oraz, lub) oraz słowa popularne (mp3, sex), czyli niewpływające na identyfikację dokumentu. Listy takie można utworzyć dla określonej dziedziny lub dla określonego języka. Istnieją stop-listy dla języka angielskiego, zawierające ok. 450 słów.

Usuwanie wyrazów nieznaczących z tekstu może się odbywać w następujący sposób:

słownikowy – z tekstu usuwane są wyrazy wymienione w specjalnym słowniku,
statystyczny – z tekstu usuwane są wyrazy, których częstość występowania znajduje się w założonym przedziale,
hybrydowy – połączenie powyższych technik.[1]
```

Usuwanie polega najczęściej na wykorzystaniu gotowych list słów - i taka listę dostarcza również biblioteka NLTK.
[Przykład 1](https://github.com/bieli/stopwords/blob/master/polish.stopwords.txt)

```
import nltk

nltk.download('stopwords')
nltk.download("wordnet")
en_stopwords = nltk.corpus.stopwords.words("english")
en_stopwords
```

```
[nltk_data] Downloading package stopwords to /root/nltk_data...
[nltk_data]   Unzipping corpora/stopwords.zip.
[nltk_data] Downloading package wordnet to /root/nltk_data...
[nltk_data]   Package wordnet is already up-to-date!
['i',
 'me',
 'my',
 'myself',
 'we',
 'our',
 'ours',
 'ourselves',
 'you',
 "you're",
 "you've",
 "you'll",
 "you'd",
 'your',
 'yours',
 'yourself',
 'yourselves',
 'he',
 'him',
 'his',
 'himself',
 'she',
 "she's",
 'her',
 'hers',
 'herself',
 'it',
 "it's",
 'its',
 'itself',
 'they',
 'them',
 'their',
 'theirs',
 'themselves',
 'what',
 'which',
 'who',
 'whom',
 'this',
 'that',
 "that'll",
 'these',
 'those',
 'am',
 'is',
 'are',
 'was',
 'were',
 'be',
 'been',
 'being',
 'have',
 'has',
 'had',
 'having',
 'do',
 'does',
 'did',
 'doing',
 'a',
 'an',
 'the',
 'and',
 'but',
 'if',
 'or',
 'because',
 'as',
 'until',
 'while',
 'of',
 'at',
 'by',
 'for',
 'with',
 'about',
 'against',
 'between',
 'into',
 'through',
 'during',
 'before',
 'after',
 'above',
 'below',
 'to',
 'from',
 'up',
 'down',
 'in',
 'out',
 'on',
 'off',
 'over',
 'under',
 'again',
 'further',
 'then',
 'once',
 'here',
 'there',
 'when',
 'where',
 'why',
 'how',
 'all',
 'any',
 'both',
 'each',
 'few',
 'more',
 'most',
 'other',
 'some',
 'such',
 'no',
 'nor',
 'not',
 'only',
 'own',
 'same',
 'so',
 'than',
 'too',
 'very',
 's',
 't',
 'can',
 'will',
 'just',
 'don',
 "don't",
 'should',
 "should've",
 'now',
 'd',
 'll',
 'm',
 'o',
 're',
 've',
 'y',
 'ain',
 'aren',
 "aren't",
 'couldn',
 "couldn't",
 'didn',
 "didn't",
 'doesn',
 "doesn't",
 'hadn',
 "hadn't",
 'hasn',
 "hasn't",
 'haven',
 "haven't",
 'isn',
 "isn't",
 'ma',
 'mightn',
 "mightn't",
 'mustn',
 "mustn't",
 'needn',
 "needn't",
 'shan',
 "shan't",
 'shouldn',
 "shouldn't",
 'wasn',
 "wasn't",
 'weren',
 "weren't",
 'won',
 "won't",
 'wouldn',
 "wouldn't"]
```
### Polish
```
from stop_words import get_stop_words
pl_stopwords = get_stop_words("pl")
pl_stopwords
```
```
Collecting stop_words
  Downloading https://files.pythonhosted.org/packages/1c/cb/d58290804b7a4c5daa42abbbe2a93c477ae53e45541b1825e86f0dfaaf63/stop-words-2018.7.23.tar.gz
Building wheels for collected packages: stop-words
  Building wheel for stop-words (setup.py) ... done
  Created wheel for stop-words: filename=stop_words-2018.7.23-cp37-none-any.whl size=32917 sha256=c658580fabaf0516f63b4ba03cb99a8c4f3c444401dd4f578ffdc93f866d5cac
  Stored in directory: /root/.cache/pip/wheels/75/37/6a/2b295e03bd07290f0da95c3adb9a74ba95fbc333aa8b0c7c78
Successfully built stop-words
Installing collected packages: stop-words
Successfully installed stop-words-2018.7.23
['ach',
 'aj',
 'albo',
 'bardzo',
 'bez',
 'bo',
 'być',
 'ci',
 'cię',
 'ciebie',
 'co',
 'czy',
 'daleko',
 'dla',
 'dlaczego',
 'dlatego',
 'do',
 'dobrze',
 'dokąd',
 'dość',
 'dużo',
 'dwa',
 'dwaj',
 'dwie',
 'dwoje',
 'dziś',
 'dzisiaj',
 'gdyby',
 'gdzie',
 'go',
 'ich',
 'ile',
 'im',
 'inny',
 'ja',
 'ją',
 'jak',
 'jakby',
 'jaki',
 'je',
 'jeden',
 'jedna',
 'jedno',
 'jego',
 'jej',
 'jemu',
 'jeśli',
 'jest',
 'jestem',
 'jeżeli',
 'już',
 'każdy',
 'kiedy',
 'kierunku',
 'kto',
 'ku',
 'lub',
 'ma',
 'mają',
 'mam',
 'mi',
 'mną',
 'mnie',
 'moi',
 'mój',
 'moja',
 'moje',
 'może',
 'mu',
 'my',
 'na',
 'nam',
 'nami',
 'nas',
 'nasi',
 'nasz',
 'nasza',
 'nasze',
 'natychmiast',
 'nią',
 'nic',
 'nich',
 'nie',
 'niego',
 'niej',
 'niemu',
 'nigdy',
 'nim',
 'nimi',
 'niż',
 'obok',
 'od',
 'około',
 'on',
 'ona',
 'one',
 'oni',
 'ono',
 'owszem',
 'po',
 'pod',
 'ponieważ',
 'przed',
 'przedtem',
 'są',
 'sam',
 'sama',
 'się',
 'skąd',
 'tak',
 'taki',
 'tam',
 'ten',
 'to',
 'tobą',
 'tobie',
 'tu',
 'tutaj',
 'twoi',
 'twój',
 'twoja',
 'twoje',
 'ty',
 'wam',
 'wami',
 'was',
 'wasi',
 'wasz',
 'wasza',
 'wasze',
 'we',
 'więc',
 'wszystko',
 'wtedy',
 'wy',
 'żaden',
 'zawsze',
 'że']
```


### Stopwords for english

```
import nltk
nltk.download('punkt')
example_text_en = "This is just an example of a text " \
                  "with some of the meaningless words."
example_text_en

non_stopwords_en = [
    word 
    for word in nltk.word_tokenize(example_text_en) 
    if word.lower() not in en_stopwords
]
non_stopwords_en
```
```
import nltk
nltk.download('punkt')
example_text_en = "This is just an example of a text " \
                  "with some of the meaningless words."
example_text_en

non_stopwords_en = [
    word 
    for word in nltk.word_tokenize(example_text_en) 
    if word.lower() not in en_stopwords
]
non_stopwords_en
```

## Korekta gramatyczna

Zadanie
```
Podzielić tekst na wyrazy i poszukac ich w słowniku, jeżeli słowo nie istanieje w słowniku to należy sprawdzić które ze słów jest najbliższe.
```
```
incorrect_text = """
To jest teskt z blendami literuwkami i bledami ortgrafcznymi. 
Bendziemy mogli sprubowacc jak metoda oparta o odleglosc 
pozwoli nam je naprawić.
"""

```

## [spacy](https://spacy.io)

```
python -m venv .env
source .env/bin/activate
pip install -U pip setuptools wheel
pip install -U spacy
python -m spacy download en_core_web_trf
python -m spacy download pl_core_news_lg
```







# Żródło
[1] https://pl.wikipedia.org/wiki/Stop_lista_(wyszukiwarki)








