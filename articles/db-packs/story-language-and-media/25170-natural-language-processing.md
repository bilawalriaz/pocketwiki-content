# Natural language processing

Natural language processing (NLP) is the branch of computer science that handles human language in speech or text form. It overlaps with artificial intelligence, information retrieval, computational linguistics, and linguistics.

The main task groups are speech recognition, text classification, natural language understanding, and natural language generation. Natural language is hard because it is ambiguous, context-dependent, and full of irregularities.

## Three eras of methods

**Symbolic NLP (1950s–early 1990s).** Researchers hand-wrote rules and dictionaries. The 1954 Georgetown experiment predicted machine translation would be solved in a few years; the 1966 ALPAC report showed it had not been, and funding collapsed. ELIZA (1964–66) showed how far simple pattern-matching could be stretched.

**Statistical NLP (late 1980s–2010s).** Machine learning replaced hand-written rules, helped by cheaper compute and a shift away from Chomskyan linguistics, whose theoretical stance discouraged the corpus-based work statistical methods needed. IBM Research published a probabilistic machine translation system in 1990. The web supplied large pools of unannotated text, pushing research toward unsupervised and semi-supervised learning.

**Neural NLP (2010s–present).** Representation learning and deep neural networks spread through the field after recurrent neural networks applied to language modeling in 2010 and the introduction of word embeddings such as Word2vec. By about 2015 neural methods made intermediate steps like part-of-speech tagging and word alignment unnecessary. Neural approaches are now dominant because they scale: a bigger, better-trained model is usually more accurate, whereas rule-based systems become unmanageable as rules accumulate.

The three approaches are not strict rivals. Rule-based preprocessing and post-processing still sit around most modern pipelines, and rule-based systems remain useful where training data is scarce, such as low-resource languages.

## Common tasks

NLP tasks build from sound and characters up to meaning:

- **Signal:** optical character recognition, speech recognition, speech segmentation, text-to-speech.
- **Words and morphology:** tokenization, lemmatization, stemming, morphological segmentation, part-of-speech tagging. Tokenization is trivial in space-separated languages like English but hard in Chinese, Japanese, and Thai, which do not mark word boundaries.
- **Syntax:** sentence boundary disambiguation, parsing (dependency and constituency), grammar induction. A typical sentence can have thousands of possible parse trees, most nonsensical, because grammar is ambiguous.
- **Word meaning:** named entity recognition, word-sense disambiguation, sentiment analysis, entity linking.
- **Sentence and discourse meaning:** semantic role labelling, coreference resolution, recognizing textual entailment, discourse analysis, argument mining.
- **Applications:** machine translation, summarization, question answering, grammatical error correction, natural language generation, dialogue management, text-to-image, text-to-video.

Machine translation is called "AI-complete" because it would in principle require all the knowledge a human uses.

## Trends and a persistent limit

Three trends appear in long-running shared evaluation tasks: targets move toward more abstract problems, from shallow parsing in 1999 to semantic parsing in 2019; coverage expands across languages, from English alone to more than 60 by 2018; and systems drop symbolic representations in favor of weakly supervised, end-to-end learned models. Early symbolic NLP had close ties to cognitive linguistics, and those ties are reviving as researchers seek explainability and multimodal models.

The persistent limit is data. NLP is most powerful where large annotated or raw corpora exist and weakest where they do not, which is why low-resource languages and ancient texts remain hard.

Source: adapted from "Natural language processing" on English Wikipedia, whose text is written by Wikipedia contributors, under CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): https://en.wikipedia.org/wiki/Natural_language_processing
