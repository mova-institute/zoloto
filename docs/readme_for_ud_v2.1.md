<!--

citing
known issues
spacing errors preserved, even OCR
holes
apostrophes
* MISC column additionally contains `Promoted=Yes` marker for nodes promoted by elision.
browse brat
play with parser
accuracy stats

 -->
## Universal Dependencies for Ukrainian
This treebank is developed by Institute for Ukrainian, NGO.

The annotation is fully manual, done for UD v2 initially (no conversions).

### Basic stats
| set   | sentences | ~tokens |
| ----- |----------:| -------:|
| train |    4080   |    80K  |
| dev   |     826   |    15K  |
| test  |     850   |    15K  |
| TOTAL |    5853   |   100K  |

### Annotation procedure
Morphology is annotated using 2+1 schema. Syntax is a single-pass plus supervisor’s check.
Consistency is further enforced by ~200 validation and autofix rules.

### Notable facts
+ Arabic and Roman numerals have full morphological info.

### Data split
Data is split to train/dev/test linearly by hand at 70%/15%/15% to balance in genre & complexity. Some large documents are divided across datasets.

### Format
UD Ukrainian data conforms to [CoNLL-U](http://universaldependencies.org/format.html) format with the following specifics:
* Sentence-level comments:
  * Document boundaries are present via `# newdoc id = xxxx`.
  * Sentence-level paragraph boundaries are present via `# newpar id = xxxx`.
  * Document titles are present via `# doc_title = Назва`.
* XPOSTAG column contains [MTE](http://nl.ijs.si/ME/V4/msd/html/msd-uk.html) tag with `U` for punctuation.
* No enhanced dependencies or empty nodes present in DEPS column.
* MISC column:
  * Token-level paragraph boundaries are present via `NewPar=Yes`.
  * Token ids are present via `Id=xxxx`.
  * `SpaceAfter=No` markers are present.
* Document, paragraph, sentence, and token ids are 4-character base-32 numbers. They survive treebank updates.

### Changelog
* 2017-11-15 **v2.1**
  * Quadrupled the amount of data up to 100K, mostly with nonfiction; improved consistency.

* 2017-02-15 **v2.0**
  * Replaced v1.4 data with 25K tokens of misc genres, mostly fiction.

* 2016-11-01 **v1.4**
  * Initial experimental release containing 1.6K tokens of grammar examples and fiction.

### Data sample
```
# doc_title = Нелагідна українізація
# newdoc id = 2cre
# newpar id = 2crf
# sent_id = 2crg
# text = Мій сусід - кінчений довбень і мудило.
1	Мій	мій	DET	_	Case=Nom|Gender=Masc|Number=Sing|Person=1|Poss=Yes|PronType=Prs	2	det	_	Id=2crh
2	сусід	сусід	NOUN	_	Animacy=Anim|Case=Nom|Gender=Masc|Number=Sing	5	nsubj	_	Id=2cri
3	-	-	PUNCT	_	PunctType=Dash	5	punct	_	Id=2crj
4	кінчений	кінчений	ADJ	_	Aspect=Perf|Case=Nom|Gender=Masc|Number=Sing|VerbForm=Part|Voice=Pass	5	amod	_	Id=2crk
5	довбень	довбень	NOUN	_	Animacy=Anim|Case=Nom|Gender=Masc|Number=Sing	0	root	_	Id=2crl
6	і	і	CCONJ	_	_	7	cc	_	Id=2crm
7	мудило	мудило	NOUN	_	Animacy=Inan|Case=Nom|Gender=Neut|Number=Sing	5	conj	_	Id=2crn|SpaceAfter=No
8	.	.	PUNCT	_	_	5	punct	_	Id=2cro
```


### Contribution/Development
The original development happens at [mova-institute/corpus](https://github.com/mova-institute/corpus), that is, `*.conllu` files in this repo are generated from source repo xmls. Do not edit or pull request `*.conllu` files directly, but do that at source repo instead.


### Contributors
Core developers: Natalia Kotsyba, Mykhaylo Romanenko, Bohdan Moskalevskyi.

Ivanka Kosovska, Oksana Orlenko, Olha Lytvyn
Bohdana Matushko, Yaroslava Rychyk, Hanna Brovko
Natalia Onyshchuk, Snizhana Umanets, Valeriia Pareviazko, Anastasiia Stetsenko

The Kyiv-Mohyla Academy department of Ukrainian language led by Liudmyla Dyka provided

### Contacts
Natalia Kotsyba: [gnatko@gmail.com](mailto:gnatko@gmail.com)

Bohdan Moskalevskyi: [msklvsk@icloud.com](mailto:msklvsk@icloud.com)

<!--
--- Machine readable metadata ---
#Do not remove
Documentation status: partial
Data source: manual
Data available since: UD v1.4
License: CC BY-NC-SA 4.0
Genre: news fiction nonfiction legal social wiki web
Contributors: Kotsyba, Natalia; Moskalevskyi, Bohdan
Contact: org@mova.institute
-->
