---
navigation:
  - parle.constants.md: « Зумовлені константи
  - parle.regex.chars.md: Подання символів »
  - index.md: PHP Manual
  - book.parle.md: Parle
title: Зіставлення з шаблоном Parle
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Зіставлення з шаблоном Parle

## Зміст

-   [Подання символів](parle.regex.chars.md)
-   [Класи символів](parle.regex.charclass.md)
-   [Класи символів Unicode](parle.regex.unicodecharclass.md)
-   [Чергування та повторення](parle.regex.alternation.md)
-   [Якоря](parle.regex.anchors.md)
-   [Угруповання](parle.regex.grouping.md)

Parle підтримує зіставлення регулярних виразів аналогічно flex. Також підтримуються такі набори символів POSIX: `[:alnum:]` `[:alpha:]` `[:blank:]` `[:cntrl:]` `[:digit:]` `[:graph:]` `[:lower:]` `[:print:]` `[:punct:]` `[:space:]` `[:upper:]`и`[:xdigit:]`

Класи символів Unicode в даний час не включені за промовчанням, передайте --enable-parle-utf32, щоб зробити їх доступними. Конкретне кодування може відображатися за допомогою правильно побудованого регулярного виразу. Наприклад, щоб відповідати символу євро, закодованому в UTF-8, можна використовувати регулярний вираз `[\xe2][\x82][\xac]`. Шаблон для рядка кодування UTF-8 може бути `[ -\x7f]{+}[\x80-\xbf]{+}[\xc2-\xdf]{+}[\xe0-\xef]{+}[\xf0-\xff]+`
