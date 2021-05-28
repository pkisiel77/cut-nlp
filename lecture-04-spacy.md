## Potoki przetwarzania języka

Kiedy wywołujesz nlp w tekście, spaCy najpierw **tokenizuje** tekst, aby utworzyć obiekt **Doc**

![image](https://user-images.githubusercontent.com/26519123/119462186-bbb9ba80-bd40-11eb-8beb-11427504d379.png)
Rysunek 1. Źródło [[1]](https://spacy.io/usage/processing-pipelines)

- [Tokenizer](https://spacy.io/api/tokenizer)
- [Tagger](https://spacy.io/api/tagger)
- [Parser](https://spacy.io/api/dependencyparser)
- [Entity Recognizer](https://spacy.io/api/entityrecognizer)
- Named Entity Recognizer
- [Lemmatizer](https://spacy.io/api/lemmatizer)
- [Text Categorizer](https://spacy.io/api/textcategorizer)
- [Custom Components](https://spacy.io/usage/processing-pipelines#custom-components)

### Config
```
[nlp]
pipeline = ["tok2vec", "tagger", "parser", "ner"]
```


## NER

## Sentences
https://github.com/explosion/spaCy/issues/6382
https://medium.com/@ashiqgiga07/rule-based-matching-with-spacy-295b76ca2b68

## Other example projects

https://github.com/explosion/projects/tree/v3/tutorials


## Literatura
[1] https://spacy.io/usage/processing-pipelines
