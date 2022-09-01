---
navigation:
  - wincache.sessionhandler.html: « Обработчик сессий WinCache
  - wincache.resources.html: Типи ресурсів »
  - index.html: PHP Manual
  - wincache.setup.html: Встановлення та налаштування
title: Перенаправлення функцій WinCache
---
## Перенаправлення функцій WinCache

*ЗВЕРНІТЬ УВАГУ:* [wincache.rerouteini](wincache.configuration.html#ini.wincache.rerouteini) видалено у WinCache 1.3.7.0. Вона була замінена автоматичним перенаправленням. Дивіться [wincache.rerouteenabled](wincache.configuration.html#ini.wincache.reroute_enabled)

Перенаправлення функцій WinCache (доступно з WinCache 1.2.0, видалено з WinCache 1.3.7.0) може використовуватися для заміни вбудованих функцій їх еквівалентами, оптимізованими для роботи з файловим кешем. Модуль WinCache включає оптимізовані під Windows реалізації функцій роботи з файлами, що може підвищити продуктивність PHP-програм у випадках роботи з файлами та мережевими папками. Оптимізовані версії представлені для таких функцій:

-   [fileexists](function.file-exists.html)
-   [filegetcontents](function.file-get-contents.html)
-   [readfile](function.readfile.html)
-   [ісreadable](function.is-readable.html)
-   [ісwritable](function.is-writable.html)
-   [ісdir](function.is-dir.html)
-   [realpath](function.realpath.html)
-   [filesize](function.filesize.html)

Для налаштування використання перенаправлення WinCache використовується файл reroute.ini, який включений в інсталяційний пакет. Скопіюйте цей файл на ту ж директорію, де знаходиться php.ini. Після цього додайте в php.ini налаштування wincache.rerouteini і вкажіть абсолютний або відносний шлях reroute.ini.

**Приклад #1 Увімкнення перенаправлення функцій у WinCache**

wincache.rerouteini = C:PHPreroute.ini

> **Зауваження**: Якщо перенаправлення функцій увімкнено, рекомендується збільшити розмір файлового кеша WinCache. Його розмір налаштовується у директиві [wincache.fcachesize](wincache.configuration.html#ini.wincache.fcachesize)

Файл reroute.ini містить опис прив'язок вбудованих функцій PHP до еквівалентів модуля WinCache. Кожен рядок файлу визначає прив'язку з використанням наступного синтаксису:

`<Имя функции PHP>:[<количество параметров функции>]=<имя функции wincache>`

Приклад файлу наведено нижче. У цьому прикладі виклик PHP-функції [filegetcontents()](function.file-get-contents.html) підміняється викликом функції **wincachefilegetcontents()** тільки якщо кількість переданих параметрів менша або дорівнює 2. Вказівка ​​кількості параметрів корисна, якщо підмінювальна функція реалізує обробку не всіх вихідних параметрів.

**Приклад #2 Вміст файлу Reroute.ini**

FunctionRerouteListfileexists=wincachefileexists filegetcontents:2=wincachefilegetcontents readfile:2=wincachereadfile isreadable=wincacheісreadable iswritable=wincacheісwritable iswriteable=wincacheісwritable isfile=wincacheісfile isdir=wincacheісdir realpath=wincacherealpath filesize=wincachefilesize
