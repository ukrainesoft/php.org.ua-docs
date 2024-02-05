---
navigation:
  - wincache.sessionhandler.md: « Обробник сесій WinCache
  - wincache.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - wincache.setup.md: Встановлення та налаштування
title: Перенаправлення функцій WinCache
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Перенаправлення функцій WinCache

*ЗВЕРНІТЬ УВАГУ:* [wincache.rerouteini](wincache.configuration.md#ini.wincache.rerouteini) видалено у WinCache 1.3.7.0. Вона була замінена автоматичним перенаправленням. Дивіться [wincache.reroute\_enabled](wincache.configuration.md#ini.wincache.reroute_enabled)

Перенаправлення функцій WinCache (доступно з WinCache 1.2.0, видалено з WinCache 1.3.7.0) може використовуватися для заміни вбудованих функцій їх еквівалентами, оптимізованими для роботи з файловим кешем. Модуль WinCache включає оптимізовані під Windows реалізації функцій роботи з файлами, що може підвищити продуктивність PHP-програм у випадках роботи з файлами та мережевими папками. Оптимізовані версії представлені для таких функцій:

-   [file\_exists](function.file-exists.md)
-   [file\_get\_contents](function.file-get-contents.md)
-   [readfile](function.readfile.md)
-   [is\_readable](function.is-readable.md)
-   [is\_writable](function.is-writable.md)
-   [is\_dir](function.is-dir.md)
-   [realpath](function.realpath.md)
-   [filesize](function.filesize.md)

Для налаштування використання перенаправлення WinCache використовується файл reroute.ini, який включений в інсталяційний пакет. Скопіюйте цей файл на ту ж директорію, де знаходиться php.ini. Після цього додайте в php.ini налаштування wincache.rerouteini і вкажіть абсолютний або відносний шлях reroute.ini.

**Приклад #1 Увімкнення перенаправлення функцій у WinCache**

wincache.rerouteini = C:\\PHP\\reroute.ini

> **Зауваження**: Якщо перенаправлення функцій увімкнено, рекомендується збільшити розмір файлового кеша WinCache. Його розмір налаштовується у директиві [wincache.fcachesize](wincache.configuration.md#ini.wincache.fcachesize)

Файл reroute.ini містить опис прив'язок вбудованих функцій PHP до еквівалентів модуля WinCache. Кожен рядок файлу визначає прив'язку з використанням наступного синтаксису:

`<Ім'я функції PHP>:[<кількість параметрів функції>]=<ім'я функції wincache>`

Приклад файлу наведено нижче. У цьому прикладі виклик PHP-функції [file\_get\_contents()](function.file-get-contents.md) підміняється викликом функції **wincache\_file\_get\_contents()** тільки якщо кількість переданих параметрів менша або дорівнює 2. Вказівка ​​кількості параметрів корисна, якщо підмінювальна функція реалізує обробку не всіх вихідних параметрів.

**Приклад #2 Вміст файлу Reroute.ini**

\[FunctionRerouteList\]file\_exists=wincache\_file\_exists file\_get\_contents:2=wincache\_file\_get\_contents readfile:2=wincache\_readfile is\_readable=wincache\_is\_readable is\_writable=wincache\_is\_writable is\_writeable=wincache\_is\_writable is\_file=wincache\_is\_file is\_dir=wincache\_is\_dir realpath=wincache\_realpath filesize=wincache\_filesize
