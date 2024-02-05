---
navigation:
  - function.imap-setflag-full.md: « imap\_setflag\_full
  - function.imap-status.md: imap\_status »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_sort
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_sort

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_sort — Отримує та сортує повідомлення

### Опис

```methodsynopsis
imap_sort(    IMAP\Connection $imap,    int $criteria,    bool $reverse,    int $flags = 0,    ?string $search_criteria = null,    ?string $charset = null): array|false
```

Отримує та сортує номери повідомлень відповідно до заданих параметрів.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`criteria`

Одне (і лише одне) з наступних значень:

-   \*\*`SORTDATE`\*\*- сортувати за датою
-   \*\*`SORTARRIVAL`\*\*- дата отримання
-   \*\*`SORTFROM`\*\*- за першою адресою у полі From
-   \*\*`SORTSUBJECT`\*\*- на тему листа
-   \*\*`SORTTO`\*\*- на першу адресу в полі To
-   \*\*`SORTCC`\*\*- за першою адресою в полі cc
-   \*\*`SORTSIZE`\*\*- за розміром повідомлення

`reverse`

Визначає сортування у зворотному порядку.

`flags`

Параметр`flags` задається бітовою маскою однієї або кількох констант:

-   \*\*`SE_UID`\*\*- повертати UID, а не номери повідомлень
-   \*\*`SE_NOPREFETCH`\*\*- не отримувати знайдені повідомлення

`search_criteria`

Рядок з пошуковим критерієм у форматі IMAP2. Докладніше дивіться в описі функції [imap\_search()](function.imap-search.md)

`charset`

Кодування MIME для сортування рядків.

### Значення, що повертаються

Повертає масив номерів повідомлень, відсортованих відповідно до заданих параметрів або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |
| 8.0.0 | `reverse` тепер є логічним типом (Bool) замість цілого числа (int). |
| 8.0.0 | `search_criteria`и`charset` тепер є nullable. |
