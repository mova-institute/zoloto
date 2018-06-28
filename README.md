Робоче репо золотого корпусу. Звідси [скриптами](https://github.com/mova-institute/lib) будуються українські [Universal Dependencies](http://universaldependencies.org).  
Використовуйте :point_right:[збудовану версію](https://github.com/UniversalDependencies/UD_Ukrainian-IU/tree/dev), викладену на UD: вона має стандартний стабільний формат. Працюйте над _створенням_ золота тутечки :woman_scientist:.

---

### екосистема

1. [машинка](https://lab.mova.institute/apps/annotator) (морфо-анотатор)
    1. [статистика](https://lab.mova.institute/api/annotator/getStats) (наперед треба увійти в анотатор)
1. [NoSketch Engine](https://mova.institute/bonito/run.cgi/first?corpname=zoloto&reload=1&iquery=&queryselector=iqueryrow&lemma=&lpos=&phrase=&word=&wpos=&char=&cql=&default_attr=word&fc_lemword_window_type=both&fc_lemword_wsize=5&fc_lemword=&fc_lemword_type=all&fc_pos_window_type=both&fc_pos_wsize=5&fc_pos_type=all&fsca_doc.title=&fsca_doc.author=&fsca_doc.original_author=&fsca_doc.date=) (корпусний рушій)
1. синт
    1. [brat](https://lab.mova.institute/brat/#/ud/) (синтакс-анотатор)
    1. [можливо-помилки](https://lab.mova.institute/files/pomylky_robochoho_tb.html) в робочій версії
    1. [дірки](https://lab.mova.institute/files/dirky_robochoho_tb.html) в робочій версії
    1. [conllu](https://lab.mova.institute/files/robochyi_tb.conllu.txt) робочої версії
    1. Turku (синтакс-пошук):
        1. [наш](https://lab.mova.institute/dep_search/)
        1. [фінський](http://bionlp-www.utu.fi/dep_search/)
    1. [UD](http://universaldependencies.org)
        1. гітхаб-репо нашого трібанку
            1. [стабільна](https://github.com/UniversalDependencies/UD_Ukrainian) гілка
            1. [робоча](https://github.com/UniversalDependencies/UD_Ukrainian/tree/dev) гілка
        1. наші питання в UD
            1. [відкриті](https://github.com/UniversalDependencies/docs/issues/created_by/msklvsk)
            1. [закриті](https://github.com/UniversalDependencies/docs/issues?q=is%3Aissue+author%3Amsklvsk+is%3Aclosed)
1. [Intertext](https://lab.mova.institute/intertext) (вирівнювач паралельних корпусів)
1. [гітхаб](https://github.com/mova-institute)
    1. [специфікація позначок](https://github.com/msklvsk/corpus/blob/master/docs/tagset.md)
    1. [іш’юзи](https://github.com/mova-institute/zoloto/issues)
1. гуглдоки
    1. [протокол морфологічного розмічування](https://docs.google.com/document/d/1giVJdDax4v_YLlv0OaZaVvf23Lwul8BiPlT8MBvZBek/edit)
    1. [підручник зі синтакс розмічування](https://docs.google.com/document/d/1ZfdtfWlNM6Ca-Ps50TVE-g416wpjXxr5Uxmex8oKzng)
    1. [роботи над помилками / старі „як це позначати“](https://drive.google.com/drive/u/0/folders/0B-eNN4I2IodObXFldURJV1VGdnM)
1. [mova.institute](https://mova.institute) (титульний сайт)
    1. [сторінка про цей корпус](https://mova.institute/золотий_стандарт)
    1. [демо аналізатора](https://mova.institute/аналізатор)


### перед випуском
1. доробити речення
1. повиправляти зловлене валідатором
1. проглянути `obl`’и без прийменників на можливі прямі додатки
1. проглянути `obj`’і в не знахідному і `iobj`’і в не давальному на можливі `obl`’и
1. переконатися, що всі документи мають повні метадані
1. по шматочку виймати тексти з навчальної вибірки і прогнати їх крізь парсер, виявивши в діфах помилки
1. перевірити на нетокенізовані `<foreign>`
1. витягти всі `fixed`’и до документації
1. перевірити NewPar, особливо де пряма мова
1. проставити `:prop` для UD щоб виконати `PROPN`?
1. всі `X` не `:foreign`
1. перечитати згенерований plaintext
1. `ADV < Inf`
1. `obl` в `Acc`: _зробив раз_ і навпаки `(Acc !>case _) <obl _`
1. `CCONJ` `SCONJ` на початку речення


### додати тексти (речення)
- купу прикладів на _ні́кого_ й решту
- з довгими числівниками словами (як на платіжних документах)
- адреси
- 20-кратний, 200-доларовий, 100-відсотковий — UDPipe неуважний
- ПДР
- NB:
- приклади Синявського
- народні приповідки?
- щось зі знаком гривні (₴)
- контракти (знайти пристойний)
- спитати що комерційно найпотрібніше
- прислів’я
