### екосистема

1. [машинка](https://lab.mova.institute/apps/annotator) (морфо-анотатор)
    1. [статистика](https://lab.mova.institute/api/annotator/getStats) (наперед треба увійти в анотатор)
1. [NoSketch Engine](https://mova.institute/corpus/engine/run.cgi/first_form) (корпусний рушій)
1. синт
    1. [brat](https://lab.mova.institute/brat/index.xhtml#/ud/) (синтакс-анотатор)
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
1. …

<!--
1.
-->

### таблиця змін

Після виходу з машинки текстів, залитих до наведеної дати, перекопати корпус на відповідну зміну.

(до таблиці також додаються [ці питання](https://github.com/msklvsk/corpus/issues?utf8=%E2%9C%93&q=%20label%3A%D0%BF%D0%B5%D1%80%D0%B5%D0%BA%D0%BE%D0%BF%D0%B0%D1%82%D0%B8%20))

дата  | зміна
---------:|----------
2017-04-04 | _близько_ `prep`
2017-03-07 | _місцями_ — прислівник
2017-03-03 | всі цифрові числівники мають мати повну морф. інфу
~~2017-03-05~~ | дієприслівники мають дієслівну лему
~~2017-03-05~~ | чортики автора мають позначатися `:typo`
~~2017-02-28~~ | _поки_ в _поки що_ — вказівний
~~2017-02-28~~ | `x:abbr` мають мати справжню ЧМ
