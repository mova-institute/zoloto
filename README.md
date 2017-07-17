### екосистема

1. [машинка](https://lab.mova.institute/apps/annotator) (морфо-анотатор)
    1. [статистика](https://lab.mova.institute/api/annotator/getStats) (наперед треба увійти в анотатор)
1. [NoSketch Engine](https://mova.institute/corpus/engine/run.cgi/first_form) (корпусний рушій)
1. синт
    1. [brat](https://lab.mova.institute/brat/#/ud/) (синтакс-анотатор)
    1. [помилки](https://lab.mova.institute/files/pomylky_robochoho_tb.html) в робочій версії
    1. [дірки](https://lab.mova.institute/files/dirky_robochoho_tb.html) в робочій версії
    1. [conllu](https://lab.mova.institute/files/robochyi_tb.conllu) робочої версії
    1. Turku (синтакс-пошук):
        1. [наш](https://lab.mova.institute/dep_search/)
        1. [фінський](http://bionlp-www.utu.fi/dep_search/)
    1. [UD](http://universaldependencies.org)
        1. гітхаб-репо нашого трібанку
            1. [стабільна](https://github.com/UniversalDependencies/UD_Ukrainian) гілка
            1. [робоча](https://github.com/UniversalDependencies/UD_Ukrainian/tree/dev) гілка
        1. наші питання в UD
            1. [Routes (e.g. Mumbai-Shanghai-SFO)](https://github.com/UniversalDependencies/docs/issues/465)
1. [Intertext](https://lab.mova.institute/intertext) (вирівнювач паралельних корпусів)
1. [гітхаб](https://github.com/msklvsk)
    1. [специфікація позначок](https://github.com/msklvsk/corpus/blob/master/docs/tagset.md)
    1. [іш’юзи](https://github.com/msklvsk/corpus/issues)
1. гуглдоки
    1. [протокол розмічування](https://docs.google.com/document/d/1giVJdDax4v_YLlv0OaZaVvf23Lwul8BiPlT8MBvZBek/edit)
    1. [роботи над помилками / старі „як це позначати“](https://drive.google.com/drive/u/0/folders/0B-eNN4I2IodObXFldURJV1VGdnM)
1. [mova.institute](https://mova.institute) (титульний сайт)
    1. [демо аналізатора](https://mova.institute/analizator)
<!--1. []()-->

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
1. …

<!--
1.
-->

### тексти (речення) на майбутнє
- речення з довгими числівниками словами (як на платіжних документах)
- адреси
- „дивні“ речення — довгі переліки, цікава синтакса, купа розділових
- ПДР
- ще законів
- P.S., NB
- приклади Синявського
- народні приповідки?
- щось зі знаком гривні (₴)
- контракти (знайти пристойний)
- спитати що комерційно найпотрібніше
