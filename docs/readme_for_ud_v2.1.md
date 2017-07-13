## Universal Dependencies for Ukrainian
This treebank is initially manually annotated for UD v2. The original development happens at [mova-institute/corpus](https://github.com/mova-institute/corpus) and .conllu files in this repo are generated from source repo xmls. Please do not edit or pull request .conllu here directly.

### Basic stats
| set   | sentences |  tokens |
| ----- |----------:| -------:|
| train |      37   |  \<1K   |
| dev   |     826   |   10K   |
| test  |   _(850)_ | _(10K)_ |
| TOTAL |     863   |   10K   |

### Notable facts
+ Arabic and Roman numerals have full morphological info.

### Data split
Data was split manually on a document level to balance train/dev/test in style.

### Format
UD Ukrainian data conforms to [CoNLL-U](http://universaldependencies.org/format.html) format with the following specific features:
* Document boundaries are present via `# newdoc` without an ID.
* Paragraph boundaries are present on both sentence (`# newpar`) and token (`NewPar=Yes`) levels without an ID.
* Sentence IDs are numeric but will survive treebank updates.
* XPOSTAG column contains [MTE](http://nl.ijs.si/ME/V4/msd/html/msd-uk.html) tag with `U` for punctuation.
* No enhanced dependencies or empty nodes present.
* MISC column additionally contains `Promoted=Yes` marker for nodes promoted by elision.

### Changelog
* 2017-02-15 **v2.2**
  * .

* 2017-02-15 **v2.0**
  * Replaced v1.4 data with 25K tokens of misc genres, mostly fiction

* 2016-11-01 **v1.4**
  * Initial release containing 1.6K tokens of grammar examples and fiction

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
Genre: fiction legal news nonfiction social spoken
Contributors: Kotsyba, Natalia; Moskalevskyi, Bohdan
Contact: org@mova.institute
-->
