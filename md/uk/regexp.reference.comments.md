---
navigation:
  - regexp.reference.conditional.md: « Умовні підмаски
  - regexp.reference.recursive.md: Рекурсивні шаблони »
  - index.md: PHP Manual
  - reference.pcre.pattern.syntax.md: Опис синтаксису Perl-сумісних регулярних виразів
title: Коментарі
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Коментарі

Службова послідовність (?# позначає початок коментаря, який триває до найближчої дужки, що закриває. Вкладені дужки не допускаються. Символи, що знаходяться всередині коментаря, не беруть участі в зіставленні шаблону.

Якщо використовується модифікатор [PCRE\_EXTENDED](reference.pcre.pattern.modifiers.md), неекранований символ «#» поза символьним класом також означає початок блоку коментаря, який триває до кінця поточного рядка.

**Приклад #1 Використання коментарів у шаблоні PCRE**

```php
<?php

$subject = 'test';

/* (?# можно использовать для добавления комментариев без включения PCRE_EXTENDED */
$match = preg_match('/te(?# this is a comment)st/', $subject);
var_dump($match);

/* Пробелы и # рассматриваются как часть шаблона, если не включён PCRE_EXTENDED. */
$match = preg_match('/te   #~~~~
st/', $subject);
var_dump($match);

/* Когда PCRE_EXTENDED включён, все пробелы и всё, что следует за неэкранированным # в той же строке, игнорируется. */
$match = preg_match('/te    #~~~~
st/x', $subject);
var_dump($match);
```

Результат виконання наведеного прикладу:

```
int(1)
int(0)
int(1)
```
