<!--

citing
known issues
spacing errors preserved, even OCR
holes



 -->
## Universal Dependencies for Ukrainian
This treebank is developed by Institute for Ukrainian, NGO.

The annotation is fully manual, done for UD v2 initially (no conversions).

### Basic stats
| set   | sentences | tokens |
| ----- |----------:| ------:|
| train |    4080   |   80K  |
| dev   |     826   |   15K  |
| test  |     850   |   15K  |
| TOTAL |    5853   |  100K  |

### Annotation procedure
Morphology is annotated using 2+1 schema. Syntax is single-pass plus supervisor’s check.
Consistency is enforced by ~200 validation/autofix rules.


### Contribution/Development
The original development happens at [mova-institute/corpus](https://github.com/mova-institute/corpus) and `*.conllu` files in this repo are generated from source repo xmls. Please do not edit or pull request `*.conllu` files directly.


### Notable facts
+ Arabic and Roman numerals have full morphological info.

### Data split
Data is split to train/dev/test linearly by hand at 70%/15%/15% to balance in genre & complexity.

### Format
UD Ukrainian data conforms to [CoNLL-U](http://universaldependencies.org/format.html) format with the following specific features:
* Document boundaries are present via `# newdoc` without an ID.
* Paragraph boundaries are present on both sentence (`# newpar`) and token (`NewPar=Yes`) levels without an ID.
* Sentence IDs are numeric but will survive treebank updates.
* XPOSTAG column contains [MTE](http://nl.ijs.si/ME/V4/msd/html/msd-uk.html) tag with `U` for punctuation.
* No enhanced dependencies or empty nodes present.
* MISC column additionally contains `Promoted=Yes` marker for nodes promoted by elision.

### Changelog
* 2017-11-01 **v2.1**
  * Quadrupled the amount of data up to 100K, mostly with nonfiction; improved consistency.

* 2017-02-15 **v2.0**
  * Replaced v1.4 data with 25K tokens of misc genres, mostly fiction

* 2016-11-01 **v1.4**
  * Initial experimental release containing 1.6K tokens of grammar examples and fiction

### Contributors


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
