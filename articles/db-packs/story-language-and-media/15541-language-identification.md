# Language identification

Language identification is the problem of determining which natural language a given piece of text is written in. In natural language processing it is treated as a special case of text categorization, solved mainly with statistical methods rather than rule-based logic.

A crude, non-statistical approach is to look for distinctive diacritics, punctuation, or common letter combinations, but this is highly uncertain.

One classical method, due to Grefenstette, counts short character sequences (n-grams, often function morphemes like English "ing" or French "que") in the unknown text and matches the resulting frequency profile against a table for each candidate language. The language whose profile is closest wins.

A second family relies on compression. The text is compressed alongside reference texts in known languages, and the candidate whose compressed output is most similar in length is chosen. This is called the mutual information based distance measure. The same trick has been used to build family trees of languages that closely match the trees produced by historical linguistics. The technique is mathematically close to ordinary model-based methods and is not generally seen as superior to simpler alternatives.

The dominant modern approach, described by Cavnar and Trenkle (1994) and Dunning (1994), trains an n-gram model for each language from a training text. Models can be built from characters (Cavnar and Trenkle) or from raw bytes (Dunning); the byte version folds character encoding detection into the same step. For an unknown text, a model is built on the fly and compared to every stored language model. The most similar one is returned. Two failure modes are common: a text in a language with no stored model will still be assigned to whichever stored language looks closest, and mixed-language text, common on the Web, resists clean classification.

As of 2025, a widely used baseline is the fastText library, which reaches accuracy comparable to deep learning while running far faster.

The hardest case for any system is distinguishing closely related languages, where vocabulary and structure overlap heavily. Bulgarian versus Macedonian and Indonesian versus Malay are typical examples. To benchmark this, the DSL shared task was organized in 2014, covering 13 languages in six groups: Bosnian, Croatian, Serbian; Indonesian, Malaysian; Czech, Slovak; Brazilian Portuguese, European Portuguese; Peninsular Spanish, Argentine Spanish; American English, British English. The best entry reached above 95 percent accuracy.

Practical detectors exist in major NLP toolkits. Apache OpenNLP ships a character n-gram statistical detector with a model covering 103 languages, and Apache Tika includes a detector for 18 languages.

Source: adapted from "Language identification" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Language_identification
