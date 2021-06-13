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


## spacy NER

```
import spacy
  
nlp = spacy.load('en_core_web_sm')
  
sentence = "Apple is looking at buying U.K. startup for $1 billion"
  
doc = nlp(sentence)
  
for ent in doc.ents:
    print(ent.text, ent.start_char, ent.end_char, ent.label_)
```

```

import spacy
  
nlp = spacy.load('en_core_web_sm')
  
sentence = "apple is looking at buying U.K. startup for $1 billion"
  
doc = nlp(sentence)
  
for ent in doc.ents:
    print(ent.text, ent.start_char, ent.end_char, ent.label_)
```

```
import spacy
from spacy.gold import GoldParse
from spacy.language import EntityRecognizer
  
nlp = spacy.load('en', entity = False, parser = False)
  
doc_list = []
doc = nlp('Llamas make great pets.')
doc_list.append(doc)
gold_list = []
gold_list.append(GoldParse(doc, [u'ANIMAL', u'O', u'O', u'O']))
  
ner = EntityRecognizer(nlp.vocab, entity_types = ['ANIMAL'])
ner.update(doc_list, gold_list)
```

### Example 1

https://medium.com/swlh/build-a-custom-named-entity-recognition-model-ussing-spacy-950bd4c6449f

### Eample 2 

https://itnext.io/nlp-named-entity-recognition-ner-with-spacy-and-python-dabaf843cab2

### Example 3

https://www.machinelearningplus.com/nlp/training-custom-ner-model-in-spacy/


### Other examples
- https://github.com/explosion/spaCy/issues/6382
- https://medium.com/@ashiqgiga07/rule-based-matching-with-spacy-295b76ca2b68
- https://suneelpatel-in.medium.com/named-entity-recognition-ner-custom-advanced-nlp-tool-using-spacy-568a8fbbe0d4

## spacy Intents similarity

https://betterprogramming.pub/the-beginners-guide-to-similarity-matching-using-spacy-782fc2922f7c

## Other example projects

https://github.com/explosion/projects/tree/v3/tutorials


## Literatura
[1] https://spacy.io/usage/processing-pipelines
